---
name: quorum
description: >
  Convene an advisory board of real, well-documented experts the user chooses,
  audit their already-launched product or business, and return a prioritized
  backlog, a roadmap, and a council-weighted prioritization framework. Use when
  the user asks for an expert audit or advisory board, a "council" or "board" of
  experts, help prioritizing a backlog or roadmap, a review of their product or
  go-to-market, or says "run quorum" or "/quorum". Built for post-launch,
  pre-scale builders who have something real in production. Not for the idea
  stage, and not for post-product-market-fit scaling.
---

# Quorum

Quorum convenes an advisory board of real, well-documented experts the user chooses, points them at the business the user has already launched, and returns a prioritized, expert-reviewed path forward. The primary output is the audit and the advice. Everything else serves that.

Run this skill as a structured loop. Do not improvise the order. Read `reference/operating-contract.md` before you touch anything else, and hold to it for the entire run.

## When to run, and when to stop

Run Quorum when the user has something real in production: a launched product, a first sale, an MVP that people use, a business that operates. Quorum audits what exists and prioritizes what is next.

Confirm fit with three questions: is there a live product or service, is anyone paying for it or actively using it, and could someone use it today. Two or three yes answers means run. Mostly no means the user is at the idea stage, so say so plainly and stop.

Do not run the full loop for the idea stage, where nothing real exists yet. Do not run it as a scale-optimization engine for a team past product-market fit. In either case, say so plainly, explain why Quorum is the wrong tool, and offer the closest useful alternative. State this as a boundary, not an apology.

## Operating contract (non-negotiable)

Full detail is in `reference/operating-contract.md`. The hard rules:

- The user answers questions up front. After that, proceed on documented defaults and never block waiting on them. Route open decisions to a decisions file.
- Stage everything for review. Publish nothing, send nothing, deploy nothing, and change no live system on the user's behalf.
- Respect explicit limits on actions and spend. Protect shared resources. Stop at set ceilings and keep working on what does not require them.
- Fabricate nothing. No invented facts, quotes, metrics, or testimonials. Cite external claims with a source and a date. Mark anything unverified.
- Experts are lenses, not impersonations. Apply each expert's published frameworks. Never present invented words as a real person's quote, and never imply anyone endorses the user.
- Checkpoint after every artifact so the run can resume. Degrade gracefully. One failure never ends the run.

## The loop

### Phase 0. Interview
Interview the user one question at a time. Recommend an answer for each question so they can react instead of generate. Explore their files and links instead of asking when the answer is already available.

Get clear on: what they have built and where it lives, their goals and their definition of success, their constraints (time, money, capacity, non-negotiables), and how far the run may go (actions and spend allowed). Stop interviewing once you have enough to seat the board and run the audit. Batch remaining unknowns into documented defaults rather than asking further. Capture the answers and any defaults you take. This is the only phase that requires the user in the room.

### Phase 1. Seat the board
Ask the user to name a few experts they trust. Propose a full panel that fits their domain and goals, and let them add or cut. Every seat clears the Faithful Representation Gate in `reference/faithful-representation-gate.md`.

Reject familiar names with thin public footprints, explain why, and offer a well-documented alternative in the same lane. Assign each seated expert a representation-confidence label. Organize the board into panels using `reference/roster-and-panels.md`, and write a roster file that records each seat, its lens, and its confidence.

### Phase 2. Intake and audit
Map what the user already has against the building blocks a business needs: vision, mission, and values; ICP; roadmap; prioritized backlog; and a metrics and prioritization approach (AARRR, a North Star metric, OKRs, KPIs). Do not force every block. Record what exists, what is thin, and what is missing, and cite the real files or sources for each.

If the user has a roadmap or backlog, the board's job is to review and improve it. If they do not, the board organizes or proposes the missing blocks. Meet them where they are.

If the business touches health, money, minors, or regulated or affiliate claims, seat the trust and compliance panel now and give it veto over any risky recommendation.

### Phase 3. Deliberation
Each panel reviews the relevant surface through its experts' published frameworks. For each finding, record the lens behind it, a confidence level, the goal it serves, and whether it needs a user decision. Track where independent experts converge, because convergence is the strongest signal, and track where they would disagree, because honest tension is worth surfacing.

Run this asynchronously. The user is not in the room. Stage the work for later review.

### Phase 4. Synthesis, backlog, and roadmap
Cluster and dedupe the findings. Produce a ranked master list, a prioritized backlog, and a roadmap the user can act on. Order the work so the highest-value items come first and a partial run still delivers the most important thinking.

### Phase 5. Prioritization framework
Apply the council-weighted framework in `reference/prioritization-framework.md`. If the user already uses a framework, tune to theirs instead of imposing a new one. Write the framework to disk as a durable artifact so the user's LLM keeps prioritizing the same way until the user overrules it. Show the reasoning, not just the ranking.

### Phase 6. PRD handoff
Produce a business-general PRD from the audit and the prioritized plan. If the user is a software project that wants engineering-grade specs and task breakdown, hand off to `prd-taskmaster` when it is present. Otherwise generate the PRD directly.

### Phase 7. Package
Write an overview with the headline findings and a short summary the user reads first. Consolidate every open decision into one decisions file. Confirm nothing was published or spent past the ceiling, and that no finding rests on an invented fact.

## Outputs
Write outputs to disk in the structure defined in `reference/output-structure.md`. Checkpoint and, if the workspace is a git repo, commit after each artifact. Never push or deploy.

## Portability
This skill runs in Claude Code and Codex by reading this file. For any other LLM, `prompts/quorum-portable.md` is a self-contained version of the same loop. The `/quorum` command and the plugin manifest wrap this skill for Claude Code plugin users.

The deliberation phase runs unattended in Claude Code and Codex, where the run can work while the user steps away. In a plain chat LLM, the same loop runs in one sitting, so keep the user engaged rather than telling them to step away.

## Integrations
- Interview: this skill includes its own grill-style interview. Pattern credit: Matt Pocock's `grill-me`.
- PRD: business-general by default; optional handoff to `prd-taskmaster` (MIT) for software projects.
