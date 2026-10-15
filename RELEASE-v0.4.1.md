# v0.4.1

独立分发版本，旧精简版仓库不受影响。

- 提供 macOS 通用架构和 Windows x64 客户端。
- 保留工作台、全部后台 / 国家总计、监控浮窗、待处理订单、审核人员查询、支付通道管理。
- 不包含留存报表同步、Google 表格授权和留存定时任务。
- 不预置平台、后台地址、账号或业务数据，新用户空白启动。
- full 对应旧 SMS Success Monitor；public 对应旧 SMS Platform Workbench，两种包功能相同。新用户推荐 public。
- 老用户使用匹配包型，保留本机已有配置和登录存储；服务器已过期的登录仍需重新授权登录。

## 升级注意

macOS：先退出旧客户端，再用同名应用替换旧程序，不要删除用户数据。

Windows：完整解压到新文件夹，退出旧客户端，运行 `Upgrade.cmd` 并选择旧 EXE。升级程序先备份，再替换。不要先手工覆盖旧 `resources` 文件夹。新用户直接运行 `SMS Client/SMS Success Monitor.exe`。

## 验证边界

已完成隔离数据兼容、模拟后台、Electron 界面和最终安装包内容检查。Windows 原生安装流程尚未实机验证，建议先单机试用。未执行生产支付操作。

安装包未经过商业代码签名 / Apple 公证。核对来源及 SHA-256，不要关闭系统安全保护。

校验文件列出的四个文件名与本页下载资产一致；将下载包与校验文件放在同一目录，可运行 `shasum -a 256 -c SHA256SUMS-v0.4.1.txt` 校验。Windows 可使用 `Get-FileHash -Algorithm SHA256` 比对。
