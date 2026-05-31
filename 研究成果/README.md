# 研究成果目录

本目录用于沉淀 GoPay / Android / 协议逆向相关的可复现研究成果。

当前公开仓库只保留第一版基础代码；这里的研究笔记可以作为二开参考。有能力的大佬可以基于这些研究成果继续深度开发，例如扩展接码平台、优化设备画像、改造并发队列、增强异常处理或复现更多协议链路。

## 当前文档

- `gopay_android_2.10.0_research.md`：GoPay Android 2.10.0 主研究笔记。
- `asset_inventory.md`：资产、设备、脚本、凭据/状态库存。
- `update_log.md`：后续更新日志。

## 维护规则

每次出现新的有效发现、绕过方法、脚本、证据文件、失败路径或环境状态变化，都要同步更新本目录对应文档；不要只把结论留在对话里。

- 2026-05-30：新增 GoPay 纯协议 signup Basic UUID、`gopay\u003aconsumer\u003aapp` WAF escape、post-signup login token 阻塞记录，详见 `gopay_android_2.10.0_research.md` 与 `asset_inventory.md`。

- 2026-05-30：纯协议 `pure_pin_only.py --pin 736294` 已完成注册/刷新登录态/设置 PIN 闭环，成功证据 `android_gopay_2.10.0/protocol/runs/pure_pin_only_attempt1_20260530_054154.json`。
- 2026-05-30：补强 PIN 完成校验，profile 只读复验返回 `is_pin_setup=true`；脚本新增 `profile_after_pin_setup` 步骤。
