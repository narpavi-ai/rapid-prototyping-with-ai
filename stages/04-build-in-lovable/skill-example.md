# Example Skill — "new-screen"

**This is optional** — a small demo of Lovable's Skills feature, not
required to finish the app. Skills are workspace-level (**Settings →
Skills**), so this applies to every project you build afterward, not just
tonight's.

## What a skill is, in one line

A set of instructions you write once that Lovable applies automatically
whenever your request matches — instead of you retyping the same
guardrails into every prompt.

## The skill: `new-screen`

Copy this into **Settings → Skills → new skill** (or say "save that as a
skill" to Lovable after building a screen the way you like, and describe
when it should apply).

**Name:** `new-screen`

**Description:** Use when building or adding a new screen to this app.

**Instructions:**

```
When building a new screen:

1. Only touch the files needed for this screen. Do not modify or restyle
   any existing screen unless explicitly asked to.
2. Use realistic, specific placeholder content instead of generic filler
   like "Item 1," "Lorem ipsum," or "Sample text here."
3. If the screen shows a list or any user data, include a friendly empty
   state for when there's nothing there yet (for example, "No events yet
   — check back soon"), not a blank screen.
4. Match the visual style already established elsewhere in the app — the
   same spacing, colors, and components — rather than introducing new
   patterns.
5. After building, summarize in one line what changed, so it's easy to
   check against the request.
```

## Why this one

Every rule in it is something this workshop already asked you to do by
hand: guardrails ([Stage 4 tips](README.md)), realistic content and empty
states ([Stage 5](../05-test-iterate)), and staying consistent
screen-to-screen. Writing it down once means Lovable applies it to every
future screen — and every future project — without you having to remember
to ask.

## Trying it live

1. Create the skill (above) before your next follow-up prompt.
2. Ask for a new screen or behavior the normal way — don't mention the
   skill.
3. Watch Lovable apply it automatically (or type `/new-screen` to invoke
   it directly if it doesn't trigger on its own).
