# Worked example — building CampusPulse screen by screen

Continuing from the [Stage 3 first build prompt](../03-lovable-prompt/example.md),
which produced a 4-screen skeleton with placeholder content and working
navigation. These are the follow-up prompts, run one at a time inside
Lovable's Build mode, that bring it to life.

## 1. Real events + interest filtering (Events Feed)

```
On the Events Feed screen, replace the sample cards with a real list of
at least 8 events, each with a title, date, short description, and one
interest tag (Tech, Sports, Arts, Free Food, Music, or Career). Filter and
sort the feed so events matching the interests picked during Onboarding
appear first.

Do not change the Onboarding screen or the interest list — leave those
exactly as they are.
```

## 2. Saving an RSVP (Event Detail → My Schedule)

```
On the Event Detail screen, make the RSVP button actually save that event
against the current user, so it shows up on My Schedule. If the user taps
RSVP again on the same event, treat it as "un-RSVP" and remove it from My
Schedule instead of adding a duplicate.

Do not change the Events Feed filtering logic we just built.
```

## 3. My Schedule showing real saved data

```
On the My Schedule screen, replace the empty-state placeholder with the
real list of events this user has RSVP'd to, soonest first. If they
haven't RSVP'd to anything yet, keep a friendly empty state that says so.

Do not change how RSVPs are saved on the Event Detail screen.
```

## 4. A rough edge, handled with Plan mode first

Suppose after prompt 2, un-RSVPing removes the event from My Schedule but
also breaks the RSVP button's label on Event Detail. Rather than
re-prompting the same fix repeatedly:

```
[Switch to Plan mode]

The RSVP button on Event Detail isn't updating its label correctly after
un-RSVPing. Walk me through what's likely happening before we change
anything.
```

Once Plan mode explains the likely cause, switch back to Build mode with a
targeted fix — this avoids looping on the same broken prompt. More on this
pattern in [Stage 5](../05-test-iterate).
