# Quorum

**Quorum convenes an advisory board of real, well-documented experts you choose, points them at the business you have already launched, and returns a prioritized, expert-reviewed path forward.**

> Status: pre-build charter (v0). This document seeds the repo README and the PRD.
> License: MIT. Runs on Claude Code and Codex, with a portable prompt core for any LLM.

## What Quorum is

Quorum is a working advisory board, not a group chat with a few chatbots. You seat the experts whose thinking you trust, and they review your real, in-production business through their own published frameworks. You leave with an honest audit, direct advice, and a prioritized way forward.

This is not "ask five models the same question," and it is not "a set of generic personas debate your memo." Quorum seats real, faithfully represented experts, points them at your actual work, and leaves a prioritization system that keeps working after the session ends.

## Who it is for, and who it is not

Quorum is for builders who are past the idea and not yet at scale. You have something real in production, a first sale or an MVP that people use, and you are deciding where to focus next. That includes software founders, creators, local and service businesses, and independent operators.

It is not for the idea stage, where nothing real exists yet. It is not for teams past product-market fit who are heads-down scaling. Quorum works in the middle, where focus and sequencing decide whether you make it.

## What you leave with

The primary output is the audit and the advice. Quorum meets you where you are.

If you already have a roadmap or backlog, the board reviews it and tells you what to change. If you do not, Quorum checks which building blocks exist and organizes or proposes the ones that are missing. It does not force every artifact every time.

The building blocks Quorum checks for:

- Vision, mission, and values
- ICP (ideal customer profile)
- Roadmap
- Prioritized backlog
- A metrics and prioritization approach that fits you (AARRR "pirate" metrics, a North Star metric, OKRs, KPIs)

Every run also returns three things you can act on immediately:

- A prioritized backlog and a roadmap.
- A council-weighted prioritization framework that becomes your LLM's default. It keeps prioritizing for you, the way you would, until you overrule it.
- A PRD-style handoff you can take straight into building.

## How it works

You are present at the start and free to leave after. The loop:

1. **Interview.** Quorum grills you one question at a time, recommends an answer for each, and gets clear on your business, your goals, and your definition of success.
2. **Seat the board.** You name a few experts you trust. Quorum proposes a full panel and lets you add or cut. Every seat clears the Faithful Representation Gate.
3. **Audit.** Quorum reviews your real business and artifacts through each expert's published frameworks.
4. **Deliberate.** Quorum runs a structured set of exercises on its own and stages the results for later review. You answer questions up front, then step away by design.
5. **Review.** You return to findings, a synthesis, a prioritized backlog and roadmap, the framework, and a PRD.

## How it behaves while you are away

Quorum runs on a fixed operating contract, so unattended does not mean unaccountable.

- You answer questions up front. Quorum then works on documented defaults and does not block waiting on you.
- Everything is staged for review. Quorum publishes nothing, sends nothing, and ships nothing on your behalf.
- Hard limits govern what it may do and spend. It protects shared resources and stops at set ceilings.
- No fabrication. Quorum invents no facts, quotes, metrics, or testimonials, and it cites external claims.
- Experts are lenses, not impersonations. Quorum applies their frameworks and never puts invented words in their mouths.
- Work is checkpointed to resume, and it degrades instead of stalling.

## The Faithful Representation Gate

A seat is earned by a public body of work, not a familiar name. Quorum seats a person only when enough authored, public material exists to represent how they actually think.

- Requires a real body of work in their own words: multiple books, a sustained blog or newsletter, a deep catalog of articles, talks, or podcasts, or an active site Quorum can draw from.
- Rejects thin footprints. One talk or one article is not enough.
- Living or modern figures qualify on an active site, articles, interviews, or a book. Historical figures qualify on multiple books or a large body of work written about them and their methods.
- The same bar applies to anyone you propose. If your pick does not clear it, Quorum tells you why and offers a well-documented alternative in the same lane.
- Each seated expert carries a representation-confidence label, so you see how grounded each lens is.

## The prioritization framework it leaves running

The default is council-weighted. Priority rises with goal-fit, expert consensus, and impact, and falls with effort, risk, and reversibility. Quorum derives it from your stated goals and shows its reasoning.

You own the framework. Override it, retune the weights, or swap it out at any time. If you already use RICE, ICE, WSJF, or your own, Quorum tunes to yours instead of imposing its own.

## Form and portability

Quorum ships plugin-first for Claude Code and Codex. It is layered so the same thing works three ways: a portable prompt and README for any LLM, the core board and prioritization engine, and the full automated loop. A Codex user with only the prompt gets value. A Claude plugin user gets the whole loop.

## Integrations

Quorum builds in a lightweight, grill-style interview (pattern credit: Matt Pocock's grill-me). It produces a business-general PRD by default, and hands off to prd-taskmaster (MIT) when the user is a software project that wants engineering-grade specs and task breakdown.

## Why it is different

The market is full of tools that query several models or spin up generic personas to argue over a document. Quorum's edge is narrow and defensible: real, faithfully represented experts you choose, an audit of your actual in-production business, and a prioritization system that keeps working after the session ends.

## Definition of success for the project

Two wins matter most: real user impact and credibility. Impact means people leave with a clearer, better-prioritized path and actually ship it. Credibility means the work represents how I think and what I build. Inbound interest in my advisory work is welcome and never gated. The project is free and open source.

## Anti-goals

Quorum protects its value by refusing to be a few specific things:

- Not for the idea stage. It requires something real in production.
- Not a scale-optimization tool for post-product-market-fit teams.
- Not a yes-man. It pushes back and prioritizes hard.
- Not generic "ask AI for advice." The roster is gated and the output is structured.
- Never an impersonator. It fabricates no expert, quote, metric, or testimonial.
- Not financial, legal, or medical advice. It is opinionated and always overrulable.
- Not a data grab. Your inputs stay local, with no phone-home.
- Not a lock-in. The prioritization framework is yours to change.

## Install

Quorum runs in Claude Code, in Codex, or in any capable LLM.

**Claude Code.** Clone this repo into your Claude Code skills directory, then start Claude Code in your project.

```
cd ~/.claude/skills
git clone https://github.com/davidbrown1775/quorum-skill.git quorum
```

Claude Code reads `SKILL.md` and activates Quorum when you ask for it or run `/quorum`.

**Codex.** Clone the repo, run Codex in that folder, and run `/init` so it reads `SKILL.md`.

```
git clone https://github.com/davidbrown1775/quorum-skill.git
cd quorum-skill
```

**Any other LLM.** Open `prompts/quorum-portable.md`, copy it, and paste it into your model. It runs the same loop without the plugin.

## Run it

1. Point Quorum at the business you have already launched. Have your files, links, and current numbers ready.
2. Answer the interview. It asks one question at a time and recommends an answer for each.
3. Seat your board. Name a few experts you trust, then edit the panel Quorum proposes.
4. Step away. Quorum audits, deliberates, and stages the results.
5. Come back to `quorum-review/00_OVERVIEW.md`, read the summary, and act on the prioritized backlog and roadmap.

Quorum stages everything for your review. It publishes nothing and sends nothing on your behalf.

## License

MIT.

## Next steps for this repo

- [x] Name chosen and checked for collisions: Quorum, command `/quorum`. Namespace any future npm installer.
- [ ] Scaffold the public repo: `SKILL.md`, portable prompt, `README.md`, `LICENSE` (MIT), `/examples`.
- [ ] Build the engine: interview, Faithful Representation Gate, audit, deliberation exercises, prioritized backlog and roadmap, council-weighted framework, PRD handoff.
- [ ] Wire the operating contract: staged output, spend and permission limits, no-fabrication, checkpoint and resume.
- [ ] Dry-run on the cases already completed, then refine.
- [ ] Write and publish the launch article.
