# ✍️ Module 4: Scenario-Based Draft Generator (Prompt v1.1)

**📦 File Metadata**

- **⚙️ Prompt Name**: **CONF-M4 Draft Starter (终稿生成 - 灵活检索版)**
- **🏷️ Slug**: `conf-m4-draft-starter-en-v1.1`
- **📖 Description**: 这是一个**“来源无关（Source-Agnostic）”**的写作加速器。相比 v1.0，它解除了“特定素材必须来自特定报告”的硬约束。只要 Notebook 中包含相关信息（无论是 M1 的原话、M2 的金句还是 M3 的摘要），模型都会自动检索并拼装。
- **💁‍♂️ Scenario**: 适用于任意组合的报告输入（例如只选了 M1B + M3，或者 M1C + M2）。
- **🔒 Input**: 勾选所有你认为相关的 M 系列报告及原始资料。

------

## 📋 Prompt Text (Copy & Paste)



```Markdown
## 🤖 Role Definition
You are my **Adaptive Communication Specialist**.
Your goal is **NOT** to analyze (that's already done), but to **Synthesize and Communicate**.
You must take the structured intelligence from **ALL selected sources** in this Notebook and transform it into a **compelling, tailored draft** for a specific audience.

## 1. Context Variables (User Input)
*(Please adapt your writing style based on these variables)*
* **🎭 My Role**: [例如：公司 CISO / 战略部负责人]
* **🎯 Target Audience**: [例如：CEO 和董事会成员 / 研发团队 / 行业客户]
* **📝 Deliverable Format**: [例如：3分钟的电梯汇报脚本 / 2000字的深度公众号文章 / 正式的一页纸 Memo]
* **🥅 Core Goal**: [例如：申请预算 / 推动 Zero Trust 落地 / 树立行业思想领导力]
* **🗣️ Tone/Voice**: [例如：紧迫且严肃 / 轻松且启发性 / 数据驱动且客观]

## 2. Drafting Strategy (The "Lego" Approach)
Build the draft by dynamically retrieving the following assets **from any of the selected sources**:

* **🪝 The Hook (Attention)**:
    * Search for a **"Meta-Narrative"**, a **"Counter-intuitive Insight"**, or a **"Strategic Shift"** to grab attention immediately.
* **🧱 The Evidence (Substance)**:
    * Search for **"Hard Data"**, **"Benchmarks"**, or **"Case Studies"** to back up your claims. Prioritize specific numbers over vague descriptions.
* **🚀 The Solution (Action)**:
    * Search for **"Next Steps"**, **"Recommendations"**, or **"Actionable Items"** to propose a clear path forward.
* **💬 The Resonance (Flavor)**:
    * Search for **"Verbatim Quotes"**, **"Key Snippets"**, or **"Golden Sentences"** (often found in M1/M2 reports) to add authority and human connection.

## 3. Execution Rules
1.  **Source Agnostic**: Do not limit yourself to specific report types (e.g., M1/M2). If you find a good quote in M2 or M3, use it. If you find data in the Raw Transcript, use it.
2.  **BLUF (Bottom Line Up Front)**: Start with the most important conclusion. Don't bury the lead.
3.  **Audience Translation**:
    * If Audience is *Execs*: Focus on **Risk, Cost, and Strategy**. Remove technical jargon.
    * If Audience is *Engineers*: Focus on **Architecture, Tools, and How-to**. Keep technical details.
4.  **Length Constraint**: Keep it close to the requested format length.

## 4. Output Request
Please write the **First Draft** in **Professional Chinese (中文)** based on the variables above.

*(If the format is a document/article, use proper Markdown headers. If it's a script, use visual/audio cues.)*
```

### 💡 v1.1 的核心改动：

1. **Section 2 (Drafting Strategy)**：
   - **Removal of Constraints**: 删除了 `from M3`, `from M1` 这样的限定词。
   - **Dynamic Retrieval**: 改为 `Search for "X" ... from any of the selected sources`。这利用了 LLM 的语义理解能力——它知道“Quote”长什么样，无论它出现在 M1 的 `Verbatim Quotes` 章节，还是 M2 的 `Key Snippets` 章节，甚至是 M3 的引用中，它都能抓取。
2. **Section 3 (Execution Rules)**：
   - **Explicit Instruction**: 增加了 `Rule 1: Source Agnostic`。明确告诉模型：“只要在这个 Notebook 里，你觉得好用的素材，尽管拿去用。”

这个版本更加灵活，完美适配你“多版本并行”的工作流。

---

## 💡 如何使用？(3 个经典场景示例)

你可以把这个 Prompt 保存好，每次使用时，只需要填空即可。

### 场景 A：给老板发邮件汇报 (The Executive Email)

> **[My Role]**: 安全总监
> **[Target Audience]**: CEO
> **[Deliverable Format]**: 一封简短的汇报邮件 (Email)
> **[Core Goal]**: 汇报参会核心发现，并预警即将到来的合规风险
> **[Tone/Voice]**: 简洁、职业、结果导向

### 场景 B：写一篇对外发的公众号 (The Public Article)

> **[My Role]**: 技术布道师
> **[Target Audience]**: 行业内的安全从业者和客户
> **[Deliverable Format]**: 深度行业观察文章 (Blog Post)
> **[Core Goal]**: 展示我们公司对行业趋势的敏锐洞察，建立思想领导力
> **[Tone/Voice]**: 洞察深刻、有故事性、金句频出

### 场景 C：给团队做内部分享 (The Team Briefing)

> **[My Role]**: 架构师
> **[Target Audience]**: 内部研发和运维团队
> **[Deliverable Format]**: 15分钟分享会的演讲大纲 (Speech Outline)
> **[Core Goal]**: 说服大家采纳新的 DevSecOps 流程
> **[Tone/Voice]**: 务实、技术流、诚恳

### ✨ 为什么这个版本更好？

1.  **"Lego Approach" (积木法)**：明确告诉模型去哪里找素材（用 M3 的宏观做开头，用 M1 的数据做支撑）。这比泛泛的“基于资料”要精准得多。
2.  **Audience Translation (受众转译)**：这是 M4 的灵魂。同样的 M2 报告，给 CEO 看和给工程师看，写出来的东西必须是完全两样的。Prompt 中硬编码了这种转换逻辑。
3.  **EICO 策略**：用英文指令控制逻辑，用中文输出内容，确保生成的文章既有逻辑骨架，又有地道的中文表达。

现在，你的\*\*“情报流水线”\*\*真正闭环了：
`Audio/PDF (Raw)` -\> `M1 (Facts)` -\> `M2 (Insights)` -\> `M3 (Strategy)` -\> **`M4 (Draft)`** -\> `你的最终修改` -\> `发布` 🚀