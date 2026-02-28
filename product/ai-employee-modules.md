# AI 员工模块体系 v2.0

> 状态：草稿，待确认 | 2026-02-27

---

## 核心理念

**「帮你配一套 AI 员工团队，按职能买，用了再付，比雇人便宜 80%。」**

每个模块 = 一个 AI 岗位，有名字、有职责、有价格。
客户选需要的岗位，Renaix 帮他配好跑起来。

---

## 三层模块体系

### 层一：核心模块（必选）

**💬 Assistant · 助理**

所有 AI 员工的中枢和对话入口，买任何模块都必须先有 Assistant。

职责：
- 对话响应：随时问随时答（「今天有几个 lead？」「张三什么情况？」）
- 主动推送：异常/提醒/巡查报告主动发给老板（含 Inspector 功能）
- Cron 后台：定时自动执行任务（刷房源、发日报、巡查数据）
- Mini App 看板：标准 Telegram Mini App，所有模块数据汇总展示

**月费：$300/月**

---

### 层二：基础模块（可选订阅）

**🗓 Scheduler · 日程员**

职责：
- 管理买家/客户/项目的时间表
- 对接 Google Calendar，自动添加日程
- 约好的事自动提醒（「明天 2PM 张三看房」）
- 多方时间协调（找所有人都有空的时间）
- 每天早上发今日待办清单

核心集成：Google Calendar、Apple Calendar、待办事项

**月费：$150/月**

---

**📋 Processor · 文员**

职责：
- 上传合同 PDF → 自动识别并高亮签字/填写位置
- 通话/会议结束后自动生成摘要推送给老板
- 对话中的信息提取存档（联系人、需求、金额、日期）
- 文件归档管理，历史记录随时可查

核心集成：PDF 处理、Supabase 数据存储

**月费：$150/月（含 50 份文件/月，超出 $2/份）**

---

**🎙 Receptionist · 前台**

职责：
- 接听来电，理解来意，回答常见问题
- 接收短信、邮件、Telegram 消息
- 判断紧急程度，自动分级处理
- 无法处理的转交给老板
- 所有来电/来信自动记录存档

核心集成：Retell AI（电话）、Twilio（短信）、Gmail

**月费：$200/月（含 200 次交互/月，超出 $0.5/次）**

---

**📞 Caller · 外呼员**

职责：
- 主动打电话约时间/确认（如：给 Listing Agent 约看房）
- 发短信/邮件跟进（lead 7 次跟进序列）
- 催款、催确认、催回复
- 执行完成后告知老板结果（「已发第 3 封，对方未回」）

核心集成：Bland AI（外呼电话）、Twilio SMS、Gmail

**月费：$200/月（含 100 次外发/月，超出 $1/次）**

---

**🛠 Technician · 技术员**

职责：
- 建网站（SEO 优化 + 强 CTA）
- 定制 Telegram Mini App（替代客户现有工具）
- 搭自动化流程
- 建数据库结构
- 后续维护和小改动

注：非一次性交付，含月度 hosting 和维护

**Setup Fee + $200/月（hosting + 维护，大改动另报价）**

---

### 层三：专业模块（按需定制）

不预设固定产品，根据客户具体需求单独评估和报价。

常见方向（举例）：
- 法务：合同 review、条款解读
- 记账：收支整理、发票追踪、对账报表
- 研究：市场调研、竞品分析、法规查询
- 推广：内容发布、评价管理、本地 SEO

**按需报价，单独定价**

---

## 定价结构

**Setup Fee（一次性）**
```
$1,500 - $3,000
视客户规模和模块数量，覆盖建设成本
```

**月费（按模块叠加）**

| 模块 | 月费 | 备注 |
|---|---|---|
| Assistant | $300 | 必选，含 Mini App |
| Scheduler | $150 | — |
| Processor | $150 | 超 50 份 $2/份 |
| Receptionist | $200 | 超 200 次 $0.5/次 |
| Caller | $200 | 超 100 次 $1/次 |
| Technician | $200 | hosting + 维护 |
| 专业模块 | 按需 | 单独报价 |

**最低承诺：3 个月**

---

## 行业套餐参考

**🏗 GC 套餐**
Assistant + Receptionist + Caller + Scheduler
Setup $2,000 + 月费 $850/月

**🏠 房产经纪套餐**
Assistant + Caller + Scheduler + Receptionist + Processor + Technician
Setup $2,000 + 月费 $1,150/月

**🔧 HVAC / Plumber 套餐**
Assistant + Receptionist + Caller
Setup $1,500 + 月费 $700/月

---

## Renaix 自用情况

| 模块 | 状态 |
|---|---|
| Assistant | ✅ 全天候（Elon） |
| Scheduler | ❌ 待建 |
| Processor | ✅ 部分（memory 整理） |
| Receptionist | ⚠️ Maya Bot 建了，API key 待修 |
| Caller | ❌ 待建 |
| Technician | ✅ renaix-library + Maya Bot |

---

## 技术栈

| 模块 | 核心技术 |
|---|---|
| Assistant | Claude + Supabase + Cloudflare Workers + Telegram Mini App |
| Scheduler | Google Calendar API + Supabase |
| Processor | Deepgram（转录）+ Claude + PDF 解析 |
| Receptionist | Retell AI（电话）+ Telegram Bot |
| Caller | Bland AI（外呼）+ Twilio SMS |
| Technician | v0.dev + Vercel / Telegram Mini App + Vite + Supabase |

统一底层：**Supabase（数据）+ Cloudflare Workers（部署）+ Claude（AI）**

---

## 待确认事项

- [ ] 模块名称最终确认（特别是 Processor 是否还有更好的名字）
- [ ] 专业模块的具体品类和定价逻辑
- [ ] 超额使用的计量方式是否对客户够透明
- [ ] Technician 的 Setup Fee 如何和其他模块的整体 Setup Fee 合并计算
- [ ] 最低承诺期（3 个月）是否合适

---

*文档由 Elon North 整理 · 基于 2026-02-27 与董事长的讨论*
