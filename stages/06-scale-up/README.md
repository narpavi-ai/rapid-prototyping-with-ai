# Stage 6 — Scale up after Lovable

**Tool:** GitHub (optional), then whatever comes next for you
**Goal:** Know what your options are once your app works in Lovable — none
of which are required to finish this workshop.

> **This entire stage is optional.** Everything through Stage 5 gives you a
> real, working, shareable app with nothing but Lovable, ChatGPT/Claude, and
> a browser. Nobody needs to leave Lovable's no-code environment to fully
> participate in this workshop. Read this stage if you're curious about
> what's next — not because you have to.

## Option 1: Connect Lovable to GitHub (two-way sync)

*(Source: [Lovable docs — GitHub integration](https://docs.lovable.dev/integrations/github),
verified July 2026.)*

Lovable can sync your project's actual code to a GitHub repository, and
keep it in sync in both directions — edits in Lovable push to GitHub, and
edits pushed to GitHub pull back into Lovable.

**Setup flow:**
1. Go to **Workspace settings → Git → GitHub** (or **Project settings →
   Git → GitHub**).
2. Click **Add account** — a GitHub popup opens.
3. Choose the GitHub account/organization and either "All repositories" or
   "Only select repositories."
4. Click **Install & Authorize**.
5. Back in Lovable, connect your project — Lovable **creates a new GitHub
   repo automatically** for it.

**Good to know before you do this:**
- You need a plain **github.com** account (Enterprise options exist on paid
  plans, not needed here).
- Lovable **creates** the repo — you can't connect an existing repo to an
  existing Lovable project.
- Sync works on **one branch at a time**.
- Renaming, moving, or deleting the connected repo will break the sync.
- Once disconnected, you can't reconnect to that exact same repository.

**Why you'd want this:** it gives you an actual, ordinary codebase — useful
if you (or a developer you bring in later) want to edit code directly, use
your own coding tools, or run the app outside Lovable entirely.

## Option 2: Everything else stays exactly where it is

If you don't connect GitHub, your app doesn't go anywhere — it keeps
living in Lovable, with a shareable link, exactly as it does today. You can
keep prompting Lovable to extend it any time.

## What "scaling up" can mean later, roughly in order of effort

1. **Custom domain** — Lovable supports pointing your own domain at your
   published app, no code required.
2. **Real backend features** — things like real user accounts, payments, or
   more complex data can be added inside Lovable via its Supabase
   integration, still without leaving the no-code environment.
3. **Handing code to a developer** — with GitHub sync on, a technical
   co-founder or contractor can now clone the repo and work in their own
   editor, using whatever tools they like (including AI coding tools like
   Claude Code).
4. **Rebuilding pieces outside Lovable** — for parts that outgrow a no-code
   builder, the synced GitHub repo is a normal codebase any developer can
   take over incrementally, screen by screen, rather than a full rewrite.

None of this needs to happen today. It's worth knowing the door exists.
