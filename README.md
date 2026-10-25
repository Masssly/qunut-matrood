# Duʿāʾ al-Qunūt · ʿAbdallāh Muḥammad al-Maṭrūd

An open, phone-first reading edition of the qunūt text prepared by Mohammed Sadat Abdulai.

## Project goals

- A comfortable mobile reading experience.
- A carefully checked transcription of the supplied 22-page PDF.
- Clear separation between the source text, transcription, editorial notes, transliteration, and any future translation.
- Adjustable text size and a downloadable, print-friendly edition once the text has been checked.
- A static website that can be hosted free on GitHub Pages.

## Editorial status

The supplied PDF is image-based and its text has not yet been reliably extracted. The transcription must be checked page by page before it is presented as authoritative. Do not silently correct or complete uncertain Arabic, transliteration, or wording. See [REVIEW.md](REVIEW.md).

## Development

The site is plain HTML, CSS, and JavaScript; no build step or paid service is required.

## Publishing

The GitHub Actions workflow in `.github/workflows/pages.yml` publishes the repository root to GitHub Pages on pushes to `main`. The expected URL is:

https://masssly.github.io/qunut-matrood/

If Pages has not previously been enabled for the repository, the workflow attempts to enable it using the GitHub Pages Actions deployment source.

## Credits

Prepared by Mohammed Sadat Abdulai. This project is an independent reading edition; source wording will be preserved carefully and uncertainties documented rather than guessed.
