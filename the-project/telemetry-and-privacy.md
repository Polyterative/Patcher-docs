# Telemetry and privacy

This page describes what Patcher observes about live usage of the product and why. It exists so that the choices Patcher makes about telemetry are legible to anyone who wants to look — not just to the people running the service.

## What runs in production only

Both telemetry systems below run in production only. Local development builds and preview builds do not send data to either.

## Error monitoring — Sentry

Patcher uses **Sentry** for error monitoring in production.

When something goes wrong in the browser — an unhandled exception, a failed request the app relies on, a bug in a view — Sentry captures a report so the maintainers can fix it. Reports include the technical context needed to diagnose the problem (browser, page, error stack).

**Session Replay on error** is enabled. When an error is reported, Sentry can attach a replay of the actions immediately preceding the error, so the maintainers can see the exact interaction that produced it rather than trying to reconstruct it from a stack trace alone. Replays are captured only around errors; there is no continuous session recording.

Sentry does not run when you browse Patcher outside of production.

## Product analytics — PostHog

Patcher uses **PostHog** for product analytics in production.

The PostHog instance Patcher relies on is **EU-hosted**, so analytics data stays inside the EU data region. PostHog **respects the browser's Do Not Track (DNT) signal**: when your browser sends DNT, Patcher does not send events for your session.

Analytics are used to understand which parts of the product are actually reached and where users get stuck. They are not used to build advertising profiles.

PostHog does not run outside of production.

## Sign-in

Patcher supports Google sign-in alongside email-and-password accounts.

For the full account model, including linked sign-in and the difference between OAuth-only and email-and-password accounts, see [Account and privacy](../learn-patcher.xyz/account-and-privacy.md).

## What you can do

- Turn on **Do Not Track** in your browser to stop PostHog analytics for your sessions.
- Sign out to browse anonymously.
- Use the **Delete data** or **Delete account** flows from [Account and privacy](../learn-patcher.xyz/account-and-privacy.md) when you want your workspace data removed.

## What this page deliberately does not publish

Public docs do not publish Sentry event names, PostHog event names, sample rates, retention windows, Sentry hosting region, or any operational threshold. That detail belongs to internal operations and would bit-rot the moment it changed.

## Related pages

- [Account and privacy](../learn-patcher.xyz/account-and-privacy.md)
- [Supported platforms](supported-platforms.md)
- [Support and status](support-and-status.md)
