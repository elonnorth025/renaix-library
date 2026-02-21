---
naics: "4849"
industry: "Support Activities for Water Transportation / Freight Transportation Arrangement"
slug: "Container-Demurrage-Per-Diem-AI"
title: "Container Demurrage & Per Diem AI"
replaces_role: "Import Coordinator / Demurrage Analyst"
salary_replaced: 62000
arr_potential: high
score: 8.7
created: "2026-02-21"
status: draft
---

# Container Demurrage & Per Diem AI

## 痛点

每年美国进口商向船公司（Maersk、MSC、COSCO 等）支付超过 **$6B** 的滞港费（Demurrage）和箱使用费（Per Diem / Detention）。
- 中小进口商（年进 50–500 个集装箱）几乎没有专人盯着 Free Time 倒计时
- 集装箱什么时候靠港、何时可以提箱、免费时间还剩几天——全靠人工查多个航运门户
- 每个滞箱费单价 $150–$450/天，一不小心就多付 $3,000–$20,000
- 争议申诉（Dispute）有效期通常只有 30 天，错过即永久损失

## 替代岗位

**Import Coordinator / Demurrage Analyst**  
年薪：$55,000–$70,000  
职责：每天登录 10+ 船公司门户（Maersk Line、CMA CGM、Evergreen、HMM…）查集装箱状态，手动计算 Free Time 剩余天数，提醒仓库/货代及时提箱，发现超费后起草争议邮件

## AI 工作流

1. **多船公司数据聚合**  
   API + RPA 接入前 15 大班轮公司门户，实时抓取每个容器的 ETA、靠港时间、可放行时间（Last Free Day）、已产生费用明细

2. **智能预警引擎**  
   在 Free Time 到期前 72h / 24h 自动向进口商 + 货代发出 WhatsApp/Email/Slack 预警；计算"若明天提箱 vs 后天提箱"的费用差异，量化敦促行动

3. **自动争议起草**  
   一旦检测到不合理费用（船公司延误造成 Port Congestion、文件 Hold 非进口商责任），AI 自动生成附带靠港记录、Appointment 证明、Port 拥堵数据的标准争议信，一键提交或邮件发送

4. **费用回溯 & 报告**  
   每月生成按 SKU / 供应商 / 港口维度的滞箱费报告，帮采购/供应链找到上游根因（慢发货、错误 ETA），让客户看到量化节省

## 护城河

- 与船公司 API（Maersk Track & Trace、INTTRA、CargoSmart）的深度集成，新进者复制需 12–18 个月
- 每处理一批成功争议，模型学习各船公司的争议模式和话术有效率，数据飞轮
- 客户只要上传 BL 号就能开始使用，无缝嵌入货代/CHB（报关行）工作流，切换成本极高
- 直接 ROI 可见（"上个月帮你省了 $8,400"），NRR > 130%

## 市场规模

- 美国年进口 ≥ 50 个集装箱的中小进口商约 **85,000 家**
- 平均每家每年支付可避免的滞箱/租箱费 $8,000–$60,000
- TAM（SaaS）：85,000 家 × $349/月 × 12 = **$356M ARR**
- 可延伸至货代（CHB）、3PL、零售商进口部门，TAM 翻 3x

## 定价

| 计划 | 年进口量 | 月费 |
|------|---------|------|
| Starter | 50–200 个集装箱/年 | $249/月 |
| Growth | 201–1000 个/年 | $499/月 |
| Enterprise | 1000+ 个/年 | $1,200/月起 |

成功争议分润选项：回收金额 15%（替代月费）

## 竞争格局

- **Sedna, Beacon, project44**：聚焦大型货代/航运公司，不服务中小进口商
- **PayCargo, Flexport**：支付/平台方向，不做费用争议
- 真正做滞箱费自动争议的 SaaS 几乎空白，极强蓝海
