# SoundIsle Downloads

[中文](README.md) | English

SoundIsle is a desktop music player and local music library manager.
This repository provides Windows downloads and release notes only. It does not contain source code, user data, cookies, account credentials, or API keys.

## Download

Current preview version: **v0.2.0-preview**

- [v0.2.0-preview release](https://github.com/wWYANG666/SoundIsle-/releases/tag/v0.2.0-preview)
- [All releases](https://github.com/wWYANG666/SoundIsle-/releases)

Download the installer from the release **Assets** section. GitHub's automatically generated `Source code (zip)` and `Source code (tar.gz)` archives contain only this documentation repository; they are not the SoundIsle source code or a runnable application.

## Windows x64 files

```text
SoundIsle-0.2.0-preview-win-x64-setup.exe
SoundIsle-0.2.0-preview-win-x64-portable.zip
SHA256SUMS.txt
```

## Runtime notes

- Java 17 is bundled with both the installer and the portable build.
- Users do not need to install Node.js, Java, or Maven separately.
- The application uses a local account and local backend by default.
- User data and configuration are stored under `%APPDATA%\SoundIsle`.
- Online music providers require the user to sign in with their own account or login state.
- AI features require a provider and API key configured in a backend controlled by the user.
- The installer is not code-signed; Windows may show an unrecognized publisher warning.

## Verify downloads

Run PowerShell from the folder containing the downloaded files:

```powershell
Get-FileHash .\SoundIsle-0.2.0-preview-win-x64-setup.exe -Algorithm SHA256
Get-FileHash .\SoundIsle-0.2.0-preview-win-x64-portable.zip -Algorithm SHA256
```

Compare the results with `SHA256SUMS.txt` from the same release before running the files.

## Support the project

If SoundIsle is useful to you, please click the ⭐ **Star** button in the upper-right corner to support continued development.

You can also use [Issues](https://github.com/wWYANG666/SoundIsle-/issues) to report a problem or suggest an improvement.

## Source code

The source repository is private and requires access permission: [wWYANG666/SoundIsle](https://github.com/wWYANG666/SoundIsle).
