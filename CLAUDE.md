# CLAUDE.md

## Project Purpose
Academic personal website and CV for Jisu Kim (Jekyll + GitHub Pages).
This repo is the single source of truth for the website and CV management.

## Key Files
- `_pages/publications.md` — publication list (website)
- `_pages/cv.md` — CV page with PDF link
- `_pages/about.md`, `_pages/etc.md`, `_pages/projects.md` — other pages
- `files/main.tex` — LaTeX source for CV (git-ignored, local only)
- `files/JisuKim_CV_YYYYMMDD.pdf` — compiled CV PDF

## Workflow: Updating CV
1. Edit `files/main.tex`
2. Compile: `cd files && pdflatex main.tex`
3. Copy: `cp files/main.pdf files/JisuKim_CV_YYYYMMDD.pdf`
4. Update PDF link in `_pages/cv.md`
5. Commit and push

## Publication Conventions
- Numbering: oldest = smallest number (J1, C1), newest = largest. New papers get next number at top.
- Display order: newest first (top of list)
- Author name: always **Jisu Kim** (bold)
- Corresponding author: marked with \* after name
- Co-author names: spell each one exactly as that paper was published — do NOT unify spellings across entries. C10 is "Benjamin S. Riggan", C8 is "Benjamin Riggan", and both are correct. Never blanket find-and-replace an author name.
- Advisor/supervisor mentions outside publication lists (about.md EDUCATION/POSITIONS, CV) use the full name: "Benjamin S. Riggan"
- Abstract presentations: tagged with (__abstract__)
- Do NOT add papers in preparation or under blind review to the public site

## Markdown Gotchas
- kramdown collapses consecutive lines into one paragraph. One-item-per-line blocks outside tables/lists (e.g. SKILLS, Contacts in `about.md`) need a trailing `<br>` on every line but the last.
- Institution names that already contain a city don't repeat it: "University of Tennessee, Knoxville, TN, USA", not "..., Knoxville, Knoxville, TN, USA"
