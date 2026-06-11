---
name: hunting-mvp-ideas
description: Use when the user wants to FIND a product, SaaS, or business idea without a specific idea in hand — "find me an idea", "loop until you find a GO idea", "hunt for a niche", or screening/batch-validating several candidate ideas at once.
---

# Hunting MVP Ideas

## Overview

A loop engine: generate candidate ideas → screen them cheaply → escalate only survivors to deep validation → repeat until one earns a GO or the budget cap is hit. Full validation costs ~8–11 agents and is irreducible, so this skill's entire job is to guard escalation and never pay twice for the same lesson. Stopping at the cap with no GO is a valid, honest outcome — report it plainly.

**REQUIRED SUB-SKILL:** deep validation of a surviving candidate uses validating-mvp-ideas (its Phase 1 questions, 5-part filter, verification gate, and verdict format). This skill orchestrates; that skill judges.

## Phase 1 — Ask before hunting (MANDATORY)

Use AskUserQuestion, recommendation listed first and marked "(Recommended)":

1. **Hunting ground** — which domain/edge to bias toward. An owned audience or insider knowledge beats every other factor; ask if they have one.
2. **Budget cap** — a hard ceiling (agents or full validations, e.g. "stop after 3 full validations"). Track spend against it; never exceed it.
3. **Stop condition** — first clean GO, or accept a CONDITIONAL-GO with a fix plan (faster, riskier).
4. **Check-in cadence** — e.g. pause and report after every K NO-GOs.

## The ledger — never pay twice

Maintain `mvp-hunt-ledger.md` in the working directory.

- **Before generating candidates:** read it. Never re-test a rejected idea. Treat its pattern lessons as generation constraints (e.g. "legible compliance niches keep having funded incumbents — bias away from them").
- **After every verdict:** append one row — date · idea · verdict · killing criterion · pattern lesson — BEFORE starting the next iteration.

## Loop body (one iteration)

1. **Generate 3–5 candidates**, biased by the hunting ground and ledger lessons.
2. **Cheap screen — 2–3 Sonnet agents for the whole batch**, each scoring ALL candidates from one lens: (a) competition / free-incumbent, (b) demand / buyer budget, (c) build feasibility + distribution. Cited evidence, honest 🟢/🟡/🔴 per candidate per lens.
3. **Kill and log** every candidate rated 🔴 on any lens.
4. **Escalate at most ONE survivor per iteration** to validating-mvp-ideas for full validation.
5. **On the verdict:** GO (or accepted CONDITIONAL-GO) → stop, deliver it with the validator's full scorecard + recommended next action. NO-GO → write the ledger row, check cadence and budget, start the next iteration.

## Red flags — STOP

- Generating candidates without reading the ledger first
- Escalating 2+ ideas from one screen — "they both look good" means the screen failed to discriminate; tighten it instead
- Any spend past the user's cap, for any reason
- A NO-GO not written to the ledger before the next iteration begins
- Running full validation on a candidate the screen already killed

## Common mistakes

| Excuse | Reality |
|---|---|
| "The screen is cheap insurance, skip it and validate directly" | Full validation is ~8–11 agents. The screen exists so duds die at 3. |
| "This rejected idea is different now" | Only if NEW primary evidence defeats the recorded kill-reason. Otherwise the ledger stands. |
| "We're so close — one more idea past the cap" | The cap is the user's, not yours. Stop, report, and ask. |
| "No GO found means the hunt failed" | A capped-out hunt with a clean ledger of kills is paid-for knowledge. Report it as such. |
