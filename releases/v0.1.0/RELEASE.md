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
2dc125805090651449952db03ddbda31e6a61f1d56bd7b2cc52018177897d201  macOS/Realm-macOS.dmg
0c362cec3352b3044699f8860dab72519d65983f031a5fbb86aaedeab353f06c  Windows/Realm-Windows.exe
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
- Windows shell was rebuilt as a native programmatic WinUI layout matching the macOS Realm design, avoiding the prior RootView XAML parse crash path.
- Installer-installed Windows launch was verified from `%LOCALAPPDATA%\Programs\Realm`; the app remained alive after delayed checks and produced no startup error file.
