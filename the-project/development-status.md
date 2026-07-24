# Development status

This page is a snapshot of what Patcher already does. It describes shipping product, not unreleased work.

Current release: **Patcher v6.5.2**. For a live release history, use the in-product `/info/changelog` route or the [Changelog](changelog.md) page.

## Shipping today

### Public browsing

- public module browsing with grouped Any / All tag filters and manufacturer filters
- public rack browsing
- public patch browsing
- public profile pages at `/u/:username`
- community trends as a public discovery surface

### Personal workspace

- module collection tracking
- rack creation and editing
- patch creation and editing
- global search across the user area
- manuals gathered from your saved modules
- contributor stats and workspace stats

### Rack workflow

- visual layout planning with undo, stale-preview indicator, and a weakest-axis hint
- duplicate / delete / blank-panel actions
- multi-panel support where available
- Power, function, layout, and signal analysis modes; layout mode adds Same HP/Combos suggestions plus Remix and Shuffle, subject to valid row formats and available module metadata. Analysis output quality depends on module data coverage — see [Racks](../learn-patcher.xyz/racks.md) for the full description.

### Patch workflow

- module-based patch capture
- connection documentation
- notes and naming for recall
- Patches distinguish repeated copies of a module as numbered instances, so each connection targets the intended copy.
- patch graph view, fullscreen mode, and PNG export
- opaque `public_id` share URLs (legacy numeric links for public patches redirect; legacy numeric links for private patches are retired)
- auto-save for patch state and edits

### Module workflow

- module detail with discovery, analysis, panel variants, and community stats — see [Modules](../learn-patcher.xyz/modules.md#analysis)
- Submit New Module and Submit-Similar contribution flows

### Project shape

- open-source codebase (Angular, TypeScript, Supabase; served through Vercel)
- public data browsing without an account
- linked sign-in with multiple providers — see [Account and privacy](../learn-patcher.xyz/account-and-privacy.md)
- mobile-friendly product direction

## Still actively improving

Patcher is still evolving. Areas that continue to move include:

- module data coverage and detail quality
- docs and onboarding
- discovery and browsing surfaces
- contributor tooling
- overall polish across core workflows

## Best way to track changes

For detailed release history, use:

- [Changelog](changelog.md) — durable pointer to the GitHub `CHANGELOG.md` and the in-product `/info/changelog` route.
- [Main GitHub repository](https://github.com/Polyterative/Patcher)
- [Discord community](https://discord.gg/JNy2HTb5ru)
