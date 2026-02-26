---
title: "Pet Grooming Salon AI Receptionist & Coat Health Tracker"
naics: "81"
naics_name: "Other Services - Pet Care Services (8123)"
slug: "Pet-Grooming-Salon-AI-Receptionist"
created: "2026-02-25"
status: "new"
score: 8.1
---

# Pet Grooming Salon AI Receptionist & Coat Health Tracker

## 替代岗位
宠物美容前台 + 健康档案记录员（Grooming Receptionist / Pet Health Note Taker）
年薪替代价值：$38,000–$52,000

## 痛点
宠物美容店 80% 是 1-3 人小店，老板既要剪毛又要接电话、记录每只宠物的皮肤/被毛状况、处理取消和追缴押金，忙到无暇顾客。客人打来电话问"我家狗上次剪了什么造型？有没有发现皮肤问题？"，老板靠纸本记录完全查不到。

## AI 怎么做（核心工作流）
1. **多渠道接入**：SMS/电话/Instagram DM 自动回复预约请求，识别宠物档案（品种、体重、过敏史、上次剪毛记录）
2. **预约确认 + 押金**：自动发 Stripe 付款链接收取 $25 预约押金，48h 前发提醒，自动处理取消/改期
3. **美容笔记生成**：美容师结束后语音说 30 秒，AI 转成结构化"本次服务报告"（皮肤状况、打结位置、建议下次周期），自动发给宠物主人
4. **主动留客**：按宠物被毛类型推算下次剪毛日期，提前 2 周发 SMS 催约，追踪流失客户

## 护城河
- 宠物健康档案数据越积越深，换店成本高（主人不想重新解释过敏史和偏好）
- 与 MoeGo、Gingr 等美容软件 API 集成，嵌入已有工作流而非替换
- 语音转美容笔记是差异化，同类 AI 预约工具不做健康记录

## 市场规模
- 美国约 **67,000 家** 宠物美容/寄养店（NAICS 8123）
- 宠物服务市场 $11B，美容占 ~35%，TAM ~$3.8B
- 可渗透 SOM：15,000 店 × $149/月 ≈ **$26.8M ARR**

## 定价
**$149/月**（含无限预约 + 宠物档案 + 100条 SMS/月）
加购：$49/月语音美容笔记模块

## 竞争对手
- MoeGo（预约软件，无 AI 沟通）
- Gingr（管理系统，无主动留客）
- **无直接对手**做"语音转健康档案 + 主动 SMS 催约"组合
