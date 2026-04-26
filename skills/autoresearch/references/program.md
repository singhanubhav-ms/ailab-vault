# Research Program

This file configures the Lighthouse autoresearch loop. The autoresearch skill reads it before every run.

---

## Search Objectives

Default objectives for every research session:

- Read existing `wiki/` coverage first so you do not redo work already filed.
- Find authoritative sources. Prefer official documentation, primary sources, established publications, peer-reviewed research, and public filings.
- Extract key entities, concepts, frameworks, and important dates.
- Note contradictions between sources and explain which source is more credible.
- Identify open questions and research gaps.
- Prefer sources from the last 2 years unless the topic is foundational or historical.

---

## Prompt Completeness Gate

Before searching, check whether the topic is specific enough.

Ask 2-3 clarifying questions if any of these are true:

- The prompt is under 15 words.
- The prompt starts with `what is`, `how to`, or `explain` without scope.
- The prompt gives no timeframe, audience, or depth signal.

Question banks:

- Scope/timeframe: specific time period, geography, industry, or sub-domain.
- Depth: quick primer vs deep dive, and whether actionable next steps are required.
- Focus: technical detail vs general overview, trusted source types, and deliberate exclusions.

If the prompt mentions code, APIs, schemas, configs, frameworks, or implementation details, bias technical. Otherwise bias general.

---

## Prompt Audit Trail

Before the first web search, save the final clarified prompt to:

`prompts/research_prompt_YYYYMMDD_HHMMSS.txt`

This is mandatory. Do not search first and save later.

---

## Confidence Scoring

Label every material claim with confidence when filing:

- **high**: multiple independent authoritative sources agree.
- **medium**: one good source, or sources partially agree.
- **low**: speculation, opinion pieces, single informal source, or claim not fully verified.

Always note the source date for factual claims. Mark claims from sources older than 3 years as potentially stale.

---

## Loop Constraints

- Max search rounds per topic: **3**
- Max web searches per task: **15**
- Max sources fetched per round: **5**
- Max wiki pages created per session: **15**
- Use a cheap tier for planning and scoping. Use a premium tier only for final synthesis when needed.
- If the page cap is reached before the loop completes, file what you have and note what was skipped in Open Questions.
- If a provider rate-limits, stop the loop, file partial results, and say what is missing.

---

## Output Style

- Declarative, present tense.
- Cite every non-obvious claim.
- Short pages: under 200 lines. Split if longer.
- No hedging language such as `it seems`, `perhaps`, or `might be`.
- Flag uncertainty explicitly.
- Prefer concrete evidence over trend-summary language.

---

## Domain Notes

This workspace is Lighthouse, Anubhav's multi-domain AI lab.

- For AI and technical research, prefer official product docs, GitHub repos, standards/specs, arXiv, and direct source code over secondary commentary.
- For business and market research, prefer filings, verified industry reports, regulatory texts, and first-party company material over press releases.
- For India-specific questions, prefer Indian regulatory, market, and policy sources when available.
- When the wiki already contains relevant source notes, use them before fetching fresh web material.
- When facts materially conflict, say so explicitly instead of averaging them together.

---

## Exclusions

Do not cite these as high-confidence sources:

- Reddit posts or forums, except as leads to primary sources.
- Social media posts.
- Undated web pages.
- Sources that do not cite their own claims.
