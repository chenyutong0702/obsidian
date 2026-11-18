# Real Chat — how to use

Auto-generated (v1.2.0). Regenerated on each update.

## Sessions & history
Five chats (1-5), each with own history, draft, model, pins, YOLO setting. Tabs auto-title from your first message.
Histories survive restarts. The ⋯ menu archives a session, opens history (reload any past chat), or exports to a note.

## YOLO mode
Header badge toggles YOLO for the current session (overrides the global default in settings). When ON, all file
changes apply with NO confirmation. Obsidian file history/trash is still your safety net. "Safe" shows when off.
When Safe asks before a change, the Apply changes / Cancel dialog no longer dismisses if you misclick on the dimmed
background around it — only the buttons (or Escape) decide, so a stray click can't silently cancel an edit.

## Memory & triggers
The file `_memory/real-chat.md` is read every message. Add a `## Triggers` section with commands like:

    - **add book**: when I say "add book <title>", append "- <title>" to "Reading/Reading list.md".

Type `add book Dune` to run it. "remember this: ..." appends to memory.

## Context
- "Ref note" feeds the open note. "Pin" keeps notes in context for the whole session (📌 chips).
- "@ note" / "Selection" / "Attach" add one-off context. Drag-drop text files too.

## Searching the vault
Two ways, both ranked (title, heading and tag matches count for more than body text; notes with all your words and
exact phrases rank highest; best matches first):
- Search box: the 🔍 Search button in the chat toolbar, or the command "Search vault (ranked)" (give it a hotkey for
  an Omnisearch-style popup). Type and results appear instantly. Arrow keys to move, Enter or click to open a note.
  No model call, no token cost.
- In chat: just ask ("find my notes about X", or /search). Slower and uses a few tokens, but the model can run several
  synonym searches and reason over the results, so it is better for conceptual "find notes about an idea" questions.

## Slash commands
Type `/` at the start of a line for a quick menu (/summarise, /search, /rewrite, etc).

## Context size
The bottom bar shows ctx ~Xk: the estimated tokens in your NEXT message (system + memory + ref + pins + history).
Click it for a breakdown showing what is taking the space. If it is heavy, trim the memory file, untick Ref note,
unpin notes, or clear/archive the session. (This is per-message context, not the running session total next to the cost.)

## Replies
Clickable links, Copy/Insert/New note/Retry, code blocks have Copy buttons, long replies collapse.
Any note/file the assistant creates or changes is auto-listed with a clickable link under the reply. Replies that ask
you to confirm or decide something get a highlighted left border so they stand out.
Regenerate last reply with a chosen model via the ⋯ menu. Per-reply and lifetime cost shown. A ⏱ timer shows think time.

## Inline edit
Select text in any note, run "Edit selection with Real Chat" (command palette / hotkey), say how to change it,
and it rewrites in place. No chat round-trip.

## Keys & voice
Enter sends, Shift+Enter newline, Esc stops. For voice, click the input and press Win+H (Windows dictation).

## Jump to latest
In a long chat, a round ↓ button appears at the bottom-right when you scroll up. Tap it to jump back to the newest
message (works on mobile too). While you are scrolled up reading, streaming replies no longer yank you to the bottom.

## Images & vision
DeepSeek has no image model, so images go to a separate provider you set in Settings (Vision provider).
Turn it on, paste a base URL, key and model (e.g. Gemini free tier or OpenRouter). Then paste, drag, or use the Image
button to attach a picture. A notice confirms which model will read it. An attached image STAYS attached (sticky chip)
so follow-up questions about the same picture keep reaching the vision model — tap × on the chip to remove it. While an
image is attached every turn is answered by the vision model and marked "Vision". The vision model runs the FULL tool
loop: it can see the image AND act on it in one go — e.g. "save this and tell me what it says" writes the real picture
into your vault (save_attached_image) and reads it back. It can also create/edit notes and search from what it sees.

## Web & files
When web access is on (Settings), the model can web_search, web_fetch and download_file.
download_file grabs an image or file from a URL and saves it to your download folder; embed with ![[path]].
## Vault housekeeping
It can also delete_note, rename_note and replace_in_note (targeted find/replace, safer than full rewrite).

## Advanced tools
Off by default (Settings, Advanced tools): run_command lets the model trigger Obsidian commands by id.
Enable only if you are comfortable with that.

## Web search note
DuckDuckGo needs no key; add a Brave or Tavily key for better search. Uses Obsidian requestUrl, so no CORS issues.

## Reasoning models
If you use a reasoning model (DeepSeek reasoner, or an OpenRouter thinking model), its chain-of-thought shows in a
collapsible "Thinking" block above the answer. It streams live, then collapses once the reply lands. The thinking is
display-only and is not sent back to the model on later turns.

## Long tasks
There is a 50-step tool-loop cap per turn. If a task hits it, the reply pauses with a Continue button — press it to
let the model carry on from where it stopped, rather than starting over.

## Limits
edit_note rewrites whole files. Vision cost is not tracked (DeepSeek pricing only).
Corrupted characters (lone surrogates from half-emojis, C0/C1 control chars, Unicode noncharacters) are stripped from every outgoing message so they no longer cause a provider 400.
