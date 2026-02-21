---
date: 2026-02-21
tags: [competitor, construction, permit, AI-agent, hackathon, crossbeam]
---

# CrossBeam 竞品深度调研

## 基本信息
- **产品名：** CrossBeam
- **创始人：** Mike Brown（加州个人伤害律师，非技术背景）
- **公司：** OnBreeze Consulting
- **LinkedIn：** https://www.linkedin.com/in/michael-t-brown-034aaa22
- **GitHub：** https://github.com/mikeOnBreeze/cc-crossbeam（公开）
- **来源：** Anthropic "Build with Opus 4.6" Claude Code Hackathon（2026-02-10~16）
- **新闻：** https://www.newsdirectory3.com/crossbeam-faster-california-building-permits-code-compliance/

## 产品定位
**AI 驱动的加州 ADU 许可证助手**

> "上传施工图 + 城市纠错函 → 生成可直接提交的专业回复包"

### 核心问题
- 加州 ADU 许可证首次提交被拒率 **90%+**
- 拒绝原因大多不是工程问题，而是行政问题（签名缺失/法条引用错误/表格不完整）
- 平均 6 个月延误 = 每个项目损失 **$30,000**

## 三大功能流程

### Flow 1：纠错函解析（已上线）
- 承包商上传：施工图 PDF + 城市纠错函
- AI agent 自动：
  1. 视觉读取施工图每一页
  2. 解析纠错项
  3. 对照加州 ADU 法（Government Code 66310-66342）
  4. 实时网络搜索城市专项市政法规
  5. 向承包商提问澄清
  6. 输出：分析报告 + 专业工作范围说明 + 回复信草稿

### Flow 2：许可证预检清单（已上线）
- 输入项目地址 + 基本信息（ADU 类型/面积/地块类型）
- 输出：提交前清单 + 城市专项注意事项

### Flow 3：城市预审（路线图，未建）
- 城市建设部门上传申请 → AI 审查 → 人工审查前提前标记问题
- 这是 Mike Brown 的开源愿景，暂未实现

## 技术架构
```
浏览器 (Next.js 16)
  ↓ API + Supabase Realtime
Cloud Run（编排服务器 Express 5）
  ↓ 启动隔离沙箱
Vercel Sandbox（Agent SDK + Claude Opus 4.6 + Skills）
  ↓ 读写
Supabase（Postgres + Realtime + Storage）
```

**为什么用隔离沙箱：** 单次纠错分析需 10-30 分钟，Vercel serverless 超时（60-300s），Cloud Run 提供持久化编排进程。

### Skills 架构（28+ 文件）
- **California ADU Skill** — HCD ADU 手册(54页) + Government Code 66310-66342 + 决策树路由 + 快速参考阈值表
- **ADU Corrections Interpreter Skill** — 多步纠错分析工作流引导
- **ADU City Research Skill** — 三模式城市研究（WebSearch/WebFetch/浏览器回退）
- **CrossBeam Ops Skill** — API 操作指南

## 技术栈
| 层级 | 技术 |
|------|------|
| 前端 | Next.js 16, React 19, shadcn/ui, Tailwind CSS 4 |
| 服务端 | Express 5, Cloud Run, Vercel Sandbox |
| AI | Claude Opus 4.6, Agent SDK |
| 数据库 | Supabase (Postgres + Realtime + Storage) |
| 知识库 | 28+ 结构化参考文件 |
| 开发工具 | Claude Code（全程使用） |

## 市场背书
- 2018 年至今加州发放 **429,000+** ADU 许可证
- ADU 占加州全新住房的 **20%**
- Buena Park 市长 Connor Trout 亲自出现在 demo 视频背书
- Boris Cherny（Claude Code 创始人）点评："我喜欢它的用户专注度"

## 与 Renaix 的战略关系

| 维度 | CrossBeam | Renaix Maya |
|------|-----------|-------------|
| 核心功能 | 许可证合规审查 | 日常沟通协调 |
| 目标用户 | GC/ADU 承包商 | GC 老板 |
| 竞争关系 | **互补，不竞争** | — |
| 扩张威胁 | 若扩展到全流程 GC 管理 | 需关注 |

**当前结论：** CrossBeam 解决"许可证提交"痛点，Maya 解决"每日协调电话"痛点，客户相同但场景不同。短期无竞争，长期是潜在整合对象（甚至合作机会）。

## 持续关注清单
- [ ] GitHub star 数变化趋势（现在公开，说明可能开源运营）
- [ ] OnBreeze Consulting 是否融资/商业化
- [ ] Mike Brown LinkedIn 动态（是否全职转型 AI 创业）
- [ ] CrossBeam 是否扩展至加州以外或 ADU 以外的许可证场景
- [ ] 是否有其他团队 fork 复制到其他州/领域

## 参考链接
- GitHub: https://github.com/mikeOnBreeze/cc-crossbeam
- 原文: https://www.digitaldigging.org/p/a-lawyer-a-road-inspector-and-a-cardiologist
- 新闻: https://www.newsdirectory3.com/crossbeam-faster-california-building-permits-code-compliance/
- Hackathon Gallery: https://cerebralvalley.ai/e/claude-code-hackathon/hackathon/gallery
