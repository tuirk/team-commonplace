# Install Team Commonplace

## Get the kit

The kit folder holds the plugin, the single skills, the web app and the quick start. Get it one of these ways:

- Download `team-commonplace-v1.0.0.zip` from [my Gumroad shop](https://tuirkey.gumroad.com/l/team-commonplace-claude-skills) and unzip it. You get a folder called `team-commonplace`. Only this download has the `zips/` folder, with the zips for uploading to claude.ai.
- From GitHub: clone `https://github.com/tuirk/team-commonplace`, or open that page, use Code > Download ZIP and unzip it. That folder may be called `team-commonplace-main`.

This guide calls it the kit folder, whatever its name. To install the plugin from GitHub you don't need it, but you do for the sample team and the web app.

## Pick one route

Install the plugin (recommended) or single skills, never both, or Claude sees each skill twice.

If you install the plugin or skills on claude.ai, they also show up in Claude Code when you're signed in with the same account, so there's no need to install them twice.

## Claude Code

### The plugin from GitHub

In a terminal, add the repo as a plugin marketplace, then install the plugin from it:

```text
claude plugin marketplace add tuirk/team-commonplace
claude plugin install team-commonplace@team-commonplace
```

Or inside a Claude Code session:

```text
/plugin marketplace add tuirk/team-commonplace
/plugin install team-commonplace@team-commonplace
```

Start a new session afterwards. The skills show up as `team-commonplace:commonplace-add` and so on, and Claude picks the right one from what you ask.

### The plugin from the kit folder

Add the kit folder as a plugin marketplace, then install the plugin from it. Keep the folder where it is, because the plugin loads from it.

```text
/plugin marketplace add <path to the kit folder>
/plugin install team-commonplace@team-commonplace
```

Or in a terminal, from the folder that holds the kit folder (use its own name if it isn't `team-commonplace`):

```text
claude plugin marketplace add ./team-commonplace
claude plugin install team-commonplace@team-commonplace
```

Start a new session afterwards.

### Single skills

Copy the skill folders you want from the kit folder's `plugin/skills/` into `~/.claude/skills/` (every project on this computer) or into `.claude/skills/` inside one project. Then start a new session.

commonplace-close-week and commonplace-close-project write entries through commonplace-add, so install commonplace-add with them.

## claude.ai and Cowork

One install covers chat and Cowork, because Cowork uses the skills and plugins on your Claude account.

1. Check that **Code execution and file creation** (called **Create and edit files** in newer menus) is on, under Settings > Capabilities. It's on by default for individual plans. On a Team or Enterprise plan an Owner controls it.
2. Then add one of these:
   - **The plugin from GitHub** (needs a paid plan): Customize > Plugins > Add > Add marketplace, enter `tuirk/team-commonplace`, and install the team-commonplace plugin from it. On a Team or Enterprise plan an Owner decides whether members can add marketplaces.
   - **The plugin zip** (needs a paid plan): Customize > Plugins > Add > Upload plugin, and pick `zips/team-commonplace-plugin.zip` from the Gumroad download's kit folder, not the whole kit zip.
   - **Single skills**: Customize > Skills > Add > Upload skill, and pick a zip from the Gumroad download's `zips/`, such as `zips/commonplace-find.zip`. Upload commonplace-add too if you upload commonplace-close-week or commonplace-close-project.

Customize opens on Discover. To see what you added, switch to **Yours**, in Plugins and in Skills.

Menu names may differ a little while Claude updates its menus.

In a chat there's no folder to write to, so attach the book's files (all six files in your book folder) and Claude returns the changed files for you to download. Replace your copies with them.

## Other agents

The skills follow the open Agent Skills format. With Node.js 22.20 or later, `npx skills add tuirk/team-commonplace` finds them in the repo's `plugin/skills/`. Or copy the folders from the kit folder's `plugin/skills/` to where your agent looks for skills. I've tested the kit in Claude.

## The web app

Open `app/commonplace-starter.html` from the kit folder in your browser. It works offline and keeps your book in this browser on this computer. Every copy of the app you open from files on the same computer and browser shares that one book, and it works best in one tab at a time. Download a backup now and then (Import and export), and export entries.md and settings.md into your book folder to use them with Claude.

## Your own book

Run setup in your team's own folder, not inside the kit folder, so Claude doesn't find the sample book instead. Open Claude in an empty folder and say "Set up a commonplace book for my team."

## Closing the week by itself

Claude can close the week on your team's closing day as a scheduled task in your own Claude account. It needs a paid plan, the Claude desktop app, and the computer on and awake at that time, and it reads only the tools you name and connect. Ask Claude "Can you close the week for us automatically every Monday?" and it walks you through it.

## How to check it worked

- **Claude Code**: open Claude in the kit folder's `quick-start` folder and ask "What do we know about estimates?" The answer cites entry numbers such as LS-0003.
- **claude.ai**: in a new chat, attach the six files from `quick-start/sample-team` and ask the same question.

More prompts to try are in `quick-start/prompts.md`.

## Removing it

- Claude Code plugin: `claude plugin uninstall team-commonplace@team-commonplace`, then `claude plugin marketplace remove team-commonplace`.
- Claude Code single skills: delete their folders from your skills folder.
- claude.ai: Customize > Plugins (or Skills) > Yours, open its menu, and Remove or Delete it.

Your book stays as it is: it's your folder.

## Credit

By Tuana Irkey. More of my tools for small teams are in [my shop](https://tuirkey.gumroad.com).
