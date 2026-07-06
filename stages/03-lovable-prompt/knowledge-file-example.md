# Reference — a reusable Workspace Knowledge file

**This is not part of the live CampusPulse walkthrough.** Lovable actually
has two kinds of Knowledge file:

- **Project Knowledge** — specific to one app (what it is, who it's for,
  its screens). This workshop skips setting one of these up live — instead,
  the single first build prompt in [`prompt.md`](prompt.md) carries that
  context directly, so there's nothing extra to configure mid-demo.
- **Workspace Knowledge** — shared across *every* project in your Lovable
  workspace (**Settings → Knowledge**, not Project settings). This is where
  general engineering standards live: coding conventions, styling rules,
  which libraries to prefer. You set it up once and it applies to
  everything you build afterward.

The example below is a Workspace Knowledge file — a reusable set of
standards, not tied to CampusPulse or any single app. Vishal will walk
through building one of these live; treat this as the reference to copy
from afterward, for your own Lovable workspace.

## Example

```
Coding standards
- Always enable TypeScript strict mode.
- Never use `any`. Use `unknown` and narrow the type.
- Prefer named exports. Do not use default exports.
- Prefer `const` over `let`. Never use `var`.

Naming conventions
- Use camelCase for variables and functions.
- Use PascalCase for components and types.
- Use kebab-case for file names.

Styling
- Use Tailwind CSS for styling.
- Do not use inline styles.
- Do not use CSS modules.

Libraries
- Use shadcn/ui components when possible.
- Use React Query for server state.
- Use Zustand for client state.

Architecture
- Route API calls through a service layer.
- Do not call `fetch` directly from React components.

Testing
- Write unit tests for new utility functions and hooks.
- Run existing tests after making changes.
- Verify new functionality in the browser before marking it complete.

Code quality
- Run the linter after significant changes.
- Remove unused imports and dead code.

Localization
- Write code comments and variable names in English.
- Use date format DD/MM/YYYY.
- Use European number formatting (comma as decimal separator).

Brand voice
- Use a friendly, professional tone in all user-facing copy.
- Use sentence case for headings and buttons (for example, "Create new
  project", not "Create New Project").
- Do not use placeholder text like "Lorem ipsum" — always write realistic
  copy.

General rules
- Do not add `console.log` statements.
- Do not use deprecated React patterns.
- Write code comments in English.
```

## Why this is separate from tonight's prompt

Mixing project-specific context (what CampusPulse is) with general
engineering standards (strict TypeScript, Tailwind, no `console.log`) into
one file makes both harder to reuse. Project Knowledge changes per app;
Workspace Knowledge doesn't. Setting up Workspace Knowledge is a one-time,
across-every-project habit — worth doing, but it's a "later tonight or
tomorrow" task, not something to configure mid-demo.

If you're technical and already have opinions on strict mode, testing, or
state management, adapt the example above to your own stack and paste it
into your workspace's **Settings → Knowledge**. If you're not, it's fine to
skip this entirely — none of it is required to finish the workshop with a
working app.
