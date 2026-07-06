# Stage 2 — Blueprint

**Tool:** ChatGPT or Claude (still not Lovable)
**Goal:** Turn your problem statement from Stage 1 into a lightweight spec —
a short list of screens, the one core flow through them, and what data comes
back to the user.

## Why this stage exists

A problem statement tells you *why* to build something. It doesn't tell you
*what* to build. Jumping from a problem straight into Lovable tends to
produce scope creep — you start describing one screen, then think of
another, then another, and end up with a sprawling half-built idea instead
of one small complete app.

This stage is where you draw the blueprint: the smallest set of screens that
lets someone go from "just found this app" to "seeing their own information
reflected back to them." That last part matters — a real app isn't just a
form or a browse screen, it's something that remembers you and shows you
something that's *yours* (a saved order, a schedule, a list).

## How to run it

1. Take the problem statement you ended Stage 1 with.
2. Open [`prompt.md`](prompt.md) and paste your problem statement into it.
3. Run it in the same ChatGPT or Claude conversation as Stage 1 (context
   carries over) or a fresh one if you paste the problem statement in.
4. Push back on the output — if it suggests more than 4-5 screens, ask it to
   cut to the smallest version that still lets someone see their own data
   reflected back.

See [`example.md`](example.md) for the CampusPulse blueprint.

## What "done" looks like

A short spec with:

- **Screen list** — 3-5 screens, no more. Each one has a single clear job.
- **The core flow** — the one path a first-time user takes through those
  screens, start to finish.
- **What comes back to the user** — the specific piece of "their own data"
  the app reflects back at the end of the flow (a saved order, a schedule,
  a list of things they've done).
- **What's explicitly out of scope** — a short list of things you're *not*
  building today, so Stage 3 doesn't quietly grow back into a 10-screen app.

Carry this spec into [Stage 3 — Lovable prompt](../03-lovable-prompt), where
it becomes a Knowledge file and your first Lovable prompt.
