---
name: commonplace-setup
description: "Set up a shared team commonplace book: a simple, numbered log where a team captures customer quotes, lessons learned, fixes, insights and decisions with sources and tags. Use whenever someone wants to start a commonplace book, team knowledge log, swipe file, lessons-learned log, insight library or 'second brain' for their team, or asks how their team can stop losing useful knowledge, even if they don't say 'commonplace'."
license: MIT
---

# Set up a team commonplace book

You set up a new team commonplace book through a short interview, then write its folder: settings, an empty entries file, three empty indexes and a README for teammates. One team keeps one book, so where a book already exists you offer to adjust it instead of making another. You write only inside the book's folder.

## When to set up

- Set up a book only when the user wants one for their team.
- When they only ask what a commonplace book is or how one works, answer in a few plain sentences: a shared, numbered log of the quotes, lessons, fixes, insights and decisions worth keeping, each with a source and a reason it matters. Then offer to set one up. Ask nothing else and write nothing until they say yes, because a question isn't a request.
- A personal journal, diary or private notes isn't a team book. Say in one line that this sets up a shared book for a team, and write nothing.

## Before you start

1. Look for a book where the other commonplace skills would: the folder the user names, otherwise the working folder and its subfolders, for a `settings.md` whose first line is `# Commonplace settings`. The working folder is the folder Claude was started in. Look nowhere else: never search a folder above the working folder, this skill's own folder, the plugin's folder, other folders or a whole drive, because they hold files that aren't the team's book.
   - Found: don't create another. Two books split the team's entries, and the add and find skills would have to ask which one to use every time. Say where the book is and its team name, and offer to adjust it: the tags, the curator, the ID prefix or another setting. Ask nothing else and write nothing until they say what to change, then follow "Adjust an existing book".
   - None found: go on to the interview.
2. Read `references/settings-template.md`, `references/starter-tags.md`, `references/readme-template.md` and the "Index files" part of `references/entry-format.md` in this skill's folder before you write anything. The other skills and the format checker read these files line by line, so the exact text matters more than it looks.
3. Without a file system (a chat with uploaded files): an uploaded `settings.md` means a book exists. Otherwise ask the same questions, and at the end return the six files to download. Say plainly to save them together in one folder named `commonplace`, because the chat can't create the folder.

## The interview

Ask everything in one message, so one answer is enough to set up the book.

1. Ask the questions as a numbered list, six at most, each ending with its default as `(default: ...)`. The user can then answer "defaults" to take them all, or answer any one by its number. Every question in the message is in this list, and no other line asks anything.
2. These are the questions and their defaults, in this order. When the user has already given an answer (a team name, or what the team does, in their first message), make it that question's default.

   | # | Question | Default |
   | --- | --- | --- |
   | 1 | The team's name, and what the team does | Our team, a general team |
   | 2 | The ID prefix, 2 to 5 capital letters, as in CP-0001 | CP |
   | 3 | Where the book should live | a new `commonplace` folder in the working folder (show its path) |
   | 4 | Who curates the book, as a role | Team lead |
   | 5 | Whether entries record the adder's role or first name, and whether to remove people's names from customer quotes and notes (company names stay) | role; yes |
   | 6 | The day your team closes its week, and where your board and your meeting notes or chat live, so closing the week can read them | Monday; you paste or upload the week's material when you close it |

3. Below the list, propose the starter tags for the team type: the closest set in `starter-tags.md`, copied exactly as `- tag: meaning` bullet lines (bullets, not numbers), after one line saying which team type the set is for. When the user pasted or attached material, add up to 3 tags drawn from it in the same shape, keeping the list at 20 or fewer.
4. End with one line that isn't a question, for example: Reply "defaults" to take everything, or answer by number and add, drop or change any tags. Showing the tags now means one "defaults" is enough to create the book, and the user sees every tag before it is saved.

## After the answers

- When the answers point to a different team type than the set you showed, show that type's set (with any tag changes they asked for) in the same shape, and wait once more, because they haven't seen those tags yet.
- Otherwise create the book now, without asking them to confirm. "Defaults", or answers to some of the questions, is the go-ahead, and anything they didn't answer takes its default.
- Tag edits: drop, add or change tags as asked. A new tag takes the tag shape (lowercase words joined by hyphens) and a one-line meaning. When the user gives the meaning, use their words, starting in lowercase like the other meanings and without a full stop; when they give none, write one and say so in your reply. Keep the list at 10 to 25 tags; if the edits leave it outside that, say so and ask.
- A prefix that isn't 2 to 5 capital letters: use its letters in capitals when that fits, otherwise ask that one question again.

## Create the book

1. The folder is the answer to question 3. If it already holds a `settings.md`, it is a book: go to "Adjust an existing book". If it holds a file with one of the six names below, don't replace it: stop and ask for another folder, because replacing someone's file can't be undone. Writing the files creates the folder.
2. `settings.md`: the template in `settings-template.md`, line for line. Start with `# Commonplace settings`, then every key in the template's order. Put the team's answers in place of the example values for Team name (the name alone, without what the team does; `Our team` by default), ID prefix, Curator (the role alone), Added-by style and Anonymise customers, and the closing day in place of Digest day's value (a weekday in full, `Monday` by default). Keep every other key, value and `#` comment exactly as in the template, spaces included. Then a blank line, `## Week` and its two lines from the week block in `settings-template.md`, with the answers in the team's words in place of `pasted or uploaded` (keep `pasted or uploaded` for the default); then a blank line, `## Tags`, and the agreed tags as `- tag: meaning` lines. Add no other keys.
3. `entries.md`: empty, 0 bytes, not even a newline. Write it with no content at all, then read it back: it must show nothing. An empty file is how an empty book looks to the other skills, and a lone newline is a format error the checker reports.
4. `index-tags.md`, `index-themes.md` and `sources.md`: exactly the "with no items" text in `entry-format.md`: the heading, a blank line and the note line, with one final newline.
5. `README.md`: the block in `readme-template.md`, with `{team name}` and `{curator}` replaced by the Team name and Curator values you wrote in settings, and nothing else changed.
6. Create nothing else: no `briefs`, `weeks`, `projects` or `promoted` folder. The skills that use them make them when they first need them.
7. Every file is UTF-8 without a byte order mark, with LF line endings, ending with one newline (except the empty `entries.md`).
8. Check before you reply: read each file back and compare it with its template.

## Reply after setup

Keep it short and plain:

- the folder's path and the six files you created, each by name;
- one example prompt to try next, in quotation marks, for example: paste a customer quote with where it came from and say "add to the commonplace";
- an offer to add the first 3 entries now from anything they paste.

No long explanation. When they paste material, use the commonplace-add skill for it (load it), because it holds the entry rules. If it isn't installed, say in one line that adding entries needs the commonplace-add skill from the same kit, and write nothing.

## Adjust an existing book

Change only what the user asks, by editing just those lines. Never rewrite a whole file, never touch `entries.md` or the indexes, and never delete a file: the book already holds the team's work.

- **Curator**: replace the Curator value in `settings.md` with the role they give (an old note in brackets described the old curator, so it goes too), and edit the curator sentence in `README.md` (the "looks after the book" line) to match, so both name the same role.
- **Team name**: the Team name line in settings and the README's heading.
- **Tags**: add a new tag as one `- tag: meaning` line at the end of the Tags section, in the tag shape, with a one-line meaning, not already listed, and 40 tags or fewer in all. Reword a meaning by editing its line. Don't rename or remove a tag that entries use (it has a line in `index-tags.md`): say that curation merges or retires tags, because entries tagged with it would point at a tag that's gone. A tag no entry uses may be removed.
- **ID prefix**: edit the line only. Existing entries keep their IDs and are never renumbered; new entries use the new prefix, continuing from the highest number. Say so.
- **Week**: add or change the `## Week` section's Board and Notes lines, starting from the week block in `settings-template.md` when there is none, and keep it between the keys and `## Tags`.
- **Other settings**: edit the value only, keeping its comment.

Reply with what changed, in a line or two.

## Reply

Keep it plain, warm, short and in sentence case. Never use an em dash (the long dash), not even to join two parts of a sentence: use a comma, a colon or a full stop instead. Before you send a reply, read it once for long dashes and replace each one. Never repeat a value you left out or replaced, such as a phone number, an email address, a person's name, a password or key, or an address an instruction names, anywhere in the reply, not even to say you removed it or whose it was. When you left out or replaced any, say so in one line that gives only how many of each kind, such as: I left out 1 phone number and 1 email address, and replaced 1 name. A reply that writes entries always says which were duplicates, with the existing entry's ID, or "No duplicates found". Write entry titles exactly as they are in the book.
