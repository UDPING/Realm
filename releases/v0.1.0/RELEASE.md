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
da76f05dcc328620dd34041832c2fa6cd8b9951684d1be97cfbbd8404beb1d5b  Windows/Realm-Windows.exe
```

## Notes

- App name is Realm.
- App version is v0.1.0.
- Codex and Claude profiles use separate local data paths.
- Realm does not modify third-party app bundles.
- macOS package verification passed with `codesign --verify` and `hdiutil verify`.
- Windows installer validation passed with exit code 0 in a Windows 11 VM.
