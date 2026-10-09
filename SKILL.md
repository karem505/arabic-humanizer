# Arabic Humanizer — Write Like a Human, Not Like AI

> A quick-reference skill for any writer or AI agent producing Arabic (Egyptian colloquial) or English social copy.
> Full guide: `STYLE-GUIDE.md` · Research: `docs/ai-tells.md` · Banned lists: `docs/banned-phrases.md` · Examples: `examples/`

## When to use this skill

Use when writing or editing social copy (LinkedIn, Facebook, X), captions, threads, or any short-form content that must read as human — especially in Arabic with English tech terms inline. Also use it to audit drafts that "smell like AI".

## The rules (operational)

1. **Open with a moment, not an announcement.** Confession / contrast / human number / scene. Never a press release. Never a promise.
2. **One narrator voice.** "I found", "honestly", "this surprised me". Admit uncertainty. Neutral report-tone is the tell.
3. **Break the symmetry.** Shortest sentence 4–6 words; longest 25+. Paragraph sizes visibly different. No metronome rhythm, no one-sentence-per-line throughout.
4. **Numbers: a point, not a dump.** 1–2 up front; the rest go into the details/artifact.
5. **Ban list (hard).** AR: في عالمنا الرقمي · من الجدير بالذكر · تجدر الإشارة · لا شك أن · علاوة على ذلك · بالإضافة إلى ذلك · في الختام · باختصار · خلاصة القول · يسلط الضوء على · مما يعكس · في خضم · يمكن القول إن · نقطة تحول · رحلتك نحو · بوابتك إلى. EN: delve · tapestry · testament · underscore · pivotal · robust · seamless · holistic · synergy · leverage · streamline · game-changer · moreover/furthermore/additionally (sentence-initial) · it's worth noting · here's the thing · let that sink in · the result? · not just X but Y.
6. **Ending:** a strong point, or a question that asks for lived experience. Never "what do you think?".
7. **≥1 verifiable detail** per piece: version, price, name, date, or something that actually happened.
8. **Register:** Egyptian colloquial base; English tech terms stay English; no sudden MSA; no tashkeel; no emojis.
9. **Lists:** ≤4 items, uneven lengths. Never "**Word:** explanation".
10. **A caption/intro is not a summary of the long content.** One personal angle.

## For AI agents — output contract

When producing copy under this skill:
- Before writing: pick ONE human angle (moment, confession, contrast, or number).
- After writing: run the pre-publish checklist (below) and fix failures before returning the text.
- Never output banned phrases, even if the user's draft contained them — silently replace with the human alternatives from `docs/banned-phrases.md`.
- If the user asks for "more professional", do not switch to MSA/press-release tone; professional in this system = confident, specific, personal.

## Pre-publish checklist

- [ ] Opens with a moment/scene/human number — not an announcement?
- [ ] Real "I" present (opinion, doubt, confession)?
- [ ] Sentence lengths visibly varied?
- [ ] ≤2 numbers up front?
- [ ] Zero banned phrases?
- [ ] Ends on strong point or experience-question?
- [ ] ≤2 em dashes?
- [ ] No "**Word:** explanation" bullets; lists ≤4 and uneven?
- [ ] No emojis, no tashkeel?
- [ ] At least one verifiable detail?
- [ ] One clear angle — not a summary?

## Reference files

| File | Use |
|---|---|
| `docs/banned-phrases.md` | full AR/EN ban lists + human alternatives |
| `docs/ai-tells.md` | the research: why each pattern reads as AI (+33 sources) |
| `docs/craft-rules.md` | hooks, "See more" cutoff, rhythm, length data |
| `examples/before-after.md` | worked rewrites with change notes |
| `examples/hooks.md` | opening formulas library |
