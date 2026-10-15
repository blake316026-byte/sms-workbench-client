# SMS Workbench Client

独立客户端分发仓库，与此前的精简版仓库分开。当前版本 **v0.4.1**。

保留工作台、全部后台 / 国家总计、监控浮窗、全平台待处理订单、提现审核人员查询和支付通道管理。**不包含留存报表同步、Google 表格授权及留存定时任务。**

安装包不预置平台、后台地址、账号、密码、登录会话或业务数据。新用户空白启动，自行添加后台并登录；老用户按下表选择对应升级包，沿用自己的本机数据。

## 下载

| 原有客户端 | macOS 13+，Apple Silicon / Intel | Windows 10/11 x64 |
| --- | --- | --- |
| SMS Success Monitor 旧完整版 | [full 升级包](https://github.com/blake316026-byte/sms-workbench-client/releases/download/v0.4.1/SMS-Upgrade-full-macOS-universal-v0.4.1.dmg) | [full 升级包](https://github.com/blake316026-byte/sms-workbench-client/releases/download/v0.4.1/SMS-Upgrade-full-Windows-x64-v0.4.1.zip) |
| SMS Platform Workbench / 后台工作台（公开版），或新用户 | [public 升级包](https://github.com/blake316026-byte/sms-workbench-client/releases/download/v0.4.1/SMS-Upgrade-public-macOS-universal-v0.4.1.dmg) | [public 升级包](https://github.com/blake316026-byte/sms-workbench-client/releases/download/v0.4.1/SMS-Upgrade-public-Windows-x64-v0.4.1.zip) |

**两类包功能完全相同，仅兼容的旧版应用标识和数据目录不同。不要交叉升级，两套数据不会自动合并。** 新用户推荐 public。

[全部下载与版本说明](https://github.com/blake316026-byte/sms-workbench-client/releases/tag/v0.4.1) · [SHA-256 校验值](https://github.com/blake316026-byte/sms-workbench-client/releases/download/v0.4.1/SHA256SUMS-v0.4.1.txt)

## 安装与升级

### macOS

1. 完全退出旧客户端，打开对应 DMG。
2. 将同名应用拖入 Applications，替换旧应用。若旧程序在其他位置，请替换原位置的同名应用。
3. 不要删除用户数据目录或使用清理工具卸载旧版。

### Windows

1. 将 ZIP 完整解压到一个新文件夹，退出旧客户端及托盘进程。
2. **老用户双击 `Upgrade.cmd`，选择旧客户端 EXE。不要先覆盖旧程序的 `resources` 文件夹。** 升级程序确认后先备份原数据和程序，再进行替换；选错包型会拒绝升级。
3. 新用户直接打开 `SMS Client` 文件夹中的 `SMS Success Monitor.exe`。这是免安装版，不能只提取 EXE，无需另装 Node.js。

升级备份位置会在完成窗口中显示。若组织策略阻止检查旧客户端进程，请联系管理员，不要绕过策略或直接覆盖旧资源。

## 数据与权限

| 系统 | full 数据目录 | public 数据目录 |
| --- | --- | --- |
| macOS | `~/Library/Application Support/SMS Success Monitor` | `~/Library/Application Support/SMS Platform Workbench` |
| Windows | `%APPDATA%\sms-success-monitor-windows` | `%APPDATA%\SMS Platform Workbench` |

升级沿用原有账号、配置和浏览器存储，但后台主动过期、撤销登录或要求验证码时仍需重新登录。macOS 13 旧版部分页面使用临时会话，无法恢复旧版退出时已经丢失的 Cookie。

支付通道变更仍需确认清单，支持分别批量开启 / 关闭充值和提现。不要求操作原因，不保存客户端支付操作记录；后台自身记录不受影响。未查询成功或没有权限的平台不能参与批量操作。

仅分发本仓库原始 DMG / ZIP。不要分发使用后的数据目录或升级备份。客户端不提供后台账号，也不绕过后台权限。

## 验证与限制

已完成升级数据兼容、模拟后台、Electron 界面及安装包内容检查。测试使用隔离数据，不涉及生产支付变更。

**Windows 安装流程尚未在 Windows 实机验证**，建议先在单台电脑验证升级结果，再推广安装。

macOS 包为临时签名，未经过 Apple 公证；Windows 包未使用商业代码签名证书，系统可能提示未知发布者。请核对下载来源和 SHA-256，仅在确认可信后通过系统提供的方式允许打开，不要关闭系统安全保护。

本仓库仅用于发布安装包和说明，不包含开发源码、私人配置或业务数据。
