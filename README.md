# validating-mvp-ideas — a cross-IDE AI skill

A rigorous **pre-MVP idea validation** skill for AI coding agents. Before you build anything, it runs your idea through a hard market filter using (parallel) research — so you kill bad ideas in minutes instead of wasting weeks of build + months of failed launch.

Works on **Claude Code, Codex, Cursor, Windsurf, Google Antigravity, Gemini CLI, and any agent that takes custom instructions.**

## What it does

When you propose a product/SaaS idea or ask "should I build this," the skill:

1. **Asks you first** — how many research agents to run (your number is a hard cap), which model, and how deep.
2. **Runs a research expedition** — competitors, demand, buyer pain, willingness-to-pay, feasibility, legal/platform risk, and a dedicated bear case — each with 2+ cited sources and a confidence rating.
3. **Scores against a 5-part filter** (ALL must pass):
   - Buyer with a real budget
   - A distribution channel you can reach that no competitor owns
   - No dominant incumbent giving the core away free
   - A moat that doesn't depend on data only a platform controls
   - Durable, not a fad with platform-ban risk
4. **Reserves a red-team agent** to attack the conclusion before any verdict.
5. **Delivers GO / CONDITIONAL-GO / NO-GO** with a scorecard, the biggest kill risk, and what evidence would change the answer.

---

## Install — paste this into your AI agent (any IDE)

> Install the AI skill at `https://github.com/ReadyAgentsIL/validating-mvp-ideas-skill`. Clone or fetch it, read its README, and set it up the correct way for whatever IDE/agent I'm using:
> - **Claude Code** → copy the `validating-mvp-ideas` folder into `~/.claude/skills/`
> - **Codex / Cursor / Windsurf** (anything using `AGENTS.md`) → merge this repo's `AGENTS.md` into my global or project `AGENTS.md`, and keep `PROMPT.md` alongside it
> - **Anything else** (Antigravity, Gemini CLI, etc.) → save `PROMPT.md` wherever that tool loads custom rules/instructions/memory
>
> Then confirm it's installed and tell me how to trigger it.

Your agent reads the README and installs the right format for its own platform.

## What each file is for

| File | For |
|---|---|
| `validating-mvp-ideas/SKILL.md` | **Claude Code** native skill (auto-triggers, spawns parallel agents) |
| `AGENTS.md` | **Codex / Cursor / Windsurf** and other `AGENTS.md`-based agents |
| `PROMPT.md` | **Universal** — paste into any agent as a custom rule/instruction |

> Note: only Claude Code gets full auto-trigger + parallel-agent speed. On other IDEs the agent follows the same logic, running the research sequentially (or with that tool's own multi-agent feature, if it has one).

---

## How to use it once installed

You don't run a command — just talk to your agent. It triggers when you do any of these:

- "I have an idea: **[your idea]**. Should I build it?"
- "Validate this idea before I build it: **[idea]**"
- "Is there a market / real demand for **[idea]**?"
- "Research the competition for **[idea]**."

The agent will then ask you the 3 setup questions (how many agents, which model, how deep), run the research, and hand you a **GO / CONDITIONAL-GO / NO-GO** verdict with a scorecard.

> Tip: on Claude Code you can also just describe the idea and the skill fires automatically. On other tools, if it doesn't trigger, say: *"Use the validating-mvp-ideas methodology to evaluate this."*

## License

MIT — use it, share it, modify it.
