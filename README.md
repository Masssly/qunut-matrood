# Duʿāʾ al-Qunūt · ʿAbdallāh Muḥammad al-Maṭrūd

An open, phone-first reading edition of the qunūt text prepared by Mohammed Sadat Abdulai.

**Website:** https://masssly.github.io/qunut-matrood/

## Project goals

- A comfortable mobile reading experience.
- A carefully checked transcription of the supplied 22-page PDF (the author's own 2012 transliteration).
- Clear separation between the source text, transcription, editorial notes, transliteration, and any future translation.
- Adjustable text size and a downloadable, print-friendly edition once the text has been checked.
- A static website that can be hosted free on GitHub Pages.

## Editorial status

The supplied PDF is a 22-page typed document: Mohammed Sadat Abdulai's own 2012 Latin-script transliteration of the qunūt, not a third-party source. It has been transcribed line by line into `index.html` (page markers included for checking), but that transcription has had only one reading pass against the original pages, not a second proofread. Arabic script has not been added. Do not silently correct or complete uncertain transliteration or wording. See [REVIEW.md](REVIEW.md).

## Development

The site is plain HTML, CSS, and JavaScript; no build step or paid service is required.

## Publishing

The GitHub Actions workflow in `.github/workflows/pages.yml` publishes the repository root to GitHub Pages on pushes to `main`. The expected URL is:

https://masssly.github.io/qunut-matrood/

If Pages has not previously been enabled for the repository, the workflow attempts to enable it using the GitHub Pages Actions deployment source.

## Credits

Prepared by Mohammed Sadat Abdulai. This project is an independent reading edition; source wording will be preserved carefully and uncertainties documented rather than guessed.
