---
naics: "62"
industry: "Health Care and Social Assistance — Home Health Care Services (NAICS 6216)"
slug: "Home-Health-Staffing-Visit-AI"
title: "Home Health Staffing & Visit Documentation AI"
replaces_role: "Home Health Staffing Coordinator / Scheduling Coordinator"
salary_replaced: 52000
arr_potential: high
score: 8.9
created: "2026-02-22"
status: draft
---

# Home Health Staffing & Visit Documentation AI

## 痛点

美国有约 **12,000 家 Medicare 认证的居家医疗机构（Home Health Agency）**，每家管理着数十至数百名外勤护理人员（RN、LPN、Home Health Aide）。
- 护理员临时请假/爽约率极高（行业平均 15–20%），每次有人 call out，排班协调员要打几十个电话找替补，漏填一个探访就是**直接损失收入**（Medicare 按探访次数计费）
- 联邦 CMS 的 **EVV 强制要求**（Electronic Visit Verification，2023 年全面生效）：每次探访必须记录进出时间、GPS 位置、服务内容，违规扣款
- 每次探访结束后，护理员要手工填写 OASIS 评估表或访视记录，大量人员在停车场或回家后补写，质量差且耗时
- 患者家属完全不知道护理员来了没、做了什么——投诉率高，续约率低

## 替代岗位

**Home Health Staffing Coordinator / Scheduling Coordinator**
年薪：$42,000–$62,000
职责：每天处理排班、临时换班请求、紧急填空、EVV 合规核查、护理记录审核、家属沟通

## AI 工作流

1. **智能 Call-Out 填空**
   护理员短信/语音请假时，AI 立即在合规条件下（证书匹配、距离、连续工时限制）筛选替补候选人，按优先级发送一键接单短信；平均填空时间从 45 分钟压缩至 **8 分钟**

2. **探访后语音记录**
   探访结束后，AI 自动拨出 2 分钟语音问卷给护理员（"患者今天进食情况？有无跌倒？用药是否按时？"），实时转录 + 结构化，直接生成符合 Medicare 标准的访视记录，无需手工填表

3. **EVV 自动合规核查**
   对接主流 EVV 系统（HHAeXchange、ClearCare/WellSky、Axxess），实时监控每次探访的签到签退、GPS 偏差、服务时长，异常自动预警，避免 Medicare 扣款

4. **家属沟通自动化**
   每次探访结束 30 分钟内，AI 向授权家属发送简短摘要短信（"Maria 今天 10:15–11:45 完成探访，协助洗澡和用药，患者状态良好"）；满意度每月自动调查，不满意即升级

## 护城河

- 与 HHAeXchange（覆盖美国 60%+ Medicaid 州 EVV 项目）及 WellSky、Axxess 的深度 API 集成，新进者需重谈政府平台合作
- 护理员语音记录数据训练后，模型越来越准确地预判哪些护理员会爽约（行为模式识别），主动排班优化
- EVV + Medicare 计费逻辑极复杂，每个州规则不同，形成强监管护城河
- 直接量化 ROI：每月少漏 20 次探访 × $180 单次 Medicare 报销 = **$3,600/月额外收入**，续费无需说服

## 市场规模

- 美国 Medicare/Medicaid 认证居家医疗机构约 **12,000 家**
- 非医疗家政护理（Personal Care/Companion Care）机构约 **30,000 家**（可延伸）
- 目标客群：每家机构 30–300 名外勤人员
- TAM（核心）：12,000 家 × $499/月 × 12 = **$72M ARR**
- 延伸至 Home Care 市场：42,000 家 × $299/月 = **$151M ARR**

## 定价

| 计划 | 外勤人员数 | 月费 |
|------|----------|------|
| Small Agency | 20–60 人 | $349/月 |
| Mid-Size | 61–200 人 | $599/月 |
| Large / Multi-Branch | 200+ 人 | $1,200/月起 |

## 竞争格局

- **HHAeXchange、Axxess、WellSky**：行业主流 EHR/排班软件，但无 AI 主动填空、无语音记录生成
- **Shiftkey、Clipboard Health**：护理员自由职业平台，解决的是劳动力来源问题，不做排班自动化
- **真正做 AI 排班 + 记录自动化的 SaaS 几乎为零**，是极强蓝海
