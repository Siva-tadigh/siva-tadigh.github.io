# Learning Portfolio Template

A small static site: one "About Me" page, plus one page per module. Built as
plain HTML/CSS so it needs no build step and hosts directly on GitHub Pages.

## Files

- `styles.css` — shared design system. Edit this once to restyle every page.
- `index.html` — the About Me page (CV summary).
- `module-template.html` — the page to copy for each new module. Comments
  inside mark what to rename and where each required section lives:
  learning outcomes, artefacts + feedback, reflection, meeting notes, and
  the skills matrix + action plan.
- `module-1.html` — a filled-in example so you can see the template with
  real content in it. Replace its content, or delete it once you've made
  your own module pages.

## Adding a new module

1. Copy `module-template.html` and rename it, e.g. `module-2.html`.
2. Fill in the module title, code, and each of the five sections.
3. In **every** page's spine nav (including `index.html` and all other
   module pages), add a matching `<li><a href="module-2.html">...</a></li>`
   so the new module shows up everywhere.
4. On the new page itself, add `class="is-current"` to its own nav link.

Duplicating artefact cards, log entries, or skills-matrix rows: each is a
single HTML block (`<article class="artefact-card">`, `<div class="log-entry">`,
or `<tr>`) — copy the block and edit the text inside.

## Deploying to GitHub Pages

1. Create a repository and push these files to it (they can sit at the
   repo root, or in a `/docs` folder — just point Pages at whichever you use).
2. On GitHub: **Settings → Pages → Build and deployment → Source**, choose
   "Deploy from a branch", pick your branch and folder, then save.
3. GitHub will publish it at `https://yourusername.github.io/yourrepo/`
   within a minute or two.

## Notes

- No JavaScript or build tools required — just static files.
- Fonts (Source Serif 4, Inter) load from Google Fonts via `styles.css`;
  swap the `@import` line there if you'd rather self-host or use different
  faces.
- The site is responsive: the dark nav becomes a top bar on narrow screens.
