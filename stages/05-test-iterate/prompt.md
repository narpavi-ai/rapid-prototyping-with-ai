# Stage 5 prompt — reporting a bug like a bug report

```
On [SCREEN NAME], when I [exact steps to reproduce the issue],
[what actually happens].

I expected [what should happen instead].

Do not change [anything else on this screen or elsewhere that's already
working correctly].
```

## If it's still broken after one retry

Don't send a third variation of the same prompt. Switch to Plan mode:

```
[Plan mode]

I've tried to fix [the issue] twice and it's still not working /
it broke [something else] instead. Before we try again, walk me through
what's likely causing this and what the smallest fix would be.
```

Then go back to Build mode with whatever narrower fix Plan mode suggests.

## Tips

- **Reproduce it precisely.** "RSVP is broken" is much harder to fix than
  "when I tap RSVP a second time on the same event, it adds a duplicate
  instead of removing it."
- **One bug report per prompt.** If you found three things, that's three
  prompts, tested one at a time — same reasoning as Stage 4.
- **It's OK to stop.** Not every rough edge needs to be fixed live. Note it
  and move on if you're running low on time.
