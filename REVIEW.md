# Text review log

## Current status

The supplied file, **Dua Al-Qunut - Abdallah Muhammad Al Matrood**, is a 22-page typed (not handwritten) document, image-scanned but clearly legible throughout. Its colophon reads "Transliterated: Muhammad Sadat, Monday, November 26, 2012" — this is Mohammed Sadat Abdulai's own transliteration, transcribed by ear from Shaykh al-Maṭrūd's actual recitation (not copied from a written source), and **the author has confirmed the wording is correct**.

The full text lives in `data.js`, one `{ar, lat, en, de, open}` object per recited line, grouped by original PDF page (`p. N` markers in the rendered page let every line be checked against the source). `lat` has been re-cast from the author's original ad-hoc phonetic spelling into the macron/ʿ-ʾ/il-ul-liaison scheme shared with al-Wird al-Laṭīf. `open` marks a line that opens a new invocation (bold in the PDF).

**What is verified:** the transliteration's wording and line order (author-confirmed).
**What is NOT yet verified:** the vocalized Arabic script and the English/German translations. These were reconstructed and translated with AI assistance, leaning on well-attested fixed texts (Qurʾān quotations, the Janāzah duʿā, known ḥadīth formulas) where the wording is recognizable, and on best-effort Classical Arabic reconstruction elsewhere. **Treat with suspicion until a qualified Arabic reader has checked them.**

### Author-confirmed intentional features (not errors — do not "fix")

- p.6, lines "Wa dahaa bi zumuuminaa" / "Wa zumuuminaa": the author confirms Shaykh al-Maṭrūd recited these as two distinct, near-rhyming phrases, not a duplicate. Reconstructed as a ḥadīth-style *hamm/ghamm* (anxiety/distress) pair: wa dhahāba humūminā / wa ghumūminā. Keep as two separate lines.
- More generally: the transliteration was taken down by ear from the live recitation, not from a written source. Where its phonetic spelling has a small quirk or an apparent near-repeat, the default is to treat it as an intentional recitation feature, not a typo — unless it is clearly a scanning/typing artifact.
- p.18: a small handwritten caret in the scan, near "Allaahummaj a⌃naa fee kulli harfin qara anaahu…", was read as an inserted "l" ("alnaa"); kept as transcribed.

### Source-verified corrections

The owner supplied a screenshot of an external reference source showing the correct Arabic for the start of p.1. Two corrections were made against it:

- p.1, line 1 ("Sodaqollahul azeemul lazee..."): was *al-Mutawaḥḥidu bi-l-Jalāli wa-l-Kamāli wa-l-Jamāli taʿaẓẓuman wa takabburā* (AI guess); corrected to *al-Mutawaḥḥidu bi-l-Jalāli, bi-kamāli-l-Jamāli, taʿẓīman wa takbīrā* per the source.
- p.1, line 3 ("Almuta aa lee bi azomatihee..."): was a paraphrase (*al-Mutaʿālī ...-lladhī anzala-l-Furqāna...*); corrected to the source's exact wording, which quotes **Qurʾān 25:1** directly: *al-Mutaʿālī bi-ʿaẓamatihi wa majdihi, tabāraka-lladhī nazzala-l-Furqāna ʿalā ʿabdihi li-yakūna li-l-ʿālamīna nadhīrā*.
- p.1, line 2 ("Almutafarridi bitasreefil...") was checked against the same source and found to already match exactly — no change needed.

This confirms the overall reconstruction approach is sound where it leans on recognizable fixed wording, but line-by-line checking against a real source beats AI reconstruction every time. If the owner can share more of this source (or where it's from), the rest of the flagged lines below should be checked against it before anything else.

### Arabic/translation lines flagged as least certain (first AI pass — needs a qualified reader)

These are best-effort reconstructions from the phonetic spelling, not drawn from a known fixed text. Everything else leans on recognizable Qurʾān verses, the Janāzah duʿā, or well-known ḥadīth formulas and is comparatively higher-confidence, but none of the Arabic has had a scholarly check yet.

- p.1: "Wanawwarannuura washa a sha a" (reconstructed as *wa anāra-n-nūra wa shāʾa mā shāʾ*) and "Wal ardo bisaaton rada a a" (*wa-l-arḍa bisāṭan farashahā* — "rada a a" is a guess at "farashahā").
- p.2: "Sodaqallaahul azeemullazee Azzafar tafa a" / "Wa alaa famtana a" (guessed as *aẓfara mani-ttaqā* / *ʿalā mani-mtuḥina* — low confidence); "Wa ala maa waajisas suduur" (*wa ʿalima wasāwisa-ṣ-ṣudūr*); "Walaa natliku diseeyatihish shadaa ilus silaab" (*wa lā nuṭīqu shiddata sulṭānih* — loose paraphrase); "Wa zalla kulla shay in li azomatihi wafado a" (second clause guessed as *wa khaḍaʿ*).
- p.3: "Alkareemullazee mannabika nafihee…" and "Al Qayyuumullazee laa yanfa u walaa yanaa" (ending reconstructed, uncertain); "Laka khado an man sajada wazalla man wajad" (second clause uncertain).
- p.4: "Allaahuma qaḍji inaaka bijam inaa mutawas sineen", "Wabizaa bika laa izeen", "Wa anaa a ataabika saa ineen" (all loosely reconstructed); "Wa amalanaa manfuuraa" (assumed close to "mashkūrā", may be a distinct word); "Walqadru khayru baytin" (assumed "wa-l-qabru", d/b transcription).
- p.9: "Irhamhu duu anaa" (guessed as *irḥam ḍuʿfanā*).
- p.10: "Ghayra fazaayaa walaa maftuuneen" (moderate confidence: *ghayra khazāyā wa lā maftūnīn*).
- p.11: "Allaahumaj al sa aranaa alaa man zolamanaa" ("sa aranaa" guessed as *thaʾranā*, "revenge").
- p.12: "Allaahummaj alijtimaa anaa feehaa zihillaylatiiti maa ammar huumaa" and "Wa tafarruqanaa tafarruqan maa suumaa" (heavily reconstructed, low confidence); "Wa hablanaa ginan laayukzeenaa" ("yukzeenaa" guessed as *yuṭghīnā*).
- p.14: "Harrarnaa hatmata kitaabik" (guessed as referring to finishing a Qurʾān recitation).
- p.15: "Manlanaa izaa qarattanaa min baabik" ("qarattanaa" guessed as *ṭuridnā*, "driven away").
- p.16: the six "Allaahummarham ___anaa" lines — "do afanaa" (confident: *ḍuʿafāʾanā*, "our weak ones") but "fushuu anaa", "tadorru anaa" and especially "binaa batanaa" are lower-confidence guesses (*fazaʿanā* / *taḍarruʿanā* / *maskanatanā*).
- p.17: "Wa yaa saabi kal fawt" (nuance of *Sābiqa-l-fawt* uncertain).
- p.18: "Wa habil musee yeena minnaa lil Muslimeen" (moderate confidence).
- p.19: "Allaahumma agifkuluubanaa bil ilmi walyakeen" (reconstructed as *aqdhif*, "cast into").
- p.20: "Allaahumma khuzbi aydeenaa…" and "Wa ahli killaahumma man abraḍohum" (both moderate-to-low confidence).
- p.20–21: "Allaahumma qayyibu khawaa qiranaa…" (reconstructed as *qayyiḍ lanā khiyāranā*, "appoint for us our best people" — moderate confidence).
- p.21: "Wa qawwiril laahumma fil khayri…" (reconstructed as *qarriri*, "establish"); "Allaahumma wassik tolabatal ilmi…" ("wassik" reconstructed as *waffiq*, "grant success").

## Review workflow

- [x] Preserve the original PDF as the reference source in the project archive.
- [x] Transcribe each page, keeping page boundaries for checking.
- [x] Compare every line with the PDF image (the transliteration's wording is author-verified).
- [x] Re-cast the transliteration into the shared academic scheme (macrons, ʿ/ʾ, il-/ul- liaison).
- [x] Add vocalized Arabic script for every line (AI-assisted first pass — see flagged lines above).
- [x] Add English and German translations for every line (AI-assisted first pass).
- [ ] Have the Arabic script checked, line by line, by a qualified Arabic reader — start with the lines flagged above.
- [ ] Have the English/German translations checked once the Arabic is settled.
- [ ] Write Hausa and Dagbanli translations (not started).
- [ ] Generate a print-friendly PDF once the Arabic and translations have been reviewed.

## Important distinction

Treat the transliteration's wording as settled (author-verified) and do not change it without the owner's say-so. Treat the Arabic script and the EN/DE translations as an unproofread first pass: do not present them as more certain than they are, and record doubts here rather than silently "fixing" them.
