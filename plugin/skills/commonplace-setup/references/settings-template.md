# Settings template

Every book has one `settings.md` at the top of its folder. Skills read it first, because it holds the team's name, the ID prefix, the tag list and the privacy choices that every other step depends on.

## The template

Write a new `settings.md` from this template, filling in the team's answers:

```markdown
# Commonplace settings
- Team name: Larchmont Studio
- ID prefix: CP
- Curator: Operations lead (rotates quarterly)
- Added-by style: role        # role | first-name
- Anonymise customers: yes    # yes = company kept, people's names removed
- Promote threshold: 5 kept entries, or 3 in 30 days
- Digest day: Monday
- Backend: markdown           # a folder of Markdown files

## Tags
- onboarding: first 30 days of a client or hire
- pricing: what customers pay, objections, discounts
- tooling: software and workarounds
```

## Keys

The file starts with the line `# Commonplace settings`. Each key is one line, `- <Key>: <value>`, above the `## Tags` section.

| Key | Required | Allowed values | Default | What it does |
| --- | --- | --- | --- | --- |
| Team name | yes | any text | none; ask | Names the book in replies, week notes and the README. |
| ID prefix | yes | 2 to 5 capital letters A to Z | `CP` | Starts every entry ID. Changing it later doesn't rename old entries. |
| Curator | yes | a role, with any note in brackets | none; ask | Who runs curation; the README names them. |
| Added-by style | yes | `role` or `first-name` | `role` | Whether entries record the adder's role ("Sales") or first name. |
| Anonymise customers | yes | `yes` or `no` | `yes` | `yes` removes people's names from customer quotes and notes and keeps company names. See privacy.md. |
| Anonymise companies | no | `yes` or `no` | `no` | The stricter setting: `yes` also replaces company names. |
| Promote threshold | yes | `<n> kept entries, or <m> in <d> days` | `5 kept entries, or 3 in 30 days` | When a tag or theme becomes a promote candidate. |
| Digest day | yes | `Monday` to `Sunday` | `Monday` | The day the team closes its week. Closing the week dates its week note by it, and a weekly scheduled run uses it. |
| Backend | yes | `markdown` | `markdown` | Where entries live: a folder of Markdown files. |

- A value may be followed by a space, `#` and a comment, as in the template. The comment is a hint for people and is not part of the value.
- Keep the keys in the template's order and add no other keys; other skills don't read them.

## Week section

A book may hold a `## Week` section between the keys and `## Tags`, saying where the week's material lives so closing the week can read it. Setup writes it from the team's answer, starting from this block:

```markdown
## Week
- Board: pasted or uploaded
- Notes: pasted or uploaded
```

- Board says where the team's board lives. Notes says where its meeting notes and chat live. Each value is free text in the team's words: a tool, a channel or a folder.
- `pasted or uploaded` means the team pastes or uploads the week's material when it closes the week. A book without the section reads the same way.
- One blank line comes before `## Week` and one before `## Tags`, so `## Tags` stays the last section. Only commonplace-close-week reads this section; the format checker ignores it.

## Tags section

- After the keys (and the Week section, when there is one) comes a blank line, then `## Tags`, then one line per tag: `- <tag>: <one-line meaning>`.
- Every tag has a meaning, so people tag the same way. Every tag takes the tag shape from schema.md, and no tag appears twice.
- Setup fills this section from starter-tags.md. The limits on the list's size and the rule for adding tags later are in schema.md.
