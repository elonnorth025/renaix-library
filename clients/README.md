# Renaix Clients

客户管理目录。每个客户一个文件夹。

## 命名规范

```
001-[client-shortname]/
002-[client-shortname]/
...
```

全部小写，用连字符分隔。

---

## 客户索引

| ID | 客户名 | 行业 | Status | Discord Channel | Setup Fee | Monthly Fee | Start Date |
|----|--------|------|--------|-----------------|-----------|-------------|------------|
| 001 | Supra Neuro | [待填写] | Prospect | #client-001-supra-neuro | TBD | TBD | 2026-02-14 |

---

## Status 说明

- **Prospect** — 潜在客户，还在谈
- **Discovery** — 已签约，调研阶段
- **Development** — Agent 开发中
- **Testing** — 测试阶段
- **Live** — 已上线
- **Churned** — 流失

---

## 文件夹结构

每个客户文件夹包含：
- `CLIENT.md` — 客户基本信息
- `AGENT.md` — Agent 配置（Soul、技能、规则）
- `DISCOVERY.md` — 业务调研笔记
- `contracts/` — 合同、协议
- `assets/` — Logo、照片、文件
- `notes/` — 杂项笔记
