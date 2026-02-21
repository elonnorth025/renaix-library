---
naics: "4849"
industry: "Truck Transportation / Support Activities for Transportation"
slug: "Carrier-Detention-Accessorial-Claims-AI"
title: "Carrier Detention & Accessorial Claims AI"
replaces_role: "Back-Office Accessorial Claims Specialist"
salary_replaced: 52000
arr_potential: high
score: 8.5
created: "2026-02-17"
status: draft
---

# Carrier Detention & Accessorial Claims AI

## 痛点

中小型货运公司（5–200辆卡车）每天都在丢钱：司机在收发货地点等待超过免费时间（2小时）后，公司本可以向经纪/货主索赔 Detention Fee（$75–100/小时），但由于后台人员不够、文件繁琐、跟进不及时，**平均只有 40–60% 的合法附加费被实际追回**。每家中型承运商每年因此损失 $50,000–$300,000 的应收收入。

## 替代岗位

**Back-Office Accessorial Claims Specialist**  
年薪：$48,000–$56,000  
职责：每天手动比对 ELD 时间戳与 BOL、识别 Detention/TONU/Layover 事件、起草索赔信、发邮件、催款、处理拒付

## AI 工作流

1. **自动数据摄入**  
   通过 API 接入 ELD 平台（Samsara / Motive / KeepTruckin）+ TMS（McLeod / Aces / Turvo），实时拉取司机到达/离开时间戳

2. **事件识别与计算**  
   自动检测 Detention、TONU（卡车被叫取消）、Layover、Lumper 费用、Fuel Surcharge 差额等可索赔事件，按合同费率计算金额

3. **自动生成 & 发送索赔**  
   根据货主/经纪联系人自动起草带 ELD 证据的索赔邮件，发送并进入追踪队列

4. **分级跟进与争议处理**  
   15/30/45 天自动跟进，拒付则升级附上更完整证据，超过阈值标记给人工

## 护城河

- 与主流 ELD（Samsara、Motive 占市场 60%）深度 API 集成，新进者需重新谈判合作
- 每处理一批索赔，模型学习哪些货主/经纪最容易推诿，优化跟进策略
- 一旦接入承运商 TMS，迁移成本极高（数据绑定）
- 直接量化 ROI（每月多回收 $3,000–$15,000），续费率高

## 市场规模

- 美国持有 MC 号的货运承运商约 **500,000 家**
- 5 辆卡车以上、有稳定后台需求的约 **150,000 家**
- 每家平均每年可追回附加费 $30,000–$150,000
- TAM：保守估计 **$1.8B+** 美国未追回的附加费收入（年）
- SaaS TAM：$150,000 家 × $299/月 × 12 = **$540M ARR**

## 定价

| 计划 | 车辆数 | 月费 |
|------|--------|------|
| Starter | 5–20 辆 | $199/月 |
| Growth | 21–75 辆 | $399/月 |
| Fleet | 76+ 辆 | $799/月 |

**ROI 主张：** 首月追回金额通常覆盖 6–12 个月订阅费

## 竞争分析

- TMS 内置报告：只显示数据，不自动追款
- 人工外包服务：$500–$2,000/月，慢且不透明
- **直接竞争：几乎为零**（2026 年 2 月仍是空白市场）

## GTM

- **目标客户：** 有 10–100 辆车的独立承运商，Owner-Operator Fleet
- **切入点：** 货运 Facebook 群组、OOIDA（美国独立卡车司机协会）、TruckingInfo 论坛
- **钩子：** "上传过去 90 天 ELD 数据，免费告诉你漏了多少钱"
- **合作渠道：** Samsara 应用市场、McLeod 生态系统

## 评分明细

| 维度 | 评分 |
|------|------|
| 痛点清晰度 | 9/10 |
| 市场规模 | 8/10 |
| 技术可行性 | 9/10 |
| 竞争空白 | 9/10 |
| 变现路径 | 8/10 |
| **综合** | **8.5/10** |
