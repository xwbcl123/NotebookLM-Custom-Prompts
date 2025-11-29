---
description: (结构化/中文) 自动分析 'git status' 和 'diff'，添加所有变更，生成提交信息，执行 'git commit'，并询问是否 'push'。
argument-hint: [可选的提交信息上下文]
allowed-tools: Bash(git add .), Bash(git commit *)
---

## 1. Purpose (目标)

 本命令的目的是自动化标准的 'git commit' 流程。它将暂存所有变更，基于变更内容生成一条提交信息，执行提交，并在最后询问是否 'push'。

## 2. Variables (变量)

* **`$ARGUMENTS` (可选)**: 用户提供的额外上下文（例如 `/git-commit 修复登录页bug`），用于辅助AI生成更精确的提交信息。
* **自动上下文**: `git status` 和 `git diff HEAD` 的输出将被自动注入到 `## 4. Workflow` 部分，作为AI分析的依据。

## 3. Instructions (指令)

* 你必须严格遵循 `## 4. Workflow` 中定义的步骤。
* 生成的提交信息应遵循常规标准（例如："feat: ..." 或 "fix: ..."）。
* 如果 `git status` 显示没有变更，请跳过所有操作，并直接在 `## 5. Report` 中告知用户。
* 你已被授予执行 `git add` 和 `git commit` 的权限，无需再次询问。

---
✨ **新增规则 (New Rules)** ✨

* **[ 强制中文 ]**：你生成的提交信息**必须**使用**简体中文（CN）**。
* **[ 禁止签名 ]**：切勿（MUST NOT）在提交信息中添加任何形式的签名、署名或提及 "Claude Code"（例如 "由...生成"）。

---

## 4. Workflow (工作流)


**步骤 1: 收集上下文**
!git status
!git diff HEAD

**步骤 2: 分析与暂存**
1.  分析上述 `git status` 和 `git diff HEAD` 的输出。
2.  *如果存在变更*: 执行 `git add .` 命令。
3.  *如果不存在变更*: 立即转到 `## 5. Report` 并报告“无变更”。

**步骤 3: 构造与执行提交**
1.  *如果已暂存变更*: 基于变更内容和 `## 2. Variables` 中提供的 `$ARGUMENTS`，**生成一条简体中文（CN）**的提交信息。
2.  使用你生成的提交信息，执行 `git commit -m "你生成的信息"` 命令。

**步骤 4: 准备报告**
1.  收集 `git commit` 命令的输出（stdout/stderr）。
2.  准备 `## 5. Report` 的内容。

## 5. Report (报告)


* [如果工作流在步骤 2 中因 "没有变更" 而停止]
* **状态**: `git status` 显示您的工作目录很干净，没有变更需要提交。

* [如果工作流成功执行]
* **状态**: 成功执行 `git add .` 并已提交变更。
* **Commit 输出**:
    ```
    [此处插入 git commit 的 stdout/stderr]
    ```
* **下一步**: 您希望我现在执行 `git push` 吗？
