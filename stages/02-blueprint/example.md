# Worked example — CampusPulse blueprint

Continuing from the [Stage 1 problem statement](../01-problem/example.md).

## Screen list (4 screens)

1. **Onboarding** — name + pick interests (tech, sports, arts, free food,
   music, career)
2. **Events feed** — upcoming campus events, filtered/sorted to match the
   interests picked during onboarding
3. **Event detail** — full description, date/time, location, an RSVP button
4. **My Schedule** — every event the user has RSVP'd to, shown as their own
   personal list

## Core flow

New user opens the app → picks their interests once (Onboarding) → lands on
the Events feed already filtered to what they care about → taps an event
they like → sees the Event detail and taps RSVP → later, opens My Schedule
and sees that event (and any others) saved there as their own list.

## What comes back to the user

**My Schedule** — the list of events they've RSVP'd to. This is the "saved
order / personal schedule" moment: proof the app remembers *them*
specifically, not just a shared list everyone sees the same way.

## Explicitly out of scope for this workshop

- No login with email/password verification — a name is enough for the demo
- No event creation flow for organizers — events are pre-seeded
- No push notifications or reminders
- No social features (comments, sharing, following friends)
- No payment/ticketing for paid events

This 4-screen, one-flow shape is exactly what gets described to Lovable in
[Stage 3](../03-lovable-prompt/example.md).
