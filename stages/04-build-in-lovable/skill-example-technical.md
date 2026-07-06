# Example Skill (technical) — "ui-states"

**This is optional** — a second demo of Lovable's Skills feature, aimed at
founders who want something more technical than
[`skill-example.md`](skill-example.md). Like that one, this is
workspace-level (**Settings → Skills**), so it applies to every project
you build afterward, not just tonight's.

## Why this one

Multiple independent write-ups on building apps with AI call out the same
gap: loading, empty, and error states are "the three UI states AI almost
never builds correctly" — it defaults to the happy path (data loaded
successfully) and skips the other three. This is a real, recognized
software-engineering gap, not a style preference, and it doesn't need a
backend or Supabase to matter — it applies to any screen with a list, feed,
or loaded data, which CampusPulse already has (Events Feed, My Schedule).

## The skill: `ui-states`

Copy this into **Settings → Skills → new skill** (or say "save that as a
skill" to Lovable after you've gotten a screen's states right, and
describe when it should apply).

**Name:** `ui-states`

**Description:** Use when building or reviewing any screen that shows a
list, feed, or data that loads from somewhere (for example, Events Feed or
My Schedule). Covers the loading, empty, and error states for that data —
not visual styling, copy tone, or screens with no dynamic data.

**Content:**

```
Steps:
1. For any screen that shows a list, feed, or fetched data, build three
   states alongside the main "data is present" view: loading, empty, and
   error. Treat all three as required, not optional.
2. Loading state: show a clear loading indicator (a spinner or skeleton
   placeholder) while data is being fetched — never a blank screen.
3. Empty state: when there's no data yet, show a specific, friendly
   message explaining what will appear there once it exists — never a
   generic "No data" or a blank screen.
4. Error state: if data fails to load, show a clear message and a way to
   retry — never fail silently into a blank or broken-looking screen.

Constraints:
- Don't skip any of the three states, even on a screen you consider
  temporary or a placeholder.
- Don't reuse generic filler text ("No data", "Error", "Something went
  wrong") — write a real, specific message for this exact screen.
- Build all three states at the same time as the screen itself, not as a
  follow-up fix later.

Examples:
- Events Feed: loading = skeleton cards while events load. Empty = "No
  events match your interests yet — check back soon." Error = "Couldn't
  load events — try again," with a retry button.
- My Schedule: loading = a brief spinner if there's any delay. Empty =
  "Events you RSVP to will show up here." Error = a retry message if
  fetching fails.

Expected output: every screen that shows dynamic data has working
loading, empty, and error states — not just the default view where
everything is present and successful.
```

## Trying it live

1. Create the skill (above) before your next follow-up prompt.
2. Ask Lovable for a new screen or feed the normal way — don't mention the
   skill by name.
3. Check whether it built all three states unprompted (or type
   `/ui-states` to invoke it directly if it didn't trigger on its own).
   This is a real, unscripted test — you're finding out live whether it
   worked, not confirming something you already knew would happen.
