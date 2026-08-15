# Portfolio Template

A single-file, responsive portfolio website — glassmorphism cards, scroll reveals,
a sticky nav, and a CV preview modal. No build step, no dependencies. Just edit
`index.html` and open it in a browser.

## Quick start

1. **Fork or download this repo.**
2. Open `index.html` in any text editor.
3. Find every `[PLACEHOLDER LIKE THIS]` and replace it with your own info (see the
   checklist below — your editor's search, <kbd>Ctrl/Cmd+F</kbd> for `[`, makes this fast).
4. Open `index.html` in a browser to preview.
5. Deploy for free with **GitHub Pages**: push to a repo, then go to
   **Settings → Pages → Deploy from branch → main → / (root)**. Your site will be
   live at `https://<your-username>.github.io/<repo-name>/`.

## What to replace

| Section | Placeholder(s) |
|---|---|
| Nav / footer | `[YOUR NAME]` |
| Hero | `[YOUR JOB TITLE]`, `[YOUR TAGLINE]`, `[WRITE A SHORT BIO ABOUT YOURSELF]`, `[X.X]` / `[X]` stat numbers |
| Profile card | `[YOUR AVAILABILITY STATUS]`, `[YOUR GRADUATION DATE]`, `[YOUR FIELD OF STUDY]`, `[LIST YOUR KEY SKILLS]` |
| About | `[WRITE A DETAILED BIO ABOUT YOUR BACKGROUND, EXPERIENCE, AND WHAT YOU DO]`, `[YOUR SCHOOL NAME]`, `[YOUR DEGREE / MAJOR & MINOR]`, `[EXPECTED GRADUATION DATE]`, `[DESCRIBE YOUR ACADEMIC FOCUS]`, `[YOUR SCHOLARSHIPS OR AWARDS]`, `[DESCRIBE WHY YOU RECEIVED THIS AWARD]` |
| Projects (×3 cards) | `[PROJECT TITLE]`, `[PROJECT SUBTITLE]`, `[PROJECT CATEGORY]`, `[PROJECT DESCRIPTION]`, `[SKILL]`, `[YOUR PROJECT LINK]`, image `alt="[YOUR PROJECT IMAGE]"` |
| Experience (×5 entries) | `[EXPERIENCE TITLE / ORGANIZATION]`, `[EXPERIENCE SUBTITLE]`, `[EXPERIENCE DATES]`, `[DURATION]`, `[CATEGORY]`, `[EXPERIENCE DESCRIPTION]` |
| Contact | `[YOUR EMAIL]`, `[YOUR PHONE NUMBER]`, `[YOUR GITHUB URL]`, `[YOUR LINKEDIN URL]`, `[WRITE A ONE-LINE SUMMARY OF YOUR BACKGROUND AND EXPERTISE]`, `[YOUR SCHOOL]`, `[YOUR FIELD]`, `[YOUR MINOR / SPECIALTY]`, `[YOUR STATUS]` |
| CV modal | `[YOUR-CV-FILE].pdf` (×3 — see below) |

The `Skills` section (Programming, Data Science & Analysis, Web Development,
Professional Skills) is left as sample content — swap the pills for your own
stack, or leave categories you don't need empty.

## Adding your CV

The "View CV" button opens a modal that loads a PDF in an iframe. To wire it up:

1. Add your résumé PDF to the repo, e.g. `my-cv.pdf`.
2. Find the three instances of `[YOUR-CV-FILE].pdf` in `index.html` and replace
   them with your actual filename (e.g. `my-cv.pdf`).

If you don't want the CV modal at all, you can just remove the "View CV" button
and the `<div class="cv-modal">` block near the bottom of the file.

## Adding real project images

Each project card currently shows a placeholder graphic (an inline SVG, so
there's nothing to break if you don't add images). To use real screenshots:

1. Add your image files to the repo (e.g. an `images/` folder).
2. Replace the placeholder `src="data:image/svg+xml,..."` on each `<img>` with
   your image path, e.g. `src="images/project-1.png"`.
3. Update the matching `alt="[YOUR PROJECT IMAGE]"` with a real description for
   accessibility.

## Structure

```
.
├── index.html   # everything — markup, styles, and scripts in one file
└── README.md
```

Everything (CSS and JS) lives inside `index.html`, so there's nothing else to
configure or install.

## Customizing further

All colors, spacing, and fonts are set as CSS custom properties at the top of
the `<style>` block (`:root { ... }`) — change `--accent`, `--bg`, etc. there to
re-theme the whole site without touching the rest of the CSS.
