# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project state

This folder holds a personal professional website for a consultant radiologist. It is a plain static site in the root folder: `index.html` (one page, all sections) and `styles.css` (light and dark mode via `prefers-color-scheme`, phone layout under 760px). There is no framework, build, lint or test setup, and the folder is not a git repository.

- Preview locally: `py -m http.server 8000 --bind 127.0.0.1`, then open http://localhost:8000 (also configured as `website` in `.claude/launch.json`). Opening `index.html` as a file in the preview pane loses the stylesheet.
- When `profile.md` changes, copy the change into `index.html` by hand; the page text is not generated from it.
- `index.html` links `styles.css?v=N`; bump N after changing the CSS so browsers don't show a cached copy.
- Publishing: upload only `index.html` and `styles.css`. Never upload the whole folder: it also holds `CV/` (phone number, citizenships), `profile.md` and `CLAUDE.md`, which must stay private.

## Files

- `profile.md` is the source of truth for the site's text: headline, short and long bios, qualifications and registrations, areas of expertise, an experience table, and FAQs. Treat it as the content draft to build pages from.
- `CV/` holds the two source CVs (PDFs): a LinkedIn profile export and a radiology CV. `profile.md` was written from these. They differ in places (name format, job titles, language levels), so check both when a fact is in question.

## Open questions in the content

All markers were resolved by the owner in November 2026. If new ones are added, the rules below apply. `profile.md` used `[ASK ME: ...]` markers for decisions only the owner can make, such as the name format, how to describe the practice location, the official award name, whether to show registration numbers publicly, whether advisory clients may be named, language-level wording, and contact details/photo.

- Don't resolve these by guessing. Ask the user, or carry them into the site as visible placeholders.
- Don't publish anything still marked `[ASK ME]`, and leave out advisory client names (e.g. names from the radiology CV) unless the user confirms they may be shown.

## Writing conventions in the content

- British English spelling (e.g. "specialising", "tumour", "haemostaseology").
- First-person voice in bios and FAQs.
- German terms are kept with an English gloss (e.g. "Facharzt Radiologie (specialist in radiology)", "Approbation (full medical licence)").
