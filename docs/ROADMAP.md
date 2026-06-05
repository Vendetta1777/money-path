# 🗺️ Money Path — Roadmap & Acceptance Criteria

> We "graduate" a milestone only when **every** acceptance criterion is checked. No half-passes.
> Milestones also live on GitHub: **Issues → Milestones**. Each issue links to one milestone.

**Legend:** ☐ = not done · ☑ = done. **Today:** 2026-06-05.

---

## How we work (the daily ritual)
Each session = one small, shippable improvement:
1. **Pick** — read `DEVLOG.md` + `gh issue list`, choose one issue tied to the current milestone.
2. **Build → Test → Ship** — implement, validate (`node --check` + headless-Chrome playthrough), commit, push (Pages auto-deploys).
3. **Log** — append to `DEVLOG.md`: what shipped, decisions, a **Coach's note** (one game-dev concept), next step. Update the GitHub issue.

> Run `/session` (in `.claude/commands/`) to start a session with this ritual.

---

## M0 — Pre-Production: Foundation & Workflow  ·  🎯 due 2026-06-06
*Set up so every future day compounds.*
- ☑ Game Design Document exists (`docs/GAME_DESIGN.md`)
- ☑ Roadmap + acceptance criteria exist (this file) and a **PDF** export
- ☑ GitHub set up as a tracker: labels, milestones, and a starter backlog of issues
- ☑ Persistent dev memory started (`docs/DEVLOG.md`)
- ☑ Daily workflow ritual documented + `/session` command
- **Graduates when:** all above checked. ✅ **Graduated 2026-06-05.**

## M1 — Vertical Slice: a polished, shippable core loop  ·  🎯 due 2026-06-19
*Make the existing game "store-demo quality."*
- ☐ **Shareable result card** (image/text) + "challenge a friend" — the viral loop
- ☑ **Deterministic seed** (seeded RNG) → reproducible runs + a **Daily Challenge** *(done 2026-06-05)*
- ☐ **Balance pass**: no dominant strategy; all-save is survivable-but-low, not instant burnout
- ☐ **Mobile-responsive + installable PWA** (looks/feels right on a phone)
- ☐ **Accessibility**: readable contrast, font scaling, `prefers-reduced-motion`
- ☐ **Onboarding**: a guided first run so new players aren't lost
- **Graduates when:** a first-time player on a phone can start, understand, finish, and share a run with zero confusion.

## M2 — Content Engine: agentic stories / characters / levels  ·  🎯 due 2026-07-10
*Stop hand-coding content; generate and validate it.*
- ☐ **Content schema** (data, not code) for characters, scenarios/"levels", and story arcs
- ☐ Move existing events/dilemmas/lives into that schema (game loads from data)
- ☐ **`/new-character`** generator (Claude Code command) → valid, on-tone character file
- ☐ **`/new-scenario`** generator + **validator** (rejects broken/unbalanced content)
- ☐ ≥ 10 new scenarios + 3 characters added *through the pipeline*
- **Graduates when:** a brand-new scenario can be generated, validated, and played without hand-editing engine code.

## M3 — Web Distribution + Analytics  ·  🎯 due 2026-07-31
- ☐ Privacy-friendly **analytics** with key funnel events (start, finish, share, replay)
- ☐ **Error/telemetry logging** (catch real-world crashes)
- ☐ A small **landing page** + clean URL (custom domain or itch.io)
- ☐ Versioned releases (tags + changelog)
- **Graduates when:** we can see how many people play, where they drop off, and ship updates with confidence.

## M4 — Mobile: iOS + Android  ·  🎯 due 2026-08-21
- ☐ Wrap with **Capacitor** → native iOS + Android builds
- ☐ App icon, splash, store screenshots, metadata
- ☐ Runs on simulator + a real device; haptics/sound feel native
- ☐ Internal test track (TestFlight / Google Play internal)
- **Graduates when:** the game installs and plays well from a phone home screen on both platforms.

## M5 — Launch & Live-Ops  ·  🎯 due 2026-09-11
- ☐ Store submission (App Store + Play) passes review
- ☐ Retention loop (daily challenge, streaks) live
- ☐ Content cadence: new scenarios shipped regularly via the engine
- ☐ Basic store optimization (title, keywords, screenshots)
- **Graduates when:** real strangers can download it, and we ship fresh content on a schedule.

---
*Dates are targets, not promises — we move them honestly as we learn.*
