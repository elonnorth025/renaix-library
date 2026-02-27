# Renaix 客户流程管理（CRM）

> 版本：v2.0 | 更新于 2026-02-27

---

## 漏斗阶段（6 阶段）

```
LEAD → PROSPECT → DISCOVERY → SETUP → PILOT → CLIENT
```

### 两种进入路径

```
Outbound（冷外联/介绍）:
LEAD → PROSPECT → DISCOVERY → SETUP → PILOT → CLIENT

Inbound（网站预约）:
直接进入 DISCOVERY → SETUP → PILOT → CLIENT
```

---

## 各阶段详解

### Stage 1: LEAD（线索）
- **定义：** 目标客户，还没有任何接触
- **来源：** Facebook 群组、Google Maps 差评、LinkedIn、朋友推荐
- **退出条件：** 建立第一次实质性接触
- **文件夹：** `pipeline/leads/`

---

### Stage 2: PROSPECT（跟进中）
- **定义：** 已接触，正在建立信任，还没约到 Discovery
- **目标：** 约到 Discovery Call
- **退出条件：** Discovery Call 时间已确认
- **文件夹：** `pipeline/prospects/`

---

### Stage 3: DISCOVERY（发现访谈）
- **定义：** Discovery Call 已完成或进行中
- **内容：** 深度访谈，挖掘痛点，了解现有工具/流程/预算
- **收费：** $0（当前 Freemake 阶段）

**退出交付物：一页纸方案（含报价）**

一页纸内容：
1. 你现在的核心痛点（用客户自己说的话）
2. Maya 怎么解决（具体功能描述）
3. 预期结果（省多少时间/电话/成本）
4. 报价：Setup Fee + 月费
5. 下一步：「如果方向对，我们下周开始 Setup」

**退出条件：** 一页纸方案发出，客户回复意向
**文件夹：** `pipeline/discovery/`

---

### Stage 4: SETUP（搭建与验收）
- **定义：** 客户认可方案，系统搭建阶段
- **周期：** 3-7 个工作日
- **文件夹：** `pipeline/setup/`

**收费结构（两笔）：**

```
客户确认方案
    ↓
付款 Setup Fee 50% → 开始搭建
    ↓
系统上线，客户验收通过
    ↓
付款 Setup Fee 剩余 50% → 进入 PILOT
```

**现阶段 Freemake：** Setup Fee = $0，两笔均免，但节点保留（以后收费直接启用）

**两条业务线的 SETUP 交付：**

| 业务线 | SETUP 交付内容 |
|---|---|
| GC / AI 员工 | 建好 Maya 系统，客户验收上线 |
| 咨询线 | 交付详细方案文档，确认实施计划 |

**退出条件：** 客户验收通过，尾款付清（或 Freemake 阶段口头确认）

---

### Stage 5: PILOT（试运行）
- **定义：** 系统正式运行，收集真实数据
- **周期：** 30 天
- **收费：** $0（验证价值阶段）

**里程碑：**
- Day 1：系统上线，客户开始使用
- Day 15：发送中期报告（展示数据，不提付费）
- Day 25：发送价值预测报告（量化节省的时间/成本）
- Day 30：发送月度报告 → 自然触发 Closing 对话

**转化目标：** 55%+ 进入 CLIENT

**退出条件：** 客户说「我要继续」，签月费合同
**文件夹：** `pipeline/pilot/`

---

### Stage 6: CLIENT（付费客户）
- **定义：** 已签约，长期付费服务
- **收费：** 月费（$2,000-4,000/月，视业务线和规模）
- **文件夹：** `clients/NNN-姓名/`（三位数序号）

---

## 核心规则

1. **同时最多 3 个 Pilot** — 资源有限，优先痛点清晰、决策快的客户
2. **Discovery 结束必须定好 Setup 开始日期** — 没有日期 = 没有承诺 = 退回 PROSPECT
3. **Setup Fee 不能全款预付** — 拆成 50/50，保护双方
4. **Inbound 客户跳过 LEAD/PROSPECT** — 直接进 DISCOVERY

---

## 当前 Pipeline（2026-02-27）

| 姓名 | 公司/行业 | Stage | 下一步 | 日期 |
|---|---|---|---|---|
| Edwin Li | Square Builders Group / GC | DISCOVERY | 周二见面，发一页纸方案 | 2026-03-03 |
| 小语 | 房产经纪 | LEAD | 约 Discovery Call，确认工具名称 | TBD |
| 邱涵 | 跨境供应链 | PROSPECT | 三月初跟进，约 Discovery | 2026-03 |
| 吉松 | SF 创业 | LEAD | 保持联系，观察合作机会 | — |

---

## 健康指标

| 指标 | 目标 |
|---|---|
| 每月新增 LEAD | 5+ |
| DISCOVERY → SETUP 转化率 | 50%+ |
| PILOT → CLIENT 转化率 | 55%+ |
| MRR 目标（Q2 2026） | $10,000 |
| MRR 目标（Q4 2026） | $30,000 |

---

## 文件夹结构

```
pipeline/
  leads/          # Stage 1
  prospects/      # Stage 2
  discovery/      # Stage 3
  setup/          # Stage 4
  pilot/          # Stage 5
clients/          # Stage 6（付费后移入）
  001-xxx/
  002-xxx/
```

每个客户一个文件夹，内含对应阶段的 .md 文件，随推进更新。
