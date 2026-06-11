# validating-mvp-ideas — a Claude Code skill

A rigorous **pre-MVP idea validation** skill for Claude Code. Before you build anything, it runs your idea through a hard market filter using parallel research agents — so you kill bad ideas in minutes instead of wasting weeks of build + months of failed launch.

## What it does

When you propose a product/SaaS idea or ask "should I build this," the skill:

1. **Asks you first** — how many research agents to spawn (your number is a hard cap), which model, and how deep — with a recommendation for your specific task.
2. **Runs a parallel research expedition** — independent agents covering competitors, demand, buyer pain, willingness-to-pay, feasibility, legal/platform risk, and a dedicated bear case — each required to cite 2+ sources and rate its confidence.
3. **Scores the idea against a 5-part filter** (ALL must pass):
   - Buyer with a real budget
   - A distribution channel you can reach that a competitor doesn't own
   - No dominant incumbent giving the core away free
   - A moat that doesn't depend on data only a platform controls
   - Durable, not a fad with platform-ban risk
4. **Reserves a red-team agent** to attack the surviving conclusion before any verdict.
5. **Delivers a GO / CONDITIONAL-GO / NO-GO** verdict with a scorecard, the biggest kill risk, and what evidence would change the answer.

## Install (paste this into Claude Code)

> Clone `https://github.com/ReadyAgentsIL/validating-mvp-ideas-skill` and copy the `validating-mvp-ideas` folder into my `~/.claude/skills/` directory so the skill is available. Confirm it's installed.

## Manual install

```bash
git clone https://github.com/ReadyAgentsIL/validating-mvp-ideas-skill.git
cp -R validating-mvp-ideas-skill/validating-mvp-ideas ~/.claude/skills/
```

Then start a new Claude Code session and the skill triggers automatically whenever you bring up a new product idea.

## License

MIT — use it, share it, modify it.
