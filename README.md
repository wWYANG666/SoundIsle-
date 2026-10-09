# SoundIsle 下载页

[English](#english) | 中文

SoundIsle 是桌面音乐播放器和本地音乐管理工具。本公开仓库提供安装包及发布说明；[源码仓库](https://github.com/wWYANG666/SoundIsle)保持私有。

## 下载 v0.2.1-preview

[完整发布页](https://github.com/wWYANG666/SoundIsle-/releases/tag/v0.2.1-preview) · [所有历史版本](https://github.com/wWYANG666/SoundIsle-/releases)

| 系统 | 架构 | 下载格式 |
| --- | --- | --- |
| Windows | x64 | [安装 EXE](https://github.com/wWYANG666/SoundIsle-/releases/download/v0.2.1-preview/SoundIsle-0.2.1-preview-win-x64-setup.exe) · [便携 EXE](https://github.com/wWYANG666/SoundIsle-/releases/download/v0.2.1-preview/SoundIsle-0.2.1-preview-win-x64-portable.exe) |
| macOS Intel | x64 | [DMG](https://github.com/wWYANG666/SoundIsle-/releases/download/v0.2.1-preview/SoundIsle-0.2.1-preview-mac-x64.dmg) · [ZIP](https://github.com/wWYANG666/SoundIsle-/releases/download/v0.2.1-preview/SoundIsle-0.2.1-preview-mac-x64.zip) |
| macOS Apple Silicon | ARM64 | [DMG](https://github.com/wWYANG666/SoundIsle-/releases/download/v0.2.1-preview/SoundIsle-0.2.1-preview-mac-arm64.dmg) · [ZIP](https://github.com/wWYANG666/SoundIsle-/releases/download/v0.2.1-preview/SoundIsle-0.2.1-preview-mac-arm64.zip) |
| Linux | x64 | [DEB](https://github.com/wWYANG666/SoundIsle-/releases/download/v0.2.1-preview/SoundIsle-0.2.1-preview-linux-amd64.deb) · [AppImage](https://github.com/wWYANG666/SoundIsle-/releases/download/v0.2.1-preview/SoundIsle-0.2.1-preview-linux-x86_64.AppImage) · [tar.gz](https://github.com/wWYANG666/SoundIsle-/releases/download/v0.2.1-preview/SoundIsle-0.2.1-preview-linux-x64.tar.gz) |
| Linux | ARM64 | [DEB](https://github.com/wWYANG666/SoundIsle-/releases/download/v0.2.1-preview/SoundIsle-0.2.1-preview-linux-arm64.deb) · [AppImage](https://github.com/wWYANG666/SoundIsle-/releases/download/v0.2.1-preview/SoundIsle-0.2.1-preview-linux-arm64.AppImage) · [tar.gz](https://github.com/wWYANG666/SoundIsle-/releases/download/v0.2.1-preview/SoundIsle-0.2.1-preview-linux-arm64.tar.gz) |

Windows ARM64 尚未提供原生下载。GitHub 自动生成的源码归档只包含本仓库文档，不能作为播放器运行。

## 运行说明

- 本次各平台包均内置对应系统和架构的 Java 17，无需另装 Java、Node.js 或 Maven。
- 本版默认使用本机账号和本机后端；数据不会自动同步到云账号。
- 配置目录：Windows `%APPDATA%\SoundIsle`；macOS `~/Library/Application Support/SoundIsle`；Linux `$XDG_CONFIG_HOME/SoundIsle`，未设置时为 `~/.config/SoundIsle`。
- 在线平台由用户自行连接账号，AI 供应商和 Key 由用户在自己控制的后端配置。
- macOS 包未进行 Developer ID 签名和公证，首次打开可能被 Gatekeeper 拦截；Windows 包也未进行发布者签名。
- Linux AppImage 需要 FUSE 支持；不能使用时可选 DEB 或完整解压 tar.gz。

与上一批次 `v0.2.0-preview.20261009` 的默认云账号不同，本版内置 Java 并默认使用本地后端。旧版下载保留。

## 校验与验证

[下载 SHA256SUMS.txt](https://github.com/wWYANG666/SoundIsle-/releases/download/v0.2.1-preview/SHA256SUMS.txt)，与下载文件的 SHA-256 比较：

```powershell
Get-FileHash .\SoundIsle-0.2.1-preview-win-x64-setup.exe -Algorithm SHA256
```

```bash
# macOS
shasum -a 256 SoundIsle-0.2.1-preview-mac-arm64.dmg
# Linux
sha256sum SoundIsle-0.2.1-preview-linux-x86_64.AppImage
```

五个原生系统/架构均完成构建、启动、内置 Java、注册、音乐导入/播放、退出重登和重启持久化测试。OS 安装、卸载、系统权限与 macOS Gatekeeper 流程仍需在用户设备验收。

欢迎通过 [Issues](https://github.com/wWYANG666/SoundIsle-/issues)提交问题，并注明系统、架构和包版本。

## English

SoundIsle v0.2.1-preview provides native downloads for Windows x64, macOS Intel/Apple Silicon, and Linux x64/ARM64. Use the table above or the [release Assets](https://github.com/wWYANG666/SoundIsle-/releases/tag/v0.2.1-preview).

Each package includes its native Java 17 runtime. This version defaults to local accounts and a local backend; Java, Node.js and Maven do not need to be installed separately.

All five platforms passed native application tests including registration, audio playback and restart persistence. OS installation/uninstallation and Gatekeeper acceptance are separate checks. macOS packages are unsigned and not notarized; Windows packages are unsigned.

Check downloads against SHA256SUMS.txt. Source archives contain documentation only; application source remains private.
