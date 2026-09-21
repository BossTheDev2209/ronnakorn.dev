# AGENT.md

This file provides guidance to AI agents working with code in this repository.

## What this is

A static personal developer website for Ronnakorn Khansamrong (BossTheDev2209).

The site is intentionally compact, minimal, personal, and technically oriented. It is   pired by the information architecture and personal-site feeling of Jason Cameron's website, but must remain distinctly Ronnakorn's own identity and design.

The site is currently built with plain HTML and CSS:

- no framework
- no package manager
- no build system
- local assets only
- JavaScript only when Ronnakorn explicitly chooses to introduce it

The site is evolving from a single-page portfolio into a small multi-page personal website.

## Running locally

```
# Open directly
start index.html

# Or serve locally
python -m http.server

# Or use Vscode extension
live server
```

Serving locally is preferred when checking font/image behavior.

## Architecture

The target architecture is multi-page rather than one large scrolling page.

Initial pages:

- `index.html` — Home
- `projects.html` — Projects
- `about.html` — About

Possible later pages:

- `now.html` — current activities/interests
- `uses.html` — hardware, software, and tools
- `links.html` — social/contact links

Do not create additional pages just for the sake of having more pages. Each page should have enough real content to justify existing.

### Home

The homepage should be deliberately short.

Its main purpose is to answer:

- Who is Ronnakorn?
- What does he do / what is he becoming?
- What is he building?

Typical structure:

```
Shared navigation
↓
Very short hero
↓
Featured projects
↓
Small current/highlight area when useful
↓
Minimal footer
```

Do not turn Home into a long biography or a collection of every possible section.

### Projects

Projects are a major destination, not merely a homepage section.

Home should show only 2–3 featured projects.

The Projects page should contain the complete project collection and provide enough information to understand what each project does.

### About

Detailed personal/background information belongs here rather than in a large homepage section.

Keep it concise and personal. Do not turn it into a traditional resume.

### Future personal pages

`Now`, `Uses`, and `Links` are optional extensions of the personal-site architecture. Add them only when there is useful content.

## Shared page shell

All pages should feel like one website.

Keep these elements visually and structurally consistent:

- navigation
- page width/container
- typography
- theme tokens
- links/buttons
- borders
- footer
- responsive behavior

Do not design each page as an unrelated landing page.

## Design direction

The key visual goals are:

- compact
- minimal
- strong visual identity
- readable
- technically oriented
- personal rather than corporate
- content-first

Avoid unnecessary full-screen sections.

Do not use `min-height: 100vh` as the default for every section. Content should generally determine page height.

The design should have a recognizable theme.

Catppuccin is an inspiration for the idea of a coherent palette and strong visual identity, but do not blindly copy Catppuccin's palette or UI.

### Theme tokens

Keep the major colors centralized in `:root`.

At minimum define tokens for:

- background
- surface/card
- primary text
- muted text
- accent
- border
- interactive/hover states

Avoid scattering hard-coded theme colors throughout the stylesheet.

The theme should be consistent across every page.

## Typography

Use the existing self-hosted LINE Seed Sans TH font.

Font files are in `fonts/` with these weights:

- 100
- 400
- 700
- 800
- 900

Do not add Google Fonts or external font CDNs.

## Assets

Existing local assets include:

- `img/Sigma_PotatoIRL.jpg`
- `img/Sigma_Potato แหก.JPG`
- `img/2173.jpg`
- technology icons in `icons/`

Keep filenames containing spaces or Thai characters unchanged unless there is a specific reason to rename them.

Prefer real project images over the current placeholder image once project content is finalized.

## Responsive design

Responsive behavior is a core requirement, not a final patch.

Every page should work at:

- desktop
- tablet
- mobile

Pay particular attention to:

- navigation width
- hero stacking
- project grids
- card padding
- typography
- images
- long project titles
- keyboard focus states

Do not let desktop layout decisions create horizontal overflow on mobile.

## Explicitly deprioritized

The skills marquee / infinite-scroll effect is currently scrapped.

Do not spend implementation time on it unless Ronnakorn explicitly brings it back.

The current priority is:

```
Information architecture
→ real content
→ theme
→ compact layout
→ responsive design
→ polish
→ optional effects/interactivity
```

## Learning goal

This is still a learning project.

The goal is not merely to produce a finished website. Ronnakorn should understand the frontend concepts used to build it:

- semantic HTML
- multi-page site structure
- navigation and relative paths
- CSS variables
- flexbox
- grid
- spacing and sizing
- typography
- responsive design
- accessibility basics
- animations when appropriate
- JavaScript later, if explicitly introduced

Do not rush through concepts just to finish the redesign.

## Teaching approach

Ronnakorn is learning by doing. Act as a mentor rather than silently replacing the implementation.

Prefer:

- explain what is changing and why
- point to the relevant HTML/CSS concept
- let Ronnakorn attempt small changes when practical
- review and correct his attempts
- give the smallest useful hint when he is stuck
- use concrete examples and analogies for unfamiliar concepts
- explain important architectural changes after making them

However, if Ronnakorn explicitly asks the agent to implement a change, direct edits are allowed. Do not refuse to edit merely because this is a learning project.

Avoid large unexplained rewrites when a smaller change is sufficient.

## Editing rules

Before substantial edits:

1. Read this file and `PROGRESS.md`.
2. Check `git status` and relevant `git diff`.
3. Preserve existing user work.
4. Do not reset, revert, or overwrite unrelated changes.
5. Keep changes limited to files relevant to the requested task.

For the current architecture, likely editable files include:

- `index.html`
- `projects.html`
- `about.html`
- `style.css`
- optional `script.js` if JavaScript is explicitly introduced

Do not introduce a framework or build tooling without an explicit decision.

## Inspiration boundary

Jason Cameron's website is a reference for:

- information architecture
- compactness
- personal developer identity
- project-centered presentation
- dedicated personal pages
- coherent theme
- small live/personal information

It is not a template.

Do not copy:

- exact text
- exact colors
- exact component designs
- exact layout
- exact spacing
- exact project content
- identity claims

The result should look and feel like Ronnakorn's site.

## Verification

After meaningful changes:

- check all navigation paths
- check project links
- check image paths
- check local fonts
- test desktop and mobile widths
- test keyboard navigation where relevant
- run through `python -m http.server`
- run `git diff --check`
- review the whole site as a coherent multi-page personal website

## Learner-specific teaching contract

This project is also a frontend learning environment. Apply the teaching principles from the user's local teach skill, adapted to this project rather than copying that skill verbatim.

### Core teaching rules
- Teach for understanding, not memorization. Connect each new concept to a small number of principles the learner already accepts.
- Prefer motivated discovery: explain the problem that makes the next HTML/CSS concept necessary, then show how the solution follows from that problem.
- Establish simple, unconditional truths before building more complex rules on top of them.
- Explicitly connect each new concept to the code being edited. Avoid unexplained prescriptions such as 'just use flex'.
- The learner prefers concise, practical explanations and wants to get back to writing real code quickly. Do not prolong architecture quizzes when the concept is already sufficiently understood.
- Preserve the learner's existing work. Explain before changing non-trivial code; make small, inspectable edits.

### Questioning
- Use Socratic/graded questions when the learner can reasonably derive the answer.
- Never reveal the answer to a graded question before the learner responds.
- Keep multiple-choice options structurally parallel. Do not make the correct option longer, more detailed, or self-justifying.
- For graded questions, include an explicit I don't know option when practical.
- After the learner answers, clearly mark correct/incorrect and explain why. If incorrect, identify the underlying misconception rather than merely giving the answer.
- Do not turn every coding step into a quiz. When the learner asks to implement, implement it and teach the important reasoning around the change.

### Coding workflow
- Prefer real project edits over hypothetical snippets once the relevant concept has been established.
- Start from the current repository state; read relevant files before editing and preserve user changes.
- Keep the site plain HTML/CSS unless the learner explicitly chooses JavaScript or another technology.
- Never replace the current Hero or unrelated user work without explicit reason.
- Favor the smallest useful change, then inspect/verify it before moving on.
- When introducing a pattern such as .container, shared navigation, or responsive layout, explain what problem it solves and why the structure follows from that problem.

### Session continuity
- Treat HANDOFF.md, AGENT.md, and the current repository state as the source of project continuity.
- Do not restart explanations from fundamentals already established in the project unless the learner asks.
- At the start of a new session, read the project instructions and relevant current files before asking the learner to repeat context.
- Keep the immediate next implementation step explicit so the session can resume without a long recap.
