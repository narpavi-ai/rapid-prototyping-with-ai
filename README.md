# Rapid Prototyping with AI

Workshop materials for **Rapid Prototyping with AI** — a hands-on,
in-person session for student founders, built entirely around no-code AI
tools.

- **Format:** 2–2.5 hours, hands-on
- **Who it's for:** Student founders — no coding experience required. Bring a
  laptop, a [Lovable](https://lovable.dev) account, and either
  [ChatGPT](https://chatgpt.com) or [Claude](https://claude.ai) (free tiers
  are fine).
- **What you'll leave with:** A real, working, multi-screen app you can share
  with a link — built entirely without a code editor or local setup.

## How the workshop is structured

Six stages, each with a short teach segment followed by a hands-on build
sprint. Every stage folder below has the same shape:

- `README.md` — what the stage is for, and how to run it
- `prompt.md` — a fill-in-the-blank prompt template you can use on *your own*
  idea, for stages where you're prompting ChatGPT/Claude or Lovable
- `example.md` — a fully worked example, using **CampusPulse** (a campus
  events + RSVP app) as the running use case, so you can see the whole arc
  end to end

| Stage | Folder | What happens |
|---|---|---|
| 1 | [`stages/01-problem`](stages/01-problem) | Dig into the problem with ChatGPT or Claude — before opening Lovable at all |
| 2 | [`stages/02-blueprint`](stages/02-blueprint) | Turn the problem into a lightweight spec: screens, flow, data |
| 3 | [`stages/03-lovable-prompt`](stages/03-lovable-prompt) | Turn the spec into one detailed, technical Lovable build prompt |
| 4 | [`stages/04-build-in-lovable`](stages/04-build-in-lovable) | Build the app screen-by-screen inside Lovable |
| 5 | [`stages/05-test-iterate`](stages/05-test-iterate) | Test what you built and fix it without getting stuck in a loop |
| 6 | [`stages/06-scale-up`](stages/06-scale-up) | What comes after Lovable — GitHub sync (optional) and beyond |

See [`resources.md`](resources.md) for the official Lovable documentation
links this workshop is based on, plus contact info.

## The example app: CampusPulse

A small, complete campus events + RSVP app used as the worked example
throughout every stage folder:

1. **Onboarding** — your name + your interests (tech, sports, arts, free
   food, etc.)
2. **Events feed** — upcoming campus events, filtered to match your interests
3. **Event detail** — description, time, place, and an RSVP button
4. **My Schedule** — the events you've RSVP'd to, reflected back to you as
   your own list

"Small" means a small, clearly-bounded app — not a single mockup screen. By
the end of Stage 4, CampusPulse is click-through-able end to end.

## Presenting the deck

`deck.html` (not committed to this repo — see `.gitignore`) is the slide
deck used during the live session. Open it directly in a browser; arrow
keys or space bar advance slides, `F` toggles fullscreen. Before presenting,
search it for `[bracket]` placeholders (wifi password, your bio, contact
email, and the real repo URL once you've pushed this repo to GitHub) and
fill them in.

## Following along live

If you're at the workshop, follow along stage by stage in this repo on your
own laptop. The slide deck used during the session names each stage and
points back here — this repo is the source of truth for the actual prompts.

---

*Generated with AI assistance as part of workshop prep; may contain errors —
verify against the linked official docs before relying on anything technical.*
