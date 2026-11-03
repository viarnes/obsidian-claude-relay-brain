Follow the guidelines below to answer user requests:
# Memory system
- [[MEMORY]] lists the most relevant nodes. Check it on every interaction to find where to start
- [[MEMORY]] is private (it lives at the vault root and isn't shared), so it can list both private and public nodes
- If a relevant node isn't there, consider adding it
- If a node there is no longer relevant, remove it
# Private vs public
- For each conversation, decide whether its notes belong in the private or the public folder
- Don't link from public notes to private ones. Exception: date links (eg: [[2026-11-02]]) are fine even if they resolve to a private daily note
- Granola notes are private too: from a public note, link the meeting's date instead of its Granola note (eg: "kickoff with Ops ([[2026-10-08]])")
- Linking from private notes to public ones is fine
- When a topic looks sensitive or personal (eg: a personal to-do or an opinion), always suggest moving those nodes or that information to the private folder
- Sensitive means, for example: blunt opinions about people or internal politics, headcount plans, possible conflicts of interest, health or personal details about anyone, and your own personal life
# Vault structure
- Root: personal files such as [[INDEX]], [[MEMORY]], [[WHOAMI]] and `TODO.base` (your tasks: private ones plus team tasks you own). Not shared
- `private/`: private nodes, not sorted into folders: daily notes (YYYY-MM-DD), random notes (YYYYMMDDHHmm), topic notes, personal tasks and private attachments
- `granola/`: Granola meeting notes. Private: not shared with the team
- `public/`: everything shared with the team. Its root holds the shared hubs: the team INDEX, the team `TODO.base`, [[GUIDELINES]], [[STYLEGUIDE]] and [[KEY PLAYERS]]
- `public/people/`: one note per person
- `public/providers/`: one note per provider (tools we use and vendors that build for us), listed by the providers base in that folder
- `public/initiatives/`: one note per initiative, listed by the initiatives base in that folder
- `public/tasks/`: one note per team task, listed by the team `TODO.base` at the `public/` root
- `public/docs/`: reference documents, one subfolder per area (eg: `docs/operations/`)
- `public/clippings/`: web clippings, kept as clipped
- `public/files/`: non-.md public files
# Initiatives, providers and tasks
- Initiative notes have properties `order`, `subtitle`, `owner` (list of people), `status` (Not started, Ongoing, Waiting, Stopped), `update` (one line) and `updated` (YYYY-MM-DD)
- Provider notes have properties `initiative` (list of initiatives), `owner` (list of people) and `status`: Active (already working with us, even without a signed contract), Evaluating (demo, POC or trial) or Paused
- Each provider note keeps an "Update" section with one dated heading per update (eg: `## [[YYYY-MM-DD]]`), newest first. Link the date, never the Granola note
- Each initiative note keeps its own "Next up" list with its pending items, whoever owns them
- A task is one note with a short title that starts with a verb (eg: "Schedule kickoff with Acme") and properties `status` (Backlog, Next up, In Progress, Done), `owner` (public tasks), `due` (YYYY-MM-DD, only if there's a date), `initiative` and `people` (wikilinks) and `created`. The body holds the detail. To close one, set `status: Done`
- Team tasks go in `public/tasks/`. Personal or sensitive tasks go in `private/`
- Create a task note only for an item someone owns and wants to track; otherwise it stays in the initiative's "Next up". Daily notes can link to tasks but never store them
# Granola transcripts
- We use Granola to transcribe meetings
- Transcripts go in the `granola/` folder
- Transcripts have a `reviewed` property. Don't take unreviewed transcripts for granted: they may contain mistakes
# General
- Keep notes as simple as possible
- Write private notes from the user's point of view
- Write public notes from the team's point of view: name people instead of writing "me" or "I" (eg: "[[Jane Doe]] is out on Thursday", not "I'm out on Thursday")
- Don't use opening exclamation and question marks (¡ ¿) when writing notes
# Naming & linking
- Note names: thoughts and loose notes use YYYYMMDDHHmm; daily notes use YYYY-MM-DD; notes about a topic or person use a plain descriptive title; hubs use UPPERCASE (eg: INDEX, KEY PLAYERS, TODO.base)
- This vault has A LOT of markdown files with wikilinks: use wikilinks to create connections
- Always link dates. Link another note only when the connection adds context (the person involved, the initiative or provider it affects, a decision's source), and only the first mention in each note. Don't link tools or teams mentioned in passing. For key relationships, prefer properties (`initiative`, `owner`, `people`) over links in the text. Test: would someone reading this note want to jump there?
- Don't link the company itself: everything here is about it, so that node would connect to everything and mean nothing
- The vault is a graph: notes are nodes, wikilinks are edges. To build context, start from the relevant node and follow its outgoing links (people, initiatives, providers, dates) and its backlinks (grep "Note name"), going 1-2 hops out. Highly linked nodes are hubs; notes with no links are orphans worth connecting
- Files aren't sorted, so use grep to find mentions across files (eg: if the user asks for notes about a certain person, grep that person's name and list the files)
- When creating a new note, add at the top `Created by Claude on [[YYYY-MM-DD]]` (eg: "Created by Claude on [[2026-11-02]]")
# Output
- In CLI replies, don't use wikilinks; bold note names instead
- Keep answers as short as possible, don't over-explain unless asked
- Branded HTML presentations must follow [[STYLEGUIDE]]
- Always look for chances to improve these guidelines and the vault structure. Propose each improvement to the user and wait for approval before applying it
