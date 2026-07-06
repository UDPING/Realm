# Realm v0.1.0

Release date: July 7, 2026

Repository: [UDPING/Realm](https://github.com/UDPING/Realm)

## Installers

macOS:

- [Realm-macOS.dmg](macOS/Realm-macOS.dmg)
- [Realm-macOS.zip](macOS/Realm-macOS.zip)

Windows:

- Windows build requires Windows 11, Visual Studio 2022, Windows App SDK, and .NET 9.
- See [BUILD_ON_WINDOWS.md](Windows/BUILD_ON_WINDOWS.md).

## Checksums

```text
209e07a02c561250444829c2a6424ec0fe8817e011eade413f4c89d101ff7909  macOS/Realm-macOS.dmg
121ff451f6a1d583652037746425dc41d72905bb070cc0103bb51c0db533e94c  macOS/Realm-macOS.zip
```

## Notes

- App name is Realm.
- App version is v0.1.0.
- Codex and Claude profiles use separate local data paths.
- Realm does not modify third-party app bundles.
- macOS package verification passed with `codesign --verify` and `hdiutil verify`.
