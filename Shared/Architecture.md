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

## Dependency Injection

macOS uses a lightweight `AppContainer` composed in `WorkspaceHubApp`.

Windows uses `Microsoft.Extensions.DependencyInjection` in `App.xaml.cs`.

## Threading

UI state is updated on the main actor or dispatcher. Disk I/O, logging, backup, and JSON encoding run on background tasks. All long-running operations expose cancellation paths.

## Error Policy

Errors are logged with structured context and surfaced to the UI through non-blocking banners or native alerts for destructive actions. Recovery errors never block app launch unless no workspace data can be read.
