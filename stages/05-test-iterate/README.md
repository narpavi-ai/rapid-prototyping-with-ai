# Stage 5 — Test & iterate

**Tool:** Lovable (Preview) + Plan mode
**Goal:** Actually click through what you built like a stranger would, find
what's broken or confusing, and fix it without getting stuck re-prompting
the same thing over and over.

## Why this stage exists

This is the stage past workshops got the most questions about. Building
screen by screen in Stage 4 gets you *something* — but it's easy to only
ever test the happy path you just built, and never notice the app breaks if
someone does things in a different order, or leaves a field empty, or
RSVPs to the same event twice.

## Testing checklist

Before you consider the app "done," go through this list:

- **Click through the whole core flow, start to finish**, as if you'd
  never seen the app before — onboarding through to seeing your own data
  reflected back.
- **Test it as a brand new user** — refresh or use a different browser/
  incognito window. Does onboarding still work correctly the second time?
- **Try the "nothing yet" state** — what does My Schedule (or your
  equivalent "own data" screen) look like *before* you've done anything?
  Is that empty state handled, or does it look broken?
- **Try doing things out of order** — go to a screen without finishing the
  step before it. Try tapping a button twice. Try going back.
- **Read every screen's text out loud** — does it make sense to someone who
  has never seen this app, not just to you?

## Iteration prompt pattern

When you find something broken or confusing, resist the urge to just say
"fix it." Describe it like a bug report:

```
On [SCREEN], when I [exact steps to reproduce], [what actually happens].
I expected [what should happen instead].

Do not change [anything else that's already working].
```

See [`prompt.md`](prompt.md) for the full pattern and
[`example.md`](example.md) for real CampusPulse bugs found and fixed this
way.

## Avoiding the re-prompting loop

If you've tried to fix the same thing two or three times and it's still
broken (or a fix breaks something else), **stop re-prompting the same way**.
This is exactly what Lovable's own best practices warn against. Instead:

1. Switch to **Plan mode** and describe the problem — ask it to explain
   what's likely happening before touching any code.
2. If you have a pinned earlier version that worked, consider reverting to
   it and re-applying the change more narrowly.
3. If you're truly stuck, it's fine to leave that one thing broken and move
   on — a small app with one known rough edge is a better outcome than
   burning your remaining time on one bug.

## What "done" looks like

You've clicked through the full flow at least twice (once as if new, once
trying to break it), fixed anything that clearly didn't work, and you know
what (if anything) is still a known rough edge.

Then move to [Stage 6 — Scale up](../06-scale-up).
