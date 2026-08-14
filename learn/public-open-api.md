# Public Open API

The Patcher Public Open API is live at `https://api.patcher.xyz/v1` for reading catalogue data from Patcher.

Every catalogue request requires an API key. There is no anonymous catalogue API access.

The source-of-truth OpenAPI document tracks the live implementation:

- [Download the OpenAPI YAML](https://raw.githubusercontent.com/Polyterative/Patcher/develop/cloudflare/public-api/openapi.yaml)
- [View the OpenAPI source on GitHub](https://github.com/Polyterative/Patcher/blob/develop/cloudflare/public-api/openapi.yaml)

## What the API is for

Use the Public Open API to read Patcher catalogue data:

- modules
- manufacturers
- standards
- tags

## Available endpoints

| Endpoint | Purpose |
| --- | --- |
| `GET /v1/modules` | List modules with pagination, sorting, sparse fields, and module filters. |
| `GET /v1/modules/{id}` | Read one module by ID. |
| `GET /v1/manufacturers` | List manufacturers. |
| `GET /v1/manufacturers/{id}` | Read one manufacturer by ID. |
| `GET /v1/standards` | List standards. |
| `GET /v1/tags` | List tags. |

Module, manufacturer, and tag IDs are positive integers. Standard IDs are nonnegative integers because `0` is
valid and means 3U. The `standard` filter accepts `0`; `manufacturer_id` and `tag` filter values must be
positive integers.

The catalogue data is published under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). If you use
it in an app, website, dataset, or generated output, include attribution to Patcher.

## What is not included

The API does not expose:

- public patches or public racks
- panel image filenames or panel image URLs
- price data or store listings
- anonymous catalogue access
- bulk export downloads

Bulk JSONL export is planned as a key-required feature, but it is deferred. Public patch and rack endpoints
are also deferred.

## Authentication

Every catalogue request requires an API key:

```bash
Authorization: Bearer $PATCHER_PUBLIC_API_KEY
```

Keys use the wire format `Bearer pk_live_<22_base64url_chars>`. The examples below use environment variable
placeholders only; never paste a real key into public docs, client-side source, screenshots, issue reports, or
shared logs.

API keys will be created from the existing Patcher User Area, but that app release is still pending. Until
self-service key creation is deployed, only already issued keys can call the API.

## Quickstart

Start with the module list:

```bash
curl "https://api.patcher.xyz/v1/modules?limit=10&sort=name" \
  -H "Authorization: Bearer $PATCHER_PUBLIC_API_KEY"
```

Request only the fields you need:

```bash
curl "https://api.patcher.xyz/v1/modules?fields=id,name,manufacturer_id,hp&limit=10" \
  -H "Authorization: Bearer $PATCHER_PUBLIC_API_KEY"
```

Sparse fields apply to top-level fields. The `id` field is always retained in sparse field responses.

## Quotas and rate limits

The free tier allows:

- 5,000 requests per month
- 60 requests per minute

Partner tier access may be granted manually. There is no anonymous tier and no paid tier.

Quota and rate limit headers are calculated per API key. Shared cache hits still authenticate the request and
count against that key's quota.

| Header | Meaning |
| --- | --- |
| `X-RateLimit-Limit-Month` | Monthly request limit for the key. |
| `X-RateLimit-Remaining-Month` | Requests remaining in the current monthly window. |
| `X-RateLimit-Limit-Minute` | Per-minute request limit for the key. |
| `X-RateLimit-Remaining-Minute` | Requests remaining in the current minute window. |
| `X-RateLimit-Reset` | Start timestamp of the current minute window. |
| `Retry-After` | Seconds to wait before retrying after a `429` response. |

## Pagination

List endpoints use cursor pagination.

- `limit` defaults to `50`.
- `limit` can be at most `100`.
- cursors are opaque; do not parse or construct them
- pass the returned cursor back exactly as received

Example:

```bash
curl "https://api.patcher.xyz/v1/modules?limit=50&cursor=OPAQUE_CURSOR_FROM_PREVIOUS_RESPONSE" \
  -H "Authorization: Bearer $PATCHER_PUBLIC_API_KEY"
```

Sample list response:

```json
{
  "data": [
    {
      "id": 123,
      "name": "Example Module",
      "manufacturer_id": 10,
      "hp": 8
    }
  ],
  "page": {
    "next_cursor": "OPAQUE_CURSOR_FROM_RESPONSE"
  }
}
```

## Sorting

List endpoints support ascending sort by:

- `name`
- `id`

Example:

```bash
curl "https://api.patcher.xyz/v1/manufacturers?sort=name" \
  -H "Authorization: Bearer $PATCHER_PUBLIC_API_KEY"
```

## Filtering modules

`GET /v1/modules` supports these filters:

- `manufacturer_id`
- `hp`
- `standard`
- `tag`

Examples:

```bash
curl "https://api.patcher.xyz/v1/modules?manufacturer_id=10&sort=name" \
  -H "Authorization: Bearer $PATCHER_PUBLIC_API_KEY"
```

```bash
curl "https://api.patcher.xyz/v1/modules?hp=8&standard=0&tag=42" \
  -H "Authorization: Bearer $PATCHER_PUBLIC_API_KEY"
```

Tag records can include a `type`. Its value is one of `nature`, `character`, `voice`, `source`, `filter`,
`modulation`, `effect`, `sequencing`, `utility`, `blank`, or `null`.

`q` is reserved for future search support. In the current implementation it returns a `400` error with the
code `unsupported_parameter`.

## Includes

Detail and list responses can include related top-level data where supported.

Modules support:

- `ins`
- `outs`
- `tags`
- `panels`

Example:

```bash
curl "https://api.patcher.xyz/v1/modules/123?include=ins,outs,tags,panels" \
  -H "Authorization: Bearer $PATCHER_PUBLIC_API_KEY"
```

Manufacturer detail supports:

- `modules`

Example:

```bash
curl "https://api.patcher.xyz/v1/manufacturers/10?include=modules" \
  -H "Authorization: Bearer $PATCHER_PUBLIC_API_KEY"
```

## Caching with ETags

Responses support `ETag` and `If-None-Match`.

`HEAD` requests are supported for checking response headers without downloading a response body.

```bash
curl "https://api.patcher.xyz/v1/modules?limit=10" \
  -H "Authorization: Bearer $PATCHER_PUBLIC_API_KEY" \
  -H 'If-None-Match: "ETAG_FROM_PREVIOUS_RESPONSE"'
```

If the data has not changed, the API can return `304 Not Modified`. The request still authenticates and counts
against the API key's quota.

## Errors

Errors use this shape:

```json
{
  "error": {
    "code": "unsupported_parameter",
    "message": "The q parameter is reserved and is not supported yet.",
    "request_id": "req_REPLACE_WITH_REQUEST_ID"
  }
}
```

Keep the `request_id` when reporting a problem.

| Status | `error.code` | Meaning |
| --- | --- | --- |
| `400` | `unknown_parameter`, `invalid_parameter`, `unsupported_parameter` | The request contains an unknown, invalid, reserved, or unsupported parameter. |
| `401` | `missing_authorization`, `malformed_authorization`, `invalid_key` | The API key is missing, malformed, or not accepted. Revoked and unknown credentials both return `invalid_key`. |
| `404` | `not_found` | The requested resource does not exist. |
| `405` | `method_not_allowed` | Only `GET`, `HEAD`, and `OPTIONS` are supported; returned with an `Allow` header before authentication is checked. |
| `429` | `rate_limit_exceeded` | The key exceeded a monthly or per-minute quota. Check `Retry-After`. |
| `503` | `configuration_error`, `authentication_unavailable`, `quota_unavailable`, `origin_unavailable` | The API is temporarily unavailable or not fully configured. |

## Endpoint examples

### List modules

```bash
curl "https://api.patcher.xyz/v1/modules?limit=25&sort=name&fields=id,name,manufacturer_id,hp" \
  -H "Authorization: Bearer $PATCHER_PUBLIC_API_KEY"
```

### Get one module

```bash
curl "https://api.patcher.xyz/v1/modules/123?include=ins,outs,tags,panels" \
  -H "Authorization: Bearer $PATCHER_PUBLIC_API_KEY"
```

### List manufacturers

```bash
curl "https://api.patcher.xyz/v1/manufacturers?limit=100&sort=name" \
  -H "Authorization: Bearer $PATCHER_PUBLIC_API_KEY"
```

### Get one manufacturer

```bash
curl "https://api.patcher.xyz/v1/manufacturers/10?include=modules" \
  -H "Authorization: Bearer $PATCHER_PUBLIC_API_KEY"
```

### List standards

```bash
curl "https://api.patcher.xyz/v1/standards?sort=name" \
  -H "Authorization: Bearer $PATCHER_PUBLIC_API_KEY"
```

### List tags

```bash
curl "https://api.patcher.xyz/v1/tags?sort=name" \
  -H "Authorization: Bearer $PATCHER_PUBLIC_API_KEY"
```

## Roadmap notes

The current API intentionally excludes write operations, public patches, public racks, bulk JSONL
export, panel image file URLs, and commercial listing data. The API is designed around catalogue reads first;
new endpoint families will be documented here and in the OpenAPI spec when they are ready.

## Related pages

- [Modules](../learn-patcher.xyz/modules.md)
- [Search and Discovery](../learn-patcher.xyz/search-and-discovery.md)
- [Development status](../the-project/development-status.md)
