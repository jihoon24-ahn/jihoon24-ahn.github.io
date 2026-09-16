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
- Name the output exactly `YYYY-MM-DD.html`.
- Replace every `{{PLACEHOLDER}}`; no placeholder may remain.
- Keep the report self-contained: inline CSS and JavaScript only, with no external assets.
- Do not modify `index.html`, `reports.json`, or `.github/workflows/update-reports.yml` when adding an ordinary daily report. The existing workflow updates the archive and calendar.

## Fixed report structure

Preserve the master template's element order, class names, CSS, navigation, responsive layout, expandable correction blocks, and print styles. Use these sections in this exact order:

1. Overall Performance
2. Performance Profile
3. Priority Patterns & Suggestions
4. Key Corrections
5. Useful Language
6. Model Answer
7. Transcript Note

## Content rules

### Overall Performance

- Write one paragraph of approximately 60 words and never exceed 70 words.
- State the conversation length or breadth only when supported by the source.
- Include the biggest strength, biggest weakness, and the single most important next step.
- Combine the executive summary and positive feedback here; do not add a separate "What You Did Well" section.

### Performance Profile

- Include all three scales: OPIc, TOEFL iBT Speaking, and CEFR Speaking.
- Treat levels as informal estimates from this conversation, not official scores.
- Do not inflate a level to be encouraging. Base it on fluency, organization, range, accuracy, and comprehensibility.
- State when formal TOEFL integrated tasks were not assessed.

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

### Useful Language

- Include 6–8 useful expressions from or relevant to the conversation.
- Give a brief plain-English meaning and, when helpful, a short example.
- Prioritize reusable collocations, phrasal verbs, and idioms.

### Model Answer

- Include one coherent model answer of approximately 100 words.
- Choose one important topic Jihoon discussed.
- Preserve his actual ideas while improving structure and naturalness.
- Bold the most reusable language chunks.

## Language and formatting

- Write the entire report in English unless the user explicitly requests another language.
- Use bold text to make key ideas and reusable phrases easy to scan.
- Use double quotation marks for quoted wording and example sentences. Do not use single quotation marks as quotation marks.
- Apostrophes inside contractions and possessives are allowed.
- Keep paragraphs short and readable on a phone.
- Use direct, supportive language without excessive praise.
- Include the transcript-quality note whenever the source is automated, unclear, or has inconsistent speaker labels.

## Verification

Before reporting completion:

1. Parse the HTML with Python's `html.parser` or an equivalent validator.
2. Check JavaScript syntax with `node` when Node.js is available.
3. Confirm the filename matches `^\d{4}-\d{2}-\d{2}\.html$`.
4. Confirm the teacher and long-form date appear in the metadata and page title.
5. Confirm Overall Performance contains no more than 70 words.
6. Confirm the three proficiency scales and all seven required sections exist.
7. Confirm every placeholder has been removed.
8. Confirm the report works at mobile widths and does not depend on external files.

If any check fails, fix the report and repeat validation.

## Git workflow

- Preserve unrelated user changes and inspect `git status` before staging.
- Stage only the new dated report unless another file is required for the requested task.
- When the user explicitly asks to publish, commit with `Add English progress report for YYYY-MM-DD` and push to `main`.
- If direct push is unavailable or protected, create a branch and pull request instead.
- Never place credentials or personal access tokens in HTML, scripts, prompts, commits, or repository files.
- After publishing, verify that the GitHub Actions run succeeds and that the new date appears on the calendar.
