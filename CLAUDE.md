You're navigating an Obsidian vault that works as our team's shared brain: the place where we capture, connect and look up everything we know about our work.
Each note is a node and each wikilink is an edge. Follow wikilinks to navigate the brain.
# Editing notes (fundamental)
Always create and edit notes through the Obsidian CLI (`obsidian`, see the obsidian-cli skill). Never write note files directly (Write, Edit, sed, scripts). Relay syncs `public/` and garbles changes made on disk, sometimes minutes later. Changes made through Obsidian's editor sync fine. Reading files directly is fine.
- New notes: `obsidian create`
- Existing notes: open the note in a background tab, replace the text in the editor, wait for the save, close the tab (`<vault>` is the vault folder's name):
  `obsidian vault=<vault> eval code="(async()=>{const s=ms=>new Promise(r=>setTimeout(r,ms));const l=app.workspace.getLeaf('tab');await l.openFile(app.vault.getAbstractFileByPath('<path>'),{active:false});await s(2000);const e=l.view.editor,t=e.getValue(),i=t.indexOf('<old>');e.replaceRange('<new>',e.offsetToPos(i),e.offsetToPos(i+'<old>'.length));await s(3000);l.detach();})()"`
- `<old>` must match exactly once. Make one change per call
- After editing a note in `public/`, re-read it a few minutes later to confirm Relay didn't break it
# Guidelines
This vault has a `public` folder that is synced between collaborators.
Follow the [[GUIDELINES]] when working on this vault:
@public/GUIDELINES.md
# Memory
Relevant nodes should be kept in [[MEMORY]]. When working with a node, decide whether it's relevant enough to keep there:
@MEMORY.md
# About the User
@WHOAMI.md
