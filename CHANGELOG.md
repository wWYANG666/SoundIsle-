# 更新日志

## v0.2.0-preview

首次公开预览发布说明（Windows x64）。

- 提供 Windows x64 安装包和可选免安装压缩包（文件在 GitHub Release Assets 中维护）。
- 安装包和免安装包内置 Java 17，普通用户无需安装 Node.js、Java 或 Maven。
- 默认使用本机账户和本机数据目录 `%APPDATA%\SoundIsle`。
- 不包含维护者的 AI API Key、第三方平台 Cookie、账号数据库或其他个人数据。
- 在线音乐平台登录由用户自行完成，用户应遵守平台规则。
- 预览版本未承诺官方应用签名。

### 发布状态

已完成隔离环境验收：无系统 Java/Node/Maven 时使用内置 Java，首次注册、WAV 导入、播放、退出重登、关闭重启后本地数据保留均通过；NSIS 载荷和免安装包均通过。未覆盖真实 Windows 安装向导交互、卸载和代码签名。

