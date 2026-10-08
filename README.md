# SoundIsle 下载页

[English version](#english-version) | 中文

SoundIsle 是桌面音乐播放器和本地音乐管理工具。
本仓库只提供 Windows 下载文件和发布说明，不包含源代码、用户数据或凭据。

## 下载

当前预览版本：**v0.2.0-preview**

- [v0.2.0-preview 发布页](https://github.com/wWYANG666/SoundIsle-/releases/tag/v0.2.0-preview)
- [所有版本](https://github.com/wWYANG666/SoundIsle-/releases)

## 运行说明

- Windows x64
- 内置 Java 17
- 不需要安装 Node.js、Java 或 Maven
- 默认使用本机账号和本机后端
- 数据保存在 `%APPDATA%\SoundIsle`
- 在线音乐平台需要用户自行登录
- AI Key 由用户自行配置
- 安装包未签名，Windows 可能显示安全提示

## 校验

```powershell
Get-FileHash .\SoundIsle-0.2.0-preview-win-x64-setup.exe -Algorithm SHA256
```

## 支持项目

如果 SoundIsle 对你有帮助，欢迎在右上角点一个 ⭐ Star，支持项目持续更新。

也欢迎通过 [Issues](https://github.com/wWYANG666/SoundIsle-/issues) 提交问题或建议，帮助 SoundIsle 做得更好。

<a id="english-version"></a>
<details>
<summary>English version</summary>

# SoundIsle Downloads

SoundIsle is a desktop music player and local music library manager.
This repository provides Windows downloads and release notes only. It does not contain source code, user data, cookies, account credentials, or API keys.

## Download

Current preview version: **v0.2.0-preview**

- [v0.2.0-preview release](https://github.com/wWYANG666/SoundIsle-/releases/tag/v0.2.0-preview)
- [All releases](https://github.com/wWYANG666/SoundIsle-/releases)

Download the installer from the release **Assets** section. GitHub's automatically generated `Source code (zip)` and `Source code (tar.gz)` archives contain only this documentation repository; they are not the SoundIsle source code or a runnable application.

## Runtime notes

- Java 17 is bundled with both the installer and the portable build.
- Users do not need to install Node.js, Java, or Maven separately.
- The application uses a local account and local backend by default.
- User data and configuration are stored under `%APPDATA%\SoundIsle`.
- Online music providers require the user to sign in with their own account or login state.
- AI features require a provider and API key configured in a backend controlled by the user.
- The installer is not code-signed; Windows may show an unrecognized publisher warning.

## Verify downloads

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

</details>
