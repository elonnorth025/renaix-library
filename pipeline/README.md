# Renaix 客户流程管理

## 漏斗阶段（5 阶段）

```
LEAD → PROSPECT → DISCOVERY → PILOT → CLIENT
  冷   →  接触中  →  访谈中   →  试用  →  付费
```

---

### Stage 1: LEAD（线索）
- **定义：** 还没接触过，只是目标或被推荐的人
- **来源：** Facebook 群组、Google Maps、LinkedIn、朋友推荐
- **目标：** 建立第一次接触
- **文件夹：** `pipeline/leads/`

### Stage 2: PROSPECT（潜在客户）
- **定义：** 已接触过，有初步兴趣，正在跟进中
- **目标：** 预约发现访谈
- **文件夹：** `pipeline/prospects/`

### Stage 3: DISCOVERY（发现访谈）
- **定义：** 已完成或正在进行发现访谈，了解痛点
- **目标：** 确认是否值得进 Pilot；拿到具体下一步承诺
- **关键问题：** 每天几通电话？最烦哪类沟通？省 3 小时用在哪？
- **文件夹：** `pipeline/discovery/`

### Stage 4: PILOT（试用/Freemake）
- **定义：** 进入免费试用期，Maya 开始为他工作
- **周期：** 30 天
- **里程碑：**
  - Day 1：系统配置完成
  - Day 15：中期报告（数据展示，不提付费）
  - Day 25：价值预测报告
  - Day 30：月度报告 → 触发 Closing
- **目标转化率：** 55%+
- **文件夹：** `pipeline/pilot/`

### Stage 5: CLIENT（付费客户）
- **定义：** 已签约付费
- **文件夹：** `clients/`
- **命名规则：** `clients/NNN-姓名/`（NNN 三位数序号）

---

## 文件模板

每个联系人一个文件夹，内含 `LEAD.md` / `PROSPECT.md` / `DISCOVERY.md` / `PILOT.md`，随阶段推进更新。

**必填字段：**
- 姓名、公司、行业
- 当前状态（Stage）
- 来源
- 关键痛点
- 下一步行动（带截止日期）
- Timeline（每次接触记录）

---

## 当前 Pipeline 概览

> 更新于 2026-02-27

| 姓名 | 公司 | 行业 | Stage | 下一步 |
|---|---|---|---|---|
| Edwin Li | Square Builders Group | GC 建筑 | DISCOVERY | 周二（3/3）见面 |
| 小语 | TBD | 房产经纪 | LEAD | 准备方案 |
| 邱涵 | TBD | 跨境供应链 | PROSPECT | 三月初跟进 |
| 吉松 | TBD | SF 创业 | LEAD | 保持联系 |

---

## 健康指标

- **目标：** 每月新增 5+ LEAD，转化 1+ CLIENT
- **Pilot 转化率目标：** 55%+
- **MRR 目标：** $10k（2026 Q2）
