# SoundIsle v0.2.0-preview

这是 SoundIsle 的 Windows x64 预览版本。

## 下载文件

从本 Release 的 **Assets** 下载：

- `SoundIsle-0.2.0-preview-win-x64-setup.exe`：Windows 安装程序。
- `SoundIsle-0.2.0-preview-win-x64-portable.zip`：可选免安装压缩包，需解压完整目录后运行。
- `SHA256SUMS.txt`：下载文件 SHA-256 校验值。

不要下载页面自动生成的 `Source code (zip)` 或 `Source code (tar.gz)` 来运行程序；它们只包含本仓库的下载文档。

## 运行前说明

发布包包含 Java 17 运行环境，用户不需要单独安装 Node.js、Java 或 Maven。

程序首次启动后，用户在自己的电脑上注册本地账号。用户数据库和配置保存在 `%APPDATA%\SoundIsle`，默认不会跨设备同步。

第三方音乐平台需要用户使用自己的账号登录或连接自己的登录态。AI 功能需要在用户自己控制的后端配置 API Key；安装包和本公开仓库不包含任何维护者 Key。

该预览包未签名或未承诺官方应用签名，Windows 可能显示安全提示。请从本 Release 下载并核对 `SHA256SUMS.txt`。

## 验收记录

发布前由维护者填写以下项目：

- [x] 在隔离的无 Java/Node/Maven 环境运行发布载荷
- [x] 首次注册账号并确认本地 profile 数据可用
- [x] 导入 WAV、播放、退出重登并确认重启后数据保留
- [x] 安装包和免安装包 SHA-256 与 `SHA256SUMS.txt` 一致
- [ ] 真实 Windows 安装向导、卸载流程和代码签名

