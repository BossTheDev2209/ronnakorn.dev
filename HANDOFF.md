# Handoff — Next Session

## Project
ronnakorn.dev — static personal developer website redesign.

## Current direction
- Multi-page personal site: Home, Projects, About.
- Home is intentionally compact: Hero/introduction → Featured Projects (3) → Contact/Footer.
- Detailed About content lives on `about.html`.
- Full project collection lives on `projects.html`.
- Inspiration: Jason Cameron's site for information architecture, compactness, and personal developer identity only. Do not copy exact design or identity.
- Visual goal: compact, minimal, technical, personal, recognizable.
- Skills section/marquee is removed from the Home direction and deprioritized.
- Keep plain HTML/CSS for now; no framework/build step.

## Latest state
- `index.html` has been successfully reduced to Hero + 3 featured project cards + Contact/Footer.
- Navigation already points to `index.html`, `about.html`, and `projects.html`.
- `about.html` and `projects.html` already exist as separate pages.
- Home stylesheet is now `index.css`.
- Featured Projects currently uses a 3-column grid.
- `.ProjectsContainer` and `.ProjectsHeader` were just introduced and are still being worked on.
- Home project content and footer contact text are still placeholder content.
- `about.css` and `projects.css` remain separate; shared styling has not yet been consolidated.

## Next session — start here
1. Read this file and inspect the current `index.html` + `index.css` before changing anything.
2. Review the user's latest CSS work rather than rewriting it.
3. Finish the Home Featured Projects header/layout, especially understanding why `.ProjectsContainer` needs the layout properties it uses.
4. Replace placeholder "view all" text with an actual link to `projects.html`.
5. Replace placeholder project/footer content when the user is ready.
6. Then improve responsive behavior for the 3-card grid.
7. After Home is stable, make `about.html` and `projects.html` visually consistent with the shared navigation/theme.
8. Keep the user's current Hero unchanged unless explicitly requested.

## Learning mode
This is a CSS/HTML learning project. Prefer real project edits by the user.
- Explain the problem first, then the smallest concept that solves it, then connect it to the actual code.
- Do not rewrite code unless explicitly asked.
- When the user is trying a change themselves, review it first and give the smallest useful correction/hint.
- Use Socratic/graded questions only when the user can reasonably derive the answer.
- For multiple-choice teaching questions, NEVER reveal the answer before the user responds.
- Focus on fixing mental models, not memorizing CSS rules.

## Important constraints
- Preserve existing user work.
- Do not redesign or overwrite the current Hero without explicit request.
- Avoid unnecessary architecture changes.
- Verify navigation, links, image paths, fonts, desktop/mobile behavior, and `git diff --check` after meaningful changes.
