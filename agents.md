# Leafinn SOP Quiz Handoff

## Cross-Project Startup

Before changing this repo, read the education-training mother-project shared context:

- `/Users/weiyang/Desktop/葉綠宿/教育訓練/projects/00_母專案/CURRENT_STATE.md`
- `/Users/weiyang/Desktop/葉綠宿/教育訓練/projects/00_母專案/PROJECT_INDEX.md`
- `/Users/weiyang/Desktop/葉綠宿/教育訓練/projects/00_母專案/shared/cross-project-context.md`
- `/Users/weiyang/Desktop/葉綠宿/教育訓練/projects/00_母專案/shared/moodle-system-concept.md`

This GitHub Pages quiz site is for partner question verification only. It is not the formal education-training entrance. Moodle remains the official training platform.

## Project Identity

- Project name: Leafinn SOP Quiz
- Local repo path: `/Users/weiyang/Desktop/葉綠宿/教育訓練/projects/01_綠宿題庫核對網站/10 GitHub Pages共享網站`
- Parent project folder: `/Users/weiyang/Desktop/葉綠宿/教育訓練/projects/01_綠宿題庫核對網站`
- Primary live Pages repo: `https://github.com/abnergreenhotel/leafinn-sop-quiz.git`
- GH5459 handoff mirror: `https://github.com/GH5459/leafinn-sop-quiz.git`
- Live URL: `https://abnergreenhotel.github.io/leafinn-sop-quiz/index.html`
- Branch: `main`
- Drive category: `02. 館內課程`
- Role: Green Hotel Leafinn SOP question review site, GIFT question-bank exports, NotebookLM quiz conversion outputs, and partner-facing verification pages.

## Repository Purpose

This repo is the deployable static quiz site. It contains generated HTML quiz pages, GIFT text files, and the index page used for question review.

It is not the full source workspace. The wider parent folder keeps source PDFs, Excel files, NotebookLM exports, scripts, Moodle cover assets, slide batches, and cleanup records.

## Local Structure

- `index.html`: quiz-site entry page.
- `*.html`: one static quiz page per SOP course/unit.
- `*.gift.txt`: Moodle-ready GIFT export paired with each quiz page.
- `_summary.json`: generated quiz/course summary data.
- `.nojekyll`: GitHub Pages setting for serving files as-is.

## Moodle Relationship

- GitHub Pages is only a review surface.
- Moodle course naming, category, question-bank grouping, completion logic, and future career-map links must follow the mother project's `shared/moodle-system-concept.md`.
- Before importing GIFT files to Moodle, questions should be reviewed and aligned to the shared course-code rules.
- Do not create a separate Leafinn-only Moodle naming system.

## Update Workflow

The broader Leafinn workspace can regenerate this repo from NotebookLM and local scripts. The usual publish flow is:

```bash
cd "/Users/weiyang/Desktop/葉綠宿/教育訓練/projects/01_綠宿題庫核對網站/10 GitHub Pages共享網站"
git status --short --branch
git remote -v
git add <intended files>
git commit -m "Refresh quiz site"
git push origin main
git push gh5459 main
```

Daily education-training close-out is normally run from the mother project:

```text
[$close-education-training-day](/Users/weiyang/.codex/skills/close-education-training-day/SKILL.md)
教育訓練每日收工
```

That close-out should inspect this repo and push both the live Pages remote and the GH5459 handoff mirror when this repo has changes.

## Security Rules

Do not commit:

- `.env`, `.env.*`, tokens, passwords, private keys, cookies, browser profiles, or `storage_state.json`.
- NotebookLM login state.
- Raw personal data, database dumps, or private staff records.
- `node_modules`, local caches, temporary preview folders, or third-party tool clones.

## Current Status

- The live site remains at the `abnergreenhotel.github.io` URL.
- The repo is also mirrored to GH5459 for cross-computer and cross-agent handoff.
- The parent project folder has the broader project inventory and cleanup guidance.

## Next Operator Notes

- Keep the old `abnergreenhotel` remote working unless the live URL is intentionally migrated.
- Keep the GH5459 mirror updated so the project can be found with the rest of the education-training repos.
- If Moodle import rules change, update the mother project's shared Moodle concept first, then update this file if Leafinn-specific handling changes.
