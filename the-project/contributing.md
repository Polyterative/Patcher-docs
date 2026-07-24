# Contributing

This page is for people who want to contribute to the Patcher codebase or these docs. If you want to contribute **module data** — new modules, panel images, manuals, spec corrections — that is done from inside the product and lives on [Contributing module data](../learn-patcher.xyz/contributing-module-data.md).

## Where Patcher lives

- **Product source code** — [github.com/Polyterative/Patcher](https://github.com/Polyterative/Patcher)
- **Docs source (this site)** — [github.com/Polyterative/Patcher-docs](https://github.com/Polyterative/Patcher-docs)
- **Issue tracker** — [github.com/Polyterative/Patcher/issues](https://github.com/Polyterative/Patcher/issues)

Both repositories are open-source. Contributions are welcome from a fresh fork or as an issue-first proposal on larger changes.

## Contributing to the docs

For copy, structure, or content contributions to these public docs:

1. Fork [`Polyterative/Patcher-docs`](https://github.com/Polyterative/Patcher-docs).
2. Make your changes on a branch.
3. Open a pull request.

Docs are GitBook-flavored Markdown. Keep image references in `.gitbook/assets/` root-relative and follow the section layout that already exists in `SUMMARY.md`.

## Contributing to the app

For code contributions to the product:

1. Fork [`Polyterative/Patcher`](https://github.com/Polyterative/Patcher).
2. Discuss larger changes as a GitHub issue first — this avoids duplicated effort and confirms the change matches the project direction.
3. Open a pull request from your branch.

### Local development

The Patcher web app is a modern browser app served through a Node-based toolchain. To run it locally:

- Install a recent Node runtime that matches the version pinned in the repository.
- Install dependencies with the package manager pinned in the repository.
- Start the local dev server.

The local dev server serves the app at **`http://localhost:5556`**. If you need to change the port, check the repository README for the current toggle — the docs deliberately do not restate implementation switches that can move.

### Image assets and the Cloudflare proxy

Module panels, screenshots, and other product image assets are served in production through a Cloudflare image proxy at **`images.patcher.xyz`**. That proxy handles resizing and format negotiation so pages stay fast on slow connections and small screens.

Local development points at either the live proxy or a local fallback depending on your setup. If images are missing during local development, check that fallback first before assuming a data problem.

## Contributor stats

Every user with signed-in workspace access has a **contributor stats** view in their [User Area](../learn-patcher.xyz/user-area.md). Contributions made through in-product flows (new modules, similar modules, improved data) surface there.

Code and docs contributions live on GitHub instead — they do not currently attach to in-product contributor stats.

## What to open an issue about

- Bugs that reproduce, especially with reproduction steps.
- Regressions after a release.
- Concrete technical proposals with enough detail to be evaluated.

For free-form feedback, feature ideas, or "is this a bug or expected?" questions, Discord is usually faster — see [Contact us / Help / Community](contact-us-help-community.md).

## Related pages

- [Contributing module data](../learn-patcher.xyz/contributing-module-data.md)
- [Contact us / Help / Community](contact-us-help-community.md)
- [Support and status](support-and-status.md)
- [Development status](development-status.md)
