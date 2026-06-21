# AGENTS.md — fadhilelrizanda.github.io

Guidance for Claude Code, AGY, Codex, and all AI agents working on this portfolio site.

## Project Overview

Static GitHub Pages portfolio for **Fadhil Elrizanda**, AI & Computer Vision / Machine Learning Engineer. The site is plain HTML/CSS/JS — no build step, no bundler, no framework. All changes go live by pushing to `origin main`.

- **Live URL**: https://fadhilelrizanda.github.io/
- **Stack**: HTML5 · Bootstrap 5.3 · vanilla JS · custom CSS (`style.css`)
- **Git remote**: `origin https://github.com/fadhilelrizanda/fadhilelrizanda.github.io`
- **CV symlink**: `cv/` → `../../CV Builder/` (absolute symlink; do not modify or recreate it)

## Directory Structure

```
fadhilelrizanda.github.io/
├── index.html          — Single-page portfolio (all sections)
├── style.css           — All custom styles; Bootstrap is loaded from CDN
├── images/             — Project screenshots and certification badges
├── videos/             — Demo video clips (vid1.mp4, vid2.mp4)
├── favicon_io/         — Favicon set (do not modify)
├── cv/                 — Symlink → CV Builder/ (read-only; managed separately)
├── robots.txt
├── sitemap.xml
└── google77bc1146cc795bf3.html  — Google Search Console verification (do not delete)
```

## Agent Behavior

### Tone & Writing Style (inherited from root AGENTS.md)
Apply the vault-level stylistic rules: no clichés, no AI filler words, objective and scholarly prose, professional humility.

### Surgical Editing
- Edit `index.html` and `style.css` with minimal diffs — preserve existing section order, class names, and Bootstrap markup conventions unless explicitly redesigning.
- Never rename or restructure sections without user confirmation.
- Do not alter `robots.txt`, `sitemap.xml`, or the Google verification file.

### Frontend Skill
This directory has a scoped `frontend-design` skill at `.claude/skills/frontend-design/`. When working on UI changes, activate it: Claude Code picks it up automatically when launched from within this directory. Apply its aesthetic guidelines (typography, motion, spatial composition) for any visual work.

Design rules specific to this portfolio:
- The site identity is **technical minimalism with depth** — clean layout, high-contrast typography, subtle motion. Avoid heavy gradients or decorative overload.
- Color palette is defined via CSS custom properties in `style.css`; extend there, never inline.
- Bootstrap utility classes are acceptable for layout; custom CSS in `style.css` for anything visual.
- Prefer CSS animations over JS-driven ones for hover states and reveals.

## Development Workflow

**No build step.** Edit files directly and open `index.html` in a browser to verify.

```bash
# Preview locally (from this directory)
python3 -m http.server 8080
# then open http://localhost:8080

# Deploy to GitHub Pages
git add <files>
git commit -m "describe change"
git push origin main
```

**Never use `git push --force`** on this repo — it is the live public site.

## Key Sections in index.html

| Section ID / anchor | Content |
|---|---|
| `#hero` | Name, title, tagline, CTA buttons |
| `#about` | Short bio, photo (`profile-img.JPG`), skills grid |
| `#experience` | Timeline of work/internship entries |
| `#projects` | Project cards with images, tags, and links |
| `#certifications` | Badge/logo grid |
| `#contact` | Social links and contact form or mailto |

When adding a project card, follow the existing card markup pattern in `#projects` exactly.

## Assets

- Project screenshots go in `images/` — use descriptive snake_case filenames.
- Videos go in `videos/` — keep under 10 MB where possible.
- The `bg-hero1.jpg` is the hero background; replace only with explicit instruction.
- `profile-img.JPG` is the headshot; do not modify.

## SEO & Metadata

- Open Graph, Twitter Card, and Schema.org tags are in the `<head>` of `index.html`. Update them when the headline or title changes.
- `sitemap.xml` and `robots.txt` are static; update `sitemap.xml` if new pages are added.
