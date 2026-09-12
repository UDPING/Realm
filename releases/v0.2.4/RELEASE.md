# Realm 0.2.4

Fixes a startup crash that could leave Realm unable to reopen after temporary build files were cleaned up.

Realm now loads its artwork directly from the installed app. Missing artwork falls back to native system icons instead of terminating the app. This fixes both provider icons and the Realm sidebar logo.

The update preserves the existing interface, installer, profiles, and preferences.

## Install

Download **Realm-macOS.dmg**, open it, and drag **Realm** into **Applications**, replacing the previous copy. Quit Realm first if it is running. Existing profile data stays in place.

Apple silicon · macOS 14 or later · Version 0.2.4, build 21.

## Validation

- All 62 enabled automated tests passed; six optional tests were skipped.
- 63 interface renders passed across pages, appearances, and languages.
- The packaged app passed relocated launch checks with its original build directory unavailable, including a separate copy with missing artwork.
- Native launch, recovery of the previous window, profile details, dashboard, Applications, command palette, and clean relaunch were verified on macOS.
- The disk image and app signature passed verification.

SHA-256:

```text
ccab5a8abccf327a41d884df7270a6c88209a6156b802d1f4dfb75bedc37520c  Realm-macOS.dmg
```

The app is ad-hoc signed and is not Apple-notarized. On first launch, macOS may require approval in **System Settings → Privacy & Security**.
