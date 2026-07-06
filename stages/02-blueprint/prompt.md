# Stage 2 prompt — from problem to blueprint

Continue in the same conversation as Stage 1 if you can (it already has your
problem statement as context). Otherwise, paste your problem statement in
first, then use this prompt.

```
Here's the problem statement we landed on:

[PASTE YOUR STAGE 1 PROBLEM STATEMENT HERE]

Now help me turn this into a lightweight blueprint for a small, complete
app — not a single screen, a small bounded app someone can click through
start to finish. Give me:

1. A screen list of 3-5 screens maximum. Each screen has one clear job.
2. The core flow: the exact path a first-time user takes through those
   screens, in order.
3. What "their own data" looks like at the end of the flow — the specific
   thing this app should save and reflect back to the user (e.g. a saved
   order, a personal schedule, a list of things they've done). Every real
   app needs this; don't let it be an afterthought.
4. An explicit "not doing this yet" list — 3-5 things a bigger version of
   this app might have, that we are deliberately leaving out.

Push back on me if I describe more than 5 screens, or if the "their own
data" step is missing or vague — ask me to cut scope rather than expand it.
```

## Tips

- **Cut, don't add.** If the AI suggests 7 screens, your job is to say
  "which 3-4 of these actually matter for the core flow" — not to accept
  all 7.
- **The "own data" screen is not optional.** A browse-only app (like a
  read-only events list) isn't a full app for this workshop's purposes — it
  needs a place where the user's own activity is saved and shown back to
  them.
- **Write down what you're skipping.** Saying "no login with email
  verification, no payments, no admin panel" out loud now saves you from
  scope creep once you're inside Lovable and everything feels possible.

When you have your screen list, core flow, and "own data" screen written
down, move to [Stage 3](../03-lovable-prompt/prompt.md).
