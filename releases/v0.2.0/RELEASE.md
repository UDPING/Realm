# Realm 0.2.0

A clearer view of your accounts, with a refined native interface and working preferences throughout.

## What’s new

- Live Codex account details, remaining usage, reset times, and additional limit buckets for each profile.
- A refreshed dashboard, profile view, local-model library, and local chat, with shorter copy and consistent controls.
- English, Persian, and Russian throughout the interface, including localized dates, counts, and right-to-left text.
- Visible accent colors on primary actions, selections, and usage meters. Installed apps are blue; running apps are green.
- Distinct plan badges: Free in gray, Plus in blue, and Pro in violet, with separate icons.
- Original Codex light/dark icons and Ollama and LM Studio provider icons.

## Fixed

- Language, refresh interval, and startup menus now have working choices with a single selected label.
- System appearance follows macOS after switching from Light or Dark.
- Automatic account refresh uses its selected 30-second, 1-minute, or 5-minute interval independently of app scans. Changes apply without a restart.
- Startup can restore the last selected profile or open the profile list. Opening the list preserves the saved profile.
- Profile switching ignores late account responses; duplicate launch clicks are guarded; filtered model selection and command-palette keyboard navigation are corrected.

## Install

**macOS 14 or later · Apple silicon**

Download `Realm-macOS.dmg`, quit Realm, and drag the new app to Applications. Existing profiles and settings are retained. This build is ad-hoc signed and is not Apple-notarized; macOS may require first-launch approval in Privacy & Security.

The Windows build remains at 0.1.0 and is available in the previous release.

## SHA-256

```text
4eddbabbee0cbe9d9340177c193f959ea337401155dff863ed41ddd202dc4500  Realm-macOS.dmg
```
