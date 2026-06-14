# SGBD MCQ Practice

Static MCQ website for SGBD / PL SQL database practice.

This folder is a copy of the latest Data Structures MCQ website shell, stripped down to one active SGBD question set.

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
- `materials.html`: placeholder materials page for future PDFs or notes.
- `data/config.json`: active set registry and UI metadata.
- `data/website.json`: startup metadata required by the current app shell.
- `sets/sgbd_uploaded_master.json`: current/default SGBD question set.
- `sets_en/sgbd_uploaded_master.json`: English mirror. The source set is already English, so this currently matches `sets/`.

## Current Set

Source:

```text
C:\Users\fgghk\Downloads\SGBD_UPLOADED_SETS_FIXED_ENGLISH_PACK\SGBD_UPLOADED_SETS_FIXED_ENGLISH\03_TRANSLATED_DEDUPED_MASTER\sgbd_uploaded_fixed_deduplicated_master_plain_en.json
```

Count:

- `sgbd_uploaded_master`: 168 questions
- 96 single-correct questions
- 72 multi-correct questions

The source is already English. The current first version mirrors the same JSON in both `sets/` and `sets_en/`, and the app defaults to English.

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

1. Replace `sets/sgbd_uploaded_master.json`.
2. Replace `sets_en/sgbd_uploaded_master.json`.
3. Update `data/config.json` if the count or file name changes.
4. Bump `APP_DATA_VERSION` in `index.html` and `answers.html`.
5. Validate JSON before deploying.

## Deploy

This repo uses `.github/workflows/pages.yml` to publish the repository root to GitHub Pages on every push to `main`.
