# FAQ

## What is Patcher?

Patcher is a digital twin workspace for Eurorack musicians.

It combines a public module database with workspace tools for collection tracking, rack planning, patch capture, manual access, and selective public sharing.

## Do I need an account to use it?

No. You can browse public modules, racks, patches, and documentation without signing in.

You only need an account when you want to save your own collection, racks, patches, or public profile.

## Is Patcher only for patches?

No.

Patcher is useful across the whole modular workflow:

- discovering modules
- tracking what you own
- planning rack layouts
- documenting patches
- sharing selected work publicly

## Why should I add modules to my collection first?

Because the collection powers the rest of the workspace.

Once your modules are saved there, they become the source for rack planning, patch capture, and manual shortcuts.

## Can I use it privately?

Yes. New racks and patches start Public. You can switch them to **Private** before creation or at any time later.

Private racks and patches are unlisted: they are removed from browse and public-profile listings, but anyone with the opaque share link can still open them. Profile visibility does not change an item's own visibility — making a profile private does not retract Public racks or patches attached to it.

For the full visibility model, including delete-data and delete-account flows, see [Account and privacy](../learn-patcher.xyz/account-and-privacy.md). For the per-item Private toggle, see [Racks](../learn-patcher.xyz/racks.md) and [Patches](../learn-patcher.xyz/patches.md).

## What happened to my old share links?

Patcher moved to opaque `public_id` share URLs. That changed how legacy numeric links resolve:

Legacy numeric links for private items are retired; legacy numeric links for public items redirect to the current token URL.

If a numeric link now lands on `/links/retired`, the item it pointed at is Private. The item may still exist under its current opaque share URL — ask the owner for the new link. See [Support and status](support-and-status.md) for what to do next.

## What is a public profile?

A public profile is the shareable page tied to your username, addressable at `/u/:username`.

It can show your public racks, public patches, profile stats, and contributor stats. See [Public profiles](../learn-patcher.xyz/public-profiles.md) for the full description and [Account and privacy](../learn-patcher.xyz/account-and-privacy.md) for how profile visibility interacts with item visibility.

## Does Patcher support repeated modules in patches?

Yes. Patches distinguish repeated copies of a module as numbered instances, so each connection targets the intended copy.

That matters when the same hardware appears more than once in a patch — the routing stays disambiguated. See [Patches](../learn-patcher.xyz/patches.md) for the editor detail.

## Can I add missing modules?

Yes. If something is missing from the catalogue, use **Submit New Module**. If a module is close to an existing one, use **Submit-Similar** from the existing module's detail page.

For the full contribution flow — including improving existing module data — see [Contributing module data](../learn-patcher.xyz/contributing-module-data.md).

## Can I upload or improve panel images?

Yes, where the relevant contribution surface is available for the module. Improving panel coverage makes rack planning better for everyone.

## Can I import data from ModularGrid?

Not directly.

If you need something that is missing, the practical path today is to add or improve the relevant data in Patcher.

## Where should I ask for help?

Start here:

- [Support and status](support-and-status.md) — status page and support entry point.
- [Contact us / Help / Community](contact-us-help-community.md) — channel directory.
- [Discord](https://discord.gg/JNy2HTb5ru)
- [GitHub issues](https://github.com/Polyterative/Patcher/issues)

## Where should I suggest features?

Discord is usually the fastest place for product discussion. GitHub issues are also useful for concrete, trackable technical proposals.
