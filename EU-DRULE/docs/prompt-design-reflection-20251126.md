# 🧩 Prompt Design Reflection Log

**Project：EU-Digital-Rule 多视角分析工作流 Prompt 系统架构**

**时间：2025.11.26**

**记录人：ChatGPT x Martin 协作**

---

## 🎯 初始目标（Intent）

> 为 NotebookLM 创建一个多角色 + 多分析视角的稳定 Prompt 架构
> 
> 
> 同时支持系统化政策研判与敏捷分析互动
> 
> 并保持对 NotebookLM 预置功能的兼容
> 

具体要求：

| 目标 | 描述 |
| --- | --- |
| 多角色支持 | What/Why/So-What/Now-What 等结构化视角 |
| Slash Command 控制 | 输入 `/xxx` → 启动对应分析模式 |
| 系统提示词规模大 | System Prompt 支持 10k 字复杂能力 |
| 兼容 NotebookLM 特性 | 不干扰自动提问、内容映射等能力 |
| 可扩展能力架构 | 按需加载，通过 Source 进行模块化扩展 |

一句话目标：

> 构建一个可随时升级、能在法规深研场景“越用越强”的 Prompt Workbench。
> 

---

## 🏗 设计演进过程（Iteration Journey）

| 阶段 | 关键动作 | 输出 |
| --- | --- | --- |
| V0 无结构目标 | 自定义风格 + 多视角需求 | 初版 system prompt 构思 |
| V1 多 Slash 命令设计 | `/what /why /so-what /now-what /all` | 主线分析框架确定 |
| V2 思维模式增强 | `/critical /system /ppp` 引入 | 多维方法论协同 |
| ⚠️ 容量溢出问题 | System Prompt 字数 >10k | 🌟 关键转折点 |
| V3 两层 Prompt 体系设计 | **Core + ADDON** 分离 | 可插拔架构成型 |
| V4 CLD 支持增强 | Mermaid 换行与渲染验证 | 图形化系统分析可用 |
| V5 扩展包规范化 | 指南（ADDON-00）成文 | 标准化与未来扩展落地 |

最终成果从单个 Prompt

演进为：

> 一个模块化数字合规知识系统
> 

---

## 🧱 最终交付成果（Deliverables）

| 文件类型 | 名称 | 作用 |
| --- | --- | --- |
| 🧠 System Prompt 核心引擎 | EU-DRULE-SystemPrompt-Core-v1.3 | 主线 Slash + 输出结构规范 |
| 📦 可选扩展包 | ADDON-01 思维模式增强包 | `/critical /system /ppp` 模块能力 |
| 📐 扩展规范指南 | ADDON-00 Extension Guideline | 未来 ADDON 制作标准 |

📌 全部严格控制在 NotebookLM 技术约束内

📌 Slash Command 行为与官方能力**无冲突**

---

## ⚙️ 技术挑战与坑（What we solved）

| 挑战 | 风险 | 如何解决 |
| --- | --- | --- |
| NotebookLM 字数上限 10k | Prompt 无法保存 | Core/ADDON 分层架构 |
| Mermaid 换行解析差异 | 语法错误无法渲染 | `<br>` 替代 `\n` 并强制断行 |
| 预置提问被干扰 | AI 自动功能失效 | 默认行为分离，Slash 才触发专业模式 |
| Prompt 塞入过多规则 | 学习能力下降 | 优先级与路由规则优化 |
| 方法论细节绑定太紧 | 不能复用 | 模块化，抽离出可选功能包 |

---

## ✨ 关键经验（Insights & Lessons）

| 类型 | 精简总结 |
| --- | --- |
| Prompt Architecture | 大 Prompt ≠ 好 Prompt → 模块化系统才可扩展 |
| Interaction Design | Slash 显式意图 > 隐式触发 更可控 |
| Cognitive Load | System Prompt 做原则，ADDON 做细节 |
| Tool Compatibility | 写 Prompt 前先验证渲染器语法差异 |
| Documentation | Prompt 应具备“自解释性”与复用结构 |

一句话总结经验：

> Prompt 不再是一句话，而是一个可以长期升级的产品体系。
> 

---

## 🚀 后续计划建议（Future Roadmap）

| 推荐优先级 | ADDON 项目 | 场景价值 |
| --- | --- | --- |
| ⭐⭐⭐⭐⭐ | ADDON-02：CRA & OSS 供应链风险 | 你正在推动的核心议题 |
| ⭐⭐⭐⭐ | ADDON-03：AI Act GPAI 模块 | 贴合 DG CONNECT / AI Office 合作方向 |
| ⭐⭐⭐ | ADDON-05：Sandbox 实践 | 支持“合作桥”定位策略 |

---

## 🙌 协作感受

这是一个从**需求探索 → 技术验证 → 产品化设计**的完整闭环

很典型地体现了：

- 🎯 清晰的愿景与逐次验证
- 🧱 实事求是的 Prompt 工程实践
- 🎨 创新与系统性思维融合

一句评价：

> 我们不是“写了一个 prompt”，而是设计了一个 EU Digital Rulebook Prompt Operating System。
> 

---