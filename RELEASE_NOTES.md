# SoundIsle v0.2.4-preview

本批次修正个人中心的账号规则：昵称可以编辑，登录用户名注册后不能修改。

## 更新

- 账号页只读显示登录用户名；删除新用户名、改名确认密码／二次验证码及提交按钮。
- 昵称仍在“个人资料”中编辑，可以重复；修改昵称不改变登录名、账号 ID、会话和音乐数据。
- 旧改名 API 返回 403，后端实体用户名字段不可更新，旧客户端也无法继续改名。
- 删除仅用于改名的 GitHub 身份确认授权，保留普通 GitHub 登录／绑定。

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

应用源码提交：`d937bb2e00680d13e55ca0fc4f02a87b43a70785`，普通 CI `38026632496`，五平台原生包与更新验收 `38026632429`。用户名专项覆盖昵称保存、原用户名登录、会话保持、音乐归属、同昵称账号、并发改名拒绝、ORM 防误改、禁用旧 GitHub 改名授权及重启持久化。

macOS 未签名／公证、Windows 未签名。OS 安装／卸载、Gatekeeper 和实际扬声器验收仍需在用户设备完成。Linux AppImage 需要 FUSE，也可使用 DEB 或完整解压 tar.gz。

## English

This release syncs email/GitHub accounts, profiles, email-code-only password changes and WebP avatars with the website. Packages use hosted accounts by default, include native Java 17 and preserve a configurable local backend. Existing local accounts are separate, and previous downloads remain available. Check SHA256SUMS.txt before running a package.
