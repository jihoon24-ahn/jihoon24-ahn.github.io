# English Progress Report Project

## Purpose

This repository publishes Jihoon Ahn's English conversation progress reports through GitHub Pages. Generate every new report from the fixed master at `templates/english-report-master.html`. Do not redesign the report or invent a new structure.

## Required inputs

Before generating a report, identify all three inputs:

1. The transcript or recording supplied by the user.
2. The class date in `YYYY-MM-DD` format.
3. The teacher's name.

Ask one concise question if the date or teacher is missing. If the source is audio, transcribe it before assessment. Automated speaker labels may be unreliable; infer attribution only from context and do not present uncertain wording as Jihoon's sentence.

## Output file

- Copy `templates/english-report-master.html` to the repository root.
- Before naming a new report, check the repository root for reports from the same date.
- Name new reports `YYYY-MM-DD-SS.html`, where `SS` is a two-digit session number beginning with `01` (for example, `2026-10-04-01.html` and `2026-10-04-02.html`).
- Treat an existing legacy file named `YYYY-MM-DD.html` as session `01`. If it already exists, name the next report `YYYY-MM-DD-02.html`; do not rename or overwrite the legacy report.
- Never overwrite a same-day report. Use the next unused session number for each additional class.
- Replace every `{{PLACEHOLDER}}`; no placeholder may remain.
- Keep the report self-contained: inline CSS and JavaScript only, with no external assets.
- Do not modify `index.html`, `reports.json`, or `.github/workflows/update-reports.yml` when adding an ordinary daily report. The existing workflow updates the archive and calendar.

## Fixed report structure

Preserve the master template's element order, class names, CSS, navigation, responsive layout, expandable correction blocks, self-test mode, and print styles. Below the metadata line, include the one-line summary and topic tags. Use these sections in this exact order:

1. Overall Performance
2. Last Time → This Time
3. Performance Profile
4. Speaking Snapshot
5. Sentences You Got Right
6. Priority Patterns & Suggestions
7. Key Corrections
8. What Your Teacher Corrected
9. Useful Language
10. Pronunciation Watch (optional; include only when there is evidence)
11. Model Answer
12. Your 2-Minute Speaking Task
13. Transcript Note

## Content rules

### Overall Performance

- Write one paragraph of approximately 60 words and never exceed 70 words.
- State the conversation length or breadth only when supported by the source.
- Include the biggest strength, biggest weakness, and the single most important next step.
- Omit caveats in Overall Performance about spoken fluency or pronunciation being unverified, or proficiency levels being informal estimates based on one conversation rather than official test scores. Jihoon already understands these limitations; keep this paragraph focused on actionable feedback.
- Combine the executive summary and positive feedback here; do not add a separate "What You Did Well" section. Sentences You Got Right is the only other place for positive feedback, and it quotes specific sentences rather than general praise.

### Summary and topic tags

- Write one sentence of no more than 25 words naming what the class covered.
- Give 2–5 short topic tags in title case. Put the same tags, comma-separated, in the `report-topics` meta tag.

### Last Time → This Time

- Review the first three Priority Patterns from the most recent earlier report, and link to that report.
- Give each one a status: Improved (`improved`), Same (`same`), Still frequent (`frequent`), or Not observed (`not-observed`).
- Support every status with one specific piece of evidence from this class. Use Not observed when the class gave no chance to judge it.

### Performance Profile

- Include all three scales: OPIc, TOEFL iBT Speaking, and CEFR Speaking.
- Treat levels as informal estimates from this conversation, not official scores.
- Do not inflate a level to be encouraging. Base it on fluency, organization, range, accuracy, and comprehensibility.
- State when formal TOEFL integrated tasks were not assessed.

### Speaking Snapshot

- Report four approximate metrics, counting only lines reliably attributed to Jihoon:
  - Talk share: Jihoon's words divided by all attributed words.
  - Average turn: Jihoon's words divided by his turns.
  - Restarts: immediately repeated words or phrases, such as "I I" or "it was it was."
  - Top filler: the most frequent filler phrase and its count, such as "you know" ×14.
- In each note, compare with the previous report's snapshot when one exists; otherwise write "First measurement."
- Omit a metric's comparison, not the metric, when the transcript is too incomplete to compare fairly, and say so in the note.

### Sentences You Got Right

- Include 2–3 sentences Jihoon actually said correctly or effectively, including successful self-corrections.
- Quote his final wording exactly, and briefly explain what to keep doing. Do not include sentences with uncertain attribution.

### Priority Patterns & Suggestions

- Include exactly five high-impact patterns supported by recurring evidence.
- Explain each pattern briefly and pair it with a practical suggestion.
- Give at least two bulleted, immediately usable example sentences per pattern.
- Prefer speaking techniques Jihoon can apply in real conversations, such as a story frame, sentence restart, timeline control, or fixed language chunks.

### Key Corrections

- Include 6–8 reliable corrections. Use fewer only when the source does not contain enough recoverable examples.
- Every correction must contain these four blocks in this exact order:
  1. Your wording
  2. Minimal correction
  3. Natural version
  4. Why?
- Preserve Jihoon's meaning in the minimal correction and make the fewest necessary changes.
- Make the natural version idiomatic, conversational, and suitable for everyday or business English.
- Briefly explain both why the original was wrong or unnatural and why the revision is better.
- Do not correct obvious transcription corruption as if Jihoon intentionally said it.
- Words that look like typos may be Jihoon's pronunciation mistakes (for example, "laser" for "razor" or "bird" for "beard"). Do not correct these as typos, grammar, or vocabulary errors, and do not present them as transcription corruption; put them in Pronunciation Watch instead.

### Self-test mode

- Keep the Self-test mode button and each "Show answer" button from the master template. They hide the minimal correction, natural version, and explanation until Jihoon has tried his own fix.

### What Your Teacher Corrected

- Include 2–4 moments where the teacher reformulated Jihoon's wording during class.
- For each, give what Jihoon said, the teacher's exact reformulation, and a one-sentence takeaway.
- Do not repeat items already listed in Key Corrections. Remove the section only when the transcript contains no teacher reformulations.

### Useful Language

- Include 6–8 useful expressions from or relevant to the conversation.
- Give every expression a separate, clearly labeled plain-English meaning and example sentence.
- Keep the meaning concise, and make the example a complete sentence in double quotation marks.
- Prioritize reusable collocations, phrasal verbs, and idioms.

### Pronunciation Watch

- Include this section only when the transcript shows likely pronunciation slips; otherwise remove the section and its navigation link.
- Include 1–3 items. For each, give the target word, what it sounded like, a short articulation tip, and a minimal-pair or phrase practice line.
- Give the correct General American IPA for each target word in slashes (for example, razor /ˈreɪzɚ/), and the IPA of what it sounded like (for example, "laser" /ˈleɪzɚ/). In the tip, name the key sound with its IPA symbol, such as /r/ or /ɪr/.
- Describe the slips as likely, because they are inferred from the transcript rather than heard directly.

### Model Answer

- Include one coherent model answer of approximately 100 words.
- Choose one important topic Jihoon discussed.
- Preserve his actual ideas while improving structure and naturalness.
- Bold the most reusable language chunks.

### Your 2-Minute Speaking Task

- Give one speaking prompt on a topic from this class.
- Provide a four-step frame with a sentence starter for each step.
- List three target chunks from this report for Jihoon to use.

## Language and formatting

- Write the entire report in English unless the user explicitly requests another language.
- Do not include transcript timestamps (for example, 22:00) or timestamp ranges anywhere in the report, including headings, explanations, corrections, and the transcript note.
- Use <strong>bold</strong> for key takeaways, corrected language chunks, and reusable expressions that Jihoon should notice first.
- Use <em>italics</em> for individual target words, grammar forms, prepositions, and short contrasts that support the explanation.
- Combine bold and italics purposefully to make the report easier to understand, but do not emphasize entire paragraphs or decorate text that is not instructionally important.
- Use double quotation marks for quoted wording and example sentences. Do not use single quotation marks as quotation marks.
- Apostrophes inside contractions and possessives are allowed.
- Keep paragraphs short and readable on a phone.
- Use direct, supportive language without excessive praise.
- Include the transcript-quality note whenever the source is automated, unclear, or has inconsistent speaker labels.

## Verification

Before reporting completion:

1. Parse the HTML with Python's `html.parser` or an equivalent validator.
2. Check JavaScript syntax with `node` when Node.js is available.
3. Confirm the filename matches `^\d{4}-\d{2}-\d{2}-\d{2}\.html$`. Legacy reports named `YYYY-MM-DD.html` remain valid but should not be used for newly generated reports.
4. Confirm the teacher and long-form date appear in the metadata and page title.
5. Confirm Overall Performance contains no more than 70 words.
6. Confirm the three proficiency scales and all required sections exist in order, with Pronunciation Watch present only when supported.
7. Confirm every placeholder has been removed.
8. Confirm the report works at mobile widths, self-test mode hides and reveals answers, and the report does not depend on external files.

If any check fails, fix the report and repeat validation.

## Git workflow

- Preserve unrelated user changes and inspect `git status` before staging.
- Stage only the new dated report unless another file is required for the requested task.
- When the user explicitly asks to publish, commit with `Add English progress report for YYYY-MM-DD session SS` and push to `main`.
- If direct push is unavailable or protected, create a branch and pull request instead.
- Never place credentials or personal access tokens in HTML, scripts, prompts, commits, or repository files.
- After publishing, verify that the GitHub Actions run succeeds and that the new date appears on the calendar.
