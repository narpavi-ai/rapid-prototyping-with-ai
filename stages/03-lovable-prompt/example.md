# Worked example — CampusPulse's first build prompt

Continuing from the [Stage 2 blueprint](../02-blueprint/example.md).

## First build prompt (paste into Lovable chat to start)

```
CampusPulse is a small campus events app for first-year university
students. Today, students find out about campus events through scattered,
passive channels — a rarely-checked university events page, club
Instagram accounts, and word of mouth — so they often hear about events
too late or forget ones they meant to attend. CampusPulse gives them one
place that surfaces events matched to their interests and keeps track of
what they've already said yes to.

Visual identity: this should feel like a festival wristband and ticket
stub, not a generic app dashboard. Concretely:
- Accent color: one bold, saturated amber/marigold, hex #F4A100 — the
  color of a festival wristband, used sparingly for the RSVP button,
  active tags, and the interest chips a user has selected.
- Type: bold, condensed display type for event titles (poster-style,
  like a gig lineup); a monospace font for dates, times, and locations
  (like a stamped ticket stub) — the two should visibly contrast.
- Layout: event cards look like ticket stubs — a perforated or dashed
  line dividing the title/description from the date-time-location block,
  slightly rounded corners, a small torn-edge detail. Dense, not
  spacious: this is a feed people scan quickly, not a slow editorial
  page.
- Icons: each interest category gets its own small icon/emoji (Tech 💻,
  Sports 🏅, Arts 🎨, Free Food 🍕, Music 🎵, Career 💼), shown next to
  its chip and its tag on event cards — this app should never end up
  100% text with no visual anchors at all.

This should feel like a festival wristband and lineup card for campus
events — not a corporate events dashboard. Keep coming back to that one
line for every screen below.

Build the foundation only — four screens with working navigation between
them, using placeholder content for now. No real filtering logic or saved
data yet, just the screens and the flow:

1. Onboarding — a name field and a multi-select of interests (Tech,
   Sports, Arts, Free Food, Music, Career), each chip showing its icon
   next to the label and turning the accent color when active, with a
   "Continue" button that goes to the Events Feed.
2. Events Feed — a list of 4-5 sample events using the ticket-stub card
   style above (title, date, short description, one interest tag with
   its icon each). Tapping an event goes to Event Detail.
3. Event Detail — full description, date/time, location, and an RSVP
   button in the accent color (no real save behavior yet). Keep the same
   condensed-display/monospace contrast as the feed cards. Include a way
   to navigate to My Schedule.
4. My Schedule — an empty state for now that says "Events you RSVP to
   will show up here," styled like an empty ticket sleeve rather than a
   blank page. This screen is where a user's own RSVP'd events will
   eventually show up — the moment the app proves it remembers this
   specific person, not just showing everyone the same list.

Guardrails:
- Do not add a login/password/email verification flow — a name is enough
  for this app.
- Do not add an event-creation flow for organizers — events are seeded
  sample data.
- Do not add payments, ticketing, notifications, or social features
  (comments, following friends) — explicitly out of scope.
- Do not wire up real data persistence or filtering yet — just the
  screens, sample content, and navigation between them. We'll build the
  real logic screen-by-screen after this.
```

## Why this version, not a plainer one

An earlier draft of this prompt just said "keep the visual tone clean and
modern, not corporate." That's a label, not a direction — Lovable (like
any AI tool) resolves vague adjectives to the average of everything ever
described that way, which is exactly the generic centered-hero,
purple-gradient look every AI app defaults to. Naming a real, concrete
reference (a festival wristband and ticket stub) instead of an adjective
gives it something specific to build toward, and pulling 2-3 real tokens
from that reference (one accent color, one type contrast, one layout
rhythm) is enough direction without writing a full design system.

This is one self-contained message: a short paragraph of app context, a
concrete visual identity, then detailed, technical, screen-by-screen
instructions. It intentionally builds a **clickable skeleton**, not the
real app — real filtering and RSVP saving happen incrementally in
[Stage 4](../04-build-in-lovable), one screen at a time.

One more lesson, learned the hard way: a real test run of this same
approach used "airport departure board" as its concrete reference for a
different app, and the result looked fantastic — dense rows, condensed
monospace type, amber accents, nothing generic about it. But it came back
with **zero images anywhere**. Nothing in that prompt was wrong — a
departure board genuinely is pure typography, no photos, and the prompt
never asked for an icon or thumbnail either. That's why this version
explicitly calls for one visual element (an icon per interest) regardless
of how strong the reference is — otherwise "give it a concrete visual
identity" can still quietly produce an app made entirely of text.
