# Realm Design System

Realm uses a dark-first, low-clutter desktop interface inspired by modern professional tools.

## Visual Principles

- Typography is calm, legible, and compact.
- Surfaces use native material blur where available.
- Corners are rounded but restrained: 8 to 14 px.
- Spacing follows a 4 px rhythm.
- Icons use platform-native symbol sets.
- Primary actions are visible, secondary actions live in context menus or command palette.
- Motion is short, functional, and native.

## Color Tokens

| Token | Dark | Light |
| --- | --- | --- |
| App background | `#0D0F12` | `#F6F7F8` |
| Sidebar | material ultra-thin | material regular |
| Panel | `#16191D` | `#FFFFFF` |
| Border | `#2A2F36` | `#D8DDE3` |
| Text primary | `#F4F6F8` | `#16181C` |
| Text secondary | `#9AA4AF` | `#5E6875` |
| Accent | `#6EA8FE` | `#2563EB` |
| Success | `#46C978` | `#168A45` |
| Warning | `#F6C350` | `#A96F00` |
| Danger | `#FF6B6B` | `#C93636` |

## Layout

- Window minimum size: 980 x 640.
- Sidebar width: 248.
- Toolbar height: 52.
- List row height: 64.
- Detail max content width: 760.
- Touch targets on Windows: 32 px minimum.
- Pointer targets on macOS: 28 pt minimum.

## Components

- Sidebar: account workspaces, filters, settings entry.
- Toolbar: search, command palette trigger, create button.
- Workspace row: favorite, account label, app association, tags, last opened.
- Detail view: account metadata, notes, profile path, configuration editor, quick actions.
- Settings: tabbed or grouped native form with theme, accent, language, startup, directory, logging, updates.
- Command palette: modal native material surface with keyboard-first filtering.

## Accessibility

- Every icon-only action has an accessibility label and tooltip.
- Focus order follows visual order.
- High contrast avoids material-only distinction.
- Dynamic type scales titles, body, captions, and controls without overlap.
- Status uses text and shape in addition to color.
