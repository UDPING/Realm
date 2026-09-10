# Realm Design System

Realm uses neutral surfaces, clear hierarchy, and compact macOS controls. Copy names the action or state in a few words. Color is reserved for account usage, provider identity, and status.

## Surfaces and type

| Token | Dark | Light |
| --- | --- | --- |
| Window | 8.5% white | 98.5% white |
| Sidebar | 11.5% white | 95% white |
| Card | 12% white | white |
| Elevated surface | 15.5% white | white |
| Border | white at 8.5% | black at 7.5% |
| Primary action | Selected accent | Selected accent |

Use native primary and secondary text styles. Informative labels must remain readable in both appearances. Page headings are 28 pt semibold, section headings 14–15 pt, body 12–14 pt, and metadata 11–12 pt. Usage percentages use 36 pt with monospaced digits.

## Layout

- Minimum window: 1080 × 700 pt.
- Sidebar: 244 pt ideal, adjustable between 220 and 276 pt.
- Toolbar: 56 pt. Status bar: 29 pt.
- Page: up to 1040 pt of content with 32 pt horizontal padding.
- Cards: 12 pt corners, 20–24 pt padding, subtle borders and shadows.
- Buttons: 36 pt high, or 30 pt for compact actions. Icon actions: 32 × 32 pt.
- Primary buttons use the selected accent with white labels; secondary buttons use a quiet fill and border.

## Components

`RealmDesignSystem.swift` defines shared cards, buttons, badges, page headings, usage meters, empty states, and keyboard hints.

The dashboard combines a restrained hero, counts, recent profiles, provider status, and activity. Profile details show the account, two usage windows, and collapsible profile settings. Applications and local models retain their own icons within the same card system. Settings separate Appearance, Profiles, and Updates.

The sidebar supports search (⌘F), filters, sorting, and context actions. The command palette (⌘K) supports search, arrow navigation, Return, and Escape. Local chat uses the same surfaces and controls, with a labeled composer and visible send state.

## Verification

The opt-in interface test renders all six main sections in light and dark modes, both additional Settings panes, modal views, and empty/loading/signed-out/low-usage states. It also checks a wider profile view and right-to-left layout. All account and conversation data in snapshots is synthetic.

Run native interaction checks alongside snapshots: profile creation and rename, search, command-palette navigation, theme changes, usage preferences, and the separate Settings window. Honor Reduce Motion for navigation and hover animations. Icon-only actions need a descriptive accessibility label.

## Brand icons and local-model color

Codex uses the supplied transparent PNGs without a background tile: `codex-light.png` is black for light appearance; `codex-dark.png` is white for dark appearance. `ApplicationBrandIconView` chooses the correct resource at render time.

Ollama and LM Studio use their actual app icons through `LocalProviderIconView`, consistently in the overview, model library, and local chat. The provider palette restores periwinkle (`0.42, 0.50, 1.0`) for Ollama and violet (`0.79, 0.40, 0.95`) for LM Studio. Apply it to subtle panel gradients, selection fills, and borders; retain the selected accent for primary actions.

## Realm 0.2.3

Keep the first beta’s dashboard, sidebar selection treatment, and spacious page layout. The Profiles overview uses a single grouped surface with quiet separators, aligned five-hour/weekly values, and adaptive rows. Retain the green Running capsule with its play icon. Free is graphite, Plus blue, Pro and Max violet; low remaining capacity is orange.

The toolbar command palette is a 32 pt search icon with a descriptive accessibility label and ⌘K shortcut. Sidebar translucency is opt-in and uses native behind-window sidebar material. The content pane stays opaque; Reduce Transparency restores a solid sidebar. Light and Dark update both the SwiftUI content and native window, while System observes the inherited macOS appearance.

Button hover/press feedback lasts 100–160 ms; page and profile transitions last 160–180 ms. Usage meters animate over 300 ms. Reduce Motion disables these effects. Settings keep Appearance, Profiles, and Updates in distinct panes.
