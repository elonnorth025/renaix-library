# 从 CompanyOS 到 LifeOS：文件系统哲学与 Maya 的启示

> 来源：[@yibie](https://x.com/yibie/status/2021778995185168650)，原始推文：[@mernit](https://x.com/mernit/status/2021324284875153544)
> 整理日期：2026-02-23

---

## 核心论点（Eli Mernit）

> "One reason that rolling out agents at enterprises is complicated is because data is siloed across many different systems."

企业 AI 难落地的根本原因：**没有共享命名空间（shared namespace）**。

发票在 Quickbooks / 邮件在 Outlook / 提案在 Sharepoint / 合同在 Netsuite / 客户信息在 Salesforce → AI Agent 无法获得完整上下文 → 无法做出好决策。

---

## 解决方案：公司即文件系统

**四个原则（Unix 哲学）：**

| 原则 | 含义 |
|---|---|
| 统一命名空间 | 所有数据映射到文件路径 |
| 文件即状态 | 公司状态 = 文件内容，极简透明 |
| 权限即治理 | 组织架构 = Unix 权限，边界清晰 |
| 读写即操作 | Agent 通过读写文件工作，接口简单可审计 |

**核心命题：**
> "The filesystem is the state."
> "The governance structure is just unix file permissions."

Agent 不需要 API 集成，不需要 RAG，只需要读写文件的权限。

---

## 从 CompanyOS 到 LifeOS

个人数据同样是孤岛：健康/财务/笔记/日程/人际关系分散在各 App。

**人生文件系统愿景：**

```
~/life/
├── /goals/          人生目标，长期愿景
├── /projects/       正在进行的项目
├── /knowledge/      学习和思考
├── /relationships/  人际关系网络
├── /health/         健康数据
├── /finance/        财务状况
├── /reflections/    反思和日记
└── /archive/        过去的记录
```

---

## 对 Maya / Renaix 的直接启示

### Maya 面对的是同样的数据孤岛

GC 老板的信息散落在：脑子里 / 手机通讯录 / 纸质笔记 / 邮件 / 短信。

Maya 的本质：**帮 GC 建一个统一文件系统**，把所有状态收拢到一个命名空间，AI 才能真正运营起来。

### Maya 的文件系统架构（设计目标）

```
/maya-gc-client/
├── /projects/
│   ├── /active/
│   │   └── /job-001-smith-kitchen/
│   │       ├── client.md        ← 业主信息
│   │       ├── subs.md          ← 分包商列表 + 状态
│   │       ├── timeline.md      ← 工期计划
│   │       └── daily-log.md     ← 工地日志（追加写入）
│   └── /archive/
├── /contacts/
│   ├── subs/                    ← 分包商通讯录
│   └── suppliers/               ← 供应商
├── /finance/
│   ├── pay-apps/
│   └── lien-waivers/
└── /comms/                      ← 所有通话记录、短信
```

**操作即文件读写：**
- GC 老板说话 → Maya 写入对应文件
- 查项目状态 → 读取 `/projects/active/`
- 工地日志 → 追加到 `daily-log.md`
- 案件归档 → 移动到 `/archive/`

### 护城河意义

竞品（Procore、Buildertrend）是孤岛型 SaaS——数据锁在他们服务器，AI 无完整上下文。

Maya 文件系统优先 → GC 数据在本地/GitHub → AI 永远有完整上下文 → **这是结构性差异，不是功能差异**。

### LifeOS → CompanyOS → GC-OS 同构

```
yibie 的 LifeOS          Renaix 的 Maya（GC-OS）
~/life/                  ~/gc-company/
├── goals/          →    ├── projects/
├── relationships/  →    ├── contacts/
├── finance/        →    ├── finance/
├── health/         →    ├── safety/
└── reflections/    →    └── daily-logs/
```

框架相同，文件夹内容是建筑行业的。

---

## 文件夹结构即价值观

> 你管理文件夹的原则，就是你为人处事的原则。

| 文件系统行为 | 映射的价值观 |
|---|---|
| 清晰的目录结构 | 有组织的思维 |
| 定期归档 | 懂得放下过去 |
| 明确的公私分界 | 健康的边界感 |
| 版本控制 | 相信成长是渐进的 |

---

## AI 分身的本质

传统 AI 助手：每次对话从头开始，无历史，无偏好。

文件系统模型下的 AI 分身：
- **持久记忆** — 所有数据在文件中，随时可访问
- **完整上下文** — 不只是对话历史，而是整个人生/公司数据
- **可审计** — 你可以看到 Agent 读了什么、写了什么
- **可控** — 通过权限设置，精确控制 Agent 能访问什么

> 当 Openclaw 或其他 Agent 可以读取你的人生文件时，它们拥有的不仅是数据，而是你的完整上下文。它们可以像了解自己一样了解你，像代表公司一样代表你。

**这就是 LifeOS / GC-OS 的终极形态。**
