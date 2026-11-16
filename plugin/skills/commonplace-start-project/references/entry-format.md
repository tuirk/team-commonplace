# Entry format

Write every entry in exactly this shape. Other skills, the web app's import and the format checker read the book line by line, so a moved line or a missing space breaks them.

## The entry block

```text
### <ID> · <Title>
- Type: <type>
- Source: <source>
- Tags: <tag>, <tag>
- Themes: <theme>, <theme>
- Links: <ID>, <ID>
- Added: <YYYY-MM-DD> by <added by>
- Status: <status>
- Promoted to: <link or path>
- Sensitivity: <sensitivity>
- Last reviewed: <YYYY-MM-DD>

<content>

**Why it matters:** <one sentence>
```

- The heading is `### `, the ID, then a space, a middle dot (`·`) and a space, then the title.
- The field lines come in exactly the order above. Write Themes, Links, Promoted to and Last reviewed only when the entry has them; leave the line out rather than writing it empty.
- Every other field line is always there: Type, Source, Tags, Added, Status and Sensitivity.
- Write one space after each colon. Separate list items (tags, themes, links) with a comma and one space.
- The Added line holds the date, the word `by`, and the added-by value: `- Added: 2026-11-03 by Sales`.
- Leave no spaces at the ends of lines.
- One blank line comes after the field lines, then the content, then one blank line, then the Why it matters line.

## Content

- A quote is a block quote: every line starts with `> `. When a quote has two paragraphs, write the blank line between them as a line holding only `>`. Keep the quotation marks.
- The `> ` markers belong to the Markdown only. In the content field (the web app, CSV and Notion) the markers are left out and the quotation marks stay, so `> "Just tell me the number."` becomes `"Just tell me the number."`.
- Every other type is plain paragraphs, separated by one blank line, kept as written.

## Why it matters

- One line: `**Why it matters:** ` and then one sentence.
- When you drafted the reason yourself, start it with `[draft] `: `**Why it matters:** [draft] Saves a confusing client email.` The marker stays part of the text in every format, including the CSV `why_it_matters` column, so curation can find drafted reasons and ask the team for theirs.
- Nothing follows the Why it matters line before the next entry's heading: no rule (`---`), no notes, no extra text.

## Entries files

- The entries live in `entries.md`. After a year split, each earlier year's entries live in a file for that year (`entries-2025.md`, `entries-2026.md` and so on), and this year's stay in `entries.md`. Book order is the year files in year order, then `entries.md`, so new entries go at the end of `entries.md`.
- Entries sit oldest first, in ascending ID order.
- A file may open with a short note above the first entry (any lines before the first `### ` heading). Keep it as written, followed by one blank line.
- Put one blank line between entries.
- Save as UTF-8 without a byte order mark, with LF line endings, and end the file with exactly one newline.
- An empty book is an empty `entries.md` (0 bytes, not even a newline), or one that holds only the note.

## Examples

A quote:

```markdown
### CP-0047 · Onboarding time drives price objections
- Type: quote
- Source: Customer call, Acme Ltd, 2026-11-03
- Tags: onboarding, pricing
- Themes: q1-pricing-review
- Links: CP-0031, CP-0039
- Added: 2026-11-03 by Sales
- Status: new
- Sensitivity: internal

> "We'd pay more if onboarding took a day, not a week."

**Why it matters:** Third customer this month tying price to setup time.
```

A lesson:

```markdown
### LS-0003 · Clients read the first invoice as the real quote
- Type: lesson
- Source: Project retro, Halden Bakery site, 2026-02-14
- Tags: pricing, estimates, communication
- Links: LS-0011
- Added: 2026-02-14 by Project manager
- Status: kept
- Sensitivity: internal

The client accepted the estimate but pushed back hard on the first invoice. Our estimate showed ranges; the invoice showed one number, and that number is what they remembered.

**Why it matters:** Show a single expected figure next to every range in estimates.
```

A quote from a call:

```markdown
### LS-0011 · "Just tell me the number"
- Type: quote
- Source: Discovery call, Corrowin Dental, 2026-03-02
- Tags: pricing, estimates
- Links: LS-0003
- Added: 2026-03-02 by Founder
- Status: kept
- Sensitivity: internal

> "I don't need three options. Just tell me the number you'd pick."

**Why it matters:** Second client this quarter asking for one recommended price, not a menu.
```

A fix with a drafted reason:

```markdown
### LS-0017 · Preview links break when the CMS draft is renamed
- Type: fix
- Source: Support thread, internal, 2026-04-21
- Tags: cms, tooling
- Added: 2026-04-21 by Developer
- Status: new
- Sensitivity: internal

Renaming a draft changes its slug, which kills any preview link already sent to the client. Lock the slug before sharing a preview, or send the preview through the share panel, which uses the page ID.

**Why it matters:** [draft] Saves a confusing client email every time a draft is renamed.
```

## Index files

The three index files are generated from the entries and never edited by hand. Rewrite all three after every write, using exactly this text.

- The file starts with its heading, a blank line, the note line `Generated from the entries. Do not edit by hand.` and a blank line.
- Then one line per item: `- <item>: <ID>, <ID>`, with the IDs in book order.
- Every entry counts, retired and restricted ones included. An entry with no themes is simply absent from the theme index.
- The tag index lists tags, and the theme index lists themes, sorted in plain character order (`cms` before `communication`, digits before letters).
- The sources list keys each line by the entry's exact Source text, in the order each source first appears in the book. Two entries with the same Source text share one line.
- With no items, the file ends right after the note line.
- Like entries files, index files are UTF-8 with LF line endings and end with exactly one newline.

`index-tags.md` with no items:

```markdown
# Tag index

Generated from the entries. Do not edit by hand.
```

`index-themes.md` with no items:

```markdown
# Theme index

Generated from the entries. Do not edit by hand.
```

`sources.md` with no items:

```markdown
# Sources

Generated from the entries. Do not edit by hand.
```

A worked example: a book holding only LS-0003, LS-0011 and LS-0017 above has these indexes.

`index-tags.md`:

```markdown
# Tag index

Generated from the entries. Do not edit by hand.

- cms: LS-0017
- communication: LS-0003
- estimates: LS-0003, LS-0011
- pricing: LS-0003, LS-0011
- tooling: LS-0017
```

`index-themes.md` has no items, because none of the three has a theme, so it is the empty text above.

`sources.md`:

```markdown
# Sources

Generated from the entries. Do not edit by hand.

- Project retro, Halden Bakery site, 2026-02-14: LS-0003
- Discovery call, Corrowin Dental, 2026-03-02: LS-0011
- Support thread, internal, 2026-04-21: LS-0017
```
