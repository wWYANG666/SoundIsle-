# SoundIsle 下载页

[English](#english) | 中文

SoundIsle 是桌面音乐播放器和音乐管理工具。本公开仓库提供安装包和发布说明；[源码仓库](https://github.com/wWYANG666/SoundIsle)保持私有。

## 下载 v0.2.2-preview

[完整发布页](https://github.com/wWYANG666/SoundIsle-/releases/tag/v0.2.2-preview) · [历史版本](https://github.com/wWYANG666/SoundIsle-/releases)

| 系统 | 架构 | 下载 |
| --- | --- | --- |
| Windows | x64 | [安装 EXE](https://github.com/wWYANG666/SoundIsle-/releases/download/v0.2.2-preview/SoundIsle-0.2.2-preview-win-x64-setup.exe) · [便携 EXE](https://github.com/wWYANG666/SoundIsle-/releases/download/v0.2.2-preview/SoundIsle-0.2.2-preview-win-x64-portable.exe) |
| macOS Intel | x64 | [DMG](https://github.com/wWYANG666/SoundIsle-/releases/download/v0.2.2-preview/SoundIsle-0.2.2-preview-mac-x64.dmg) · [ZIP](https://github.com/wWYANG666/SoundIsle-/releases/download/v0.2.2-preview/SoundIsle-0.2.2-preview-mac-x64.zip) |
| macOS Apple Silicon | ARM64 | [DMG](https://github.com/wWYANG666/SoundIsle-/releases/download/v0.2.2-preview/SoundIsle-0.2.2-preview-mac-arm64.dmg) · [ZIP](https://github.com/wWYANG666/SoundIsle-/releases/download/v0.2.2-preview/SoundIsle-0.2.2-preview-mac-arm64.zip) |
| Linux | x64 | [DEB](https://github.com/wWYANG666/SoundIsle-/releases/download/v0.2.2-preview/SoundIsle-0.2.2-preview-linux-amd64.deb) · [AppImage](https://github.com/wWYANG666/SoundIsle-/releases/download/v0.2.2-preview/SoundIsle-0.2.2-preview-linux-x86_64.AppImage) · [tar.gz](https://github.com/wWYANG666/SoundIsle-/releases/download/v0.2.2-preview/SoundIsle-0.2.2-preview-linux-x64.tar.gz) |
| Linux | ARM64 | [DEB](https://github.com/wWYANG666/SoundIsle-/releases/download/v0.2.2-preview/SoundIsle-0.2.2-preview-linux-arm64.deb) · [AppImage](https://github.com/wWYANG666/SoundIsle-/releases/download/v0.2.2-preview/SoundIsle-0.2.2-preview-linux-arm64.AppImage) · [tar.gz](https://github.com/wWYANG666/SoundIsle-/releases/download/v0.2.2-preview/SoundIsle-0.2.2-preview-linux-arm64.tar.gz) |

共 12 个应用附件。Windows ARM64 暂无原生下载。自动生成的源码归档只包含文档，不能作为播放器运行。`v0.2.1-preview` 及所有历史下载保留。

## 本次更新

- 默认连接 `https://music.123936.xyz`，使用与网站相同的邮箱／GitHub 账号。
- 新增个人中心：头像、昵称、简介、用户名及账号安全。
- 修改密码必须使用当前已验证邮箱收到的专用验证码。
- 头像支持 PNG、JPEG、WebP；实际为 WebP 但名称为 JPG 的下载图片也可上传。
- 登录后可同步账号数据；本机音乐文件仍保留在你的设备上。

## 运行说明

- 每个包内置对应系统／架构的 Java 17，无需另装 Java、Node.js 或 Maven。
- 旧本机账号和云账号分开保存，不自动合并。需要本地后端时设置 `MUSICFLOW_ACCOUNT_MODE=local`；本地邮箱注册／改密需要配置自己的 SMTP。
- 配置目录：Windows `%APPDATA%\SoundIsle`；macOS `~/Library/Application Support/SoundIsle`；Linux `$XDG_CONFIG_HOME/SoundIsle` 或 `~/.config/SoundIsle`。
- macOS 未签名／公证，Windows 未签名。Linux AppImage 需要 FUSE，也可选择 DEB 或完整解压 tar.gz。
- OS 安装、卸载、系统权限、Gatekeeper 与实际扬声器验收需在用户设备完成。

## 校验

[下载 SHA256SUMS.txt](https://github.com/wWYANG666/SoundIsle-/releases/download/v0.2.2-preview/SHA256SUMS.txt)，与下载文件的 SHA-256 比较：

```powershell
Get-FileHash .\SoundIsle-0.2.2-preview-win-x64-setup.exe -Algorithm SHA256
```

原生包验收覆盖隔离账号登录、内置 Java、音乐导入／播放、退出重登和重启持久化；邮箱注册和改密另有真实 TLS SMTP fixture 测试。欢迎通过 [Issues](https://github.com/wWYANG666/SoundIsle-/issues)提交问题，并附上系统、架构和版本。

## English

SoundIsle v0.2.2-preview includes Windows x64, macOS Intel/Apple Silicon and Linux x64/ARM64 packages with native Java 17. Downloads use the website's hosted email/GitHub accounts by default, with profile editing, email-code-only password changes and WebP avatar conversion. Existing local accounts are separate; previous downloads remain available.

Check all downloads against SHA256SUMS.txt. Packages are unsigned, and macOS builds are not notarized. Application source remains private; automatic source archives contain download documentation only.
