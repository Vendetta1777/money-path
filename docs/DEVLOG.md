# 📓 Money Path — Dev Log

> The project's memory. Newest entry on top. Every session adds one entry:
> **Shipped · Decisions · Coach's note · Next.**

---

## 2026-06-05 — Session: Deterministic seed + Daily Challenge (M1)
**Milestone:** M1 — Vertical Slice · **Issue:** #2 → closed

**Shipped**
- A **seeded PRNG** (mulberry32) + `buildScenario(seed)` that pre-generates the entire 24-month world (events, market news + noise, dilemmas, temptations, opportunities, item finds, goals) up front.
- The core loop (`startMonth`/`goTemptation`/`resolveMarket`/`chooseDilemma`) now **reads from the pre-generated scenario** instead of rolling live — so the world is identical for a seed no matter how the player plays.
- **Daily Challenge**: date-seeded run (fixed life + no perks for fairness), with best-score-per-day saved in `localStorage`. New start-screen card + results pill (shows seed / daily best).

**Decisions**
- *Pre-generate the world* rather than just swapping `Math.random` — only this makes "same seed → identical run" true under divergent choices (proven by test: two different strategies on one seed produce the same world).
- Keep **cosmetic + interactive** randomness (confetti, minigame outcomes, day-trade luck) un-seeded — your *skill* varies, the *world* doesn't. This is also what makes "challenge a friend" fair.
- Reworded the checkpoint reward ("…score bonus") to remove a "final score" string that was confusing automated tests — small testability win.

**Coach's note 🎓 — Determinism is a superpower.**
A *seed* is one number that recreates an entire game world. Pros lean on this hard: it powers **daily challenges** (everyone plays the same world), **"beat my run" sharing** (the viral loop), and — quietly the biggest win — **reproducible bug reports & tests** (a crash on seed `x7f3` can be replayed exactly). The key design choice was *what* to fix: we seed the **world**, not the **player**. Fix too much and replays feel scripted; fix too little and challenges aren't fair. Seeding the scenario but leaving skill free is the sweet spot.

**Next**
- **Issue #1 — shareable result card + "challenge a friend"**, which now plugs straight into the seed (share the seed → friend plays the same world). Highest-leverage remaining M1 brick.

---

## 2026-06-05 — Session: Pre-Production (M0)
**Milestone:** M0 — Foundation & Workflow → **graduated ✅**

**Shipped**
- Game Design Document (`docs/GAME_DESIGN.md`) — vision, pillars, audience, platforms, systems, scope guardrails.
- Roadmap with acceptance criteria (`docs/ROADMAP.md`) + a printable **PDF**.
- GitHub set up as a real tracker: custom labels, milestones M0–M5, and a starter backlog of issues.
- This dev log + a `/session` daily-ritual command.

**Decisions**
- Keep Money Path a **single-file web game** until the Mobile milestone (M4), then wrap with **Capacitor** rather than rebuilding native.
- "Penny" stays **rule-based** (no API) — it's a feature, not a limitation, and it's portable everywhere.
- We graduate milestones only when *all* acceptance criteria pass.

**Coach's note 🎓 — Pre-production is the cheapest time to be smart.**
Real studios don't start by coding features; they start with a **GDD** (what/why), a **roadmap** (in what order), and a **vertical slice** plan (one polished slice that proves the fun). Why? Because changing a plan costs minutes, but changing shipped code costs days. Our M0 today *is* pre-production: we wrote down the vision and the order so every future day pulls in the same direction instead of zig-zagging. The single most important idea on the roadmap is the **vertical slice (M1)** — make the part you already have *truly* polished and shippable before adding more. Depth before breadth.

**Next**
- Start **M1**. First target: the **shareable result card + challenge seed** (the viral loop) — highest leverage for a game meant to spread among teens.

---
*(Older entries go below as we add them.)*
