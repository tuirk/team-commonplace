# Commonplace book schema

Every entry is one fragment with a permanent ID, a source, 1 to 5 tags and a reason it matters. The skills, the web app and its CSV export all use this same schema, so a team can move its book from one to another without losing anything.

Every skill folder carries its own copy of these references (schema, entry format, settings template, privacy, starter tags and the teammate README), so any one skill works when it is installed alone. The copies are identical; read them as one contract.

## Entry fields

Each entry has these 15 fields. The CSV column name is also the field's name in the web app's data and in exports.

| Field | CSV column | Required | Format | Rules |
| --- | --- | --- | --- | --- |
| ID | `id` | yes | `<PREFIX>-<4 digits>`, for example `CP-0047` | See "IDs" below. |
| Title | `title` | yes | 3 to 10 words | A short handle a person can scan. Draft one when the user gives none. |
| Type | `type` | yes | one of `quote`, `insight`, `fix`, `lesson`, `decision`, `idea`, `reference` | Pick the type yourself; the user can override it. |
| Content | `content` | yes | a verbatim excerpt (quote) or a short paraphrase | Quotes stay verbatim and in quotation marks. Other types are 1 to 5 sentences. |
| Source | `source` | yes | free text: what, who (role or organisation), when | For example "Customer call, Acme Ltd, 2026-11-03". A web address may be added. "Unknown" is allowed, and curation flags it. |
| Why it matters | `why_it_matters` | yes | 1 sentence | The team's reason to keep it. When the user gives none, draft one and start it with `[draft] `. |
| Tags | `tags` | yes | 1 to 5, lowercase, hyphenated | From the controlled list in settings. See "Tags" below. |
| Themes | `themes` | no | names of projects or themes, in the tag shape | For project indexes: a launch, a key account, a research question. |
| Links | `links` | no | a list of entry IDs | Cross-references to related entries, in both directions where possible. |
| Added by | `added_by` | yes | a role or a first name, as settings choose | Settings pick role ("Sales") or first name. Never an email address or a phone number. |
| Added on | `added_on` | yes | ISO date, `YYYY-MM-DD` | Set it to today's date yourself; never ask for it. |
| Status | `status` | yes | `new`, `kept`, `promoted`, `retired` | See "Status lifecycle" below. |
| Promoted to | `promoted_to` | no | a link or a file path | Set when the entry fed a doc, SOP, FAQ or skill. |
| Sensitivity | `sensitivity` | yes | `internal` (the default) or `restricted` | Restricted entries stay out of week notes, project pages and shared briefs. See privacy.md. |
| Last reviewed | `last_reviewed` | no | ISO date, `YYYY-MM-DD` | Set by curation. |

The CSV header is exactly this line, in this order:

```csv
id,title,type,content,source,why_it_matters,tags,themes,links,added_by,added_on,status,promoted_to,sensitivity,last_reviewed
```

## Status lifecycle

| Status | Meaning | Set by |
| --- | --- | --- |
| `new` | Added, not yet seen in a curation pass | add |
| `kept` | Checked in curation and worth keeping | the curator |
| `promoted` | Fed a doc, SOP, FAQ or skill; still kept for its history | the team |
| `retired` | Duplicate, wrong, out of date or no longer useful; kept with its ID and hidden from default views | the curator |

Never delete an entry. When an entry is no longer useful, retire it instead, so its ID and history stay in the book.

## IDs

- An ID is the settings prefix, a hyphen, then exactly 4 digits from `0001` to `9999`. The prefix is 2 to 5 capital letters A to Z, set in settings (default `CP`).
- A new entry takes the next number after the highest ID ever used in the book. Count every entries file and every retired entry, and read the highest number rather than counting entries, because gaps and retired entries are normal.
- Never reuse an ID and never renumber one. A retired entry keeps its ID. People cite IDs in docs and chats, and a reused number would point them at the wrong entry.
- Each ID appears once in the whole book.
- `CP-47` and `CP-0047` are the same entry. Some tools show the short form; read it as the four-digit form. Always write the four-digit form in Markdown.

## Tags

- Settings hold the controlled tag list, and each tag has a one-line meaning, so everyone tags the same way.
- A new book starts with 10 to 25 tags. The list holds 40 tags at most, because a longer list stops being scannable.
- Every entry has 1 to 5 tags from the list, with no repeats.
- A tag is lowercase letters or digits, in words joined by hyphens: `pricing`, `client-onboarding`, `q1-pricing-review`. Letters from other languages are fine when they are lowercase.
- When an entry needs a tag that isn't on the list, propose it in your reply and add it to settings only after the user agrees. A silently added tag splits one topic into two.
- The curator proposes merges for near-duplicate tags (`pricing` and `price`) and flags tags used only once in 90 days.

## Themes and links

- Themes name a project or a question the team follows over time (a launch, a key account, a research question). They take the tag shape, are optional, and are not limited to the tag list. An entry lists each theme once, with no repeats.
- Links are entry IDs, each listed once, with no repeats. When a new entry links to an older one, add the link to both entries, so either entry leads to the other.

## Indexes

The book has three indexes, borrowed from the commonplace tradition:

- the tag index, `index-tags.md`: each tag and the IDs of its entries;
- the theme index, `index-themes.md`: each theme and the IDs of its entries;
- the sources list, `sources.md`: each source and the IDs of the entries taken from it.

Regenerate all three from the entries after every write, and never ask anyone to edit them by hand; a hand-edited index drifts from the entries. Their exact text is in entry-format.md.

## Promote threshold

A tag or theme becomes a promote candidate when it has 5 or more kept entries, or 3 or more entries added within 30 days. Both numbers live in settings (`Promote threshold`), so a team can change them.

## Folder structure

A Markdown book is one folder:

```text
commonplace/
  settings.md        team name, ID prefix, tags, curator, privacy rules, thresholds
  entries.md         every entry, oldest first, append-only
  index-tags.md      generated: tag to IDs
  index-themes.md    generated: theme to IDs
  sources.md         generated: source to IDs
  README.md          how this book works, for teammates
  briefs/            briefs made by find
  weeks/             week notes and candidates
  projects/          project start and close pages
  promoted/          optional: docs the team wrote from entries
```

When `entries.md` holds more than 400 entries and some of them were added in an earlier year, offer once to split it by year. Each earlier year's entries move, unchanged and oldest first, into a file for that year (`entries-2025.md`, `entries-2026.md` and so on), and this year's entries stay in `entries.md`. IDs keep counting across the files. New entries keep going at the end of `entries.md`, the last file in book order (entry-format.md, "Entries files").

## Handling the book

Every skill follows these rules, whatever its job:

- Start by locating `settings.md`. If there is none, say so in one line and offer to run setup, rather than guessing where the book is or what it holds.
- Entries are append-only: add new entries at the end of the book. Change an existing entry only when the user asks for that entry by ID. The only other changes to an existing entry are the ones a skill's own steps make: the back-link when a new entry links to it, and the status, Promoted to and Last reviewed lines that curation and promotion set.
- With a file system (a desktop app or coding tool with a folder open), read and write the folder the user names.
- Without one (a chat with uploaded files), read the uploaded files and return the updated files to download. Say plainly that the user must replace their copy with the new files, because the chat can't change their folder.
