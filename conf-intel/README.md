# NotebookLM 会议挖掘提示词库 (Conf-Mining)

这是一个专为 NotebookLM 设计的高级提示词库，用于从会议录音和文档中提取深度洞察。

## 📁 目录结构

```
Conf-Mining/
├── overview/          # 📖 总览与指南
├── cn/               # 🇨🇳 中文提示词库 (v2.4)
├── en/               # 🇬🇧 英文优化版（EICO策略, v2.4）
└── review/           # 🧱 设计评审与评价
```

## 🚀 快速开始

1. **查看总览**：从 [`overview/`](./overview/) 开始了解整个提示词体系
2. **选择语言**：
   - 中文用户 → 使用 [`cn/`](./cn/) 中的提示词
   - 追求最佳效果 → 使用 [`en/`](./en/) 中的 EICO 策略提示词
3. **参考评价**：查看 [`review/`](./review/) 了解设计理念

## 📚 模块说明 (v2.4)

### 模块 1：基础还原层
- **M1**: 全息会议还原 (v2.3)
- **M1B**: 智能价值评估 (v3.4)
- **M1C**: 事实分析与系统解构 (v1.0)

### 模块 2：深度洞察层
- **Universal**: 通用深度研判 (v2.4)
- **M2A**: 逻辑与论证审计
- **M2B**: 战略与地缘研判
- **M2C**: 创新与知识发现

### 模块 3：综合报告层
- **Executive**: 决策者摘要
- **Macro**: 宏观战略综合 (v3.1)

### 模块 4：终稿生成层
- **Draft Starter**: 场景化终稿生成 (v1.2)

## 💡 v2.4 核心理念

1.  **独立运行 (Standalone Architecture)**:
    - 所有模块 (M1-M4) 均可独立运行，直接分析原始 Transcript/Slides，不再强制依赖上游报告。
    - "Raw Data is King".

2.  **北极星法则 (North Star Directive)**:
    - **用户直觉优先**: 如果 Notebook 中包含 `[Author_Intuition]` 或 `[Notes]`，模型将优先以用户的关注点为真理，凌驾于原始文本之上。
    - "User Intuition is God".

3.  **EICO 策略**:
    - **E**nglish **I**nstructions（英文指令）：确保逻辑精确性
    - **C**hinese **O**utput（中文输出）：保证表达地道性

## 📝 版本说明

- v1.0: 初始版本
- v2.2: 成熟版本
- v2.4: **独立架构 & 北极星版** (当前推荐)

## 🤝 贡献

欢迎提交 Issue 和 Pull Request 来改进这个提示词库。

---

*最后更新：2024-12-05*