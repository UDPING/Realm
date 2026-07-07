# Realm v0.1.0

Release date: July 7, 2026

Repository: [UDPING/Realm](https://github.com/UDPING/Realm)

## Installers

macOS:

- [Realm-macOS.dmg](macOS/Realm-macOS.dmg)

Windows:

- [Realm-Windows.exe](Windows/Realm-Windows.exe)
- See [BUILD_ON_WINDOWS.md](Windows/BUILD_ON_WINDOWS.md).

## Checksums

```text
13d5b472b3b44040d1fd4e64f59aee4c9c0af68fc451800b4e2d43fc5f132397  macOS/Realm-macOS.dmg
48828265170da22a5671e54efab318926bb6e4c61e30b93f442cc9450648fa2f  Windows/Realm-Windows.exe
```

## Notes

- App name is Realm.
- App version is v0.1.0.
- Codex and Claude profiles use separate local data paths.
- Realm does not modify third-party app bundles.
- macOS package verification passed with `codesign --verify` and `hdiutil verify`.
- Windows installer validation passed with exit code 0 in a Windows 11 VM.
- Windows App SDK runtime files are bundled to avoid the Windows App Runtime 1.5 install prompt.
