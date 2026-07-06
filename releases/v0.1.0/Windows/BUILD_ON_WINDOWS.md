# Windows Build Artifact

This macOS environment does not have `dotnet`, Visual Studio, or the Windows App SDK, so a real WinUI 3 Windows build cannot be produced here.

On a Windows 11 machine with Visual Studio 2022, the Windows App SDK workload, and the .NET 9 SDK installed:

```powershell
cd Windows\WorkspaceHub
.\package.ps1
```

The script publishes a self-contained `win-x64` build and creates:

```text
dist\Windows\Realm-Windows-win-x64.zip
```
