# SoundIsle 下载页

SoundIsle 是一个桌面音乐播放器项目。本仓库是公开的**下载与发布说明仓库**，不包含程序源代码、用户数据库、浏览器资料、Cookie、账号凭据或 API Key。

## 下载

当前预览版本：**v0.2.0-preview**

- [v0.2.0-preview 发布页](https://github.com/wWYANG666/SoundIsle-Downloads/releases/tag/v0.2.0-preview)
- [所有版本](https://github.com/wWYANG666/SoundIsle-Downloads/releases)

请在发布页的 **Assets** 区域下载安装包。GitHub 自动显示的 `Source code (zip)` 和 `Source code (tar.gz)` 只包含本下载说明仓库的文档，不是 SoundIsle 程序源码，也不是可运行安装包。

计划使用的 Windows x64 文件名：

```text
SoundIsle-0.2.0-preview-win-x64-setup.exe
SoundIsle-0.2.0-preview-win-x64-portable.zip
SHA256SUMS.txt
```

本预览包已完成隔离环境验收；发布页中的 Assets 和 `SHA256SUMS.txt` 是下载依据。

## 运行说明

目标 Windows x64 安装包会内置 Java 17 运行环境，普通用户不需要另外安装 Node.js、Java 或 Maven。此项以发布页中实际上传并验收的安装包为准。

首次启动时，用户在本机注册自己的账号。用户数据库和配置保存在：

```text
%APPDATA%\SoundIsle
```

账号和播放数据默认保存在当前电脑，不会自动同步到其他设备。更换电脑时不会自动带上原电脑的本地数据。

在线音乐平台需要用户使用自己的账号登录或连接自己的登录态；请遵守相应平台的服务条款。AI 功能需要用户在自己控制的后端配置供应商和 API Key，发布包不附带维护者的 Key，也不会要求把个人 Key 提交到仓库。

此预览包未承诺具有官方应用签名。Windows 可能显示未识别发布者提示，用户应从本仓库的 Release 页面下载并核对 SHA-256。

## 源码

源码和开发文档位于私有仓库 `wWYANG666/SoundIsle`。本仓库只负责公开下载入口、版本说明和校验信息。

## 校验下载文件

Windows PowerShell：

```powershell
Get-FileHash .\SoundIsle-0.2.0-preview-win-x64-setup.exe -Algorithm SHA256
Get-FileHash .\SoundIsle-0.2.0-preview-win-x64-portable.zip -Algorithm SHA256
```

将输出的哈希与 Release 中的 `SHA256SUMS.txt` 比较。只有哈希一致时才使用下载文件。

当前校验值：

```text
8ddb98e76ea09d566e3e0f5c0be9d7130023518688496f7c8d57e65ea400d841  SoundIsle-0.2.0-preview-win-x64-setup.exe
06845eb43d3a4b05d057d13ddeeee9d768967a3feee30a0ceb93b7d92d685a23  SoundIsle-0.2.0-preview-win-x64-portable.zip
```

