# AI Writing Tells — Research for the "Never Sound Like AI" Style Guide

**Purpose:** Eliminate AI-sounding patterns from Arabic social copy (LinkedIn + Facebook; Egyptian colloquial Arabic with English tech terms inline; no emojis; no tashkeel).
**Compiled:** 2026-10-09 · **Method:** live web research (DuckDuckGo/Brave/Bing + direct fetches + r.jina.ai; Playwright Chromium for blocked pages). Every claim carries a source ID that maps to §7 References. Items I could not fetch are explicitly marked **UNVERIFIED**.
**Verification rule used:** primary source fetched = "verified"; summaries/paraphrases of paywalled items fetched from a secondary outlet = "verified (secondary)"; everything else = marked.

---

## 0. Executive summary

- AI-ness is **density of patterns + emptiness of substance**, not any single word. "No single sign convicts — three or four signs failing at once in the same passage is the fingerprint" [S2].
- On LinkedIn specifically, templated turns **measurably cost reach** and generic substance costs far more: posts with no concrete detail / no lived experience sat **23% below the author's own average** (since late Jul 2026), while a concrete detail went **+14%** and a lived experience **+25%** [S7].
- LinkedIn now officially flags "AI slop": internal classifiers "correctly identifying generic content 94% of the time"; a "Seems like AI slop" report option rolled out (Jul 30, 2026) [S7][S10].
- Arabic AI text has its own documented fingerprint: MSA-formal, connector-chained (علاوة على ذلك…), symmetric, hedge-heavy, zero-specifics prose, plus a recognizable phrase list §3 [S21][S24][S25][S26][S27].
- The worst thing you can do is "de-slop" by hunting detector scores — detectors are unreliable both ways (61% false-positive rate on non-native English writers in a Stanford study; OpenAI killed its own classifier at 26% detection / 9% false positives) [S24][S15]. Fix **substance and voice**, not detector scores.

---

## 1. General / English AI tells (what makes text read as ChatGPT)

Numbered tells below; each with example + source. (E = example.)

### 1a. Vocabulary tells

1. **AI vocabulary density.** A specific register of "style words" exploded post-2022: *delve, tapestry, testament, underscore (v.), pivotal, landscape (abstract), robust, showcase, vibrant, meticulous, intricate/intricacies, interplay, garner, bolster, foster, enhance, crucial, valuable, enduring, aligns with, boasts, deep dive*. One per post = nothing; a **cluster** is the tell. Measured: *delves* at ~25× pre-ChatGPT rate; *showcasing/underscores* ~9×; ≥10% (up to 30% in some fields) of 2024 PubMed abstracts LLM-assisted [S1][S2][S3]. — E: "Let's delve into the intricate tapestry of the AI landscape."
2. **Tiered ban list** (Tier 1 "kill on sight", 28 words): *delve, utilize, leverage, facilitate, elucidate, embark, endeavor, encompass, multifaceted, tapestry, testament, paradigm, synergy, holistic, catalyze, juxtapose, realm, myriad, plethora, underscore, galvanize, epitomize, unravel, supercharge, spearhead, catapult, conceptualize* — "they travel in packs… a room full of words all wearing the same suit" [S3].
3. **Corporate verb inflation:** *utilize/facilitate/streamline/leverage* where *use/help/tidy/use* would do; more than one per ~300 words = inflation not vocabulary [S2]. — E: "This robust framework empowers teams to streamline their workflow" → "This framework cuts the steps from nine to four" [S4].
4. **Hollow "big" adjectives:** *crucial, paramount, vital, essential, comprehensive, dynamic, seamless, innovative* — "when everything is crucial, nothing is" [S5][S20]. — E: "a comprehensive, seamless, robust solution."
5. **Empty adverbs as texture:** *just, literally, honestly, simply, actually, truly, fundamentally* sprinkled, not spoken [S4].
6. **Synonym cycling (elegant variation):** the agent → the assistant → the tool → the system, all the same thing; humans repeat the clear word [S4][S1].

### 1b. Sentence- and structure-level tells

7. **Negative parallelism / binary contrast — "It's not X, it's Y" / "Not only… but also" / "not just…, but…"** The single most common AI structure ("negate-then-reframe pivot"). On LinkedIn it costs **-4.9% reach** within an author's own baseline (and -5.1% on 2025 posts alone) [S1][S4][S5][S7]. — E: "That's not a branding question. That's a system question." / "This isn't about writing faster. It's about writing better."
8. **Negative listing (louder cousin):** "Not a tool. Not a platform. A movement." [S4].
9. **Rule of three on autopilot:** adjective-adjective-adjective / phrase-phrase-phrase triplets everywhere — "clear, concise, and compelling", "plan, execute, optimize". Humans use them occasionally; AI runs "more than one polished triplet per 200 words" [S1][S2][S5]. — E: "efficient, scalable, and reliable."
10. **Trailing "-ing" pseudo-analysis:** sentences ending in a participle that pretends to explain significance: "…, highlighting the team's commitment", "…, underscoring the importance", "…, showcasing", "…, reflecting broader trends", "…, contributing to". These "never contain information" [S1][S4]. — E: "The update adds offline mode, showcasing the company's user-first philosophy" → "…, so the app works on the subway."
11. **Copula avoidance / fake-strong verbs:** *serves as / stands as / functions as / represents / boasts / features* where *is / has* belongs. Measured: >10% drop in "is/are" in academic writing in 2023, with no prior trend [S1][S4]. — E: "Gallery 825 serves as LAA's exhibition space" (was "is").
12. **Uniform sentence length (low burstiness):** every sentence lands in the same 15-20-word band. Formula: stdev ÷ mean of sentence lengths; human ≈ **0.6-1.2**, model output clusters ≈ **0.2-0.4** (GPTZero methodology); a stdev <5 words across 20+ sentences is unusual [S2][S21][S25]. — "AI writing is a metronome" [S2].
13. **Symmetrical paragraphs / stacked one-liners:** every paragraph exactly 3-4 sentences, or the "one sentence per line with blank lines" LinkedIn silhouette — **91% of 500 analyzed AI LinkedIn posts** used one-sentence-per-line formatting, and **82% used just three opening structures** [S8][S21]. — "does the post look like a list of captions, or like someone wrote paragraphs?" [S8].
14. **Transition-word stacking:** paragraphs opening with *Furthermore / Moreover / Additionally / Ultimately*. On 29,000 popular LinkedIn posts, essentially nobody opens a line with "Furthermore" — "it is not a person with an unusual style. It is AI that nobody cleaned up" [S7][S2][S21].
15. **Hedged seesaw:** "While X, it is important to consider Y", "can potentially help to", "there are valid perspectives on both sides". AI "rarely takes a strong position" [S5][S21][S25].
16. **Restating the question before answering it** [S21][S25].
17. **Rhetorical setups / self-answered questions / colon reveals / dramatic fragmentation:** "What if I told you…?", "Think about it:", "The result?", "The catch: nobody reads it.", "That's it. That's the whole thing." Every third paragraph ending in a colon reveal is "the rhythm… the tell" [S4]. "The result?" cliffhanger costs **-4.8% reach** on LinkedIn and "Stop X, start Y" / "the key is" costs **-6.7%** (firmest number in that dataset) [S7].
18. **Throat-clearing openers and faux-insight setups:** "Here's the thing", "Let me be clear", "It's worth noting", "Here's what nobody tells you", "The part everyone misses", "Here's what most people get wrong". "Here's what/how" openers cost **-4.3% reach**; "It's worth noting that" is a "dead giveaway" (0% of top-100 creators as a habit) [S4][S7][S8].
19. **Empty-opener clichés:** "In today's fast-paced world", "In the digital age", "In a world where", "Picture this" — "a human editor deletes the first one on sight and a model produces them as a default" [S2][S5][S20].
20. **Fake authority / weasel attribution:** "Studies show", "Experts agree", "Industry reports", "Observers have cited", "widely regarded as" — uncited authority claims >50% of the time is the tell; name the study or cut the claim [S1][S2][S4].

### 1c. Content-level tells

21. **Importance puffery / undue emphasis on significance:** "marks a pivotal moment", "stands as a testament", "plays a vital role", "solidifies its position", "reflects broader trends", "key turning point", "evolving landscape", "leaves an indelible mark" [S1][S4]. — E: "The launch marks a pivotal moment for the company" → "The launch is the company's first paid product."
22. **Outline-like "Challenges"/"Future" endings:** "Despite its [positives], X faces several challenges…" ending in vague optimism, or a "Future Prospects" section — the rigid formula is the tell [S1].
23. **Fake-profound kicker / pseudo-wisdom:** "In the end, the best prompt is the one you never have to write." "The key is to find balance." "True growth comes from within." Delete-and-replace test: remove the sentence; if the paragraph loses zero information it was filler [S1][S2][S4].
24. **Summary-recap endings:** "In conclusion…", "Ultimately…", a closing paragraph restating what was just read — end on the last thing that is actually new [S4][S5][S21].
25. **Substance vacuum (the strongest single tell):** after reading a paragraph you cannot restate one concrete thing — no name, number, date, cause, trade-off. "AI text is engineered to sound informative while committing to nothing"; if >half the paragraphs fail the restatement test, it's substance-poor [S2]. Measured on LinkedIn: absence of a checkable detail/lived experience = **-23%** reach [S7].
26. **Generic CTA closer:** "What do you think? Drop a comment below" — invites affirmation, not experience; posts with friction (a question requiring real experience) get **4-6× more comments per impression** [S8].
27. **"Let that sink in" / "Read that again" / "I used to believe…" confessional openers:** frequency anomalies — "Let that sink in" at **28×**, "Read that again" at **22×** the normal rate; "Here's the thing" appeared **170 times across 500 AI posts (~1 in 3)** vs ~1 per 50 articles in normal professional writing [S8].

### 1d. Formatting tells

28. **Bold-colon bullet format** ("**Clarity:** We believe…"), over-bolding in "key takeaways" style, **emoji bullets/headings**, a header for every two-sentence section [S1][S19][S4].
29. **Emoji placement oddity / tone familiarity:** unusual or over-optimized emoji use and "highly polished, neutral tone" flagged by readers as AI signs (Bloomberg story) [S13].
30. **Punctuation drumbeat:** em dash density in short modern prose. Data: LinkedIn posts containing an em dash went **<2% (pre-AI) → 15.6% (2025) → 10.4% (2026)**; top creators keep it to ~3% of posts [S7]. Measured prose: GPT-4.1 ≈ 10.62 em dashes per 1,000 words vs a 3.23 matched human baseline; threshold where detectors start counting: **>20 per 1,000 words** [S2]. Note: **not proof on its own** — Mark Twain scores 10.13/1,000 [S2]. Also flagged in Arabic press as "excessive punctuation marks" [S23].
31. **Markdown/format leakage:** title case headings, curly quotes, bold sprinkled mid-sentence, tables where prose belongs [S1][S19].

### 1e. Platform & scale facts (LinkedIn)

- **Scale of the problem:** 81.2% of 5,000 long-form (100+ word) public LinkedIn posts sampled in July 2026 were classified "Likely AI" (up from ~half in late 2024) [S10]; Pangram's detector study flagged **41% of longform LinkedIn posts as fully AI-generated** (30% short-form), LinkedIn the most AI-saturated major platform [S11][S12].
- **Audience effect:** AI posts got **45% less engagement** than human posts across 2,726 posts (2022-2024); human posts outperformed AI by +80% in Innovation & Strategy, +73% in Marketing & Branding; the exception: Leadership & Inspiration, where AI posts *outperformed* by +75% (motivational register fits there) [S8]. Low-polish posts (1-3/10) averaged 2.1% engagement vs high-polish (8-10) at 0.4% — "Rough beats smooth" [S8].
- **Account-level cost:** views -50%, engagement -25%, follower growth -59% year-over-year in van der Blom's Algorithm Insights 2025 report, "generic AI content named as a substantial driver" [S8].
- **LinkedIn's official stance:** (May 2026, per S7) LinkedIn VP/Executive Editor Laura Lorenzetti's post "Keeping conversations real on LinkedIn": "It's ok to use AI to help you write, but your posts and comments need to represent your voice and your perspectives"; systems separate content that "adds perspective, context, or expertise" from what "feels generic or repetitive, even if it appears polished on the surface" — generic content is "less likely to be widely distributed"; "we're correctly identifying generic content 94% of the time"; Jul 30, 2026: classifiers + a "Seems like AI slop" report option [S7][S10].
- **Mechanism:** LinkedIn says it doesn't penalize AI authorship as a category; it suppresses posts that fail to hold attention (low dwell time, weak comments/reshares). Classifiers score content at creation time (~200ms); repeated low-dwell posts build "behavioral debt" that lowers an account's predicted engagement for *future* posts (360Brew recommender) [S8][S9].
- **Do NOT strip these** (they look "LinkedIn-y" but do not hurt reach, some help): a genuine closing question (98% of top creators use it), a P.S./CTA (+5.9% in 2025, neutral since), real candor/vulnerability like "Let's be honest" followed by something actually honest (+4.6%) [S7].

### 1f. What is NOT evidence of AI (avoid overcorrecting)

- Perfect grammar; mixing casual and formal registers; "clinical + emotional" tone; "bland/robotic" feel; formal or academic prose *in itself*; transition words in isolation; unsourced content [S1].
- Detectors: 61% false-positive rate on essays by non-native English writers (Stanford study in *Patterns*); OpenAI's own classifier was retired at 26% detection / 9% false positives; Substack's detector flagged pre-AI text and flipped verdicts on a two-word edit [S24][S15].
- Practical conclusion: audit **writing quality + substance**, not "detector score" [S2][S26].

---

## 2. AI tells in social/tech posts — condensed "top 12" (for the style guide header)

1. "It's not X, it's Y" / negative parallelism (-4.9% reach).
2. Rule-of-three triplets everywhere.
3. "Here's how/what…" promise openers (-4.3%).
4. "The result?" / "Stop X, start Y" / "the key is" templates (-4.8% / -6.7%).
5. Moreover/Furthermore/Additionally paragraph starts — "dead giveaway".
6. Trailing "-ing" significance clauses (…مما يعكس / highlighting…).
7. Importance puffery: pivotal moment / testament / vital role.
8. Copula avoidance: serves as / stands as / represents instead of is.
9. Em dash drumbeat (>20/1,000 words in short prose; LinkedIn em-dash usage 15.6% in 2025).
10. Uniform sentence length (burstiness < 0.4) + symmetric paragraphs / one-line-per-sentence stacks (91% of AI posts).
11. Zero specifics: no names, numbers, dates, or lived experience (-23% reach); generic "drop a comment" CTA.
12. Hedging seesaw + fake authority ("studies show", "experts agree") + "In conclusion" recap endings.

---

## 3. Arabic AI tells

**Method note:** Arabic-native sources were found and fetched (S21-S29). One widely-shared listicle exists only as a machine translation on LinkedIn ("تمت ترجمة هذا المقال آليًا" [S30]) — its Arabic renderings are indicative only; phrases below marked **[MT]** come from it and were kept only when they overlap native Arabic sources or map to the well-documented English equivalents. Pangram's Arabic page [S22] similarly presents translated counts of English phrases (e.g. «بصفتي نموذج لغة ذكاء اصطناعي…» = 294,000 hits [S22]).

### 3a. Arabic AI phrase blacklist (documented in Arabic sources)

| Arabic phrase | Why it reads AI | Human alternative | Source |
|---|---|---|---|
| في عالم اليوم المتسارع / في عالمنا سريع الخطى / في عالم يتطور باستمرار | Empty-opener cliché; near-universal AI opener | ادخل في الموضوع مباشرة | [S21][S26][S22] |
| يُعد … من أهم … | Prestige filler; announces importance instead of saying it | قل رأيك: "أفضل طريقة جربتها هي…" | [S26] |
| علاوة على ذلك / بالإضافة إلى ذلك (سلاسل الربط) | Connector-chain; essay-style linking words stacked across paragraphs | "وكمان" / "والأهم" / أو لا رابط أصلًا | [S21][S26][S24][S25] |
| من الجدير بالذكر أن… | Throat-clearing; "إن كان جديرًا بالذكر فاذكره" | احذفها | [S26][S30 MT] |
| من المهم ملاحظة / من المهم الإشارة إلى | Same throat-clearing pattern in Arabic table of tells | احذفها وابدأ بالنقطة | [S24][S25][S22] |
| لنتعمق في الموضوع / دعونا نتعمق / الغوص في التفاصيل | "delve" in Arabic clothing | احكِ عن التفصيلة نفسها | [S24][S25][S30 MT] |
| في الختام / باختصار / خلاصة القول / لتلخيص ذلك | Tidy-summary ending | اختم بأقوى نقطة لديك بدون إعلان الختام | [S26][S21][S25][S30 MT] |
| رحلتك نحو… / بوابتك إلى… | Journey/portal metaphors | لغة مباشرة بلا استعارات مستهلكة | [S26] |
| يمكن القول إن… / يمكن أن يساعد جزئيًا في… / بينما توجد وجهات نظر مختلفة | Permanent hedging | احسمها: "يساعد" | [S25][S21] |
| لا شك أن… | Inflated certainty formula | اذكر الواقعة | [S30 MT] |
| بشكل ملحوظ / ومن الجدير بالذكر أن النتائج تشير… | Notice-me phrase + "findings suggest" formula | اذكر الرقم/النتيجة نفسها | [S30 MT][S24] |
| نقطة تحوّل | "turning point" puffery | اشرح اللي اتغير فعلا | [S24] |
| لا يتعلق الأمر بـ X فقط، بل بـ Y أيضًا / من X إلى Y | Negative-parallelism templates in Arabic | قل النقطة مباشرة | [S24] |
| سؤال استفهامي كافتتاحية | Rhetorical-question opener template | افتح بالموقف/الحدث | [S24] |
| في المشهد الرقمي اليوم | "In today's digital landscape" | احذفها | [S24] |
| يشهد العالم / في خضم / يسلط الضوء على / مما يعكس / مما يؤكد أهمية | Trailing-significance + grand-context constructions (Arabic cousins of "highlighting/underscoring") | اذكر النتيجة الفعلية | [S24][S1 mapping] |
| نسيج نابض بالحياة / كتذكير قوي / يعمل كشهادة / دور محوري / في التفاعل المعقد / تقدم نتائجنا رؤى جديدة / واجه العديد من التحديات | Pangram's Arabic-rendered overused phrase set (from its phrase database) | احذف أو استبدل بتفصيل حقيقي | [S22] |
| بصفتي نموذج لغة ذكاء اصطناعي… | AI self-identification (294,000 hits) — appears when a refusal leaks into text | — (hard tell, delete) | [S22] |
| تشير النتائج إلى أن / هذا يبرز الحاجة إلى مزيد من… / لفهم أفضل | "Findings suggest / this highlights the need" research-cliché endings | اذكر ما ستفعله أنت | [S30 MT][S25] |

### 3b. Arabic structural tells

- **Register: excessive MSA formality.** AI Arabic stays in "polished, formal, slightly detached" MSA; human tech posts in Egypt mix 3ammeyya + English terms, use حوارية and direct address [S24][S28][S29].
- **Translated feel ("ركيك / مترجم").** Arabic content generators produce "مترجم" prose — literal translations of English slogans; the fix is re-saying the idea the way people actually talk [S29][S28].
- **Sentence-length metronome.** Every sentence 15-20 words; suspiciously uniform rhythm; stdev <5 words across 20+ sentences [S21][S25].
- **Symmetrical paragraphs** — each exactly 3-4 sentences; give one paragraph a single sentence, let another run long [S21][S26].
- **Rule of three in Arabic** — «واضح وموجز ومقنع»-style triplets; keep one per page [S21].
- **Zero specifics** — no numbers, names, or examples; one concrete detail per claim [S21][S24].
- **Question restatement before answering** [S21].
- **Tidy conclusion** restating everything [S21][S26].
- **Excessive punctuation** — overuse of dashes/punctuation noted in Arabic press coverage of AI-text research [S23].
- **Hollow adjectives as corporate gloss** — سلس، شامل، قوي، حيوي، محوري، نابض بالحياة [S21][S26][S30 MT].
- **Neutrality bias** — "no sharp opinion, every viewpoint 'has its merits'; humans are not like that" [S26].
- **Artificial enthusiasm** — "same rhyming phrases, same expected structure, same manufactured enthusiasm" on LinkedIn [S26].

### 3c. Arabic detection research (for completeness)

- Peer-reviewed Arabic stylometric/AI-detection research exists (e.g. *"Arabic machine-generated text detection: Stylometric analysis"* ScienceDirect S0957417425042599; *"Toward Robust Arabic AI-Generated Text Detection: Tackling Diacritics Challenges"* MDPI 2078/2489 and *"AI-Generated Text Detector for Arabic Language"* MDPI 2504-2289 — both **UNVERIFIED**: pages returned 403/blocked to this session; cited as pointers, not evidence) [S33].

---

## 4. "Never sound like AI" — authenticity checklist for Egyptian Arabic tech posts

Rules are grounded in the fetched sources; the Arabic examples follow the house style (Egyptian colloquial, English tech terms inline, no emojis, no tashkeel).

### A. Substance first (the biggest lever)

1. **DON'T publish a post without one checkable detail.** Add a number, version, price, name, metric, date. Measured: a concrete detail = +14% reach (was +2%), missing both detail and experience = -23% [S7][S2][S21].
2. **DON'T speak in generalities — DO tell what actually happened.** "جربتها في مشروع client في اسكندرية وطلعت مشكلة في الـ migration" beats "أنا أؤمن إن الـ migration محتاج تخطيط". Lived experience = +25% reach [S7][S26].
3. **DON'T hedge — DO take a side.** Kill "يمكن القول إن" / "بينما توجد وجهات نظر مختلفة". A sharp opinion that can be disagreed with is a human marker [S5][S26].
4. **DON'T pad — DO run the deletion test.** Any line that can be deleted with zero information loss, delete it. Filler is >1/3 of sentences in slop [S2].
5. **DON'T be perfectly safe.** Admit a mistake or a failure ("أول مرة عملت deploy فيها على prod بالطريقة دي، كسرت staging"). This is impossible to fake and immune to AI-suspicion [S26].

### B. Voice: Egyptian, natural, code-switched

6. **DO write 3ammeyya as your base layer** with English tech terms inline (this mix *is* the authentic Egyptian dev register; literal English→Arabic translation is what reads as "مترجم") [S28][S29].
7. **DON'T translate expressions literally — DO use real Egyptian phrasing:** "نورتنا" / "إيه رأيك؟" / "احكيلنا في التعليقات" / "خلينا نقول" / "بص" — natural, warm CTAs instead of stiff translated ones [S28].
8. **DON'T write like a press release.** Ban: يُعد… من أهم، من الجدير بالذكر، في عالمنا الرقمي، في خضم، يسلط الضوء على، نقطة تحول، رحلتك نحو، بوابتك إلى [S26][S24].
9. **DON'T chain connectors.** Zero "علاوة على ذلك / بالإضافة إلى ذلك"; use "وكمان" / "والأهم" / nothing. (In English posts: never start a paragraph with Moreover/Furthermore — of the top-100 LinkedIn creators studied, only 3 ever used a single "Moreover" and none as a habit [S7].)
10. **DON'T use hollow adjectives.** سلس، شامل، قوي، حيوي، محوري، نابض بالحياة → replace with the concrete fact that made you want to say it [S21][S26].
11. **DO keep humor where it fits (بخفة دم مصرية / إيفيه مناسب)** — Egyptian content culture runs on wordplay; but avoid dated trends (a 2-week-old trend reads as late) and nothing vulgar [S28].
12. **DON'T fake authority.** No "الخبراء بيقولوا" / "الدراسات بتقول" without naming the study/person; name it or cut it [S1][S4]. (In AI/tech posts: name the model, the version, the benchmark — this is also your topic.)

### C. Rhythm & structure (break the metronome)

13. **DO vary sentence length hard.** Cut one sentence to 3-4 words; let another run 30+. Target burstiness like human prose (stdev/mean ≈ 0.6-1.2), avoid the 15-20-word band [S2][S21].
14. **DO break paragraph symmetry.** One-sentence paragraph somewhere; a 4-5 sentence paragraph elsewhere. Never "every paragraph 3-4 sentences" [S21][S26].
15. **DO limit rule-of-three to one per post.** Break the rest into 2s and 5s [S21][S2].
16. **DON'T use the LinkedIn silhouette** (one sentence per line, blank line between). Mix: prose paragraphs + occasional line breaks for beats [S8].
17. **DON'T stack bold-colon bullets ("**كذا:** …").** Use natural lists or prose [S19][S1].
18. **DON'T do "The result?" cliffhangers / "Stop X, start Y" / "the key is".** Connect cause→result directly. These are the measured reach-killers on LinkedIn (-4.8%, -6.7%) [S7].
19. **DON'T open with the 5 opening templates** (contrarian hook / humble confession / shock line / rhetorical question / "Here's what nobody tells you"). Open mid-action or mid-thought: "امبارح قعدت ٣ ساعات أدور على bug…" [S8][S24][S26].

### D. Endings, emojis, and style rules

20. **DO end on your strongest concrete point.** Never "في الختام"; never a fake-deep metaphor kicker [S26][S4].
21. **DO keep a real closing question** (it doesn't hurt reach — 98% of top creators use them) but make it require actual experience to answer, not "إيه رأيكم؟" generic [S7][S8].
22. **DON'T use emojis** (brand rule) — and note this doubles as anti-AI: emoji placement is one of the loudest reader-flagged tells [S13][S24].
23. **DON'T use tashkeel** (brand rule) — fully vocalized prose reads formal/detached and unlike any Egyptian writing online [S24 mapping].
24. **DON'T recycle an identical P.S./CTA every post** (P.S. itself is fine and even helped in 2025) [S7].
25. **DO scan the draft for the Arabic phrase blacklist (§3a) before publishing** — every surviving phrase from that table is a leak [S26][S21].
26. **DO the read-aloud test:** anything you wouldn't say to a colleague, rewrite; anything that sounds like you, keep — even if imperfect [S4][S26].
27. **DON'T chase "100% human" detector scores.** Detectors are unreliable both ways; the goal is content worth reading in your voice [S26][S24][S15].

### E. Pre-publish 60-second check

- [ ] One checkable detail present? One lived moment present?
- [ ] Opener: no template (starts with a real situation/claim)?
- [ ] Connectors: zero علاوة على ذلك / moreover-type chains?
- [ ] Triplets: ≤1? Bold-colon bullets: none? Emojis: none? Tashkeel: none?
- [ ] Sentence lengths: visibly varied? Paragraph shapes: visibly irregular?
- [ ] Ending: concrete point (or real question), no "في الختام", no kicker?
- [ ] Opinion: sharp enough that someone could disagree?

---

## 5. Master ban list for the style guide

**Arabic (hard ban unless literally quoting):** في عالمنا الرقمي · في عالم اليوم المتسارع · في عالم يتطور باستمرار · من الجدير بالذكر · تجدر الإشارة · من المهم ملاحظة · من المهم الإشارة إلى · لا شك أن · علاوة على ذلك · بالإضافة إلى ذلك · في الختام · باختصار · خلاصة القول · لتلخيص · لنتعمق · دعونا نتعمق · الغوص في · يُعد من أهم · رحلتك نحو · بوابتك إلى · نقطة تحول · يسلط الضوء على · مما يعكس · مما يؤكد أهمية · في خضم · يمكن القول إن · بينما توجد وجهات نظر مختلفة · نابض بالحياة · نسيج · محوري (as hollow praise) · شامل/سلس/قوي (as hollow glosses) · بشكل ملحوظ · تشير النتائج إلى أن · هذا يبرز الحاجة.
**English (inline tech posts):** delve · tapestry · testament (to) · underscore (v.) · pivotal · landscape (abstract) · robust · vibrant · seamless · holistic · synergy · leverage (v.) · utilize · facilitate · streamline · game-changer · realm · myriad · plethora · embark · multifaceted · meticulous · moreover/furthermore/additionally (sentence-initial) · it's worth noting · in today's fast-paced world · here's the thing · let that sink in · read that again · here's what nobody tells you · the result? · stop X, start Y · not just X, but Y · in conclusion.

---

## 6. Verification notes

- **Verified by direct fetch (primary):** S1-S12, S14(partial), S15-S32. Fetched 2026-10-09 via curl / r.jina.ai / headless Chromium.
- **Verified (secondary):** S13 = The Ledger Asia's summary of Bloomberg (Bloomberg body not retrievable); S23 = Al-Jarida's Arabic summary of Roger Kreuz (The Conversation); NYT "Why Does A.I. Write Like That?" (2025-12-03) referenced by Wikipedia [S1] — page not fetchable (paywall/CAPTCHA), so no separate claims made from it.
- **UNVERIFIED / not fetchable:** MDPI + ScienceDirect Arabic detection papers [S33] (403); Reddit threads (blocked); Bloomberg body; karam — none of their content was used beyond titles in §3c.
- **MT caveat:** S30 is a machine-translated Arabic listicle; items tagged [MT] are Arabic renderings of English phrases, not native attestations. All [MT] items either appear in native Arabic sources too or map directly to documented English tells [S1][S2][S3].
- **Statistical caveats:** S2's thresholds are the detector vendor's own lines; S7/S8's reach percentages are observational within-author comparisons (S7 explicitly says "not strictly causal, no proven ranking penalty"); S10/S11 figures are detector-based estimates, not censuses (S12 notes false-positive caveat).

---

## 7. References

| ID | Source | URL |
|---|---|---|
| S1 | Wikipedia:Signs of AI writing (community-maintained master taxonomy; cites Kobak 2024, NYT 2025, Juzek & Ward) | https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing |
| S2 | SlopDetector — "Signs of AI Writing: 12 Patterns With Reproducible Thresholds" (2026) | https://slopdetector.org/blog/signs-of-ai-writing |
| S3 | SlopDetector — "The AI Words List: 120+ Phrases ChatGPT Overuses" (tiered; Kobak/FSU studies) | https://slopdetector.org/blog/ai-words-list |
| S4 | AIPromptIndex — "AI Slop: The 19 Writing Patterns That Scream ChatGPT" (adapted from Peter Yang's no-ai-slop, MIT) | https://aipromptindex.io/guides/remove-ai-slop-from-writing/ |
| S5 | Naturalistic AI — "ChatGPT Writing Signatures" (10 signatures + replace table) | https://naturalistic.ai/blog/chatgpt-writing-signatures |
| S6 | aismells — "Signs of AI Writing" field guide | https://aismells.com/ai-writing-tells |
| S7 | MagicPost — "11 Patterns to Spot an AI-Written LinkedIn Post in 2026" (45,965 + 129,000 + 287,000 posts; LinkedIn official quotes) | https://magicpost.in/blog/spot-ai-written-linkedin-post |
| S8 | SocialNexis — "How human readers spot AI-generated LinkedIn posts" (500-post analysis; Originality 2,726-post study; van der Blom report) | https://socialnexis.com/guides/ai-linkedin-post-reader-signals |
| S9 | SocialNexis — "How LinkedIn Spots AI Posts Before Anyone Reads Them" (Tskip, 360Brew, behavioral debt) | https://socialnexis.com/guides/how-linkedin-detects-ai-posts |
| S10 | Originality.ai — "LinkedIn AI Content Study: 81% of Long-Form Posts Are Likely AI" (July 2026; "Seems like AI slop" rollout; Hari Srinivasan quote) | https://originality.ai/blog/ai-content-published-linkedin |
| S11 | Gizmodo — "A Study Tried to Quantify How Many LinkedIn Posts Are 100% AI" (Pangram: 41% longform) | https://gizmodo.com/a-study-tried-to-quantify-how-many-linkedin-posts-are-100-ai-its-a-lot-2000784412 |
| S12 | ScienceSensei — "LinkedIn Is 40% AI-Written — and Your Brain Can't Detect It" (Pangram study + false-positive caveat) | https://sciencesensei.com/linkedin-is-the-most-ai-saturated-platform-new-study-suggests/ |
| S13 | The Ledger Asia — "AI-Written LinkedIn Posts Spark Debate Over Emoji Use…" (summary of Bloomberg, 2026-01-30) | https://theledger.asia/ai-written-linkedin-posts-spark-debate-over-emoji-use-and-other-tell-tale-signs/ (original: bloomberg.com/news/articles/2026-01-30/chatgpt-written-linkedin-posts-have-users-analyzing-emojis-other-ai-signs) |
| S14 | Washington Post — "What are the clues that ChatGPT wrote something?" (328,744 gpt-4o messages analysis; em dash/emoji tells) | https://www.washingtonpost.com/technology/interactive/2025/how-detect-chatgpt-em-dash/ |
| S15 | The Conversation — Ambuj Tewari (U. Michigan), "Why it's so hard to tell if a piece of text was written by AI" | https://theconversation.com/why-its-so-hard-to-tell-if-a-piece-of-text-was-written-by-ai-even-for-ai-265181 |
| S16 | Juzek & Ward — "Word Overuse and Alignment in LLMs: The Influence of Learning from Human Feedback" (arXiv 2508.01930) | https://arxiv.org/abs/2508.01930 |
| S17 | Shaib et al. — "Measuring AI 'Slop' in Text" (arXiv 2509.19163; slop taxonomy: density, relevance, factuality, bias, repetition, templatedness, coherence, verbosity, word complexity, tone) | https://arxiv.org/html/2509.19163v1 |
| S18 | jalaalrd/anti-ai-slop-writing (GitHub; 50+ banned words, 35+ phrases, 16 openers, 10 structural patterns; cites Carnegie Mellon 2025 + Buffer 52M-post analysis) | https://github.com/jalaalrd/anti-ai-slop-writing |
| S19 | ngmeyer/skills — banned-words.md (phrase blacklist + structural tells incl. bold-colon, neat-bow endings) | https://raw.githubusercontent.com/ngmeyer/skills/main/skills/productivity/write-well/references/banned-words.md |
| S20 | Async (Podcastle) — "Overused AI words" | https://async.com/blog/overused-ai-words/ |
| S21 | Sahihly — "١٠ علامات تكشف أن النص من ChatGPT (مع الإصلاحات)" (AR; also EN version) | https://sahihly.com/ar/blog/chatgpt-writing-tells · https://sahihly.com/blog/chatgpt-writing-tells |
| S22 | Pangram — "جولة في أكثر العبارات شيوعًا في مجال الذكاء الاصطناعي" (AR; phrase counts incl. «بصفتي نموذج لغة…» 294,000×) | https://www.pangram.com/ar/blog/walking-through-ai-phrases |
| S23 | Al-Jarida (KU) — "علامات ترقيم نصوص الـ chatGPt «مفرطة» وكلماتها «نادرة»" (summary of Roger Kreuz / The Conversation) | https://www.aljarida.com/article/106390 |
| S24 | Chatday — "كيف تعرف أن النص مكتوب بالذكاء الاصطناعي" (AR tells table; Graphite ~50% stat; Stanford 61% false positives; OpenAI classifier retired) | https://www.hub.chatday.ai/ar/blog/how-to-tell-if-text-is-written-by-ai |
| S25 | Plagly — "كيفية التحقق مما إذا كان النص مكتوبًا بالذكاء الاصطناعي" (AR; hedging, uniform sentences, listicle structure) | https://plagly.ai/ar/blog/how-to-check-if-text-is-written-by-ai |
| S26 | Nekhely Academy — "كيف تجعل محتوى الذكاء الاصطناعي يبدو بشريًا" (AR giveaway-phrase table with human alternatives; humanization equation) | https://nekhelyacademy.com/humanize-ai-content-guide/ |
| S27 | Techania Plus — "كيف تكتب محتوى عربي طبيعي لا تكتشفه أدوات الذكاء الاصطناعي؟" (AR; paragraph-by-paragraph method) | https://www.techaniaplus.com/2026/01/write-arabic-content-not-detected-by-ai-2026.html |
| S28 | Glancers — "كيف تكتب محتوى وسائل التواصل بالعامية المصرية؟" (Egyptian colloquial content guide) | https://glancers.co/ar/blog/how-to-write-social-media-content-in-egyptian-arabic-dialect-for-clients |
| S29 | DaleelAI — "كتابة المحتوى العربي بالذكاء الاصطناعي" (AR content challenges; models English-trained, "مترجم" feel) | https://daleelai.org/blog/ai-arabic-content-writing |
| S30 | LinkedIn (Asif Iqbal) — "أفضل 50 كلمة وعبارة مفضلة لدى ChatGPT" — **machine translation** of an English listicle | https://ae.linkedin.com/pulse/chatgpts-top-50-favorite-words-phrases-asif-iqbal-mba-cmbe-lavpe?tl=ar |
| S31 | SearchAtlas — "17 AI Writing Patterns" (7 categories incl. hedging/epistemic cowardice, fabricated sourcing) | https://searchatlas.com/blog/ai-patterns-in-writing/ |
| S32 | Khaled Taleb (Substack) — "كيف تجعل ChatGPT يكتب بأسلوبك أنت تمامًا" (AR; style-block technique) | https://khaledtaleb.substack.com/p/chatgpt-d0e |
| S33 | Arabic AI-detection research (UNVERIFIED — pages not fetchable from this session; pointers only) | sciencedirect.com/science/article/pii/S0957417425042599 · mdpi.com/2078-2489/15/7/419 · mdpi.com/2504-2289/8/3/32 |
