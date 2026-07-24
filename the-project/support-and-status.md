# Support and status

If Patcher is misbehaving or you cannot open something you expected to, start here.

## Is it me or is it Patcher?

The service status page shows current uptime and any known incidents:

- [patcher.statuspage.io](https://patcher.statuspage.io/)

If the status page reports an incident, sit tight — the maintainers are already on it. If everything looks green and you are still hitting a problem, the issue is more likely on your end (browser, network, or your specific data) and the channels below are the right place to reach out.

## Where to get help

- **Discord** — the fastest channel for questions, quick help, and product discussion.
  [https://discord.gg/JNy2HTb5ru](https://discord.gg/JNy2HTb5ru)
- **GitHub issues** — the right place for bug reports, regressions, and trackable technical proposals.
  [https://github.com/Polyterative/Patcher/issues](https://github.com/Polyterative/Patcher/issues)
- **Email** — for anything that does not fit the two channels above.
  [europatcher@outlook.com](mailto:europatcher@outlook.com)

The channel directory with a bit more guidance on which to pick is on the [Contact us / Help / Community](contact-us-help-community.md) page.

## Share links

Share links behave differently depending on whether the item they point at is Public or Private, and whether they use the current opaque `public_id` scheme or a legacy numeric URL.

- Public racks and patches are addressable through **opaque `public_id`** share URLs — the current canonical format.
- **Private items are unlisted, not hidden.** They are removed from public browse and public-profile listings, but anyone with the opaque share link can still open them anonymously. Private is not a security boundary; use it to declutter listings, not to protect sensitive material. See [Account and privacy](../learn-patcher.xyz/account-and-privacy.md) for the full model.
- **Legacy numeric links for private items are retired.** If someone shared a numeric URL to a private rack or patch, it no longer resolves. You will land on `/links/retired`, which is the intentional stop for those old URLs — the item may still exist under its current opaque share link, in which case the owner can share the new URL directly.
- **Legacy numeric links for public items redirect to the current token URL.** No action required — the browser just settles on the new canonical URL.
- **Profile visibility does not change an item's own visibility.** Toggling a profile private does not retract Public racks or patches; those stay reachable through their share URLs.

If you arrived on `/links/retired` from an old link, that is why. Ask the owner for the current opaque `public_id` link and try again.

## Reporting a problem

When reporting a bug, adding the following makes it much easier to diagnose:

- What you were doing when it happened.
- Which browser and version.
- Whether it reproduces after a reload.
- Screenshots, when they help.
- The share URL if the problem is tied to a specific rack, patch, or profile.

## Related pages

- [Contact us / Help / Community](contact-us-help-community.md)
- [Project and support](../README.md#project-and-support) — the top-level support pointer on the docs home
- [Supported platforms](supported-platforms.md)
- [Telemetry and privacy](telemetry-and-privacy.md)
- [Account and privacy](../learn-patcher.xyz/account-and-privacy.md)
- [FAQ](readme.md)
