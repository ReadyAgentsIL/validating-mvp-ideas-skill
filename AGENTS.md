# AGENTS.md — validating-mvp-ideas skill

> For Codex, Cursor, Windsurf, and any agent that reads `AGENTS.md`. Merge this block into your project's (or global) `AGENTS.md`.

**When the user proposes a new product / SaaS / business idea, asks "should I build this," or requests market / competitor / demand validation before building**, follow the methodology in `PROMPT.md` (in this repo):

1. Ask first: how many parallel research agents (recommend by scope; their number is a hard cap), which model, and what depth. If you can't spawn sub-agents, run the research sequentially yourself.
2. Score the idea against the 5-part filter — ALL must pass, one hard failure = NO-GO: real-budget buyer · unowned distribution channel · no free incumbent · moat not dependent on platform-controlled data · not a fad with platform-ban risk.
3. Run the research expedition (competitors, demand, buyer pain, willingness-to-pay, feasibility, legal/platform risk, bear case). Require 2+ sources and a confidence rating per claim; reserve a final red-team pass.
4. Deliver a GO / CONDITIONAL-GO / NO-GO verdict with a scorecard, the biggest kill risk, and what evidence would change it.

Full details: see `PROMPT.md`.
