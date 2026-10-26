# Duʿāʾ al-Qunūt · ʿAbdallāh Muḥammad al-Maṭrūd

An open, phone-first reading edition of the qunūt text prepared by Mohammed Sadat Abdulai.

**Website:** https://masssly.github.io/qunut-matrood/

## Project goals

- A comfortable mobile reading experience.
- A verified transcription of the supplied 22-page PDF (the author's own 2012 transliteration), with Arabic script, transliteration, and English/German translations as separate, clearly labelled layers.
- Adjustable text size, and toggles for which layers to show.
- A downloadable, print-friendly edition once the Arabic and translations have been checked.
- A static website that can be hosted free on GitHub Pages.

## Editorial status

The supplied PDF is a 22-page typed document: Mohammed Sadat Abdulai's own 2012 Latin-script transliteration of the qunūt, not a third-party source, and the wording has been **verified by the author**. It has been transcribed line by line into `data.js`, re-cast into the same academic transliteration scheme (macrons, ʿayn/hamza, il-/ul- liaison) used by the companion [al-Wird al-Laṭīf](https://masssly.github.io/wird-al-latif/) edition.

Vocalized Arabic script and English/German translations have since been added for every line, reconstructed and translated with AI assistance. **These have not yet been checked by a qualified Arabic reader** — see [REVIEW.md](REVIEW.md) for the specific lines flagged as least certain. Hausa and Dagbanli translations are planned but not yet written. Do not silently correct or complete uncertain Arabic or wording — record doubts in REVIEW.md instead.

## Development

The site is plain HTML, CSS, and JavaScript; no build step or paid service is required. All text lives in `data.js` (one `{ar, lat, en, de, open}` object per recited line, grouped by original PDF page) — edit that file to correct a line, not `index.html`'s rendering of it.

## Publishing

The GitHub Actions workflow in `.github/workflows/pages.yml` publishes the repository root to GitHub Pages on pushes to `main`. The expected URL is:

https://masssly.github.io/qunut-matrood/

If Pages has not previously been enabled for the repository, the workflow attempts to enable it using the GitHub Pages Actions deployment source.

## Credits

Prepared by Mohammed Sadat Abdulai. This project is an independent reading edition; source wording will be preserved carefully and uncertainties documented rather than guessed.
