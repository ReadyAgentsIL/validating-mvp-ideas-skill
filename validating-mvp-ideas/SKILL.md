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
| Multiple candidate ideas (funnel) | 2–3 screen agents score the WHOLE batch, then full validation only on survivors | Sonnet screen; escalate per row above |

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
- Every agent prompt must: state today's date, require WebSearch/WebFetch, require 2+ independent sources per load-bearing claim, require a URL per claim (the gate below needs them), require explicit labeling of any absence-of-evidence claim as `UNVERIFIED-ABSENCE`, cap output (~650 words), forbid file writes, and instruct "be brutally honest — if the space is occupied, say so; that kills the thesis."
- Source classes (used by the gate): **PRIMARY** = platform docs/changelogs, pricing pages, filings, dated press releases by the company itself · **PRESS** = named independent outlet · **VENDOR-SEO** = competitor blogs and self-descriptions ("the leading X platform" is marketing, not fact) · **UGC** = Reddit/forums/X (excellent for pain language, unreliable for numbers) · **AI-WIKI** = AI-generated aggregators (Grokipedia etc.) — never load-bearing.
- Reserve the final agent as a red-team verifier that attacks the surviving conclusion AND its evidence ledger. MANDATORY before any GO or CONDITIONAL-GO — red-teams routinely kill the "open wedge" the finder agents missed. The ONLY permitted skip: a decisive NO-GO whose kill rests on primary-verified cruxes (don't pay agents to re-confirm a dud). If the NO-GO leans on anything weaker than primary-verified evidence, the red-team still runs.

## Phase 3.5 — Verification gate (MANDATORY before any verdict)

Multi-agent research produces confident-sounding synthesis of unverified claims — the #1 failure mode. This gate converts "agents said so" into graded evidence. It costs roughly zero extra agents: steps 1–4 and 6 are orchestrator discipline; step 5 is a few WebFetches or one verifier agent (counts toward the cap).

1. **Build the claim ledger.** Every load-bearing claim from every agent: claim | URL(s) | source class | which agents cited it | role (CRUX / supporting / color). **Correlation rule: two agents citing the same URL = ONE source, not two.** Agent reports routinely converge on the same 4–5 pages; "independently confirmed" must mean independent *origins*.
2. **Reconcile cross-agent contradictions.** Hunt for numbers that cannot coexist (e.g., "3.5B monthly views" and "$1.7M lifetime payouts" imply a CPM under $0.001 — one is wrong or stale). An unresolved contradiction touching a crux blocks the verdict.
3. **Extract the cruxes (≤5).** A crux is a claim that flips the verdict if false. Write each as "If X is false, the verdict becomes Y." If you can't name the cruxes, you don't understand your own verdict yet.
4. **Discard agent confidence stamps.** Agents rating their own claims "high confidence" is self-grading homework. Confidence is assigned by this gate from source class and verification status — never inherited.
5. **Primary-verify every crux.** Fetch the primary source yourself; capture a verbatim quote + URL + publication date. Mandatory first for: conveniently-timed claims ("announced yesterday"), single-source kill-shots, and any crux currently resting on VENDOR-SEO/AI-WIKI. A crux that survives only on those classes — or on UNVERIFIED-ABSENCE — is NOT verified.
6. **Run the flip test.** Write the strongest concrete case that your verdict is wrong. If that case requires only facts you haven't primary-verified, the verdict isn't done — verify them or downgrade.

**Confidence caps:** crux primary-verified with quote → may state high confidence · PRESS-corroborated (independent origins) → medium · VENDOR-SEO / AI-WIKI / single-source / UNVERIFIED-ABSENCE → low, can never alone justify GO or NO-GO; mark the verdict "(provisional)" if it leans on one.

## Phase 4 — Verdict format

Deliver: **GO / CONDITIONAL-GO / NO-GO** + a filter scorecard (pass/fail per criterion with evidence) + the single biggest kill risk + what new evidence would change the verdict + recommended next action.

Plus a **reliability statement** — this is what makes the verdict trustable without double-checking:
- **Verified** (primary source, quoted): the cruxes and their quotes/dates.
- **Corroborated** (independent press/multi-origin): claims believed but not primary-verified.
- **Still assumed**: anything load-bearing that resisted verification — stated plainly, with how it skews the verdict if wrong.
- **Check-it-yourself in 10 minutes**: for each crux, the one URL or action the user can use to confirm it independently.

## Common mistakes

| Excuse | Reality |
|---|---|
| "Demand is huge, so competition matters less" | Both must pass. Massive-demand spaces still yield single-digit success odds when occupied. |
| "We already researched the adjacent space" | Every pivot changes the buyer — re-run the filter on the NEW buyer. |
| "Founder reports $X MRR" | Self-reported ≠ verified. Check for Stripe/third-party verification. |
| "I know the scope, skip asking the user" | Agent count, model, and budget are the user's call. Ask first, every time. |
| "Research was thorough, red-team is redundant" | Mandatory before any GO/CONDITIONAL-GO — it kills what nine thorough agents missed. Only a decisive, primary-verified NO-GO may skip it. |
| "Three agents confirmed it" | If they cite the same page, it's one source wearing three hats. Check origins, not counts. |
| "The agent said high confidence" | Self-rated stamps are theater. The gate assigns confidence from source class + verification. |
| "Found no complaints, so the pain isn't real" | Ten minutes of searching absence is not absence. UNVERIFIED-ABSENCE is never load-bearing. |
| "An article about the market says..." | Check the domain owner. Vendor SEO poses as neutral analysis; a competitor's blog is marketing. |
| "It was announced yesterday — game over" | Conveniently-timed kill-shots are exactly the claims most worth a verbatim-quote check. |

## Red flags — STOP

- About to dispatch agents without the Phase 1 questions answered
- A verdict forming from one source or self-reported revenue
- Declaring a wedge "open" without a red-team pass
- Exceeding the user's agent cap for any reason
- About to deliver a verdict without the claim ledger, crux list, and flip test (Phase 3.5)
- A crux sourced to an AI-generated wiki, a competitor's blog, or "we found nothing"
- Two agents' numbers contradict and the synthesis quietly picked one
- Quoting an agent's "high confidence" as if it were your own verification
