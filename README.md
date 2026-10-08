# SoundIsle 下载页

SoundIsle 是桌面音乐播放器和本地音乐管理工具。
本仓库只提供 Windows 下载文件和发布说明，不包含源代码、用户数据或凭据。

## 下载

当前预览版本：**v0.2.0-preview**

- [v0.2.0-preview 发布页](https://github.com/wWYANG666/SoundIsle-Downloads/releases/tag/v0.2.0-preview)
- [所有版本](https://github.com/wWYANG666/SoundIsle-Downloads/releases)

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
