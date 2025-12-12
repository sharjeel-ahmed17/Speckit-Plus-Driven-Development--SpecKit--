# Speckit-Plus Driven Development (SpecKit+)

A complete guide to starting and running AI-native, specification-first projects using **SpecifyPlus** workflow with free Claude Code (via Gemini, Deepseek, Qwen, Bonsai) + MCP + Sub-agents.

Official Book: [https://ai-native.panaversity.org/](https://ai-native.panaversity.org/)

Gemini CLI Tutorial Series:  
https://medium.com/google-cloud/gemini-cli-tutorial-series-77da7d494718

---

## Hackathon Links

1. **Hackathon I: Physical AI & Humanoid Robotics Textbook**  
   [Document Link](https://docs.google.com/document/d/1nw6D37JmTfhPLHo0IfTeCcKajX3Lw9PidDmBjMG1G5o/edit?tab=t.0)

2. **Hackathon II: Todo Spec-Driven Development**  
   [Document Link](https://docs.google.com/document/d/1KHxeDNnqG9uew-rEabQc5H8u3VmEN3OaJ_A1ZVVr9vY/edit?usp=sharing)

## Project Requirements

### Core Tools & Requirements

| Category              | Requirement / Tool                                  | Notes                                      |
|-----------------------|-----------------------------------------------------|--------------------------------------------|
| Main Workflow         | **SpecifyPlus** (`specifyplus`)                     | Spec-driven development CLI                |
| Primary LLM           | **Claude** (free via CCR setups)                    | Gemini / Deepseek / Qwen / Bonsai backends |
| MCP Servers           | GitHub MCP + Context7                               | Model Context Protocol integration         |
| OS (Windows users)    | PowerShell + WSL/Ubuntu/Bash recommended            | Native Bash works best                     |
| OS (Linux/macOS)      | Bash                                                |                                            |

### Software to Install

- **Node.js ≥ v20** → comes with `npm`, `npx` `nvm` (use lts version - https://nodejs.org/en)
- **Python ≥ 3.12** → install `uv` for fast Python tooling (https://www.python.org/downloads/)

### Supported Terminals

- PowerShell (Windows)
- Command Prompt (Windows)
- Bash (Linux/macOS/WSL)
- WSL / Ubuntu terminal

### CLI Tools Used

- `github` (GitHub CLI - https://cli.github.com)
- `gemini` (Google Gemini CLI - https://geminicli.com/)
- `qwen` (Alibaba Qwen CLI - https://github.com/QwenLM/qwen-code)
- `bonsai` (Bonsai CLI – https://docs.trybons.ai/bonsai-cli)

### CCR (Claude Code Runner) Free Setups

| Model       | Setup Guide                                                                                                    |
|-------------|----------------------------------------------------------------------------------------------------------------|
| Gemini      | https://ai-native.panaversity.org/docs/AI-Tool-Landscape/claude-code-features-and-workflows/free-claude-setup |
| Deepseek    | https://github.com/Mohsinraza23/Claude-Code-Gemini-Full-Setup                                                   |
| Qwen        | https://github.com/DanielHashmi/Q4_learning/blob/main/spec-driven-development/tutorials/How%20to%20Use%20Claude%20Code%20with%20Qwen%20models%20for%20Free%20on%20Linux%20and%20macOS%20(sh%20and%20bash).md |
| Bonsai        | https://docs.trybons.ai/bonsai-cli                                                                             |

### Architecture

- `specify` → basic spec-driven workflow (https://github.com/github/spec-kit)
- `specifyplus` → advanced version with MCP, sub-agents, skills, and orchestration (https://github.com/panaversity/spec-kit-plus)

### MCP (Model Context Protocol) Servers

- Official list: https://github.com/modelcontextprotocol
- Integration guide with Claude Code:  
  https://ai-native.panaversity.org/docs/AI-Tool-Landscape/claude-code-features-and-workflows/mcp-integration

### Sub-agents & Skills

- Sub-agents & Orchestration:  
  https://ai-native.panaversity.org/docs/AI-Tool-Landscape/claude-code-features-and-workflows/subagents-and-orchestration
- Agent Skills:  
  https://ai-native.panaversity.org/docs/AI-Tool-Landscape/claude-code-features-and-workflows/agent-skills

### Claude Code Cheat Sheet

https://github.com/DanielHashmi/Q4_learning/blob/main/spec-driven-development/tutorials/%F0%9F%9A%80%20The%20Ultimate%20Claude%20Code%20CheatSheet.md

---

## How to Start a New Project (SpecKit+ Flow)

```bash
# 1. Initialize project
specifyplus init <projectName>

# 2. Select backend LLM (you will be prompted)
#    → Choose Claude via Gemini / Deepseek / Qwen / Bonsai

# 3. Select terminal/shell
#    Windows → PowerShell (or Bash via WSL)
#    Linux/macOS → Bash

# 4. Add MCP servers (project + global level)
#    (follow prompts or manually edit .mcp/config.json)

# 5. Create agents & skills (optional but recommended)
#    → Follow the sub-agents guide above

# 6. Create AGENTS.md in project root
#    Template: https://agents.md/
```

### Full SpecKit+ Workflow (per spec)

```text
One-time (project level):
/sp.constitution        ← Set project principles, constraints, success criteria

For each new feature/spec:

1. /sp.specify           ← Write the specification
2. /sp.clarify (optional) ← Ask questions, remove ambiguity
3. /sp.plan              ← Architecture, research approach, decisions, testing strategy
4. /sp.tasks             ← Generate task breakdown
5. /sp.analyze (optional) ← Deeper analysis, trade-offs
6. /sp.implement         ← Start coding/research/writing
   or
   /sp.implement phase <name>   ← e.g., /sp.implement phase research
```

### Example Prompts

#### 1. Constitution (run once)
```
/sp.constitution

Project: Research paper on AI-native software development

Core principles:
- Accuracy through primary source verification
- Clarity for academic audience (computer science background)
- Reproducibility (all claims cited and traceable)
- Rigor (peer-reviewed sources preferred)

Key standards:
- All factual claims must be traceable to sources
- Citation format: APA style
- Source types: minimum 50% peer-reviewed articles
- Plagiarism check: 0% tolerance before submission
- Writing clarity: Flesch-Kincaid grade 10-12

Constraints:
- Word count: 5,000–7,000 words
- Minimum 15 sources
- Format: PDF with embedded citations

Success criteria:
- All claims verified against sources
- Zero plagiarism detected
- Passes fact-checking review
```

#### 2. Specification Example
```
/sp.specify Research paper on AI's impact on K-12 classroom efficiency

Target audience: Education administrators evaluating AI adoption
Focus: Teacher workload reduction and student outcome improvements

Success criteria:
- Identifies 3+ concrete AI applications with evidence
- Cites 8+ peer-reviewed academic sources
- Reader can explain ROI of classroom AI after reading
- All claims supported by evidence

Constraints:
- Word count: 3000–5000 words
- Format: Markdown source, APA citations
- Sources: Peer-reviewed journals, published within past 10 years
- Timeline: Complete within 2 weeks

Not building:
- Comprehensive literature review of entire AI field
- Comparison of specific AI products/vendors
- Discussion of ethical concerns (separate paper)
- Implementation guide or code examples
```

#### 3. Plan Example
```
/sp.plan

Create: architecture sketch, section structure, research approach, quality validation.
Decisions needing documentation: list important choices with options and tradeoffs.
Testing strategy: validation checks based on acceptance criteria.

Technical details:
- Use research-concurrent approach (research while writing, not all upfront)
- Follow APA citation style from Constitution
- Organize by phases: Research → Foundation → Analysis → Synthesis
```

#### 4. Tasks & Implementation
```
/sp.tasks
/sp.implement
# or phased
/sp.implement phase research
/sp.implement phase writing
```

---


## start project 

- specifyplus init <projectName>
- select claude 
- select powershell (for window-user (use bash linux or mac))
- add mcp server (project and global level)
- create (agents and skills)
- create AGENTS.md in root directory (https://agents.md/)

## SpecKit+ Workflow Commands

### One-Time Setup
- `/sp.constitution`  
  (Run once per project; can be updated later as needed)

### Per-Spec Workflow
Repeat the following sequence for each new specification/feature:

#### First Spec (and every subsequent spec)
1. `/sp.specify`  
   Define the specification
2. `/sp.clarify` *(optional)*  
   Ask clarifying questions to remove ambiguity
3. `/sp.plan`  
   Create architecture sketch, section structure, research approach, decisions, and testing strategy
4. `/sp.tasks`  
   Generate a detailed task breakdown
5. `/sp.analyze` *(optional)*  
   Perform deeper analysis or trade-off evaluation
6. `/sp.implement`  
   **or**  
   `/sp.implement phase <phase-name>`  
   (e.g., `/sp.implement phase research`, `/sp.implement phase coding`)

#### Example for Second Spec
1. `/sp.specify`
2. `/sp.clarify` *(optional)*
3. `/sp.plan`
4. `/sp.tasks`
5. `/sp.analyze` *(optional)*
6. `/sp.implement` **or** `/sp.implement phase <name>`

#### Example for Nth Spec
1. `/sp.specify`
2. `/sp.clarify` *(optional)*
3. `/sp.plan`
4. `/sp.tasks`
5. `/sp.analyze` *(optional)*
6. `/sp.implement` **or** `/sp.implement phase <name>`

> **Tip**: The workflow is iterative. You can revisit earlier steps (e.g., clarify or re-plan) as new information emerges during implementation.

## Official Hands-on Guide

Follow along with the complete step-by-step tutorial:  
https://ai-native.panaversity.org/docs/SDD-RI-Fundamentals/spec-kit-plus-hands-on

Happy spec-driven building! 🚀
