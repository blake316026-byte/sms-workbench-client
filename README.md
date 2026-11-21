# SMS Workbench Client

**统一完整版 v0.5.5**。每个系统只有一个下载包，新用户和两种旧版用户共用，不再区分 full/public。Windows 为未签名版。

本次修复 macOS 网页“汇入／上传”点击无反应，恢复系统文件选择框。新增待处理订单创建时间、等待时长筛选和提现挂单 TG 报警，可勾选报警平台。保留天成定期 Google 验证恢复、财务查询、后台自动登录及全部已发布功能。支付或配置操作不自动提交、不自动重试。

## 下载

| 系统 | 统一下载 |
| --- | --- |
| macOS 13+，Apple Silicon / Intel | [下载 macOS 安装包](https://github.com/blake316026-byte/sms-workbench-client/releases/download/v0.5.5/SMS-Workbench-macOS-universal-v0.5.5.dmg) |
| Windows 10/11 x64 | [下载 Windows 客户端](https://github.com/blake316026-byte/sms-workbench-client/releases/download/v0.5.5/SMS-Workbench-Windows-x64-v0.5.5.zip) |

[最新版本说明](https://github.com/blake316026-byte/sms-workbench-client/releases/latest) · [SHA-256 校验值](https://github.com/blake316026-byte/sms-workbench-client/releases/download/v0.5.5/SHA256SUMS-v0.5.5.txt)

## 功能与数据

包含全部后台、监控浮窗、待处理订单、提现审核人员查询、支付通道管理、短信通道管理、留存报表同步及定时任务。

**功能完整，个人配置不附带。** 新用户空白启动，不含开发者的平台、后台地址、账号、密码、登录数据、Google 授权、目标表格或业务数据。自行添加后台、登录和设置留存报表。

老用户升级保留自己的已有配置和持久登录数据。兼容 SMS Success Monitor、SMS Platform Workbench、SMS Workbench；发现多套旧数据时选择一套，不自动混合。网站主动过期或撤销的会话需要重新认证；已配置有效凭据并开启自动登录的平台会尝试恢复，需要人工处理的安全验证仍会暂停。

## 安装与升级

**macOS：** 退出旧客户端，打开 DMG，运行 **Install SMS Workbench**。安装器识别旧应用和数据；原应用在其他目录时选择原应用。旧程序保留备份。

**Windows 老用户：** 完整解压到新目录，退出原客户端及托盘进程，运行 **Upgrade.cmd** 并选择原客户端 EXE。自动备份、保留数据并升级，不要手动覆盖旧 resources 文件夹。

**Windows 新用户：** 完整解压后打开 **SMS Client / SMS Success Monitor.exe**。无需安装 Node.js，不要只提取 EXE。EXE 沿用旧名称以兼容原快捷方式，不代表功能版本不同。

## 安全提示

macOS 包为临时签名，未经 Apple 公证；Windows 包未使用商业代码签名证书，系统可能提示未知发布者或阻止运行。先核对来源和 SHA-256。

### Windows 智能应用控制拦截

若提示“智能应用控制已阻止可能不安全的应用”，并且你信任本包、理解风险且有设备管理权限，可手动进入：

**Windows 安全中心 → 应用和浏览器控制 → 智能应用控制设置 → 关闭**，确认提示后重开客户端。

这会影响整台电脑，不是只放行本应用；目前没有单个应用例外。不要关闭 Defender 实时保护或防火墙。能否重新开启取决于 Windows 更新和设备状态，以本机提示为准，旧系统可能需要重置。不愿降低防护时请保留开启，不运行未签名包。组织设备请联系管理员，客户端不会自动关闭安全保护。

[完整说明与微软官方指引](WINDOWS.md)。不同的 SmartScreen 或病毒检测提示不要套用此方法。

仅分发原始安装包，不要分发使用后的用户数据目录或备份。本仓库只发布安装包、说明和验证流程，不含开发源码、私人配置或业务数据。旧版本仅作为历史归档，新装和升级都使用上方统一下载。
