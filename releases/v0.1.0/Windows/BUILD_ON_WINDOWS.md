# Windows Build Artifact

`Realm-Windows.exe` was built in a Windows 11 VM with Visual Studio Build Tools, the Windows App SDK toolchain, and .NET 9.

To reproduce the Windows build on a Windows 11 machine with Visual Studio 2022, the Windows App SDK workload, and the .NET 9 SDK installed:

```powershell
cd Windows\WorkspaceHub
.\package.ps1
```

The script publishes a self-contained `win-x64` build. The release installer embeds that payload and creates:

```text
dist\Windows\Realm-Windows.exe
```
