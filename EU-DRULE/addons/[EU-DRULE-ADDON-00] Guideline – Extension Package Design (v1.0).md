# 📦 EU-DRULE ADDON Package 设计规范指引

### （Guideline for Future Extension Packs v1.0）

> **定位**：ADDON 是 System Prompt 的“可选扩展功能模块”，用于增强分析方法、行业视角或专有情境能力。
>  **要求**：可插拔，不改变系统核心运行逻辑；引用关系清晰；版本可追踪。

------

## 🧩 ADDON 开发目标

新增的 ADDON 必须满足其中至少一个目标：

| 模块类型         | 价值说明                          | 示例                                     |
| ---------------- | --------------------------------- | ---------------------------------------- |
| 🧠 思维模式增强包 | 增加新的 Slash Command 或分析框架 | `/finance` `/cyber-risk` `/supply-chain` |
| 🏭 行业/领域专包  | 预置特定行业分析模板              | Telco / Cloud / Automotive               |
| 📜 法规专题专包   | 针对某一法规做深入 SOP            | AI Act GPAI Title / CRA OSS 供应链       |
| ⚗ 实验与验证专包 | 为合规实验允许输出特类型式        | Sandbox Playbook / Pilot Case Template   |

------

## 📂 文件结构与命名规范

> 格式必须统一，便于 NotebookLM 自动识别和管理。

```
[EU-DRULE-ADDON-XX] 英文短标题 – 中文说明 (vX.Y).md
```

示例：

```
[EU-DRULE-ADDON-01] Thinking-Modes – Critical System PPP (v1.0).md
[EU-DRULE-ADDON-02] CRA-SupplyChain – Open Source & Vendor Risk (v1.0).md
```

------

## 🧱 ADDON 内部文档结构（强制）

遵循以下章节模板：

1️⃣ **标题（H1）**
 《[EU-DRULE-ADDON-XX] {英文短标题} – {中文说明} (vX.Y)》

2️⃣ **导语：目标 + 关联 System Prompt**

- 说明此包扩展哪些 Slash / 分析模式、适用场景
- 强调：当用户输入特定 Slash 时才启用本包

3️⃣ **模块清单**

- 本包定义了多少 Slash Command
- 每个 Slash 的定位一句话说明

4️⃣ **每个 Slash 分节定义（核心部分）**

每节必须包含：

| 要素           | 含义                               |
| -------------- | ---------------------------------- |
| 🎯 任务定位     | 这个 slash 要回答什么问题          |
| 🧱 输出结构模板 | Step-by-step 固定格式              |
| 📋 事实判断分层 | `[F]` vs `[J]` vs 经验假设         |
| 🧩 视角建议     | 必填分析维度，例如 T/NT、经济/战略 |
| 🧪 可选工具     | 如 Mermaid CLD、矩阵表、回路模型   |
| 📝 示例         | 小型 demo 或 starter content       |

> 输出结构必须严格格式化，方便 System Prompt 调用。

5️⃣ **与核心 System Prompt 协同方式**

- 明确哪些指令保持优先级
- 无 slash 时不主动启用本包

6️⃣ **版本变化日志（可选）**

------

## 🧬 ADDON 的引用策略（System Prompt 端）

每新增一个 ADDON，System Prompt 必须：

| 修改点               | 内容                                  |
| -------------------- | ------------------------------------- |
| **开头增加引用声明** | 提及已启用 ADDON 名称、版本           |
| **Slash 总览更新**   | 在 `1.2` 小节加入新 Slash 一句话简介  |
| **详细结构引用外部** | 在主文中不展开，由 ADDON 提供结构规则 |

**核心原则：**

> System Prompt = 主线框架
>  ADDON = 方法 / 场景增强模块
>  主体逻辑不被捆绑

------

## 🧩 Slash 扩展规范（新增 Slash 必须遵守）

- Slash 名必须小写英文：`/xxx`
- 必须满足：
  - 有明确分析目标
  - 有固定结构模板
  - 有高管可用的交付物格式
- 必须兼容以下三种写作：

| 层级                  | 输出形式         |
| --------------------- | ---------------- |
| Executive Summary     | 200 字全景       |
| Structured Sections   | 逻辑骨干         |
| Visual Aid (Optional) | 表格/CLD/RACI 等 |

------

## 🛠️ 可交付组件

每个 ADDON 必须能输出至少 1 种战略文档：

| 文档框架                | 举例           |
| ----------------------- | -------------- |
| Key Message Set         | 对外监管方沟通 |
| RACI Matrix             | 内部组织执行   |
| Timeline & KPI          | PMO 追踪       |
| Risk–Opportunity Matrix | 战略判断       |
| Mermaid CLD 图          | 系统反馈机制   |

------

## 🧱 扩展一致性要求（跨 ADDON 统一）

- **命名风格一致**
- **术语风格统一**（EN/法规条款 / [F]/[J] 标签）
- Markdown 一级标题不重复
- 章节编号从 0 开始（Meta → 功能模块）
- 表格字段尽可能复用（便于横向比较）

------

## 📡 示例设计方式（Agent 可直接 follow）

> 给 Agent 的命令如下👇

```
按照《EU-DRULE ADDON Package 设计规范指引 v1.0》创建一个新的扩展包：
名称：[EU-DRULE-ADDON-XX] {示例标题}
场景：{用户输入场景}
新增 Slash Commands：{列举 Slash}
为每个 Slash 完整写出「任务定位 + 输出结构模板 + 示例」
并在 System Prompt 中加入引用声明与简要路由规则
输出：两个文件（System Prompt 修改版 + ADDON 文档）
```

------

## 🧨 未来扩展路线图（你可以自由添加）

| 数字档次 | 类型   | 示例                                |
| -------- | ------ | ----------------------------------- |
| ADDON-01 | 已完成 | 思维模式增强 Critical/System/PPP    |
| ADDON-02 | 🆕 推荐 | CRA + Open Source Supply Chain Risk |
| ADDON-03 | 🆕      | AI Act – GPAI Compliance            |
| ADDON-04 | 🆕      | NIS 2 Telco Sector Enforcement      |
| ADDON-05 | 🆕      | Sandbox Methodology SOP             |

你只需说一句：

> “请根据 Guideline 生成 ADDON-02：{主题}”

我就能立刻产出 📦 文件 + 🧠 System Prompt 更新。

------

## 🎯 目标总结

| 价值       | 说明                                  |
| ---------- | ------------------------------------- |
| 🧱 模块化   | 主体不变，能力无限升级                |
| 🔌 可插拔   | 不影响 NotebookLM 预置功能            |
| 🧠 高可靠性 | System Prompt 不溢出、不超字数        |
| 🚀 快速迭代 | 任何新分析方向都能小时级落地          |
| 📈 高复用性 | 可转移到其他 Notebook / GPTs / Agents |

