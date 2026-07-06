# Stage 3 — The Lovable prompt

**Tool:** ChatGPT or Claude, to *draft* the prompt · then Lovable, to receive
it
**Goal:** Turn your Stage 2 blueprint into one detailed, technical first
build prompt — the single message that kicks off Stage 4.

## Why this stage exists

Lovable isn't just a text box — your first message matters more than any
other, since it sets the foundation everything else gets built on top of.
Rather than guessing at what makes a good first prompt, we ask ChatGPT/
Claude — which already has your blueprint in context — to draft it for you,
following Lovable's own documented prompting principles.

This workshop keeps Stage 3 to **one artifact**: a single, self-contained
prompt that describes the app *and* gives detailed, technical build
instructions. Lovable also supports a separate "Knowledge file" concept for
persistent context — see
[`knowledge-file-example.md`](knowledge-file-example.md) if you want to set
one up later, but it's a workspace-level habit for future projects, not
something this workshop configures live.

### Lovable's five prompting principles

*(Source: [Lovable Academy — Learn to Prompt](https://academy.lovable.app/academy/prompting),
verified July 2026.)*

1. **Know what you're building before you build it** — this is what Stages
   1 and 2 were for.
2. **Build one piece at a time** — a working foundation, then one screen at
   a time, not the whole app in one message.
3. **Say exactly what you want, and what you don't** — give Lovable
   guardrails ("don't touch X") the same way you'd brief a teammate.
4. **Use the right tool for the job** — Plan mode for thinking things
   through, Build mode for actually implementing, Visual Edits for quick
   tweaks. (More on this in [Stage 4](../04-build-in-lovable).)
5. **Think in iterations, not in one shot** — expect to go back and forth,
   not to nail it in a single message.

## How to run it

1. Open [`prompt.md`](prompt.md) in this folder.
2. Paste in your Stage 2 blueprint (screen list, core flow, "own data"
   screen, out-of-scope list).
3. Run it in ChatGPT or Claude. It will draft **one detailed, technical
   prompt** — app description plus screen-by-screen build instructions.
4. Save that prompt — you'll paste it into Lovable's chat to kick off
   [Stage 4](../04-build-in-lovable).

See [`example.md`](example.md) for this worked out for CampusPulse.

## What "done" looks like

A single prompt that:

- Opens with a short paragraph describing what the app is and who it's for
- Names a **concrete visual identity** — a real reference (an object, a
  physical medium, a specific product's look), not a vague adjective like
  "clean" or "modern." Vague adjectives are exactly why AI-built apps
  default to the same generic look; a concrete reference gives Lovable
  something specific to build toward.
- Explicitly asks for **at least one real visual element** — an icon,
  badge, or thumbnail — regardless of the reference. Some concrete
  references (a departure board, a spreadsheet, a ticket stub) are
  inherently typographic and won't produce any images unless the prompt
  asks for one directly.
- Is precise and technical about every screen, field, and the exact
  navigation flow between them
- Asks for the **foundation only** — placeholder content and working
  navigation, not real data logic or the entire app in one shot
- Includes explicit guardrails for what not to build yet

Later screens and real logic come as follow-up prompts during the live
build in Stage 4.
