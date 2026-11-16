# Team Commonplace

Team Commonplace is a free kit of Claude skills for keeping a small team's shared commonplace book, built around micro.P3.express, the open method for running small projects in weeks. It follows the team's week: start a project with what the team already knows, add lessons as they happen, close each week by keeping what's worth keeping, and close a project with what you'd do differently next time.

It has six skills, an offline web app and a made-up sample team. The book is a numbered log of the customer quotes, lessons learned, fixes, insights and decisions worth keeping, each with a source and why it matters, in plain Markdown files.

## What a commonplace book is

A commonplace book is a notebook of passages worth keeping, copied under topic headings so you can find them again. In the 16th and 17th centuries, keeping one was a standard way to read. John Locke's method for indexing one, printed in English in 1706, after his death, files each entry by the first letter and the first vowel of its heading. Thomas Jefferson kept one: most of its 407 passages were entered between the ages of 15 and 30. John Milton kept one too.

A team commonplace book is the same habit, shared. Every entry gets a permanent number, a source and a line on why it matters, so anyone on the team can find it again by number.

## Who it's for

Teams of 1 to 7 that plan and close their work in weeks: the micro-projects micro.P3.express is made for, and small studios, agencies and consultancies. It's for the person who coordinates the work, for the teammates who add to the book and look things up, and for a team of one.

## How it follows micro.P3.express

micro.P3.express asks teams to capture lessons as they go, not at the end, and to mark the important ones in each weekly close (E3) so they're easy to find later. Those lessons stay on each project's board, and nothing carries them into the next project. The book is where they go, so the next project starts from what the team already knows.

Team Commonplace is built around [micro.P3.express](https://omimo.org/en/modules/micro.p3.express/), a way of running small projects in weeks. The method is published at omimo.org under the [Creative Commons Attribution 4.0 licence](https://creativecommons.org/licenses/by/4.0/). This kit is not affiliated with or endorsed by its owners. The step codes below are only labels:

- A3: set up the book with commonplace-setup.
- A4: start a project with commonplace-start-project.
- D1: add lessons, fixes and decisions as they happen with commonplace-add.
- E3: close the week with commonplace-close-week.
- F5: close a project with commonplace-close-project.

## What's inside

- **Six Claude skills**, as one plugin or as six single skills:
  - commonplace-setup makes a new book from a few plain questions, or adjusts one.
  - commonplace-add turns a quote, note, call, chat or article into numbered entries with a source, tags and why it matters, and leaves personal details out.
  - commonplace-find answers "what do we know about..." from the book and cites entry numbers.
  - commonplace-close-week reads the week's board, notes and chat, suggests what's worth keeping, adds the ones you pick and saves a short week note.
  - commonplace-start-project gathers what the book already knows that bears on a new project and saves a one-page note.
  - commonplace-close-project gathers a finished project's entries, asks about lessons nobody wrote down, and saves a one-page "what we'd do differently" page.
- **The Commonplace Starter**, a web app in one file (`app/commonplace-starter.html`) for adding and browsing entries without Claude, with import, export and print.
- **A quick start** with a made-up web studio of seven people, its book, some raw material to add and a week to close, plus the prompts to try (`quick-start/prompts.md`).
- **INSTALL.md**, the install guide, and the MIT licence.

## Try it on the sample team

The sample team lives in the kit folder. Get it by cloning this repo, with GitHub's Download ZIP, or as the download from [my Gumroad shop](https://tuirkey.gumroad.com/l/team-commonplace-claude-skills). Install the plugin (see "Where it runs" or INSTALL.md), open Claude in the kit folder's `quick-start` folder, and try these from `quick-start/prompts.md`:

1. "What do we know about estimates?" Claude answers from the sample book and cites entries such as LS-0003.
2. "Here are notes from today's client call. Anything worth keeping?", with the call note from `quick-start/raw/client-call-note.md` pasted after it. Claude lists what's worth keeping. Then say "Add all of them." Claude adds numbered entries and tells you what it left out.
3. "We're starting the Marrowfen Flowers Valentine's Day orders project: a click-and-collect order page for their bouquets." Claude saves a one-page note of what the team already knows.

## Where it runs

- **Claude Code**: add this repo as a plugin marketplace, then install the plugin. In a terminal:

  ```text
  claude plugin marketplace add tuirk/team-commonplace
  claude plugin install team-commonplace@team-commonplace
  ```

  Or in a session, `/plugin marketplace add tuirk/team-commonplace`, then `/plugin install team-commonplace@team-commonplace`. You can also install the plugin from a downloaded kit folder, or copy single skills into your skills folder (INSTALL.md). Claude Code isn't on the Free plan.
- **claude.ai and Cowork**: Customize > Plugins > Add > Add marketplace, and enter `tuirk/team-commonplace`; or upload the plugin zip. The upload zips are in the Gumroad download (the kit zip, free from [my Gumroad shop](https://tuirkey.gumroad.com/l/team-commonplace-claude-skills)), in its `zips/` folder. Plugins there need a paid plan (Pro, Max, Ultra, Team or Enterprise). Cowork uses the skills and plugins on your Claude account, so one install covers both.
- **Single skills on claude.ai**: Claude's help pages say skills work on every plan, Free included. If you don't see Upload skill (Customize > Skills > Add), use the plugin on a paid plan, or Claude Code.
- Skills need **Code execution and file creation** (called Create and edit files in newer menus) turned on under Settings > Capabilities. It's on by default for individual plans. On Team and Enterprise plans an Owner controls it.
- If you install on claude.ai, the same plugin or skills also show up in Claude Code when you're signed in with that account, so there's no need to install twice.
- **Other agents**: the skills follow the open Agent Skills format, so agents that read SKILL.md folders can use them. `npx skills add tuirk/team-commonplace` installs them (it needs Node.js 22.20 or later). I've tested them in Claude.
- **Without Claude**: the web app works on its own. Open `app/commonplace-starter.html` in a browser.

## What it's not good at

- Sharing by itself. The book is a folder; your team shares it the way you share any folder (a shared drive, a repo, a synced folder).
- Knowing what nobody wrote down. It keeps what the team adds, and it can ask about lessons people mention, but it can't invent them.
- Running when your computer is off. A scheduled close of the week runs on your computer, so it needs the computer on and awake, with the Claude app running.
- Very large books. Each entries file is meant to stay in the hundreds: past 400 entries, Claude offers to split it by year.
- The web app keeps one book per browser, and every copy of the app you open from files on the same computer and browser shares that one book. It works best in one tab at a time. Download a backup now and then.

## Privacy

Everything runs in your own Claude, your own browser and your own files. Nothing is sent to me, and there's no tracking or analytics. The skills remove personal details such as phone numbers and personal emails before they write an entry, keep sensitive entries out of shared notes, and read only the tools you name or point them to. They never post or send anything.

## FAQ

- **Is this made by Anthropic?** No. It's an independent kit built on Claude.
- **Is this a wiki or a knowledge base?** No. Team Commonplace keeps the short things a wiki never gets a page for, such as one quote, one fix or one lesson, each with a number, a source and why it matters. It sits beside your wiki or docs, not in place of them.
- **Do I have to pay for it?** No. The kit is free here, and the same kit is free on [my Gumroad shop](https://tuirkey.gumroad.com/l/team-commonplace-claude-skills), where you can pay what you want if it helps. Some Claude routes need a paid Claude plan (see "Where it runs").
- **Does it change anything outside the book folder?** No. The skills write only inside the book's folder, and they never delete an entry.
- **Can I use it without Claude?** Yes, with the web app.

Team Commonplace is independent. It isn't made by or affiliated with Anthropic, or with the owners of micro.P3.express.

## Licence

MIT. See LICENSE.

## Credit

By Tuana Irkey. More of my tools for small teams are in [my shop](https://tuirkey.gumroad.com).
