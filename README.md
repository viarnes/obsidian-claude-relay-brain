# Brain
A boilerplate for a collaborative Obsidian vault that works as a team's shared brain, built to be used with Claude Code.

- **Private and public notes.** Everything in `private/` is just for you. Everything in `public/` is shared with your team through Relay.
- **Shared rules for Claude.** The base `CLAUDE.md` points to the shared guidelines in `public/GUIDELINES.md`, so everyone's Claude follows the same conventions. It also loads `MEMORY.md`, your private list of relevant nodes.
- **Best with Claude Code.** Open Claude Code in the vault folder and ask things like:
  - "Summarize this week's meetings with X"
  - "Add a to-do for Y"
  - "Find anything I might be missing"
- **New to Obsidian?** Read [HOWTO](HOWTO.md) for the basics of Obsidian and this vault.

**This is an opinionated boilerplate: change whatever you want (and tell me if it worked).**
# Setup
1. **Get your copy.** Click **Use this template** on GitHub (or download the ZIP). Don't `git clone` this repo: your vault would keep it as its remote.
2. **Open it in Obsidian.** Choose "Open folder as vault" and pick the folder. When Obsidian asks, click **Trust author and enable plugins**.
3. **Make [INDEX](INDEX.md) your home.** It's your private map of the vault: link your hot nodes, to-dos and anything else you want at hand. Pin it (or delete it).
4. **Personalize `CLAUDE.md`.** Add any instructions you want Claude to follow when working with you. Shared rules belong in `public/GUIDELINES.md` instead.
5. **Set up Relay with your teammates** (see below).
# Working with your team
- The **Relay** plugin comes installed. Sign in from its settings, then one person shares the `public/` folder and invites the rest.
- Keep anything personal or sensitive in `private/`. It isn't shared with your team (Claude still reads it when you work with it).
- To share a note, move it from `private/` to `public/` (inside Obsidian, so links update).
- Only `public/` syncs. Changes to skills, `CLAUDE.md` or Obsidian settings have to be shared by hand.
# Syncing to GitHub (optional)
Relay already keeps everyone in sync, so you only need GitHub if you want version history or to use the brain with Claude remotely.

1. Create a Git repo in the vault root or in `public/`, depending on what you want to version. The included `.gitignore` leaves out `private/`, `granola/` and personal Obsidian state.
2. Push it to a private GitHub repo.
3. Optionally, install the **Git** community plugin to pull and push automatically.

**Recommendation:** run the GitHub sync on a single machine where nobody edits the vault directly (eg: an always-on server). Relay brings everyone's changes to that machine, and it alone pushes to GitHub. This avoids Git conflicts between teammates.
# Using the brain remotely with Claude
First, sync the vault to GitHub (see above) and connect GitHub to your Claude account. Then pick one:
- **To ask questions (read-only):** on claude.ai, create a project, add the repo to it, and say in the project instructions that Claude must follow the repo's `CLAUDE.md`. Works from anywhere, including your phone, but Claude can't write notes.
- **To read and write:** start a Claude Code session on the web (claude.ai/code) with the repo. It follows `CLAUDE.md` automatically. Its changes land on a Git branch: merge it, and they reach Relay once the sync machine pulls them.
# Skills
The vault ships with a few skills in `.claude/skills/`:
- **obsidian-\*** (by [kepano](https://github.com/kepano/obsidian-skills), MIT licensed): teach Claude Obsidian's markdown, Bases and CLI, so it handles the vault correctly.
- **granola-sync** (requires the Granola connector in Claude): imports your Granola meetings into a private `granola/` folder, one note per meeting. It covers today by default, or you can pass a date or a date range. Each note has three sections:
	- the meeting's to-dos,
	- possible transcript mistakes (misheard names, odd terms, phrases that don't make sense),
	- a summary.
# License
[MIT](LICENSE)
