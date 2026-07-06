# Stage 4 prompt pattern — wiring up one screen

Use this shape for each follow-up prompt inside Lovable, once your Stage 3
skeleton exists. One screen (or one piece of logic) per prompt — resist
combining several.

```
On the [SCREEN NAME] screen, [do this one specific thing]:

- [Exact behavior — what should happen, in plain language]
- [What data this needs to read or save]
- [Any edge case that matters — e.g. "if there are no events yet, show..."]

Do not change [SPECIFIC FILE OR SCREEN] — leave it exactly as it is.
```

## Tips

- **One prompt, one screen (or one behavior).** If you catch yourself
  writing "and also," stop — that's a second prompt.
- **Name the guardrail every time**, even if it feels repetitive. Lovable's
  own guidance is that repeating important instructions across prompts
  helps — it does not assume it remembers your earlier intent perfectly.
- **Test after each prompt**, not after five. It's much easier to find what
  broke when you only changed one thing.
- **If a fix doesn't land after one or two tries**, stop re-prompting the
  same way — switch to Plan mode and describe what's going wrong instead.
  See [Stage 5](../05-test-iterate) for this exact situation.

See [`example.md`](example.md) for this pattern used on CampusPulse's real
screens.
