# SMS Workbench Client

**统一完整版 v0.5.1**。每个系统只有一个下载包，新用户和两种旧版用户共用，不再区分 full/public。

本次修复天成充值总开关联动子渠道后批量操作中断的问题，支持充值子渠道独立开关，并在确认清单列出联动范围。子渠道只控制充值，提现查看主渠道行。

## 下载

| 系统 | 统一下载 |
| --- | --- |
| macOS 13+，Apple Silicon / Intel | [下载 macOS 安装包](https://github.com/blake316026-byte/sms-workbench-client/releases/download/v0.5.1/SMS-Workbench-macOS-universal-v0.5.1.dmg) |
| Windows 10/11 x64 | [下载 Windows 客户端](https://github.com/blake316026-byte/sms-workbench-client/releases/download/v0.5.1/SMS-Workbench-Windows-x64-v0.5.1.zip) |

[最新版本说明](https://github.com/blake316026-byte/sms-workbench-client/releases/latest) · [SHA-256 校验值](https://github.com/blake316026-byte/sms-workbench-client/releases/download/v0.5.1/SHA256SUMS-v0.5.1.txt)

## 功能与数据

包含全部后台、监控浮窗、待处理订单、提现审核人员查询、支付通道管理、短信通道管理、留存报表同步及定时任务。

**功能完整，个人配置不附带。** 新用户空白启动，不含开发者的平台、后台地址、账号、密码、登录数据、Google 授权、目标表格或业务数据。自行添加后台、登录和设置留存报表。

老用户升级保留自己的已有配置和持久登录数据。兼容 SMS Success Monitor、SMS Platform Workbench、SMS Workbench；发现多套旧数据时选择一套，不自动混合。网站主动过期或撤销的登录会话仍需重新登录。

## 安装与升级

**macOS：** 退出旧客户端，打开 DMG，运行 **Install SMS Workbench**。安装器识别旧应用和数据；原应用在其他目录时选择原应用。旧程序保留备份。

**Windows 老用户：** 完整解压到新目录，退出原客户端及托盘进程，运行 **Upgrade.cmd** 并选择原客户端 EXE。自动备份、保留数据并升级，不要手动覆盖旧 resources 文件夹。

**Windows 新用户：** 完整解压后打开 **SMS Client / SMS Success Monitor.exe**。无需安装 Node.js，不要只提取 EXE。EXE 沿用旧名称以兼容原快捷方式，不代表功能版本不同。

## 安全提示

macOS 包为临时签名，未经 Apple 公证；Windows 包未使用商业代码签名证书，系统可能提示未知发布者。请核对来源和 SHA-256，通过系统提供的方式允许可信应用，不要关闭安全保护。

仅分发原始安装包，不要分发使用后的用户数据目录或备份。本仓库只发布安装包、说明和验证流程，不含开发源码、私人配置或业务数据。旧版本仅作为历史归档，新装和升级都使用上方统一下载。
