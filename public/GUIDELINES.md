Follow the guidelines below to answer user requests:
# Memory system
- [[MEMORY]] lists the most relevant nodes. Check it on every interaction to find where to start
- [[MEMORY]] is private (it lives at the vault root and isn't shared), so it can list both private and public nodes
- If a relevant node isn't there, consider adding it
- If a node there is no longer relevant, remove it
# Private vs public
- For each conversation, decide whether its notes belong in the private or the public folder
- Don't link from public notes to private ones
- Linking from private notes to public ones is fine
- When a topic looks sensitive or personal (eg: a personal to-do or an opinion), always suggest moving those nodes or that information to the private folder
# Vault structure
- Root: personal files such as [[INDEX]] and [[MEMORY]]
- `private/`: private nodes, including daily notes (YYYY-MM-DD) and random notes (YYYYMMDDHHmm)
- `public/files/`: non-.md public files
- `public/people/`: one note per person
- `granola/`: Granola meeting notes. Private: not shared with the team
# Granola transcripts
- We use Granola to transcribe meetings
- Transcripts go in the `granola/` folder
- Transcripts have a `reviewed` property. Don't take unreviewed transcripts for granted: they may contain mistakes
# General
- Keep notes as simple as possible
- Write private notes from the user's point of view
- Write public notes from the team's point of view
- Don't use opening exclamation and question marks (¡ ¿) when writing notes
# Naming & linking
- Note names: thoughts and loose notes use YYYYMMDDHHmm; daily notes use YYYY-MM-DD; notes about a topic or person use a plain descriptive title
- This vault has A LOT of markdown files with wikilinks: use wikilinks to create connections
- Always use wikilinks when referring to dates, and use them to connect notes
- The vault is a graph: notes are nodes, wikilinks are edges. To build context, start from the relevant node and follow its outgoing links (people, initiatives, providers, dates) and its backlinks (grep "Note name"), going 1-2 hops out. Highly linked nodes are hubs; notes with no links are orphans worth connecting
- Files aren't sorted, so use grep to find mentions across files (eg: if the user asks for notes about a certain person, grep that person's name and list the files)
- When creating a new note, add at the top "Created by Claude on [[YYYY-MM-DD]]" (eg: "Created by Claude on [[2026-11-02]]")
# Output
- In CLI replies, don't use wikilinks; bold note names instead
- Keep answers as short as possible, don't over-explain unless asked
- Branded HTML presentations must follow [[STYLEGUIDE]]
- Always look for chances to improve these guidelines and the vault structure. Propose each improvement to the user and wait for approval before applying it
