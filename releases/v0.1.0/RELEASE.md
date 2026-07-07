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
1a8b1d3820e348ceacceb7e2e68dd9a2c27bb7b7ce5e1e073bb714cd553ca638  Windows/Realm-Windows.exe
```

## Notes

- App name is Realm.
- App version is v0.1.0.
- Codex and Claude profiles use separate local data paths.
- Realm does not modify third-party app bundles.
- macOS package verification passed with `codesign --verify` and `hdiutil verify`.
- Windows installer validation passed with exit code 0 in a Windows 11 VM.
- Windows installer now installs first and leaves launch to the Start Menu to avoid non-interactive installer-session WinUI crashes.
- Windows App SDK runtime files are bundled to avoid the Windows App Runtime 1.5 install prompt.
- Windows payload now includes the generated `WorkspaceHub.pri` WinUI resource file; interactive launch was verified in the active Windows console session.
