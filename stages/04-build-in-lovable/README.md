# Stage 4 — Build in Lovable

**Tool:** Lovable
**Goal:** Turn the clickable skeleton from Stage 3 into a working app, one
screen at a time, using Lovable's own recommended build workflow.

## Why this stage exists

This is the stage most people think "prototyping with AI" means — but it
works far better once Stages 1-3 have already done the thinking. Now it's
about *how* you drive Lovable itself, not what you ask it to build.

## Lovable's own recommended workflow

*(Source: [Lovable docs — Best practices](https://docs.lovable.dev/tips-tricks/best-practice),
verified July 2026.)*

1. **App context up front** — already done: your Stage 3 prompt opened
   with a short description of the app, so Lovable has that context from
   message one.
2. **Plan mode early and often.** Lovable has two main modes:
   - **Plan mode** — a conversational, reasoning mode. It explores ideas,
     investigates issues, and reasons about a change *before any code is
     written*. It costs 1 credit per message and **never modifies your
     code** — safe to use freely.
   - **Build mode** *(formerly called Agent mode)* — the mode that actually
     implements changes: it explores your project, edits files, and
     resolves issues that come up.

   Lovable's own guidance: use Plan mode for roughly **60-70% of your
   time** — debugging, brainstorming, and deciding what to do next — and
   switch to Build mode only once you know exactly what you want built.
3. **Build incrementally, one screen at a time**: create the screen → add
   the UI layout → connect real data → add the logic → test it. Don't ask
   for the whole app in one message.
4. **Connect a database (Supabase) last** — only once the front-end and
   flow feel stable. Wiring in real data storage too early makes every
   later UI change riskier.
5. **Pin stable versions as you go** — once a screen works the way you
   want, mark that point so you can always get back to it if a later
   prompt breaks something.
6. **When something goes wrong, don't just keep re-prompting the same
   fix.** Switch to Plan mode, describe the problem, and let Lovable reason
   about it before trying an edit again — see [Stage 5](../05-test-iterate)
   for what to do when you're stuck in a loop.

## Bonus: turn these habits into a Skill

*(Source: [Lovable docs — Skills](https://docs.lovable.dev/features/skills),
verified July 2026.)*

Everything above — guardrails, realistic content, one screen at a time —
is a habit you have to remember to type into every prompt. Lovable has a
feature for exactly this: a **Skill** is a reusable instruction set you
write once, at the workspace level, and Lovable applies it automatically
whenever it's relevant — across every project in that workspace, not just
this one.

A skill is a markdown file (`SKILL.md`) with three parts: a name (lowercase,
hyphens), a description that starts with "Use when…" (so Lovable knows
when to trigger it), and the instructions themselves. You can write one by
hand in **Settings → Skills**, or just tell Lovable "save that as a skill"
after a good interaction and describe when it should apply.

Two worked examples, both optional and nice to build live if there's time:

- [`skill-example.md`](skill-example.md) — a "new screen" skill that
  bakes in the guardrails and realistic-content habits from this stage,
  so you stop retyping them.
- [`skill-example-technical.md`](skill-example-technical.md) — a more
  technical one: loading, empty, and error states, a gap that's commonly
  cited as something AI app builders skip by default.

## How this runs live at the workshop

This stage is a **live build**, driven from the projector — not something
you follow along with screenshots. Vishal builds CampusPulse's real logic
screen by screen in Lovable, narrating the mode he's in (Plan vs. Build)
and why, live.

[`prompt.md`](prompt.md) has the pattern for a good "wire up this one
screen" follow-up prompt, and [`example.md`](example.md) has the actual
follow-up prompts used to bring CampusPulse's filtering and RSVP-saving to
life — useful as a reference once you're building your own app.

## What "done" looks like

By the end of this stage, your app:

- Has all the screens from your Stage 2 blueprint, wired with real (not
  placeholder) data and logic
- Actually saves the user's own data (RSVPs, orders, schedule entries —
  whatever your blueprint's "own data" screen was) and reflects it back
- Is click-through-able start to finish, as a real, shareable app

Then move to [Stage 5 — Test & iterate](../05-test-iterate).
