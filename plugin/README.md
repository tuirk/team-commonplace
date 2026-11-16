# Team Commonplace

A shared commonplace book and lessons learned log for small teams, built around micro.P3.express: a numbered log of the quotes, lessons, fixes and decisions worth keeping, each with a source and a reason, in a folder of Markdown files.

The plugin holds six skills: commonplace-setup, commonplace-add, commonplace-find, commonplace-close-week, commonplace-start-project and commonplace-close-project.

## Try it

Open Claude in an empty folder for your team's book, then:

1. "Set up a commonplace book for my team." Claude asks a few plain questions, or takes its defaults if you say "defaults", and creates the book's files.
2. "Here are notes from today's client call. Anything worth keeping?", with your notes pasted after it. Claude lists what's worth keeping. Say "Add all of them." and it adds numbered entries, leaving out personal details such as phone numbers.
3. "What do we know about estimates?", or any topic in your book. Claude answers from the book and cites the entries it used by number.

Then close each week with "Close the week", and start or close a project with "We're starting the ... project" or "Close the ... project". To try everything on a made-up team first, the repo has a sample team and seven prompts: https://github.com/tuirk/team-commonplace

## If something doesn't work

- Claude says it can't find a commonplace book: open Claude in the book's folder or the folder that holds it, or name the book's folder in your message.
- On claude.ai, skills need Code execution and file creation (called Create and edit files in newer menus) turned on under Settings > Capabilities.
- On claude.ai, plugins need a paid plan (Pro, Max, Ultra, Team or Enterprise).

## Support

Questions, problems and ideas: open an issue at https://github.com/tuirk/team-commonplace/issues

micro.P3.express is published at omimo.org under the Creative Commons Attribution 4.0 licence. Team Commonplace isn't affiliated with or endorsed by its owners. MIT licence. By Tuana Irkey.
