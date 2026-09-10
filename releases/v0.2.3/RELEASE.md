# Realm 0.2.3

The first beta’s familiar layout, with the second beta’s cleaner Profiles view.

- A grouped profile list with aligned remaining limits, colored plans, adaptive density, and the original green Running badge.
- Subtle button feedback, page transitions, and profile transitions that respect Reduce Motion.
- A search icon for the command palette. The ⌘K shortcut works throughout the app.
- Correctly applies Light, Dark, and System appearance when switching themes.
- Optional native sidebar translucency in Settings → Appearance, with a solid fallback when Reduce Transparency is enabled.
- Claude account limits, plan information, and reset times from each profile’s own sign-in. Clear messages for sign-in, Keychain access, and provider errors; expired limits display a dash while awaiting fresh data.

## Install

Download **Realm-macOS.dmg**, open it, and drag Realm to Applications. Quit an older copy of Realm before replacing it. This is the stable app and uses the existing Realm library; the beta apps and their libraries remain separate.

Requires Apple silicon and macOS 14 or later. Codex and Claude must be installed separately. For Claude limits, sign in inside the Realm profile and use **Allow access** if Realm requests Keychain authorization. Checks are cached for up to five minutes.

This build is ad-hoc signed, not Apple-notarized. On first launch, macOS may require approval in **System Settings → Privacy & Security**.

## Validation

59 enabled regression tests passed, covering profile launch/stop, account isolation, startup preferences, refresh scheduling, Claude parsing/authentication/error handling, and native window transparency. Interface renders cover both themes, three languages, density choices, and unavailable states. Claude success/error responses were tested with fixtures; authenticated live Claude usage was not available for validation.

Checksums are supplied in **SHA256SUMS.txt**. Source code remains private.
