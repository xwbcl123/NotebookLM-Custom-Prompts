# EU-DRULE 🇪🇺

EU Digital Regulation Analysis System - A modular prompt system designed for NotebookLM to conduct in-depth analysis of EU digital regulation reports.

## 🎯 System Overview

EU-DRULE is a multi-role AI analysis system specifically designed for parsing and analyzing EU digital regulation documents. The system features a modular architecture, including a core engine and extensible plugin packages, providing users with comprehensive regulatory analysis capabilities.

### Core Features
- **Multi-Role Analysis**: Legal Expert, Policy Analyst, Impact Assessor, Action Advisor, Consultation Specialist, Intelligence Analyst
- **Modular Extensions**: Support for dynamic loading of functional extension packages
- **Structured Output**: Multiple report format templates
- **Meta-Analysis Capabilities**: Integration of critical thinking and system dynamics methodologies

## 📁 Directory Structure

### 🚀 core-prompts/
**Core System Prompt Files** - EU-DRULE's analysis engine

Contains the system's core prompt files:
- `EU-DRULE-SystemPrompt-Core-v1.3.md` - Core system prompt v1.3
- `EU-DRULE-SystemPrompt-Core-v1.4.md` - Core system prompt v1.4 (supports ADDON integration)
- `notebooklm_eu_reg_system_prompt_v1_3.md` - English version core prompt v1.3
- `notebooklm_eu_reg_system_prompt_v1_4.md` - English version core prompt v1.4

### 🔧 addons/
**Extension Package Files** - System functionality enhancement modules

Contains 4 main extension packages:

#### 📋 [EU-DRULE-ADDON-00] Guideline – Extension Package Design (v1.0).md
Standards and specifications for extension package development, providing a design framework for creating new extension packages.

#### 🧠 [EU-DRULE-ADDON-01] Thinking-Modes – Critical-System-PPP (v1.0).md
Enhanced analysis methodologies, providing:
- `/critical` - Critical analysis mode
- `/system` - System dynamics analysis
- `/ppp` - Public-Private Partnership analysis

#### 🛠️ [EU-DRULE-ADDON-02] Custom Report Prompt Builder – NotebookLM (v1.0).md
Meta-prompt system for generating structured NotebookLM report prompts, supporting the `/rprompt` command.

#### 📊 [EU-DRULE-ADDON-03] Report-Format-Toolkit (v1.0).md
Contains 10 professional report format templates:
- Impact Analysis Report
- White Paper
- Policy Brief
- Regulatory Compliance Assessment
- Risk Assessment Report
- Implementation Roadmap
- Stakeholder Analysis
- Cost-Benefit Analysis
- Technical Standards Evaluation
- Strategic Recommendation Report

### 📚 docs/
**Documentation Files** - Project documentation and design reflections

- `prompt-design-reflection-20251126.md` - Prompt design reflection log (2025-11-26)
- `prompt-design-reflection-20251128.md` - Prompt design reflection log (2025-11-28)

Documents the evolution journey and key insights of the EU-DRULE system from simple prompts to modular architecture.

## 🔧 Usage Instructions

### Basic Usage
1. Import core system prompt files into NotebookLM as primary analysis sources
2. Load corresponding extension package files as needed
3. Use slash commands to activate specific analysis modes

### Extension Integration
- Use NotebookLM's "Source" feature to dynamically load ADDON files
- Different extension packages can be combined for more complex analysis
- Version compatibility: Core v1.4 supports all ADDON v1.0 extension packages

## 📊 Version Information

- **Core System**: v1.3 → v1.4 (added ADDON support)
- **Extension Packages**: v1.0 (all compatible)
- **Language Support**: Chinese + English versions

## 🎯 Application Scenarios

- In-depth analysis of EU digital regulations
- Policy impact assessment
- Regulatory compliance checking
- Strategic recommendation development
- Multi-stakeholder analysis

---

*This system is designed specifically for NotebookLM's single-source deep analysis, with prompt lengths limited to under 300 words to ensure optimal performance.*

---

## 📖 Additional Languages

- **[🇨🇳 中文版 (README-CN.md)](README-CN.md)** - Chinese language documentation