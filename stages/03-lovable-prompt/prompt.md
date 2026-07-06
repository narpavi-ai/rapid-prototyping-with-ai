# Stage 3 prompt — draft one detailed, technical first build prompt

Continue in the same ChatGPT/Claude conversation as Stages 1-2 if you can.

```
Here's the blueprint we built:

[PASTE YOUR STAGE 2 BLUEPRINT: screen list, core flow, "own data" screen,
out-of-scope list]

I'm about to build this in Lovable (a no-code AI app builder). Write me
the single message I should send Lovable first — a detailed, technical
build prompt. It needs to be self-contained, since it's the only context
Lovable will have: start with a short paragraph describing what this app
is and who it's for, then give detailed, technical, screen-by-screen build
instructions.

Also give it a real visual identity, not a generic one. Do NOT describe
the look with vague adjectives like "clean," "modern," or "minimal" —
those produce the same average-looking UI every AI tool defaults to
(centered hero, purple gradient, three icon cards). Instead:
- Name one concrete, specific reference point the visual design should
  feel like — a real object, a physical medium, or a specific product's
  visual language. Not an adjective; a thing.
- From that reference, pull 2-3 concrete tokens: one accent color as an
  exact hex code (not just "amber" — say "#FFC107"), one type
  personality (e.g. condensed display headings vs. a monospace detail),
  and one layout rhythm (dense vs. spacious, card-based vs. list-based).
- Some concrete references are purely typographic (a departure board, a
  spreadsheet, a ticket stub) and won't naturally produce any images on
  their own. Regardless of the reference, require at least one real
  visual element beyond text and color — an icon per category, a small
  color-coded badge, or a placeholder thumbnail — so the result isn't
  100% typography with zero visual anchors.
- End the visual identity section with a single one-line tagline that
  restates the reference (e.g. "this should feel like X for Y"). Repeating
  it keeps later follow-up prompts in Stage 4 consistent with the same
  visual language, not just the first screen.

Follow these rules, which are Lovable's own documented prompting
principles:
- Ask for the FOUNDATION only: the basic screens and navigation between
  them, with placeholder content — not the full app, not real data logic,
  not styling polish, in one message.
- Be precise about every screen, field, button, and the exact navigation
  flow between them — detailed and technical, even though it stays in
  plain language, no code.
- Include explicit guardrails: what to leave alone or not build yet.
- Write it the way you'd brief a capable teammate — nothing left for
  Lovable to guess, but narrow in scope.

Give me the finished prompt as one copy-pasteable block.
```

## Tips

- **Name a thing, not an adjective.** "Clean and modern" is a label, so
  Lovable returns the average of everything ever labeled that way — which
  is exactly the generic look you're trying to avoid. "Feels like a
  festival wristband and ticket stub" or "feels like a library card
  catalog" gives it something concrete to resolve to one coherent look.
- **A concrete reference can still mean zero images.** An airport
  departure board, a spreadsheet, a ticket stub — these are legitimate,
  distinctive references, but they're inherently typographic. If nothing
  in your prompt explicitly asks for an icon, badge, or thumbnail, don't
  be surprised if the build comes back as text and color with no images
  at all — that's the prompt following your brief correctly, not Lovable
  cutting a corner.
- **One prompt, not two.** This workshop skips the separate per-project
  Knowledge file step — it's fiddly to set up mid-demo. Instead, the app
  description lives right at the top of this one prompt, so nothing extra
  needs configuring before you build. See
  [`knowledge-file-example.md`](knowledge-file-example.md) if you want to
  set up a *workspace-wide* Knowledge file later — that's a different,
  optional thing.
- **Detailed doesn't mean big.** A good first prompt is technical and
  precise — exact screens, fields, and flow — while still being narrow in
  scope (foundation only). Precision and scope are different dials; turn
  up the first, not the second.
- **Resist a first prompt that tries to build everything.** The best first
  prompt gets you a clickable skeleton — screens exist and you can navigate
  between them — with the real content and logic added screen-by-screen
  afterward. That's what [Stage 4](../04-build-in-lovable) is for.
- **Save the finished prompt somewhere you can find it** — you'll paste it
  into Lovable's chat to kick off Stage 4.
