# SoundIsle v0.2.3-preview

本批次加入程序内 GitHub 更新功能，同时保留网站的账号与个人中心功能。

## 更新

- 显示 GitHub 官方下载地址；手动刷新检查，或在启动时检查。
- 下载匹配当前系统、架构和安装方式的更新包，显示进度，可取消、重试。
- 下载大小与 SHA-256 必须匹配才显示可用；跨重启恢复下载记录，打开前再次校验。
- Windows 安装版确认后退出并打开安装器；便携版和 macOS／Linux 提供更新文件和目录入口。
- 启动检查可关闭，不自动下载或安装。旧版首次需手动升级到此版本，后续可在程序内检测和下载。

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

应用源码提交：`53dced19905fca85162f68b5705a306fc85d20cf`，普通 CI `38023298134` 全部通过。macOS／Linux 原生包来自 `38023298454` 中各自成功的任务；Windows 使用 `38024016837` 重新验收。后续源码提交 `64d1661ca85110485b5190fe9fea9bed9ddeb224` 只调整测试截图和构建目标选择，不改变应用代码。更新专项覆盖版本／格式校验、流式下载、取消、错误、文件校验、目录及重启，以及真实 GitHub Release 资产重定向和校验文件下载。macOS Intel 构建曾遇到 runner 的 `hdiutil` 资源忙，重新运行后通过并上传了对应附件。

macOS 未签名／公证、Windows 未签名。OS 安装／卸载、Gatekeeper 和实际扬声器验收仍需在用户设备完成。Linux AppImage 需要 FUSE，也可使用 DEB 或完整解压 tar.gz。

## English

This release syncs email/GitHub accounts, profiles, email-code-only password changes and WebP avatars with the website. Packages use hosted accounts by default, include native Java 17 and preserve a configurable local backend. Existing local accounts are separate, and previous downloads remain available. Check SHA256SUMS.txt before running a package.
