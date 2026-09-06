<p align="center">
  <img src="docs/assets/realm-icon.png" width="72" alt="Realm">
</p>

<h1 align="center">Realm</h1>
<p align="center">Your accounts. One workspace.</p>
<p align="center">
  A native Mac app for Codex, Claude, and your local models.
</p>
<p align="center">
  <a href="https://github.com/UDPING/Realm/releases/download/v0.2.0/Realm-macOS.dmg"><strong>Download for macOS</strong></a>
  &nbsp; · &nbsp;
  <a href="https://github.com/UDPING/Realm/releases/tag/v0.2.0">What’s new in 0.2.0</a>
</p>
<p align="center"><sub>Apple silicon · macOS 14 or later</sub></p>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="docs/screenshots/realm-profile.png">
  <source media="(prefers-color-scheme: light)" srcset="docs/screenshots/realm-profile-light.png">
  <img src="docs/screenshots/realm-profile.png" alt="Realm profile with account details, remaining Codex usage, and reset times">
</picture>

### A little less switching.

Keep personal and work accounts in named profiles. Open the one you need, see what’s running, and pick up where you left off.

- **Accounts at a glance.** Email, plan, remaining Codex limits, and reset times for the selected profile.
- **Your models, together.** Browse Ollama and LM Studio libraries and chat through their local servers.
- **Made for your Mac.** Light, Dark, or System appearance. Four accent colors. English, فارسی, and Русский.

### Local models. Familiar tools.

Realm discovers existing model libraries, including GGUF and LM Studio MLX models, without copying the weights. Start a provider, choose a model, and open a chat.

<img src="docs/screenshots/realm-local-models.png" alt="Realm’s local-model library with Ollama and LM Studio">

<details>
<summary>Explore the interface</summary>

**Your workspace**

<img src="docs/screenshots/realm-dashboard.png" alt="Realm dashboard with recent profiles and local providers">

**Applications**

<img src="docs/screenshots/realm-applications.png" alt="Applications with green Running and blue Installed status badges">

**Make it yours**

<img src="docs/screenshots/realm-settings.png" alt="Realm appearance settings with themes, accent colors, and language selection">

Screenshots use sample accounts and usage data.

</details>

### Get started

1. Download the [macOS installer](https://github.com/UDPING/Realm/releases/download/v0.2.0/Realm-macOS.dmg).
2. Open it and drag **Realm** to **Applications**. Quit an older copy before replacing it.
3. Open Realm, create a Codex or Claude profile, and sign in through that app.

Codex and Claude must be installed separately. Local chat requires Ollama or LM Studio and a downloaded model. Claude usage is available in Claude’s own settings.

This build is ad-hoc signed and is not Apple-notarized. macOS may require approval in **System Settings → Privacy & Security** on first launch. [Release notes and checksums](https://github.com/UDPING/Realm/releases/tag/v0.2.0) accompany every download.

### Thoughtfully local

Profile metadata stays in `~/Library/Application Support/Realm/`. Account sessions are separate; supported project and chat data can be shared between profiles. Realm leaves the installed Codex and Claude apps intact.

Account checks contact the provider through Codex. Local-model chats use your local server. Update checks fetch releases from this repository.

| Action | Shortcut |
| --- | --- |
| New profile | ⌘ N |
| Find a profile | ⌘ F |
| Command palette | ⌘ K |
| Settings | ⌘ , |

---

[Report an issue](https://github.com/UDPING/Realm/issues) · [All releases](https://github.com/UDPING/Realm/releases) · [Earlier Windows build (0.1.0)](https://github.com/UDPING/Realm/releases/tag/v0.1.0)

<sub>This repository contains downloads and product documentation. Application source is private. Realm is an independent app and is not affiliated with OpenAI, Anthropic, Ollama, or LM Studio.</sub>
