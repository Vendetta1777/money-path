# 🎮 Money Path — Game Design Document (GDD)

> A living document. It captures *what* the game is and *why*. When the game and this doc disagree, fix one of them.

**Status:** in development · **Last updated:** 2026-06-05 · **Owner:** Vendetta1777

---

## 1. Vision (one sentence)
A short, replayable life-sim where you learn real money skills by *living* them — earning, budgeting, investing, and surviving 24 months — without it ever feeling like a lecture.

## 2. Pillars (the 3 things we protect)
1. **Meaningful trade-offs.** Score = *Net Worth × Happiness*, so hoarding and splurging both lose. Every choice costs something.
2. **A new story every run.** Random events, dilemmas, market swings, perks, and unlockables mean no two runs repeat.
3. **Feels like a game, teaches like life.** Juice, progression, and a board you travel — concepts land through play, not text.

## 3. Audience & tone
- **Primary:** teens (13–18) on phones; secondary: anyone curious about money.
- **Tone:** friendly, snappy, a little funny. Relatable teen scenarios (sneaker flips, festival tickets, first car).

## 4. Platforms (target order)
1. **Web** (today) — single-file `index.html`, GitHub Pages.
2. **Web, polished + analytics** (distribution).
3. **iOS + Android** — wrap the web game (Capacitor) → native stores.

## 5. Core loop (one "month")
`Surprise event (slot reveal) → Budget (needs / fun / save / invest) → Temptation → Market → [Checkpoint every 6 mo] → next month`
Repeat 24× → **Results**: grade, score, life-story recap, unlocks.

## 6. Systems (what exists today)
- **Lives** (difficulty/identity), **perks**, **multi-asset investing** (bonds/blue-chip/crypto/real estate), **6 minigames**, **branching dilemmas**, **3 run goals**, **boss checkpoints**, **power-up items**, **journey board**, **avatars/themes**, **life-story recap**.
- **Penny** — a rule-based *reasoning* advisor (no AI/API): reads signals (runway, diversification, months left, risk, creep) and gives prioritized, number-specific advice. This is a signature feature; keep it transparent and smart.
- **Balance** is centralized in `BAL` (config) + `GRADES`.

## 7. What it is NOT (scope guardrails)
- Not a realistic stock simulator. Not multiplayer (for now). Not pay-to-win. Not a textbook.

## 8. The "fun loop" we're chasing
Play → get a story + a score → unlock something / learn a lesson → *want one more run* → tell a friend.

## 9. Open design questions (decide later)
- Should all-save be a slow-loss instead of a quick burnout? (playtest flagged this)
- Daily challenge (shared seed) — how prominent?
- How far does the agentic content engine go (procedural scenarios, characters, story arcs)?

---
*See `ROADMAP.md` for milestones & acceptance criteria, and `DEVLOG.md` for the running history.*
