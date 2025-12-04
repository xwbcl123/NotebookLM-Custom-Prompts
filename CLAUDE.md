# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This repository contains a library of prompts designed for NotebookLM, focusing on single-source analysis of lengthy reports. The project is organized into several specialized systems and prompt categories, with a 300-word limit per prompt imposed by NotebookLM.

## Key Architecture

### Core Components
- **EU-DRULE System**: A comprehensive multi-role AI system specialized for EU digital regulations analysis
- **Prompt Categories**: Analysis, Extraction, Generation, and System prompts
- **All-in-One Compilation**: Single file containing all prompts for easy reference
- **Custom Commands**: Git automation and README updating workflows

### MCP Integration
The repository uses MCP (Model Context Protocol) with MiniMax server:
- **Configuration**: `.mcp.json` contains MiniMax MCP server setup
- **Preferred Tool**: Use MCP tools (`mcp__MiniMax__web_search`) instead of built-in `WebSearch`
- **Image Analysis**: Use `mcp__MiniMax__understand_image` for image content analysis and understanding
- **Alternative**: Use `Task` tool with specialized agents for complex searches

## Essential Commands

### Git Operations
- **`/git-commit [optional context]`**: Automated git workflow that analyzes changes, stages files, generates Chinese commit messages, and commits. Located in `.claude/commands/git-commit.md`
- **Standard git commands**: Use with proper MCP tool integration

### Repository Maintenance
- **`/update-readme`**: Updates README with new prompts and sections (automates documentation updates)
- **Prompt validation**: Ensure all prompts stay within 300-word NotebookLM limit

## File Structure Knowledge

### Main Directories
- `EU-DRULE/`: Specialized EU regulation analysis system with multi-role prompts
- `report-analysis/`: Comprehensive report analysis and insight prompts
  - `analysis/`: Quick evaluation prompts for report assessment
  - `extraction/`: Data extraction prompts for specific information types
  - `generation-prompts/`: Report generation and summary prompts
  - `system-prompts/`: AI personality and system configuration prompts
  - `one-in-all/`: Comprehensive compilation of all prompts
- `.claude/commands/`: Custom automation commands

### Key Files
- `README.md`: Main documentation with prompt matrix and usage guide
- `report-analysis/one-in-all/all-prompts.md`: All prompts compiled with bilingual descriptions
- `CLAUDE.md`: This file - Claude Code operational guidance

## Development Guidelines

### Prompt Development
- **Word Limit**: All prompts must stay under 300 words for NotebookLM compatibility
- **Bilingual Support**: Maintain both English and Chinese descriptions where applicable
- **Naming Convention**: Use descriptive, category-based naming (e.g., `analysis/worth-the-read.md`)

### Adding New Prompts
1. Follow existing directory structure and naming conventions
2. Add to appropriate category (analysis, extraction, generation, system)
3. Update `one-in-all/all-prompts.md` with the new prompt
4. Run `/update-readme` to refresh main documentation
5. Use `/git-commit` with descriptive message for changes

### Content Quality
- Focus on practical, actionable prompts that add value beyond NotebookLM's default behavior
- Maintain the "healthy skepticism" approach found in existing system prompts
- Ensure prompts are optimized for single-source analysis scenarios

## Language Preference
Always respond in Chinese (CN) with proper emoji embedding as specified in the original CLAUDE.md context.

## MCP Tool Usage Strategy
When needing external capabilities:
1. **Web Search**: Use `mcp__MiniMax__web_search` for real-time information and current events
2. **Image Analysis**: Use `mcp__MiniMax__understand_image` for analyzing images from files or URLs
3. **Complex Research**: Use `Task` tool with specialized agents for comprehensive codebase exploration
4. **Avoid Built-in Tools**: Do not use built-in `WebSearch` or similar tools - prefer MCP integration

## Image Analysis Workflow
For image-related tasks:
- Local files: Provide relative or absolute paths (remove @ prefix if present)
- URLs: Provide full HTTP/HTTPS URLs
- Supported formats: JPEG, PNG, WebP
- Use for analyzing screenshots, diagrams, or visual content in the repository 

