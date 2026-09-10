# Realm Architecture

Realm uses Clean Architecture with inward-facing dependencies.

```text
Presentation -> Application -> Domain
Infrastructure -> Application / Domain contracts
Services -> Composition root and platform adapters
```

## Domain

The domain contains workspace aggregates, account profile metadata, managed application status models, activity events, and repository contracts. It has no dependency on UI frameworks, file systems, notifications, or platform APIs.

## Application

Use cases coordinate domain operations and persistence:

- Create workspace
- Rename workspace
- Delete workspace
- Duplicate workspace
- Toggle favorite
- Search, sort, and filter
- Open workspace
- Detect supported AI apps
- Launch and reveal supported apps without modifying them
- Create app-associated account profiles with isolated local profile paths
- Record activity events
- Load and recover persisted state

Use cases are asynchronous and cancellation-aware on both platforms.

## Presentation

Presentation contains native views, reusable components, command definitions, and view models. View models depend only on application interfaces and DTOs.

## Infrastructure

Infrastructure implements file persistence, backups, recovery, logging, and platform adapters. It is injected into the application layer at startup.

Local-model infrastructure has two adapters:

- `MacLocalModelCatalogService` merges live Ollama and LM Studio API results with on-disk discovery when either server is offline.
- `MacLocalCodexLaunchService` starts installed providers and launches the Codex CLI with an ephemeral `--oss` provider override, leaving user and project Codex configuration untouched.

## Dependency Injection

macOS uses a lightweight `AppContainer` composed in `WorkspaceHubApp`.

## Threading

UI state is updated on the main actor or dispatcher. Disk I/O, logging, backup, and JSON encoding run on background tasks. All long-running operations expose cancellation paths.

## Error Policy

Errors are logged with structured context and surfaced to the UI through non-blocking banners or native alerts for destructive actions. Recovery errors never block app launch unless no workspace data can be read.

## Account limits on macOS

Codex checks use the app-server account APIs with each Realm profile’s own configuration. Claude checks read that profile’s own desktop sign-in and request usage from Claude. The cookie store is opened read-only, credentials remain in memory, redirects are disabled, and Realm never falls back to another profile or the default browser account. Background checks do not prompt for Keychain access; a visible Allow access action lets the user authorize access when required.

The view model caches usage per profile and shares in-flight work. Claude caches successful responses for up to five minutes and backs off on rate limits. Missing or expired data stays unavailable until a fresh response arrives. Profile changes and sign-out invalidate the relevant cached credentials.
