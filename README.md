# SoundIsle 下载页

[English version](#english-version) | 中文

SoundIsle 是桌面音乐播放器和本地音乐管理工具。
本仓库提供客户端下载文件和发布说明，不包含源代码、用户数据或凭据。

## 下载

当前发布批次：**v0.2.0-preview.20261009**（应用内版本为 `0.2.0-preview`）。

- [2026-10-09 预览版发布页](https://github.com/wWYANG666/SoundIsle-/releases/tag/v0.2.0-preview.20261009)
- [Windows x64 安装包](https://github.com/wWYANG666/SoundIsle-/releases/download/v0.2.0-preview.20261009/SoundIsle-0.2.0-preview-win-x64-setup.exe)
- [Windows x64 便携 EXE](https://github.com/wWYANG666/SoundIsle-/releases/download/v0.2.0-preview.20261009/SoundIsle-0.2.0-preview-win-x64-portable.exe)
- [SHA-256 校验文件](https://github.com/wWYANG666/SoundIsle-/releases/download/v0.2.0-preview.20261009/SHA256SUMS.txt)
- [所有版本](https://github.com/wWYANG666/SoundIsle-/releases)

### 系统支持

| 系统 | 当前下载状态 |
| --- | --- |
| Windows x64 | 本次提供安装 EXE 和便携 EXE，目录包启动与音频播放验证通过 |
| Windows ARM64 | 已增加构建配置，尚未发布下载 |
| macOS Intel / Apple Silicon | 已增加 DMG / ZIP 构建配置，待对应系统构建和验收 |
| Linux x64 / ARM64 | 已增加 AppImage / DEB / tar.gz 构建配置，待对应系统构建和验收 |

下载发布页 **Assets** 中的应用文件。GitHub 自动生成的 `Source code (zip)` 和 `Source code (tar.gz)` 仅包含这个下载文档仓库，不能作为播放器运行。

## 运行说明

- Windows x64
- 默认连接统一账号服务器 `https://music.123936.xyz`，该模式不需要安装 Java
- 本次包内带后端 JAR，未内置 Java 运行环境；可选本地账号模式需要 Java 17 或更高版本，并设置 `JAVA_HOME` 或将 `java` 加入 `PATH`
- 不需要安装 Node.js 或 Maven
- 数据保存在 `%APPDATA%\SoundIsle`
- 在线音乐平台需要用户自行登录
- 默认账号与 AI 服务由服务器管理；本地音频仍保存在用户电脑
- 安装包未签名，Windows 可能显示安全提示

## 校验

```powershell
Get-FileHash .\SoundIsle-0.2.0-preview-win-x64-setup.exe -Algorithm SHA256
Get-FileHash .\SoundIsle-0.2.0-preview-win-x64-portable.exe -Algorithm SHA256
```

请与同一发布批次的 `SHA256SUMS.txt` 对比。旧版发布文件保留在原发布页，新旧批次的账号模式和 Java 运行要求不同。

## 支持项目

如果 SoundIsle 对你有帮助，欢迎在右上角点一个 ⭐ Star，支持项目持续更新。

也欢迎通过 [Issues](https://github.com/wWYANG666/SoundIsle-/issues) 提交问题或建议，帮助 SoundIsle 做得更好。

## English version

# SoundIsle Downloads

SoundIsle is a desktop music player and local music library manager.
This repository provides application downloads and release notes only. It does not contain source code, user data, cookies, account credentials, or API keys.

## Download

Current release batch: **v0.2.0-preview.20261009**. The application version remains `0.2.0-preview`.

- [2026-10-09 preview release](https://github.com/wWYANG666/SoundIsle-/releases/tag/v0.2.0-preview.20261009)
- [Windows x64 installer](https://github.com/wWYANG666/SoundIsle-/releases/download/v0.2.0-preview.20261009/SoundIsle-0.2.0-preview-win-x64-setup.exe)
- [Windows x64 portable EXE](https://github.com/wWYANG666/SoundIsle-/releases/download/v0.2.0-preview.20261009/SoundIsle-0.2.0-preview-win-x64-portable.exe)
- [SHA-256 checksums](https://github.com/wWYANG666/SoundIsle-/releases/download/v0.2.0-preview.20261009/SHA256SUMS.txt)
- [All releases](https://github.com/wWYANG666/SoundIsle-/releases)

Download the installer from the release **Assets** section. GitHub's automatically generated `Source code (zip)` and `Source code (tar.gz)` archives contain only this documentation repository; they are not the SoundIsle source code or a runnable application.

## Runtime notes

- Windows x64 downloads are available. Windows ARM64, macOS, and Linux build configurations have been added, but their downloads await native builds and acceptance.
- The default cloud account mode connects to `https://music.123936.xyz` and does not require a local Java installation.
- This batch includes the backend JAR, but does not bundle a Java runtime. Optional local account mode requires Java 17 or newer through `JAVA_HOME` or `PATH`.
- Node.js and Maven are not required on the user's computer.
- User data and configuration are stored under `%APPDATA%\SoundIsle`.
- Online music providers require the user to sign in with their own account or login state.
- Account and AI services are managed by the server in the default mode. Local audio files remain on the user's computer.
- The installer is not code-signed; Windows may show an unrecognized publisher warning.

## Verify downloads

```powershell
Get-FileHash .\SoundIsle-0.2.0-preview-win-x64-setup.exe -Algorithm SHA256
Get-FileHash .\SoundIsle-0.2.0-preview-win-x64-portable.exe -Algorithm SHA256
```

Compare the results with `SHA256SUMS.txt` from the same release before running the files.

## Support the project

If SoundIsle is useful to you, please click the ⭐ **Star** button in the upper-right corner to support continued development.

You can also use [Issues](https://github.com/wWYANG666/SoundIsle-/issues) to report a problem or suggest an improvement.

## Source code

The source repository is private and requires access permission: [wWYANG666/SoundIsle](https://github.com/wWYANG666/SoundIsle).
