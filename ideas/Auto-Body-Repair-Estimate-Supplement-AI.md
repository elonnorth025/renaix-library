---
naics: "8111"
sector: "Other Services - Auto Body / Paint Shops"
slug: "Auto-Body-Repair-Estimate-Supplement-AI"
title: "Auto Body Supplement Negotiator AI"
created: "2026-03-01"
status: "new"
---

# Auto Body Supplement Negotiator AI

## 替代岗位
汽车钣金修复店的 **Supplement Writer / Insurance Liaison**（估损补充谈判专员）

## 核心痛点
保险公司初始估损（Initial Estimate）几乎从不涵盖实际维修所需的全部工作。店主需要人工拍照、写补充报告、反复和调查员扯皮，每辆车耗时 2-4 小时，积压严重时直接导致交车延误和客户投诉。

## AI 工作流
1. 维修技师拍摄拆解照片上传 → AI 自动识别受损零件、工时范围
2. 与保险公司原始 CCC/Mitchell 估单自动比对，生成逐行 Supplement Request
3. 自动起草给保险调查员的沟通邮件，包含技术依据和行业 Labor Rate 数据
4. 跟踪 Supplement 批复状态，超 48h 未回复自动升级催促

## 护城河
- 需要深度训练 CCC One / Mitchell / Audatex 三大估损平台格式
- 积累成功/拒绝案例的 fine-tune 数据集越多，谈判话术越精准
- 与 OEM 零件价格数据库实时集成，估价可信度高于人工

## 市场规模
- 美国约 33,000 家独立汽车钣金/喷漆店（NAICS 8111）
- 每家每月平均处理 40-80 辆，Supplement 发生率 ~70%
- TAM ≈ $480M/年（按 $15/辆 收费测算）

## 定价
$299/月（含无限 Supplement，支持 3 位技师账号）
