# SoundIsle v0.2.0-preview.20261009

2026-10-09 Windows x64 预览发布批次。应用内版本仍显示 `0.2.0-preview`。

## 下载文件

从本 Release 的 **Assets** 下载：

- `SoundIsle-0.2.0-preview-win-x64-setup.exe`：Windows x64 安装包。
- `SoundIsle-0.2.0-preview-win-x64-portable.exe`：单文件便携启动程序。
- `SHA256SUMS.txt`：这两个文件的 SHA-256 校验值。

GitHub 自动生成的 `Source code (zip)` / `Source code (tar.gz)` 仅包含下载页文档，不是播放器。原 `v0.2.0-preview` 附件保留。

## 本次更新

- 修复本地音乐文件路径和 URL 编码，包括特殊字符、Windows 盘符、UNC 及 POSIX 路径。
- 使用系统音乐目录，补充跨平台图标、macOS 菜单和窗口恢复、Linux 托盘兼容处理。
- 适配代码增加 Windows ARM64、macOS Intel / Apple Silicon、Linux x64 / ARM64 构建目标。

**本次实际下载只有 Windows x64。macOS、Linux 和 Windows ARM64 尚未完成原生构建与验收，没有对应附件。**

## 运行要求

- 默认连接统一账号服务器 `https://music.123936.xyz`，该模式不需要安装 Java。
- 本次包携带后端 JAR，未内置 JRE。可选本地账号模式需要 Java 17 或更高版本，并通过 `JAVA_HOME` 或 `PATH` 提供 `java`。
- 用户不需要安装 Node.js 或 Maven。
- Windows 本地配置保存在 `%APPDATA%\SoundIsle`；本地音频仍保留在用户电脑。
- 在线音乐平台由用户使用自己的账号连接；默认账号和 AI 服务由服务器管理。
- 安装包未签名，请核对同一发布批次的校验文件。

## 验证结果

- Windows x64 目录包：启动、页面、preload 桥接、随机端口 Java 健康检查通过。
- 真实 WAV 播放、特殊字符文件路径、HTTP 206 范围响应通过。
- 本地音频和播放相关专项测试：15 项通过。
- 发布载荷与已验证目录包的 `app.asar` 和后端 JAR 校验值一致。
- 便携 EXE 已解压并启动。完整自动化验收采用同内容的目录包；NSIS 外壳无法向 Playwright 转发所需的调试输出。
- 未执行真实安装向导、卸载和覆盖升级测试。其他系统需在对应系统完成验收。

## SHA-256

```text
A84F76D6952CE257F5C7B4BB8445FF529CA5D4976D9ED1B994AC781DE9738313  SoundIsle-0.2.0-preview-win-x64-setup.exe
D0CCF1F6C6BACA95462408878100094B207C3307DDA5C0A1307DE1DF2AE998D9  SoundIsle-0.2.0-preview-win-x64-portable.exe
```

