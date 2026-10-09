# Before / After — Rewrites with Notes
# قبل وبعد — إعادة كتابة مع تفسير التغييرات

> Each example: the AI-sounding original, the human rewrite, and the exact changes that were made.
> كل مثال: النسخة اللي بتبان AI، النسخة البشرية، والتغييرات بالظبط.

---

## 1) Tech announcement (Arabic)

### ❌ Before (AI-flavored)
> DeepSeek عملتها تاني — المرة دي مش بموديل جديد، بل بتقنية تخلي الموديلات الشغالة أسرع 60–85% لكل مستخدم: بنفس الأوزان، وبنفس الجودة بالحرف.
>
> اسمها DSpark — إطار speculative decoding بيحل معضلة قديمة: المسودات السريعة بتفقد دقتها في آخر البلوك، والدقيقة بطيئة. الحل عندهم 3 أجزاء:
> 1) مسودة شبه تلقائية: هيكل موازي سريع + رأس Markov صغير يربط كل توكن باللي قبله
> 2) رأس ثقة يرمي المسودات الفاشلة قبل ما تستهلك قدرة التحقق
> 3) جدولة تعرف حمل الـ GPU: تزيد التحقق وقت الهدوء وتقلله وقت الزحمة
>
> النتائج على حركة إنتاج حقيقية: أسرع 60–85% لكل مستخدم، +51% في الـ throughput، وطول القبول +26–31%. وكل ده من غير إعادة تدريب — المخرجات بنفس التوزيع الأصلي بالضبط.
>
> التفاصيل الكاملة في الكاروسيل.

**What makes it read as AI:** negative parallelism ("مش بموديل جديد، بل بـ…") · perfectly numbered 3-part list · results dumped as number pile · em dashes · formulaic close ("التفاصيل الكاملة في الكاروسيل") · zero "I".

### ✅ After (human)
> قعدت أقرا ورقة DeepSeek الجديدة ولقيت نفسي ببتسم.
>
> مش عشان التقنية عبقرية أوي. عشان حل مشكلة كنت شخصياً فاكرها اتقفلت خلاص.
>
> الفكرة ببساطة: كل ما موديل بييجي يكتب، بيضيع وقت رهيب في خطوة واحدة سخيفة — بيحمّل أوزانه كلها من الذاكرة عشان يطلع توكين واحد. زي ما تكون بتشغّل الموتور كله عشان تتحرك خطوة لقدام.
>
> فكرة "خلّي موديل صغير يتوقع كام توكين ورا بعض" قديمة. المشكلة إن الشغل كان بيبوظ في آخر البلوك: أول توقعين حلوين، وبعدها الموديل الصغير بيخرف.
>
> اللي DeepSeek عملوه إنهم جزّأوا الحكاية: جزء يتوقع بسرعة، وجزء صغير يصلح التوقع على ضوء اللي قبله. ومعاها حاجة لطيفة — الموديل بيقيس ثقته في كل توقع، ولو حس إنه بيخرف بيقصّر ويرجع لطريقة أأمن.
>
> النتيجة الرسمية: ردود أسرع 60-85% للمستخدم، بنفس الناتج بالحرف. مش "شبه" نفس الجودة. نفس التوزيع بالظبط.
>
> والورقة والكود والأوزان كلها مفتوحة لو حابب تتفرج.
>
> سؤال ليك: لو الإجابة نفسها بالظبط، بس أسرع، إيه اللي لسه بيخليك تستحمل الانتظار؟

**Changes made:** opens with a moment ("قعدت أقرا… وابتسمت") · real "I" ("كنت شخصياً فاكرها") · everyday simile (الموتور) · honest colloquial word (بيخرف) · no numbered list · numbers reduced to 1-2 · no "الخلاصة:" · ends with an experience question.

---

## 2) Content-carousel intro (Arabic)

### ❌ Before
> الـ LLMs بقت عصب كل تطبيقات الـ AI — بس معظم الناس بتستخدمها من غير ما تعرف الأنواع ولا الفرق بينها.
>
> جمعت لك في الكاروسيل ده خلاصة بحث مكثف: إيه هي الـ LLMs، إزاي بتتبني من جوه، وإيه الفرق الحقيقي بينها.
>
> الخلاصة: اختيار الموديل قرار هندسي — مش "مين الأشهر" ولا "مين الأغلى". افهم الأنواع الأول، وبعدين اختار.

**What makes it read as AI:** announcement-style opening · "جمعت لك… خلاصة بحث مكثف" (self-important) · "الخلاصة:" · symmetric closing triplet.

### ✅ After
> لما حد يسألني "أستخدم أنهي موديل؟" بجاوب بسؤال: عايز مين يشيل الشيلة.
>
> في ناس فاكرة إن الموديلات كلها زي بعض والفرق في الاسم والسعر بس. وفيه ناس تانية عارفة الفرق بس محتاجة حد يقعدلها الحكاية ببساطة.
>
> جمعت الفروق اللي بتفرق فعلاً: إمتى Dense بيهزم MoE رغم إنه أصغر، وإمتى العكس. ليه موديل بسياق مليون بيبقى أرخص من موديل صغير. وإيه اللي بيخلي موديل شغال محلياً على لابتوب أجدع من واحد سحابي في شغلك.
>
> إنت آخر مرة غيّرت موديل شغلك — إيه اللي خلاك؟

**Changes:** opens with a real scene (someone asking a question) · answers with an analogy ("مين يشيل الشيلة") · deletes "الخلاصة:" · ends with an experience question.

---

## 3) Product update (English)

### ❌ Before
> In today's fast-paced AI landscape, we're thrilled to announce a game-changing update to our platform. This robust, seamless release leverages cutting-edge technology to deliver a comprehensive set of enhancements.
>
> Key highlights:
> - **Performance:** Significantly improved speed
> - **Reliability:** Enhanced stability
> - **Security:** Strengthened protections
>
> We're committed to empowering teams to do their best work. Let us know your thoughts in the comments!

**What makes it read as AI:** empty opener · "game-changing/robust/seamless" cluster · bold-colon bullets · rule of three x2 · "empowering teams" filler · "let us know your thoughts" generic CTA · zero specifics.

### ✅ After
> We shipped something I didn't expect to care about: the app now opens 3× faster.
>
> The number sounds small. But we spent two months profiling and the culprit turned out to be one dumb thing — we were re-fetching the entire workspace on every launch. One caching fix, and the whole thing feels different.
>
> The team's most senior engineer called it "the most boring win of the year." I'll take it.
>
> If you had given up on the slow loading — give it one more shot.

**Changes:** opens mid-action ("We shipped…") · one concrete number · a real anecdote with an internal quote · admission of surprise ("didn't expect to care") · CTA is specific to a lived behavior, not "thoughts?".

---

## Pattern summary — ملخص الأنماط

| AI habit | Human replacement |
|---|---|
| Announcement opener | Moment/confession/contrast opener |
| Number pile | 1–2 numbers, woven into a story |
| Numbered 3-part list | Prose, or ≤4 uneven bullets |
| "الخلاصة:" / "In conclusion" | End on the strongest point |
| Generic CTA | Experience question |
| Zero "I" | Visible opinions, doubt, confession |
| Uniform rhythm | Long-short sentence mix |
| Similes from nowhere | Everyday analogies (cars, coffee, queues) |
