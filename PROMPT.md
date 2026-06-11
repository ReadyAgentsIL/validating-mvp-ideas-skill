# validating-mvp-ideas — portable methodology

Paste this into any AI coding agent / IDE as a custom instruction or rule. It is self-contained and assumes no Claude-Code-specific tooling.

**Trigger:** Whenever the user proposes a new product, SaaS, or business idea, asks "should I build this," or requests market / competitor / demand validation before building, follow this process.

## Step 1 — Ask before researching (do this FIRST, every time)
Ask the user, with a recommended default for each:
1. **How many research agents to run in parallel** — recommend by scope: 1–3 for a single fact/competitor, 4–6 for one category's landscape, 8–10 (reserve 1 as red-team) for full validation. The user's number is a hard cap; never exceed it.
2. **Which model** to use for the research agents.
3. **Depth** — quick scan vs full expedition (state the rough token/time cost).

> If your environment cannot spawn parallel sub-agents, say so and run the research **sequentially yourself** — but still ask the questions and still cover every angle.

## Step 2 — The 5-part filter (ALL must pass; one hard failure = NO-GO)
1. **Buyer with a real budget** — kill if willingness-to-pay is anchored to tiny incomes or free-tool culture.
2. **Distribution channel findable AND not competitor-owned** — kill if buyers congregate inside an incumbent's walled garden.
3. **No dominant incumbent giving the core away free** — kill if a platform bundles your product natively.
4. **Moat independent of platform-controlled data** — kill if your quality/accuracy ceiling is structurally below the incumbent's.
5. **Durable, not a fad; no platform-ban exposure** — kill if the core mechanic violates platform ToS or crackdown/backlash press exists.

## Step 3 — Research expedition
Cover these angles (one agent each if parallel; otherwise sequentially):
direct competitors · adjacent incumbents moving in · demand/market size · buyer pain in their own words · willingness-to-pay price anchors · technical feasibility + unit economics · legal/platform risk · a dedicated bear case.

Every research step MUST: state today's date · use web search · cite 2+ independent sources per load-bearing claim · give a confidence rating per conclusion · include URLs · and be told "be brutally honest — if the space is occupied, say so; that kills the thesis."

**Evidence hierarchy:** third-party payment-verified revenue (e.g. Stripe/TrustMRR) > press-corroborated > founder self-reported > listicle/SEO content (treat as noise).

**ALWAYS reserve a final red-team pass** that attacks the surviving conclusion before any verdict — it routinely kills the "open wedge" the finder agents missed.

## Step 4 — Verdict
Deliver: **GO / CONDITIONAL-GO / NO-GO** + a pass/fail scorecard per filter criterion (with evidence) + the single biggest kill risk + what new evidence would change the verdict + a recommended next action.

## Common traps to refuse
- "Demand is huge, so competition matters less" → both must pass.
- "We already researched the adjacent space" → every pivot changes the buyer; re-run the filter on the NEW buyer.
- "Founder reports $X MRR" → self-reported ≠ verified; check for third-party verification.
- "Research was thorough, skip the red-team" → the red-team exists to kill what thorough agents missed.
