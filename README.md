# SGBD MCQ Practice

Static MCQ website for SGBD / PL SQL database practice.

This folder is a copy of the latest Data Structures MCQ website shell, adapted for SGBD / PL SQL practice and materials.

GitHub repo:

```text
https://github.com/FiredMosquito831/SGBD-prep-and-site-an2-sem2
```

GitHub Pages URL:

```text
https://firedmosquito831.github.io/SGBD-prep-and-site-an2-sem2/
```

## Contents

- `index.html`: main quiz app.
- `answers.html`: correct-answer search page.
- `materials.html`: curated materials page with ordered PDF study resources and usage guidance.
- `materials/`: downloadable SGBD / PL SQL study PDFs exposed on `materials.html`.
- `data/config.json`: active set registry and UI metadata.
- `data/website.json`: startup metadata required by the current app shell.
- `sets/sgbd_uploaded_master.json`: current/default SGBD question set.
- `sets_en/sgbd_uploaded_master.json`: current mirror. This currently matches `sets/` until the final bilingual split is prepared.
- `sets/diaconita_1.json`: Diaconita 1 compact set.
- `sets_en/diaconita_1.json`: mirror for Diaconita 1.
- `sets/diaconita_2.json`: Diaconita 2 compact set.
- `sets_en/diaconita_2.json`: mirror for Diaconita 2.
- `sets/diaconita_dedupped.json`: Diaconita dedupped compact set.
- `sets_en/diaconita_dedupped.json`: mirror for the dedupped set.

## Current Set

Source:

```text
C:\Users\fgghk\Downloads\SGBD_UPLOADED_SETS_FIXED_PACK\SGBD_UPLOADED_SETS_FIXED\03_FIXED_DEDUPED_MASTER\sgbd_uploaded_fixed_deduplicated_master_plain.json
```

Count:

- `sgbd_uploaded_master`: 168 questions
- `diaconita_1`: 39 questions
- `diaconita_2`: 77 questions
- `diaconita_dedupped`: 22 questions
- 96 single-correct questions
- 72 multi-correct questions

The current version mirrors the same fixed source JSON in both `sets/` and `sets_en/` until the final bilingual split is prepared.

## Materials Library

The study materials page is intentionally ordered by prep value:

1. `materials/plsql-mcq-theory-synthesis.pdf`
   - Fastest exam-oriented theory compression. Best first read for MCQ prep.
2. `materials/courses-1-8.pdf`
   - Full course backbone and formal source coverage.
3. `materials/plsql-cheatsheet-1-9.pdf`
   - Condensed structured reference across courses and seminars.
4. `materials/seminars-1-9-organized.pdf`
   - Reorganized seminar walkthrough for application-focused understanding.
5. `materials/ex-practice-set.pdf`
   - Graduated exercise pack from easier tasks to harder PL/SQL work.
6. `materials/all-practice.pdf`
   - Short supplemental practice sheet for quick implementation reps.

## Run Locally

From this folder:

```powershell
python -m http.server 8000
```

Then open:

```text
http://localhost:8000/
```

Opening `index.html` directly can fail in some browsers because the app loads JSON files with `fetch()`.

## Update The Set

1. Replace the target file under `sets/`.
2. Replace the mirror under `sets_en/`.
3. Update `data/config.json` if the count, file name, or display order changes.
4. Bump `APP_DATA_VERSION` in `index.html` and `answers.html`.
5. Validate JSON before deploying.

## Deploy

The standalone GitHub repo uses `.github/workflows/pages.yml` to publish the repository root to GitHub Pages on every push to `main`.
