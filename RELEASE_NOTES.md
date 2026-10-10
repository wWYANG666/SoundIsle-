# SoundIsle v0.2.2-preview

本批次将下载版本同步到网站的账号与个人中心功能。

## 更新

- 邮箱验证码注册，GitHub 注册／登录；不接入 QQ 账号注册登录。
- 新增个人中心：头像、昵称、简介、用户名及账号安全。
- 修改密码只能通过当前已验证邮箱收到的验证码，其他旧会话随后失效。
- 支持 PNG、JPEG、WebP 头像，解决实际是 WebP 却命名为 JPG 的图片上传失败；失败后保留资料草稿。
- 下载默认连接 `https://music.123936.xyz`，使用与网站相同的账号。旧本地账号不自动合并，历史下载保留。

## 下载

| 系统 | 架构 | 格式 |
| --- | --- | --- |
| Windows | x64 | setup.exe、portable.exe |
| macOS Intel | x64 | DMG、ZIP |
| macOS Apple Silicon | ARM64 | DMG、ZIP |
| Linux | x64 | AppImage、DEB、tar.gz |
| Linux | ARM64 | AppImage、DEB、tar.gz |

各包内置对应架构的 Java 17，无需另装 Java、Node.js 或 Maven。本地后端可通过 `MUSICFLOW_ACCOUNT_MODE=local` 启用，邮箱注册／改密需配置自己的 SMTP。本机音乐文件留在设备上。

共 12 个应用附件与 `SHA256SUMS.txt`，请核对 SHA-256。Windows ARM64 尚无原生下载；自动源码归档只包含文档，应用源码仓库保持私有。

## 验证范围

原生包使用隔离账号验证启动、内置 Java、登录、导入、播放、退出重登、重启持久化及后端退出。邮箱／GitHub、个人资料和改密流程有独立前端／浏览器／Java／实际 TLS SMTP fixture 测试。测试不向生产用户发信或修改其资料。

构建源码提交：`70296b741326568abba3da29843c0153bface25c`。普通 CI `38018791756` 与五平台原生构建 `38018791687` 全部通过。本地源码验证为 Java 111/111、前端 140/140、生产构建与 lint 通过。

macOS 未签名／公证、Windows 未签名。OS 安装／卸载、Gatekeeper 和实际扬声器验收仍需在用户设备完成。Linux AppImage 需要 FUSE，也可使用 DEB 或完整解压 tar.gz。

## English

This release syncs email/GitHub accounts, profiles, email-code-only password changes and WebP avatars with the website. Packages use hosted accounts by default, include native Java 17 and preserve a configurable local backend. Existing local accounts are separate, and previous downloads remain available. Check SHA256SUMS.txt before running a package.
