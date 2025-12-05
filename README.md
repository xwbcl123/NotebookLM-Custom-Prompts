# NotebookLM Custom Prompts 📚

> **Quick Start**: 🚀 [**All-in-One File**](report-analysis/one-in-all/all-prompts.md) | 🇪🇺 [**EU-DRULE System**](EU-DRULE/README.md) | 🗣️ [**Conf-Intel System (v2.4)**](conf-intel/README.md)

## Motivation

I've spent a decent chunk of my career working in fields where "thought leadership" and report-writing are rife.

Thought leadership, done well, is an important endeavor. So is staying up to date on what's happening in an industry.

However, there is also an undeniable trend, in certain industries, to produce long documents just because it feels or looks productive to be doing so.

Reports are often mixed bags: a few original ideas buried amidst chapters of dreary regurgitated statistics. How can one—sorry to be trite—separate wheat from chaff?

Large language models (LLMs) are fantastic companions in this regard. I love NotebookLM, but it is inherently polite and deferential. Which is why I've found value in maintaining a few slightly more blunt prompts that can be pasted into the custom generation section (or used any other way you wish!)

---

## 🚀 Specialized Systems

### 🇪🇺 EU-DRULE - EU Digital Regulation Analysis System
*A comprehensive multi-role AI system specialized for EU digital regulations analysis*

**[📖 View EU-DRULE Documentation](EU-DRULE/README.md)**

**Core Components:**
- **[🎯 Core System Prompts](EU-DRULE/core-prompts/)** - Multi-role AI analyst engine (Legal, Policy, Impact, Action, Consultation, Intel)
- **[🔧 Extension Packages](EU-DRULE/addons/)** - Modular enhancements for critical analysis, custom reporting, and format templates
- **[📚 Design Documentation](EU-DRULE/docs/)** - System architecture and development insights

**Quick Links:**
- **[CN Version v1.4](EU-DRULE/core-prompts/EU-DRULE-SystemPrompt-Core-v1.4.md)** - Latest Chinese core system
- **[EN Version v1.4](EU-DRULE/core-prompts/notebooklm_eu_reg_system_prompt_v1_4.md)** - Latest English core system

**Extension Packages:**
- **[🧠 Critical Thinking Modes](EU-DRULE/addons/[EU-DRULE-ADDON-01]%20Thinking-Modes%20–%20Critical-System-PPP%20(v1.0).md)** - 6 analytical frameworks (Devil's Advocate, First Principles, Red Team, etc.)
- **[🔧 Custom Report Builder](EU-DRULE/addons/[EU-DRULE-ADDON-02]%20Custom%20Report%20Prompt%20Builder%20–%20NotebookLM%20(v1.0).md)** - Modular prompt generator
- **[📊 Report Format Toolkit](EU-DRULE/addons/[EU-DRULE-ADDON-03]%20Report-Format-Toolkit%20(v1.0).md)** - 10 professional report templates

---

### 🗣️ Conf-Intel - Meeting Intelligence System (v2.4)
*A comprehensive multi-layer workflow for extracting deep insights from meeting recordings and transcripts*

**[📖 View Conf-Intel Documentation](conf-intel/README.md)**

**Core Components:**
- **[🔄 M1: Holographic Restoration](conf-intel/)** - Complete meeting reconstruction with structure and key data
- **[🔍 M2: Deep Insight Matrix](conf-intel/)** - Multi-dimensional analysis (Logic Audit, Strategic Assessment, Knowledge Discovery)
- **[📋 M3: Executive Synthesis](conf-intel/)** - Cross-meeting integration and macro perspectives
- **[✍️ M4: Draft Generation](conf-intel/)** - Scenario-based output generation

**Key Features (v2.4):**
- **Standalone Architecture**: All modules run independently on Raw Data ("Source Resilience").
- **North Star Directive**: Embedded logic prioritizes user intuition (`[Notes]`) over AI analysis.
- **EICO Strategy**: English Instructions, Chinese Output for maximum logic and fluency.

**Quick Links:**
- **[📄 All-in-One (EN Edition)](conf-intel/consolidated/all-in-one.md)** - Complete conference analysis workflow (v2.4)
- **[CN: Complete Analysis Workflow](conf-intel/cn/conf-m2-insight-matrix-v2.4.md)** - Chinese comprehensive system
- **[EN: Module 2 Deep Insights](conf-intel/en/conf-m2-universal-en-v2.4.md)** - English analytical framework
- **[EN: Executive TL;DR](conf-intel/en/conf-m3-executive-tldr-en-v2.2.md)** - Decision-maker summary

---

## 📋 Core Prompt Collections

*These are the foundational prompt libraries. For specialized systems with their own comprehensive prompt ecosystems, see [EU-DRULE](EU-DRULE/README.md) and [Conf-Intel](conf-intel/README.md).*

### 🎯 Quick Access Matrix

| **Purpose** | **Prompts** | **Quick Link** |
|------------|-------------|----------------|
| **🔍 Quick Evaluation** | 3 prompts for rapid report assessment | [View Analysis →](#quick-evaluation-prompts-analysis) |
| **📊 Data Extraction** | 5 prompts for specific information extraction | [View Extraction →](#data-extraction-prompts) |
| **📝 Report Generation** | 2 prompts for comprehensive outputs | [View Generation →](#report-generation-prompts) |
| **🤖 System Configuration** | 1 prompt for AI personality setup | [View System →](#system-prompts) |

### 📖 Comprehensive Compilation
- **[📄 All Prompts (Single File)](report-analysis/one-in-all/all-prompts.md)** - Complete collection with descriptions and usage guidance in both English and Chinese

---

## 🤖 System Prompts

- **[The Jaded Report Reader](report-analysis/system-prompts/report-skeptic.md)** - A personality-defining system prompt for creating a skeptical assistant that evaluates reports with healthy skepticism

---

## 🔍 Quick Evaluation Prompts (Analysis)

*For rapid assessment of report value and originality*

- **[Anything Interesting?](report-analysis/analysis/anything-interesting.md)** - Evaluates whether a report contains original ideas, noteworthy statistics, or strong opinions
- **[Original Thinking?](report-analysis/analysis/original-thinking.md)** - Assesses whether a report contains genuinely new ideas or just regurgitated content
- **[Worth The Read?](report-analysis/analysis/worth-the-read.md)** - Provides a verdict on whether a report justifies the reader's time investment

---

## 📊 Data Extraction Prompts

*For extracting specific types of information from reports*

- **[Main Arguments Roundup](report-analysis/extraction/main-arguments.md)** - Identifies and summarizes the report's core thesis, supporting arguments, evidence strength, and counterarguments
- **[Noteworthy Findings](report-analysis/extraction/noteworthy-findings.md)** - Identifies unexpected or novel findings that contradict or extend previous research
- **[Interesting Statistics](report-analysis/extraction/interesting-stats.md)** - Extracts and organizes key statistics thematically with page references
- **[Case Studies Analysis](report-analysis/extraction/case-studies.md)** - Extracts and organizes case studies thematically, identifying what they demonstrate and providing page references
- **[Key Snippets](report-analysis/extraction/key-snippets.md)** - Extracts memorable quotes and key passages from the report

---

## 📝 Report Generation Prompts

*For creating comprehensive analysis outputs*

### Executive Summary
- **[Executive Summary](report-analysis/generation-prompts/exec-summary/exec-summary.md)** - Generates a critical executive summary evaluating both content and credibility

### Comprehensive Analysis
- **[Comprehensive Report Analysis](report-analysis/generation-prompts/combined/comprehensive-report-analysis.md)** - An all-in-one prompt combining read/skip assessment, opinionated executive summary, statistical overview, case studies analysis, and key quotes extraction

## 💡 How to Use These Prompts

### 🚀 Quick Start Options

1. **📄 All-in-One**: Use the [comprehensive file](report-analysis/one-in-all/all-prompts.md) for all prompts in one place
2. **🇪🇺 EU-DRULE**: For EU regulations, use the [specialized system](EU-DRULE/README.md)
3. **🗣️ Conf-Intel**: For meeting analysis, use the [conference intelligence system](conf-intel/README.md)
4. **🎯 Individual**: Pick specific prompts from the categories below

### 📱 NotebookLM Workflow

![NotebookLM Screenshot 1](screenshots/1.png)

![NotebookLM Screenshot 2](screenshots/2.png)

**Current UI Flow (as of November 2025):**

1. Add report as source
2. Go to Studio
3. Create report
4. Create your own
5. Copy and paste a prompt from this repository

### 🎯 Prompt Selection Guide

| **Your Goal** | **Recommended Prompt** | **Category** |
|---------------|----------------------|--------------|
| "Should I even read this?" | [Worth The Read?](report-analysis/analysis/worth-the-read.md) | Quick Evaluation |
| "Anything actually new here?" | [Original Thinking?](report-analysis/analysis/original-thinking.md) | Quick Evaluation |
| "Just give me the key points" | [Executive Summary](report-analysis/generation-prompts/exec-summary/exec-summary.md) | Report Generation |
| "I need specific data" | [Interesting Statistics](report-analysis/extraction/interesting-stats.md) | Data Extraction |
| "Analyze EU regulations" | [EU-DRULE System](EU-DRULE/README.md) | Specialized System |
| "Analyze meeting recordings" | [Conf-Intel System](conf-intel/README.md) | Specialized System |
| "Everything in one go" | [Comprehensive Analysis](report-analysis/generation-prompts/combined/comprehensive-report-analysis.md) | Report Generation |

---

## 🏗️ Repository Structure

```
NotebookLM-Custom-Prompts/
├── 📋 README.md                    # This file
├── 🇪🇺 EU-DRULE/                   # Specialized EU regulation analysis system
│   ├── core-prompts/               # Multi-role AI analyst (v1.4)
│   ├── addons/                     # Extension packages
│   └── docs/                       # Design documentation
├── 🗣️ conf-intel/                  # Conference/meeting intelligence system
│   ├── cn/                         # Chinese optimized versions
│   ├── en/                         # English versions (EICO strategy)
│   ├── overview/                   # System architecture
│   └── review/                     # Design evaluations
├── 📊 report-analysis/             # Report analysis and insight prompts
│   ├── 🔍 analysis/                # Quick evaluation prompts
│   ├── 📊 extraction/              # Data extraction prompts
│   ├── 📝 generation-prompts/      # Report generation prompts
│   ├── 🤖 system-prompts/          # System configuration prompts
│   └── 🚀 one-in-all/              # All prompts in single file
└── 📸 screenshots/                 # Usage examples
```

---

## 🤝 Contributing

Feel free to submit issues or enhancement requests. When adding new prompts:

1. Follow the existing naming conventions
2. Include clear descriptions and use cases
3. Test with NotebookLM's 300-word limit
4. Consider adding to the [all-in-one file](report-analysis/one-in-all/all-prompts.md)

---

*Last updated: December 2025 | Prompts optimized for NotebookLM's 300-word limit* 