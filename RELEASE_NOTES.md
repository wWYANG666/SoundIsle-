# SoundIsle v0.2.1-preview

本次补齐跨平台预览下载。从 **Assets** 选择适合系统和处理器的安装包：

| 系统 | 架构 | 格式 |
| --- | --- | --- |
| Windows | x64 | setup.exe、portable.exe |
| macOS Intel | x64 | DMG、ZIP |
| macOS Apple Silicon | ARM64 | DMG、ZIP |
| Linux | x64 | AppImage、DEB、tar.gz |
| Linux | ARM64 | AppImage、DEB、tar.gz |

共 12 个应用附件以及 `SHA256SUMS.txt`。Windows ARM64 尚未提供原生下载；GitHub 自动生成的源码归档只包含下载文档。

## 运行要求

- 每个包内置对应系统/架构的 Java 17，无需另装 Java、Node.js 或 Maven。
- 默认使用本地账号、本地后端和系统 SoundIsle 配置目录。与上一批次默认云账号的 Windows 包不同。
- 在线平台账号和 AI 配置由用户自行管理。
- macOS 包尚无 Developer ID 签名/公证，首次启动可能被 Gatekeeper 拦截；Windows 安装器同样未签名。
- Linux AppImage 需要 FUSE 支持，也可安装 DEB 或完整解压 tar.gz。

## 修复与验证

- 修复 macOS/Linux 本地音乐路径、特殊字符编码与大小写区分，保留 Windows 盘符及 UNC 兼容。
- 补充跨平台图标、macOS 菜单/窗口恢复、Linux 托盘兼容。
- 保留源码仓库内置 Java 与本地账号能力，生成各架构原生 runtime。
- 五个原生 GitHub runner 均构建成功，并通过页面/桥接、内置 Java、注册、导入、WAV 播放、206 范围响应、退出重登、重启数据保留与后端退出测试。
- 原有前端/浏览器/Java CI 全部通过。
- 构建源码提交：`52b35a44f4fc43c7d0652aa17d9c5b531e9b7970`。
- 私有源码仓库原生构建运行编号：`37879303500`，普通 CI：`37879303450`。

下载归档与 GitHub Actions SHA-256 一致，各发布附件也核对 GitHub 返回摘要。OS 安装、卸载、Gatekeeper 和实际扬声器发声不在 CI 验收范围内。旧版 Release 保留。

## English

Native Windows x64, macOS Intel/Apple Silicon and Linux x64/ARM64 downloads are included. Every package bundles a native Java 17 runtime and uses local accounts/backend by default. All five targets passed native builds and application tests. Check the Assets against SHA256SUMS.txt.

macOS packages are unsigned and not notarized; Windows packages are unsigned. OS installation/uninstall and first-launch Gatekeeper checks remain separate acceptance steps.

