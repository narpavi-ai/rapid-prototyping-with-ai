# Worked example — testing and fixing CampusPulse

## What the testing pass found

Walking through the checklist from [`README.md`](README.md) on the
CampusPulse build from Stage 4 turned up three real issues:

1. Tapping RSVP twice on the same event created two entries in My Schedule
   instead of un-RSVPing.
2. Before RSVPing to anything, My Schedule showed a broken-looking blank
   screen instead of a friendly empty state.
3. Going "back" from Event Detail to Events Feed reset the interest filter,
   so the feed showed unfiltered events again.

## Bug report prompts used to fix them

**Duplicate RSVP:**

```
On Event Detail, when I tap RSVP on an event I've already RSVP'd to, it
adds a second duplicate entry on My Schedule instead of removing the
existing one. I expected tapping RSVP again to un-RSVP (remove it from
My Schedule).

Do not change how RSVPs are saved for events I haven't RSVP'd to yet.
```

**Empty state regression:**

```
On My Schedule, when a user has zero RSVPs, the screen shows blank
instead of the friendly "Events you RSVP to will show up here" message we
had in the original skeleton. I expected that message to still show when
the list is empty.

Do not change the layout for when there ARE saved events.
```

**Filter reset on back-navigation** — this one didn't get fixed on the
first or second try, so instead of a third variation, Plan mode was used:

```
[Plan mode]

Going back from Event Detail to Events Feed resets the interest filter
back to "all events" instead of keeping the filtered view I had. I've
tried fixing this twice already. Before we try again, walk me through
what's likely causing the filter state to reset on back-navigation.
```

Plan mode identified that the filter was being recalculated fresh on every
screen load instead of persisting — the actual fix was a small,
narrowly-scoped follow-up prompt in Build mode based on that explanation,
rather than a fourth blind attempt.
