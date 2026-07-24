# Contributing module data

Patcher's public module database is only as good as the data behind it. This page covers the in-product flows for adding new modules, adding variants of existing modules, and improving records that are already there.

This is the user-facing contribution surface. For code, docs, or repository-level contribution, see [Contributing](../the-project/contributing.md) under Project.

## Submit New Module

When a module does not exist in the catalogue yet, use the **Submit New Module** flow.

1. Open **Modules**.
2. Use the submit action from the modules browser.
3. Fill in the fields the form asks for — at minimum name, manufacturer, size, format, and description; add power and I/O information when you have it.
4. Attach panel images and a manual link if you can.
5. Submit.

Submitting a new module helps both the public catalogue and your own workflow, because once the module exists you can add it to your collection and use it in racks and patches.

## Submit-Similar

**Submit-Similar** is the flow for adding a module that is almost the same as one already in the catalogue — a revision, an alternate panel, or a close variant.

The **Submit-Similar** action lives on a module's detail page.

1. Open the detail page of the module that is closest to the one you want to add.
2. Trigger **Submit-Similar**.
3. The form arrives prefilled with the existing module's data.
4. Edit the fields that differ — usually the name suffix, panel image, and any changed spec.
5. Submit.

Submit-Similar is the right choice when the new entry is genuinely close but not identical. It saves typing and keeps related modules consistent with each other.

## Improving existing module data

If a module exists but its record is thin, improving that record is often the more useful contribution than submitting a new one.

Common areas to improve:

- **Panels** — add a missing panel image or an additional variant.
- **Manuals** — attach a manual URL that has not been added yet. See [Manuals](manuals.md).
- **Metadata** — power, size, format, category or function tags, I/O counts.
- **Description** — a clearer one-paragraph description tends to make the whole record more useful.

Improved data flows out to every user who has the module in their collection: their [Racks](racks.md), [Patches](patches.md), and [Manuals](manuals.md) all get better without them having to do anything.

## What not to submit

- Modules that already exist under a different name. Search first, then decide between improving the existing record or using Submit-Similar for a real variant.
- Private customizations or one-off builds that are not sold as products. The catalogue is for released modules.
- Speculative or unreleased modules.

## Boundary with repo-level contribution

This page covers the in-product data contribution flows. Contributions to the Patcher codebase or these docs live in a separate page:

- [Contributing](../the-project/contributing.md) — repo-level code and docs contribution.

## Related pages

- [Modules](modules.md)
- [Manuals](manuals.md)
- [Collection](collection.md)
- [User Area](user-area.md)
