---
name: validating-mvp-ideas
description: Use when the user proposes a new product, SaaS, or business idea, asks "should I build this", or requests market research, competitor analysis, demand validation, or niche hunting before committing to build an MVP.
---

# Validating MVP Ideas

## Overview

Kill bad ideas with cheap research before they cost weeks of build plus months of failed go-to-market. An idea is buildable only when demand AND market openness BOTH verify — huge demand alone is never enough. A NO-GO verdict that prevents a doomed build is a win; deliver it plainly.

## Phase 1 — Ask the user BEFORE dispatching (MANDATORY)

Never launch research agents without first using AskUserQuestion to confirm, with your recommendation listed first and marked "(Recommended)":

1. **Agent count** — recommend from the scope table; the user's number is a hard cap. Never exceed it.
2. **Model for research agents** — recommend per task type below.
3. **Depth** — quick scan vs full expedition (affects token spend; state the rough cost).

| Scope | Agents | Model guidance |
|---|---|---|
| Single fact check (pricing, one competitor) | 1–3 | Sonnet |
| Competitive landscape of one category | 4–6 | Opus for adversarial angles, Sonnet for fact-gathering |
| Full idea validation (run the filter below) | 8–10, reserve 1 as red-team | Opus |

## Phase 2 — The 5-Part Filter

ALL five must pass. One hard failure = NO-GO. Assign criteria to dedicated agents; demand cited evidence, not vibes.

| # | Criterion | Kill condition |
|---|---|---|
| 1 | Buyer with a real budget | WTP anchored to tiny incomes or free-tool culture |
| 2 | Distribution channel findable AND not competitor-owned | Buyers congregate inside an incumbent's walled garden |
| 3 | No dominant incumbent giving the core away free | A platform bundles your product natively |
| 4 | Moat independent of platform-controlled data | Your accuracy/quality ceiling is structurally below the incumbent's |
| 5 | Durable, not a fad; no platform-ban exposure | Core mechanic violates platform ToS; crackdown/backlash press exists |

## Phase 3 — Expedition rules

- Dispatch all independent agents in ONE message (parallel), each with a distinct angle.
- Standard angles: direct competitors · adjacent incumbents moving in · demand/market size · buyer pain in their own words · willingness-to-pay price anchors · technical feasibility + unit economics · legal/platform risk · dedicated bear case.
- Every agent prompt must: state today's date, require WebSearch/WebFetch, require 2+ independent sources per load-bearing claim, require a confidence rating per conclusion, cite URLs, cap output (~650 words), forbid file writes, and instruct "be brutally honest — if the space is occupied, say so; that kills the thesis."
- Evidence hierarchy: third-party payment-verified revenue (e.g., TrustMRR/Stripe API) > press-corroborated > founder self-reported > listicle/SEO content (treat as noise).
- ALWAYS reserve the final agent as a red-team verifier that attacks the surviving conclusion before any verdict is delivered. Red-teams routinely kill the "open wedge" the finder agents missed.

## Phase 4 — Verdict format

Deliver: **GO / CONDITIONAL-GO / NO-GO** + a filter scorecard (pass/fail per criterion with evidence) + the single biggest kill risk + what new evidence would change the verdict + recommended next action.

## Common mistakes

| Excuse | Reality |
|---|---|
| "Demand is huge, so competition matters less" | Both must pass. Massive-demand spaces still yield single-digit success odds when occupied. |
| "We already researched the adjacent space" | Every pivot changes the buyer — re-run the filter on the NEW buyer. |
| "Founder reports $X MRR" | Self-reported ≠ verified. Check for Stripe/third-party verification. |
| "I know the scope, skip asking the user" | Agent count, model, and budget are the user's call. Ask first, every time. |
| "Research was thorough, red-team is redundant" | The red-team exists to kill what nine thorough agents missed. Never skip it. |

## Red flags — STOP

- About to dispatch agents without the Phase 1 questions answered
- A verdict forming from one source or self-reported revenue
- Declaring a wedge "open" without a red-team pass
- Exceeding the user's agent cap for any reason
