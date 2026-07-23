# SAGA — an AI that makes you reason

> In an age of infinite answers, the scarce thing is a mind that can still reason.

A coach, not a vending machine; a scaffold, not a crutch — built so you need it
less over time, not more.

SAGA is the offline AI viva for Indian classrooms — an AI that asks until the
student can defend what they know, on phones they already own. The teacher
certifies the questions; the student defends their understanding in Socratic
dialogue, fully offline; the teacher sees which concepts held and which slipped —
the class's comprehension shape — before the next lecture. Never a rank. Built,
running today.

This repository hosts SAGA's public landing page. Live site:
**https://primalumiere.github.io/**

## What's built

Offline Socratic sessions on a ~4B open model via our own llama.cpp FFI ·
encrypted vault · signed content pipeline · teacher dashboard with an
aggregate-only privacy gate · 540 mobile + 228 server automated tests green ·
verified end-to-end on a live phone.

## How it's different

- **Never-rank, enforced in code** — class views are aggregate-only; a class
  smaller than five shows the teacher nothing; there is no score in the system to
  rank by.
- **Teacher-certified content** — every question set is human-curated and
  cryptographically signed before a student ever sees it.
- **User-owned data** — the student's work lives in an encrypted vault on their
  own device, exportable by them under India's data law, never a company
  data-lake.

Privacy is by construction, not policy: all inference on-device, no network
calls — shown, not promised.

## The architecture in one paragraph

Student inference runs entirely on the student's own phone — a ~4B open model
executed through our own llama.cpp FFI, so a session makes no network calls and
costs our servers nothing. The server is Rust/Axum over Postgres; it generates
the teacher's certified content, which is signed with Ed25519 before any student
sees it, so cost grows with lectures and never with enrolment. The student's work
lives in an encrypted on-device vault they own and can export. Teacher views are
aggregate-only, gated so a cohort smaller than five is never individually visible.

## Ethics core

1. **Never rank the person** — dignity at the floor, competition only for distinction.
2. **Sovereign by construction** — your device, your data, leave with everything.
3. **Loyal to the human it touches** — measured by outcomes, never attention.
4. **Makes you reason** — never reasons for you.
5. **No engagement machinery** — no streaks, badges, or leaderboards; checkable by absence.
6. **Teacher-in-the-loop** — a human certifies everything a student sees.

## Status

Pre-pilot. The product is built and verified end-to-end on a live phone. Three
campuses have committed to hosting demos in the new academic session; the problem
was confirmed in every one of five institutional conversations. We run an evidence
ledger and never count demand above its dated rows — that discipline is the
company.

## Contact

Ansuman Mahapatro — Bhubaneswar, India — <ansumanmahapatro24@gmail.com>

---

© 2026 Ansuman Mahapatro. All rights reserved. See `LICENSE.md`.
