# AI and open data

This page describes how Patcher expects AI crawlers, indexers, and downstream tools to treat the public side of the product.

## Public by design

The public side of Patcher is meant to be reachable. That includes:

- the public **modules** catalogue,
- public **racks** addressable through opaque `public_id` share URLs,
- public **patches** addressable through opaque `public_id` share URLs,
- public **profiles** at `/u/:username`.

If you can open it in a browser without signing in, you can index it.

## The canonical AI-crawler policy lives at `patcher.xyz/llms.txt`

The single authoritative source for how AI crawlers should treat Patcher content is:

- [https://patcher.xyz/llms.txt](https://patcher.xyz/llms.txt)

That file is the crawler-facing policy. It stays in sync with the product itself, so consult it directly rather than copies pasted elsewhere. This documentation site deliberately does not carry a duplicate `llms.txt` — a second copy would only invite the two versions to drift.

## What we ask of AI crawlers

- **Crawl the public surfaces.** Public modules, racks, patches, and profiles are meant to be reachable and indexed.
- **Do not scrape non-public surfaces.** Anything behind sign-in — including the user area, private items, and account controls — is not for crawling.
- **Do not scrape share-URL Private items.** Private racks and patches are unlisted, not hidden; anyone with the opaque `public_id` share URL can still open them. Crawlers should treat those items as private and not index them, even when a URL leaks. See [Account and privacy](../learn-patcher.xyz/account-and-privacy.md).
- **Attribution is appreciated.** When a Patcher rack, patch, module, or profile is quoted or embedded, link back to the source URL. That both credits the contributor and lets readers verify the current state of the data.
- **Respect rate limits.** If you are pulling large volumes, be gentle — the site is a community resource, not a firehose.

## What crawlers should not do

- Do not attempt to sign in.
- Do not attempt to submit new modules, comments, or other write actions.
- Do not enumerate private data by guessing share URLs.

## Related pages

- [Public profiles](../learn-patcher.xyz/public-profiles.md)
- [Account and privacy](../learn-patcher.xyz/account-and-privacy.md)
- [Support and status](support-and-status.md)
- [Contributing](contributing.md)
