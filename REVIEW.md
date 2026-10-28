# Text review log

## Current status

The supplied file, **Dua Al-Qunut - Abdallah Muhammad Al Matrood**, is a 22-page typed (not handwritten) document, image-scanned but clearly legible throughout. Its colophon reads "Transliterated: Muhammad Sadat, Monday, November 26, 2012" — this is Mohammed Sadat Abdulai's own transliteration, transcribed by ear from Shaykh al-Maṭrūd's actual recitation (not copied from a written source), and **the author has confirmed the wording is correct**.

The full text lives in `data.js`, one `{ar, lat, en, de, open}` object per recited line, grouped by original PDF page (`p. N` markers in the rendered page let every line be checked against the source). `lat` has been re-cast from the author's original ad-hoc phonetic spelling into the macron/ʿ-ʾ/il-ul-liaison scheme shared with al-Wird al-Laṭīf. `open` marks a line that opens a new invocation (bold in the PDF).

**What is verified:** the transliteration's wording and line order (author-confirmed), plus the Arabic for most of the text, now checked against either a hand-typed reference source (p.1) or a full auto-caption (ASR) transcript of the actual recitation video (all 22 pages — see below).
**What is NOT yet verified by a human who reads Arabic:** even where the Arabic has been checked against the audio, that check was done by AI alignment against noisy auto-captions, not by a qualified reader. Two lines remain genuinely unresolved (p.3, p.19 — see below). **Treat all of it as a careful, source-backed draft, not a final text, until a qualified Arabic reader has checked it.**

### Author-confirmed intentional features (not errors — do not "fix")

- p.6, lines "Wa dahaa bi zumuuminaa" / "Wa zumuuminaa": the author confirms Shaykh al-Maṭrūd recited these as two distinct, near-rhyming phrases, not a duplicate. Reconstructed as a ḥadīth-style *hamm/ghamm* (anxiety/distress) pair: wa dhahāba humūminā / wa ghumūminā. Keep as two separate lines.
- More generally: the transliteration was taken down by ear from the live recitation, not from a written source. Where its phonetic spelling has a small quirk or an apparent near-repeat, the default is to treat it as an intentional recitation feature, not a typo — unless it is clearly a scanning/typing artifact.
- p.18: a small handwritten caret in the scan, near "Allaahummaj a⌃naa fee kulli harfin qara anaahu…", was read as an inserted "l" ("alnaa"); kept as transcribed.

### Source-verified corrections

The owner supplied a screenshot of an external reference source showing the correct Arabic for the start of p.1. Two corrections were made against it:

- p.1, line 1 ("Sodaqollahul azeemul lazee..."): was *al-Mutawaḥḥidu bi-l-Jalāli wa-l-Kamāli wa-l-Jamāli taʿaẓẓuman wa takabburā* (AI guess); corrected to *al-Mutawaḥḥidu bi-l-Jalāli, bi-kamāli-l-Jamāli, taʿẓīman wa takbīrā* per the source.
- p.1, line 3 ("Almuta aa lee bi azomatihee..."): was a paraphrase (*al-Mutaʿālī ...-lladhī anzala-l-Furqāna...*); corrected to the source's exact wording, which quotes **Qurʾān 25:1** directly: *al-Mutaʿālī bi-ʿaẓamatihi wa majdihi, tabāraka-lladhī nazzala-l-Furqāna ʿalā ʿabdihi li-yakūna li-l-ʿālamīna nadhīrā*.
- p.1, line 2 ("Almutafarridi bitasreefil...") was checked against the same source and found to already match exactly — no change needed.

A second round from the owner covered p.1 lines 4–7 ("Wasodaqa Rasuulahuu...", "Allazee arsalahul laahu...", "Wadaa iyan ilallaahi...", "Sodaqallaahul haqqul azeemullazee nazzalal Qur aanal kareema..."): all four already matched the source exactly, word for word. The only addition was noting that "Wadaa iyan ilallaahi bi iznihee wasiraajan muneeraa" is itself a direct quote of **Qurʾān 33:46**, which the source marks with a citation — added to the EN/DE text.

A third round covered p.1 lines 8–11 and p.2 lines 1–2. This one found real corrections, including two that resolve lines previously flagged below as uncertain:
- p.1, "Wanawwarannuura washa a sha a" (**previously flagged** as uncertain): was *wa anāra-n-nūra wa shāʾa mā shāʾ* (AI guess); corrected to *wa nawwara-n-nūra wa shaʿshaʿahu* ("and lit up the light, and made it shine resplendently") per the source. Flag removed below.
- p.1, "Wal ardo bisaaton rada a a" (**previously flagged** as uncertain): was *wa-l-arḍa bisāṭan farashahā* ("spread it out", AI guess); corrected to *wa-l-arḍa bisāṭan waḍaʿahu* ("laid it down") per the source. Flag removed below.
- p.1, "Sodaqallaahul haqqul azeemullazee sanna ddeena washara a": minor fix, *wa sharaʿ* → *wa sharaʿahu* (object pronoun restored).
- p.1, "Walaa ilaaha illaahuwa ja alas samaa a...": minor fix, the closing pronoun is *rafaʿahu* (referring to the roof/ceiling, masculine), not *rafaʿahā*.
- p.2, "Wa ala maa waajisas suduur": was *wa ʿalima wasāwisa-ṣ-ṣudūr* ("knew the whispers of hearts", AI guess); corrected to *wa ʿalima hājisa-ṣ-ṣudūr* ("knew the innermost thoughts of hearts") per the source.
- p.2, "Sodaqallaahul azeemullazee Dabbarad duhuura..." and "Wa anzalal Qur aana hudan wanuur": checked against the source and already matched exactly — no change.

This confirms the overall reconstruction approach is sound where it leans on recognizable fixed wording, but line-by-line checking against a real source beats AI reconstruction every time.

### Full-text pass against YouTube auto-captions (ASR) of the recitation video

The owner found and confirmed the recitation video itself: YouTube id `DBngjJNK_nQ`, "Duaa Abdullah Al-Matrood", ~25 minutes, description "Abdullah Al Matrood complete Dua" — and pasted a full auto-caption (ASR) transcript of it into the conversation. This is the first time the *entire* text had a real source to check against, not just page 1.

**Method:** the ASR transcript is continuous, unvocalized, has no line breaks, and is noisy in predictable ways (dropped short/formulaic words, merged or split words, near-homophone substitutions like ه/خ, ق/ط, ف/ث, ز/ذ, ص/س). It was aligned word-by-word against all 343 existing lines in order. Where it agreed with the existing text, that was treated as confirmation. Where it disagreed with a line already confirmed against the owner's hand-typed source (p.1, lines 1–11), the hand-typed source won — ASR noise doesn't override a cleaner source. Everywhere else, a clear, repeated ASR disagreement that also made better grammatical or rhyme sense than the prior AI guess was treated as a real correction.

**Real corrections made** (Arabic, transliteration, and EN/DE updated together):
- p.2: "Azzafar tafa a" / "Wa alaa famtana a" → *ʿazza fa-rtafaʿa* / *wa ʿalā fa-mtanaʿa* ("is mighty, and so exalted" / "is high, and so unattainable") — was a low-confidence guess, now replaced.
- p.2: "Walaa natliku diseeyatihish shadaa ilus silaab" → *wa lānat li-qudsiyyatihi-sh-shadāʾidu-ṣ-ṣilāb* ("the hardest hardships softened before His holiness") — also now fits the page's "-āb" rhyme scheme, which the old guess broke.
- p.3: "Al Qayyuumullazee laa yanfa u walaa yanaa" → *al-Qayyūmu-lladhī lā yaghfulu wa lā yanām* ("who never neglects and never sleeps") — a much better fit, echoing the Āyat al-Kursī idiom.
- p.4: "Wa manzallazee nas alu wa anntar rabbul ma aduud" → ends *...wa anta-r-Rabbu-l-Maʿbūd* ("the Lord who is worshipped"), not "Lord of the counted."
- p.4: "Allaahuma qaḍji inaaka bijam inaa mutawas sineen" / "Wabizaa bika laa izeen" / "Wa anaa a ataabika saa ineen" — all three were loose guesses; replaced with *Allāhumma qad jiʾnāka bi-jamʿinā mutawassilīn, wa bi-bābika lāʾidhīn, wa ʿalā aʿtābika sāʾilīn* ("O Allah, we have come to You together seeking intercession, seeking refuge at Your door, begging on Your thresholds").
- p.4: "Wakbal udwanaa..." → *wa-qbal ʿudhranā* ("accept our excuse"), not "our supplication"; "Wa amalanaa manfuuraa" → *wa ʿamalanā mawfūrā* ("our deeds abundant"), not "mashkūrā."
- p.8: "min deekin luhuudi wamaraati idduud" → *min ḍīqi-l-luḥūdi wa martaʿi-d-dūd* ("the narrowness of the graves and the haunt of worms"), not "bitterness of worms."
- p.8: "fee butuunil alhaadi" → *fī buṭūni-l-alḥādi* ("within the burial-niches"), not "the bowels of the earth."
- p.9: "Irhamhu duu anaa" → *irḥam khuḍūʿanā* ("have mercy on our humble submission"), not *ḍuʿfanā*.
- p.12: "Wa lā khayran illā dalaltanā ʿalayh" → *wa lā ḥayrāna illā dalaltahu* ("none bewildered except that You guided him") — fits the surrounding "man/thing + illā + verb-suffix" pattern much better than the old reading.
- p.14: "Harrarnaa hatmata kitaabik" → *ḥaḍarnā khatmata kitābik* ("we have been present at the completion of the recitation"), not *ḥarrarnā* ("we completed"). Also "taqabbal hādhihi minnā" → *taqabbalhā minnā* ("accept it from us") in both repeats.
- p.15: "Manlanaa izaa qarattanaa min baabik" → *idhā ṭaradtanā* ("if You drive us away"), and the following "laa taqrudinaa khaa ibeen" in the same stanza → *lā taṭrudnā* — this stanza specifically uses the "drive away" (ṭarada) root, distinct from the "turn away" (radda) refrain used elsewhere in the text.
- p.16: "fushuu anaa" → *khushūʿanā* ("our humility"), not *fazaʿanā*; "binaa batanaa" → *inābatanā* ("our penitent return"), not *maskanatanā*. The other four of the six "Allāhumma-rḥam ___anā" lines were already correct, confirmed by the ASR.
- p.18: "Wa habil musee yeena minnaa lil Muslimeen" → *li-l-muḥsinīn* ("to the good-doers"), not "to the Muslims" — the classical wrongdoer/good-doer (musīʾ/muḥsin) pairing, confirmed independently by the audio even though it conflicts with the original phonetic transliteration's spelling.
- p.20: "Wa ahli killaahumma man abraḍohum" → *wa ahliki Allāhumma man abghaḍahum* ("destroy, O Allah, whoever hates them"), not "be an enemy to."
- p.20–21: "Allaahumma qayyibu khawaa qiranaa binasratil Islaami..." (×2) → *Allāhumma ṭayyib khawāṭiranā bi-naṣrati-l-Islāmi wa-l-Muslimīn* ("O Allah, gladden our hearts with the triumph of Islam and the Muslims") — a known, common supplication; the old reading ("appoint for us our best people") was a weak guess.
- p.21: "Allaahumma aaminnaa fee waqninaa haazaa" → *fī waṭaninā hādhā* ("in this homeland of ours"), not "in this time of ours" — matches the very next line about "the rest of the Muslim lands."
- p.21: "Wa qawwiril laahumma fil khayri..." → *wa ṭawwili Allāhumma...* ("lengthen, O Allah, their lives in goodness"), not *qarriri* ("establish").
- A few minor, meaning-preserving corrections: p.6 "Aw ʿallamtahu" → *aʿlamtahu*; p.16 "unẓur ilaynā" → *unẓurnā*; p.20 "nashtāqu" → *ishtaqnā* (matching the parallel line on p.19).

**Confirmed correct, flags removed** (ASR matched the existing text, or matched it closely enough that the difference is clearly ASR noise, not a real variant): p.2 "khoda at li a zomatihir riqaab"; p.3 "Laka khado an man sajada..."; p.4 "Walqadru khayru baytin" (confirms *al-qabru*, not *al-qaṣru*); p.10 "Ghayra fazaayaa walaa maftuuneen"; p.11 "sa aranaa" (confirms *thaʾranā*); p.12 "ijtimaa anaa feehaa zihillaylatiiti..." and "tafarruqanaa tafarruqan..." (both matched exactly); p.12 "yukzeenaa" (confirms *yuṭghīnā*, matched exactly); p.16 "do afanaa" and "tadorru anaa" (both matched exactly); p.17 "Wa yaa saabi kal fawt"; p.20 "khuzbi aydeenaa..." (matched exactly); p.21 "wassik tolabatal ilmi..." (confirms *waffiq*, matched exactly).

**Still genuinely uncertain** (the ASR didn't clearly resolve these — needs a qualified reader, not another guess):
- p.3: "Alkareemullazee mannabika nafihee alaa man shaa a min ibaad" — the ASR rendering ("من بكلفه") doesn't clearly resolve to anything better than the existing guess (*manna bi-nafʿihi*, "bestowed His benefit").
- p.19: "Allaahumma agifkuluubanaa bil ilmi walyakeen" — the ASR rendering ("اغز قلوبنا") is itself unclear; existing guess (*aqdhif*, "cast into") kept pending better evidence.

Per REVIEW.md's own standing rule: where the ASR disagreed with a line already confirmed by the owner's hand-typed source (p.1 lines 1–11, and the p.6 "humūminā/ghumūminā" pair the owner separately confirmed as intentional), the hand-typed/owner-confirmed reading was kept unchanged — auto-captions are noisier than a human source and don't get to override one.

## Review workflow

- [x] Preserve the original PDF as the reference source in the project archive.
- [x] Transcribe each page, keeping page boundaries for checking.
- [x] Compare every line with the PDF image (the transliteration's wording is author-verified).
- [x] Re-cast the transliteration into the shared academic scheme (macrons, ʿ/ʾ, il-/ul- liaison).
- [x] Add vocalized Arabic script for every line (AI-assisted, now checked against the actual recitation audio via ASR — see above; 2 lines remain unresolved).
- [x] Add English and German translations for every line (AI-assisted, updated alongside each Arabic correction).
- [ ] Have the Arabic script checked, line by line, by a qualified Arabic reader — start with the 2 lines still flagged as genuinely uncertain (p.3, p.19).
- [ ] Have the English/German translations checked once the Arabic is settled.
- [ ] Write Hausa and Dagbanli translations (not started).
- [ ] Generate a print-friendly PDF once the Arabic and translations have been reviewed.

## Important distinction

Treat the transliteration's wording as settled (author-verified) and do not change it without the owner's say-so. Treat the Arabic script and the EN/DE translations as an unproofread first pass: do not present them as more certain than they are, and record doubts here rather than silently "fixing" them.

### Follow-up: comparison with the human-prepared on-screen Arabic (2026-10-28)

The owner supplied the video file and clarified that the Arabic shown on screen is believed to be human-prepared, while the pasted transcript was machine-generated. For now, where the on-screen reading is clear and makes good grammatical and contextual sense, it takes precedence over the noisy ASR transcript. This is a source-priority decision, not a claim that every on-screen word has been independently verified by an Arabic specialist.

**High-confidence changes made in `data.js`:**
- p.3: `يُنَادِيكَ` (*yunādīka*, “call upon You”) changed to `يُنَاجِيكَ` (*yunājīka*, “confide/address You intimately”), matching the on-screen text and improving the meaning of the rhetorical question. English and German were adjusted accordingly.
- p.4: `وَعَمَلَنَا مَوْفُورًا` (*mawfūrā*, “abundant”) changed to `وَعَمَلَنَا مَغْفُورًا` (*maghfūrā*, “forgiven”), matching the on-screen text and making the paired supplication coherent: accept our excuse, make our efforts appreciated, and forgive our deeds. The transliteration and both translations were updated. This supersedes the earlier ASR-based choice of *mawfūrā* recorded above; the conflict is now resolved in favor of the human-prepared on-screen reading.
- p.9: `الْأَسْرَاءُ` changed to `الْأَسْرَى` (*al-asrā*, “the captives”), matching the on-screen spelling and the intended phrase `الأسرى بين يديك`. The transliteration was updated.

**Still unresolved; do not change without further discussion:**
- p.3: the phrase around `مَنَّ بِنَفْعِهِ` / the alternative suggested by the supplied transcript. We need to inspect the on-screen Arabic closely and listen to the audio before choosing a reading.
- p.19: resolved in favor of the human-prepared on-screen reading `أَغِثْ قُلُوبَنَا بِالْعِلْمِ وَالْيَقِينِ`, which is now in `data.js`. English and German were updated to reflect the sense of bringing relief/help to our hearts through knowledge and certainty.
- Any other disagreement between the on-screen text, spoken wording, transliteration, and translations remains a review item until the evidence is clear.

No interface changes were made in this stage. The website and deployment workflow remain untouched.


### Follow-up: page 19 decision (2026-10-28)

Following review of the on-screen Arabic, the owner approved changing p.19 to `اللَّهُمَّ أَغِثْ قُلُوبَنَا بِالْعِلْمِ وَالْيَقِينِ`. The transliteration is now *Allāhumma aghith qulūbanā bi-l-ʿilmi wa-l-yaqīn*. English: “O Allah, bring our hearts relief through knowledge and certainty”; German: “O Allah, schenke unseren Herzen durch Wissen und Gewissheit Hilfe und Stärkung.” Page 3 remains unchanged pending explicit resolution of its disputed word; the owner notes that the audio sounds clear to them, but the exact reading has not yet been documented in this review log.
