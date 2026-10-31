# 🛡️ E.V.A: The Aegis Framework (AI Architect Skill)
**Engineered by [BH-SYSTEMS](https://nexus.bh-systems.be)** | Stop vibecoding. Start architecting.

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![Claude Code](https://img.shields.io/badge/Claude_Code-Compatible-purple.svg)]()
[![Cursor](https://img.shields.io/badge/Cursor-Compatible-black.svg)]()

## ⚠️ The Problem: AI Generates Technical Debt
The era of "vibecoding" is here. AI tools can generate thousands of lines of code in seconds. But there is a dark side nobody talks about: **90% of that output is unscalable, insecure, spaghetti-code that will collapse in production.**

Founders, Lead Devs, and CTOs are handing over their critical projects to AI without an architectural safety net, mistaking speed for engineering. 

## 🏗️ The Solution: The Aegis Framework
At **BH-SYSTEMS**, we refuse to build fragile software. 

We created **E.V.A (Elite Vibecoding Architect)**—a proprietary, master-level gating system for AI coding assistants. 

When you load the E.V.A skill, your AI **will refuse to write a single line of code** until the 8 foundational pillars of Enterprise Architecture are locked in.

---

## 💎 Choose Your Tier

### 🆓 E.V.A [Lite Edition] (Included in this repo)
Perfect for validating a project idea and setting up the basic requirements. The AI will guide you through:
- Document 01: The Golden Circle
- Document 02: PRD (Product Requirements Document)
- Document 03: TRD (Technical Requirements Document)
*The AI will pause execution after Document 03 to prevent insecure coding.*

### 👑 E.V.A [Elite Edition] - 97€
The full Enterprise Architecture protocol. Built for CTOs, agencies, and senior developers who need production-ready, secure, and idempotent code. Unlocks the full 8-Document gating system, strict database idempotency rules, CI/CD pipeline structures, and the Aegis Security Shield.

👉 **[🚀 UNLOCK E.V.A ELITE HERE] https://buy.stripe.com/dRm4gy3EM1zf1c08uQ9EI00**

---

## 🛠️ Installation (Lite Edition)
### For Claude Code
Run these commands from the root of your project. They install two things:
- **the skill** (`.claude/skills/eva-lite/`): what the AI asks, and in which order;
- **the rule** (`CLAUDE.md`): when the skill applies. Without it, a plain request like *"write server.js"* skips the skill and the AI writes code straight away.

macOS / Linux:
```bash
git clone https://github.com/AEGIS-CORE-BH-SYSTEMS/aegis-framework.git /tmp/aegis-framework
mkdir -p .claude/skills
cp -r /tmp/aegis-framework/skills/eva-lite .claude/skills/
cat /tmp/aegis-framework/templates/CLAUDE.md >> CLAUDE.md
```

Windows (PowerShell):
```powershell
git clone https://github.com/AEGIS-CORE-BH-SYSTEMS/aegis-framework.git $env:TEMP\aegis-framework
New-Item -ItemType Directory -Force .claude\skills | Out-Null
Copy-Item -Recurse $env:TEMP\aegis-framework\skills\eva-lite .claude\skills\
Get-Content $env:TEMP\aegis-framework\templates\CLAUDE.md | Add-Content CLAUDE.md
```

`>>` and `Add-Content` append the rule, so an existing `CLAUDE.md` is kept.

Then start Claude Code and ask for anything: *"Build me a todo API in Node.js."* The AI stops, explains why, and asks the 3 questions of Document 01. Each approved document is saved in `docs/` and ends with `Status: approved`.

> E.V.A is instructions the AI reads, not a lock. If you tell it to skip the documents, it can.

### For Cursor / Windsurf
Copy the content of `skills/eva-lite/SKILL.md` into your `.cursorrules` or `.windsurfrules` file.
