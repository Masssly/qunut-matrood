# Text review log

## Current status

The supplied file, **Dua Al-Qunut - Abdallah Muhammad Al Matrood**, is a 22-page typed (not handwritten) document, image-scanned but clearly legible throughout. Its colophon reads "Transliterated: Muhammad Sadat, Monday, November 26, 2012" — this is Mohammed Sadat Abdulai's own transliteration, not an unverified third-party text.

The full text has been transcribed line by line into the `PAGES` array in `index.html`, in original page order, with a `p. N` marker before each page's lines so every line can be checked against the source PDF page. Bold lines in the PDF (each new "Allaahumma…" invocation) are marked in the data with a leading `§` and rendered bold.

This is a **first transcription pass only** — read once, carefully, against each page, but not yet cross-checked a second time. The website says so in the "First transcription pass" note.

### Known rough spots from the first pass

- p.6: "Wa dahaa bi zumuuminaa" / "Wa zumuuminaa" are two distinct lines in the PDF that transliterate almost identically — worth a close look against the scan.
- p.18: "Allaahummaj a[handwritten caret]naa fee kulli harfin qara anaahu…" had a small handwritten insertion mark in the scan; transcribed as "alnaa" per the apparent correction.
- The underdot emphatic letters (ḍ ṣ ṭ ẓ) are reproduced where they were visible in the scan, but are not marked with full consistency by the original 2012 document itself — don't "fix" apparent inconsistencies without checking the actual page image.

## Review workflow

- [x] Preserve the original PDF as the reference source in the project archive.
- [x] Transcribe each page, keeping page boundaries for checking.
- [ ] Compare every line with the PDF image a second time.
- [ ] Mark uncertain words instead of guessing.
- [ ] Decide whether the reading text should be Arabic script, the supplied Latin-script transliteration, or both.
- [ ] If Arabic script is added, have it checked by a competent Arabic reader.
- [ ] Keep any translation as a separate, clearly attributed layer.
- [ ] Generate a print-friendly PDF only after the text has been reviewed.

## Important distinction

Treat the supplied document as the primary source for transcription. Do not silently change its wording based on a guess. Record uncertain readings and resolve them explicitly during review.
