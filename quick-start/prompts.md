# Prompts to try

Seven prompts to try on Larchmont Studio's book.

- In Claude Code, open Claude in this `quick-start` folder, so it finds the book in `sample-team`.
- On claude.ai, start a new chat and attach the six files from the `sample-team` folder. Claude gives you the changed files to download instead of changing your folder.

Try them in a copy of this folder if you want to keep the sample as it is.

## 1. Find what the team knows

> What do we know about estimates?

Claude answers from the book in a few lines and cites the entries it used by number, such as LS-0003.

## 2. Add from a call note

> Here are notes from today's client call. Anything worth keeping?

Paste the text of `raw/client-call-note.md` after it, or attach the file. Claude lists the things worth keeping as a numbered list. Then say:

> Add all of them.

Claude adds them as new numbered entries and says what it left out, such as phone numbers and email addresses.

## 3. Close the week

> Close the week. Here is this week's material: the cards we closed, a call note and our team chat.

Paste or attach the three files in `raw/week`. Claude suggests the things worth keeping from the week as a numbered list and asks which to add. Pick some, for example:

> Add 1, 2 and 4.

Claude adds the ones you picked and saves a short week note in `sample-team/weeks`.

## 4. Start a project

> We're starting the Marrowfen Flowers Valentine's Day orders project: a click-and-collect order page for their bouquets.

Claude gathers what the book already knows that bears on the project and saves a one-page note in `sample-team/projects`, citing entry numbers.

## 5. Close a project

> Close the Halden Bakery orders project.

Claude lists the project's entries and asks whether there are lessons the team talked about but never wrote down. Answer with one, for example:

> Yes, one we talked about but never wrote down: agree before launch who answers customers' questions about their orders. The bakery expected us to, and we spent the first week answering their customers for them. I'm the project manager.

Or say "No, write the page." Claude adds the lesson if you gave one, then saves a one-page "what we'd do differently next time" page in `sample-team/projects`.

## 6. Set up your own book

Open Claude in your team's own empty folder, not in this one, and say:

> Set up a commonplace book for my team.

Claude asks a few plain questions, or takes its defaults if you say "defaults", and creates the book's six files.

## 7. Close the week by itself

> Can you close the week for us automatically every Monday?

Claude explains, in a few short steps, how to set it up as a scheduled task in your own Claude account and what it needs. It doesn't set anything up by itself.
