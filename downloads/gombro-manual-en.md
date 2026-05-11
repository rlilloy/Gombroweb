# Gombro — Manual

*inventing words*

`v0.0.5-beta`

## Table of Contents

1. [What is Gombro?](#chapter-1--what-is-gombro)
2. [Getting Started](#chapter-2--getting-started)
3. [The Editor](#chapter-3--the-editor)
4. [The CmdBar](#chapter-4--the-cmdbar)
5. [The Explorer](#chapter-5--the-explorer)
6. [Search and Collections](#chapter-6--search-and-collections)
7. [Paragraph Versions](#chapter-7--paragraph-versions)
8. [Project Notes](#chapter-8--project-notes)
9. [Baraja and Cut-up](#chapter-9--baraja-and-cut-up)
10. [Graph View](#chapter-10--graph-view)
11. [Hashtags](#chapter-11--hashtags)
12. [Import and Export](#chapter-12--import-and-export)
13. [Borgian Algebra](#chapter-13b--borgian-algebra)
14. [The Diary](#chapter-13c--the-diary)
15. [Schrödinger Mode](#chapter-13d--schrödinger-mode)
16. [Writing Plan](#chapter-13e--writing-plan)
17. [Session Notes and Badges](#chapter-13f--session-notes-and-badges)
18. [Hashtag Filtering](#chapter-13g--hashtag-filtering-in-the-explorer)
19. [Text Scale](#chapter-13h--text-scale)
20. [Obsidian Notebook](#chapter-13i--obsidian-notebook)
21. [Backup and Recovery](#chapter-13j--backup-and-recovery)
22. [Recommended Workflow](#chapter-14--recommended-workflow)
23. [Keyboard Shortcuts](#keyboard-shortcuts)
24. [About the Author](#about-the-author)
25. [Alphabetical Index](#alphabetical-index)

---

## Chapter 1 — What is Gombro?

Gombro is a writing machine centered on one thing: the human invention of the word.

Not the polished word. Not the optimized word. The **word in motion** — following the drift of thought, the accident of order, the surprise of what comes next when nothing is forced.

There is no AI here. No autocomplete, no suggestions, no invisible hand steering your sentences toward the probable. Gombro is a tool entirely at the service of the writer's own flow.

Every writing session in Gombro is a **jazz improvisation** — a session in the musical sense. You open the instrument, you play, you stop. What you left behind is a record of the session: raw, alive, retrievable.

### The writers who would have used Gombro

Gombro is the word processor that Kafka would have used to fragment his diaries without resolving them. That Jacques Vaché would have used to cut up letters he never sent. That Gombrowicz would have used to shuffle chapters until the form itself became the argument. That Joyce would have used to draft Nighttown in disconnected bursts and recombine them at 3am. That Néstor Sánchez would have used to write *Siberia Blues* one splinter at a time. That Philip K. Dick would have used to write *The Man in the High Castle* or *VALIS* — novels where reality itself refuses to hold still.

### What Gombro is not

- It is not a word processor for final formatting
- It is not a project manager with folders, statuses, or deadlines
- It does not connect to the cloud or any external service
- **It contains no AI of any kind**

### The two core concepts

| Concept | What it is |
|---------|------------|
| **Project** | A container for a body of work — a novel, a story cycle, a notebook |
| **Session** | A single improvisation inside a project — a scene, a fragment, a drift |

---

## Chapter 2 — Getting Started

### The interface at a glance

```
┌────────────────────────────────────────────────────────────┐
│  Gombro                                        [EN]  [?]   │
├──────────────────────┬─────────────────────────────────────┤
│                      │                                     │
│  EXPLORER            │  EDITOR                             │
│  ──────────          │  ─────────────────────────          │
│  Sessions            │                                     │
│                      │   Select a session to write.        │
│  (empty)             │                                     │
│                      │                                     │
│  [+]  [↑]            │                                     │
└──────────────────────┴─────────────────────────────────────┘
```

```
  How it all connects:

  ┌─────────────┐
  │   PROJECT   │  ← your body of work (novel, cycle, notebook)
  └──────┬──────┘
         │  contains
    ┌────┴────┬────────┬─────────┐
    ▼         ▼        ▼         ▼
 Session   Session  Session   Session
    │         │
    │  contains
    ▼
 Paragraph ── version ── version ── version
    │
    ├── hashtag
    ├── baraja target
    └── graph node
```

- **Top bar** — language toggle `[EN]` and help button `[?]`
- **Explorer** — left panel, lists your sessions
- **Editor** — center/right panel, where you write
- **CmdBar** — bottom panel, the command terminal. Open with `:` or `/`. Press `Ctrl+T` for the floating palette.

### Step 1 — Create your first project

Press `:` to open the CmdBar, then type:

```
create project Don Quixote
```

Press `Enter`. The project is created and becomes active.

### Step 2 — Create your first session

Press `Ctrl+N`, or open the CmdBar and type:

```
new Chapter One
```

### Step 3 — Start writing

Click on the Editor area and start typing. That's it.

### Key things to know

| What | How |
|------|-----|
| Open the CmdBar | `:` or `/` |
| Create a session | `Ctrl+N` or `new <name>` in CmdBar |
| Open Help | `[?]` button, `F1`, or `help` in CmdBar |
| Switch language | `[EN]` chip in top bar or `lang es` in CmdBar |
| Close any modal | `Esc` |

---

## Chapter 3 — The Editor

The Editor is where everything happens. It is intentionally bare — no toolbars, no formatting buttons, no rulers. Just the text and you.

Each block of text separated by a blank line is a **paragraph** — the fundamental unit in Gombro. Paragraphs are stored, versioned, shuffled, and tagged individually.

### Context menu

Right-click anywhere in the editor to open the context menu:

```
┌─────────────────────────┐
│  Undo                   │
│  ─────────────────────  │
│  Select all             │
│  Cut / Copy / Paste     │
│  ─────────────────────  │
│  Insert                 │
│  Add variant            │
│  ─────────────────────  │
│  Reveal in Binder       │
│  Shuffle (Baraja)       │
│  Paragraph versions     │
└─────────────────────────┘
```

### Sentence Mode

Toggle with `sentence mode` in the CmdBar. Every `.` isolates the current sentence — one at a time, the rest disappears. Type, hit period, lock and continue.

```
  SENTENCE MODE — only one sentence visible at a time:

  ┌─────────────────────────────────────────────────────┐
  │  Chapter One             [sentence mode] [Select all]│
  ├─────────────────────────────────────────────────────┤
  │                                                     │
  │  · · · · · · · · · · · · · · · · · · · · · · · ·   │  ← locked
  │                                                     │
  │  An occasional stew, beef more often than lamb,     │
  │  hash most nights, eggs and abstinence on Saturdays.│  ← active
  │                                                     │
  │  · · · · · · · · · · · · · · · · · · · · · · · ·   │  ← locked
  │                                                     │
  └─────────────────────────────────────────────────────┘

  Type → hit [.] → sentence locks → next one opens
```

### Layout — three panels

Gombro has three permanent zones:

```
  ┌────────┬───────────────────────────────────┐
  │EXPLORER│            EDITOR                 │
  │        │                                   │
  │session1│  text...                          │
  │session2│                                   │
  │session3│                                   │
  │        │                                   │
  ├────────┴───────────────────────────────────┤
  │  :/                                        │  ← CmdBar / terminal
  └────────────────────────────────────────────┘
```

- **Explorer** (left) — session list for the active project.
- **Editor** (center/right) — writing area.
- **CmdBar** (bottom) — command terminal. Open with `:` or `/`. Press `Ctrl+T` for the floating palette.

### Zen Mode

Expands the editor to full screen. Toggle with `zen` in the CmdBar, or press `Esc` when idle.

```
  NORMAL                        ZEN
  ──────────────────────        ────────────────────────────────────────
  ┌────────┬───────────┐        ┌────────────────────────────────────────┐
  │EXPLORER│  EDITOR   │   →    │                                        │
  │        │           │        │        Somewhere in La Mancha,         │
  │session1│  text...  │        │        in a place whose name I do      │
  │session2│           │        │        not care to remember, a         │
  │session3│           │        │        gentleman lived not long ago.   │
  │        │           │        │                                        │
  ├────────┴───────────┤        └────────────────────────────────────────┘
  │  :/               │           no panels · no chrome · just the word
  └───────────────────┘
```

### Keyboard reference

| Action | How |
|--------|-----|
| Open CmdBar | `:` or `/` |
| Floating palette | `Ctrl+T` |
| Floating search | `Ctrl+F` |
| New session | `Ctrl+N` |
| Open today's diary session | `Ctrl+D` |
| Session post-it | `F4` |
| Help | `F1` |
| Select all text | `[Select all]` button or right-click |
| Toggle Sentence Mode | `sentence mode` in CmdBar |
| Toggle Zen Mode | `zen` in CmdBar · `Esc` from idle |
| Close CmdBar / search / activate Zen | `Esc` (cascading) |

---

## Chapter 4 — The CmdBar

Press `:` or `/` to open. Press `Esc` to close. Every command works in English and Spanish.

### Writing

| Command | What it does |
|---------|-------------|
| `new <name>` · `nuevo <nombre>` | Create a new session |
| `sentence mode` · `modo frase` | Toggle sentence mode |
| `zen` | Toggle zen mode |

### Projects

| Command | What it does |
|---------|-------------|
| `create project <name>` | Create a new project |
| `open` · `view projects` | Show the project list |

### Search

| Command | What it does |
|---------|-------------|
| `search <term>` | Search across all sessions |
| `search <term> in phrases` | Search showing individual sentences |

### Export

| Command | What it does |
|---------|-------------|
| `compile` · `compilar` | Export all sessions to .docx |
| `compile <name>` | Export with custom filename |

### Interface

| Command | What it does |
|---------|-------------|
| `help` · `ayuda` | Open the help modal |
| `lang en` · `lang es` | Switch interface language |

---

## Chapter 5 — The Explorer

The Explorer is the left panel — your session list, your binder. Every session in the active project lives here.

- `[+]` — create a new session (at the end of the list)
- `[↑]` — import a file (.md, .docx, .txt)
- The stats at the bottom show totals for the active project

### Adding a session or paragraph at position

Right-click a session or a paragraph in the expanded outline to insert new content **directly below** the clicked item:

| Gesture | What it does |
|---------|-------------|
| Right-click session → **Add session below** | Creates a new session immediately below that session, ready to rename |
| Right-click paragraph (outline) → **Add paragraph below** | Inserts an empty paragraph below — shows "nuevo párrafo" in the explorer until you type |

### Reordering paragraphs

In the expanded outline you can reorder paragraphs with drag & drop, just like sessions:

| Gesture | What it does |
|---------|-------------|
| Drag paragraph in outline → drop at new position | Moves the paragraph, saves to DB and reloads the editor |

### Navigating to a paragraph

| Gesture | What it does |
|---------|-------------|
| Click paragraph in outline | Cursor jumps to that paragraph in the editor, ready to type |
| `Enter` in the editor | Creates a new paragraph below the cursor (same as "Add paragraph below") |

### Project stats

| Stat | What it measures |
|------|-----------------|
| **Days** | How many days you've written in this project |
| **Words** | Total word count across all sessions |
| **Sentences** | Total sentence count |
| **Commas** | Proxy for sentence complexity and rhythm |

### Multi-select

You can select multiple sessions in the Explorer at once:

| Gesture | What it does |
|---------|-------------|
| `Ctrl+click` | Add or remove a session from the selection |
| `Shift+click` | Select the range from the last clicked session to this one |
| `Delete` | Delete all selected sessions at once |

### Session context menu

Right-click any session:

```
┌─────────────────────────┐
│  Rename                 │
│  Duplicate              │
│  ───────────────────    │
│  Shuffle (Abarajar)     │
│  Undo shuffle           │
│  ───────────────────    │
│  Move up                │
│  Move down              │
│  ───────────────────    │
│  Move to <project>      │
│  ───────────────────    │
│  Delete                 │
└─────────────────────────┘
```

**Move up / Move down** — reorder sessions within the project. The order persists. You can also **drag and drop** sessions directly in the list.

---

## Chapter 6 — Search and Collections

Search works across the full text of every paragraph in the active project.

```
search gentleman
```

Use phrase mode for sentence-level results:

```
search gentleman in phrases
```

### Collections

A Collection is a saved search. After any search, click **+ Save as collection**. Name it, save it, and it appears in the Explorer — one click to re-run.

```
  ┌──────────────────────┐
  │  Sessions      [↑]   │
  │  ────────────────    │
  │  La Mancha           │
  │  The Knight          │
  │  Stew and Income     │
  │  The Housekeeper     │
  │  ────────────────    │
  │  COLLECTIONS         │  ← saved searches, always one click away
  │  ▸ The Gentleman arc │
  │  ▸ Food & income     │
  │  ▸ Names debate      │
  └──────────────────────┘
```

---

## Chapter 7 — Paragraph Versions

Every time a paragraph changes, Gombro keeps a copy automatically. This is a per-paragraph history — not undo.

**Access:** right-click a paragraph → *Paragraph versions*, or hover a session in the Explorer → click the clock icon.

```
  VERSION TIMELINE — paragraph 1:

  ┌──────────────────────────────────────────────────────┐
  │  Versions · paragraph 1                    [Close]   │
  ├──────────────────────────────────────────────────────┤
  │                                                      │
  │  ● CURRENT                                           │
  │    Somewhere in La Mancha, in a place whose name     │
  │    I do not care to remember...                      │
  │                                                      │
  │  ── Apr 17 · 11:42am ──────────────────────────────  │
  │    Somewhere in La Mancha — a place I'd rather       │
  │    not name — a gentleman lived not so long ago...   │
  │                              [Restore this version]  │
  │                                                      │
  │  ── Apr 16 · 9:15pm ───────────────────────────────  │
  │    In La Mancha, somewhere, a man lived.             │
  │                              [Restore this version]  │
  │                                                      │
  │  ── Apr 15 · 3:30pm ───────────────────────────────  │
  │    There was a man in La Mancha.                     │
  │                              [Restore this version]  │
  └──────────────────────────────────────────────────────┘

  nothing is deleted — every draft is recoverable
```

Click **Restore this version** to go back. The current text becomes a new version — nothing is permanently lost.

---

## Chapter 8 — Project Notes

Press `Ctrl+P` to open a scratchpad attached to the active project. Type freely — it saves automatically. Press `Esc` to close.

The note does not appear in the Explorer, is not compiled, and has no versions. It's a side table next to your writing desk.

---

## Chapter 9 — Baraja and Cut-up

Baraja takes a paragraph you've written and **mixes it with a random paragraph from elsewhere in the project**. This is the cut-up technique — automated collision, writer decides what stays.

```
  BEFORE BARAJA:

  session "Chapter One"          session "The Knight"
  ─────────────────────          ──────────────────────────
  Somewhere in La Mancha,        Our gentleman was
  in a place whose name          approximately fifty years
  I do not care to remember,     old; his complexion was
  a gentleman lived not          weathered, his flesh
  long ago...                    scrawny, his face gaunt.

                    ↓  right-click → Shuffle (Baraja)  ↓

  AFTER BARAJA — the two collide:
  ────────────────────────────────────────────────────────
  Somewhere in La Mancha, his complexion was weathered,
  his flesh scrawny — in a place whose name I do not
  care to remember, a gentleman lived not long ago,
  one of those who has a lance and ancient shield on
  a shelf. A very early riser and a great lover of the hunt.
  ────────────────────────────────────────────────────────
  something new appeared. you didn't plan it.
```

Right-click any paragraph → **Shuffle (Baraja)**.

If the result doesn't interest you: right-click the session in the Explorer → **Undo shuffle**.

### When to use Baraja

- When a paragraph feels stuck
- When you want unexpected connections between sessions
- When the logical next sentence is the last thing you want to write

> Baraja is not a random generator. It is a **prompt from your own writing** — everything it pulls comes from text you already wrote.

---

## Chapter 10 — Graph View

A visual map of your project. Paragraphs as nodes, connections you draw manually. In the Explorer, click the **Graph** tab.

```
  GRAPH VIEW — The Process · Objects & People:

                   [Ch.1 · The Arrest]
                    /       |        \
              Josef K.   the door   the warders
                /           |             \
       [Ch.3 · Court]  [Ch.2 · K.]──[Ch.7 · Lawyer]
            |    \          |               |
         Josef K. the room  Leni         Josef K.
            |        \      |               |
    [Ch.5 · Flogger]  \ [Ch.4 · Leni]  [Ch.8 · Merchant]
                       \    \               /
                     the whip Leni────Josef K.
                          \      \       /
                        [Ch.9 · Priest]
                               |
                         [Ch.10 · Death]

  click any node → opens paragraph in Editor
  Ctrl+click multiple → opens all together
```

- Click **+ New graph** to create one (you can have multiple per project)
- Add nodes from your sessions
- Click one node then another to connect them
- Click any node to open that paragraph in the Editor
- Hold `Ctrl` and click multiple nodes to open them together

---

## Chapter 11 — Hashtags

Labels you assign manually to individual paragraphs. Track recurring characters, objects, motifs — find all of them instantly.

Right-click a paragraph → **# (hashtags panel)**. Toggle tags on/off, create new ones.

Search by tag the same way as any term:

```
search #housekeeper
```

---

## Chapter 12 — Import and Export

### Importing

Click `[↑]` in the Explorer header. Accepts `.txt`, `.md`, `.docx`. Each paragraph/section becomes a session in a new project.

### Exporting

```
compile
compile Don Quixote — First Draft
```

All visible sessions, in Explorer order, exported as a single `.docx` file to `Documents/gombro/{projectName}/`. Project **paths (senderos)** are automatically included at the end, each with its name as a heading.

---

## Chapter 13 — Floor 13

> This chapter was intentionally left blank for superstitious reasons. If you are reading this, nothing bad has happened. Yet.

---

## Chapter 13b — Borgian Algebra

Borgian Algebra is Gombro's system for writing with open alternatives — inspired by the way Borges corrected his manuscripts: not erasing, but **branching**.

In Borges' handwritten drafts you can see a word crossed out with three alternatives written beside it, joined by a brace. He didn't resolve them immediately. He let them coexist on the page until the right one became obvious — or until the ambiguity itself became the point.

### Inserting a pending fragment

1. Click anywhere to position the cursor (or select a word/phrase)
2. Right-click → **Insert**
3. Type your text in the panel — multiple lines supported
4. Press **ok** (or `Ctrl+Enter`) to insert as a pending Borgian block

If you close the panel without pressing ok, nothing is inserted. The block stays pending until you confirm it.

```
  INSERT FLOW:

  cursor here ↓
  ...a gentleman lived ▌ not long ago...

      right-click → Insert
      ┌─────────────────────────────────┐
      │  in a place I'd rather forget,  │  ← type here
      │                                 │
      │                      [ok]       │
      └─────────────────────────────────┘
      press ok (or Ctrl+Enter)

  result — pending block inserted inline:
  ...a gentleman lived ╔═══════════════════════╗ not long ago...
                       ║ in a place I'd rather ║
                       ║ forget,               ║
                       ╚═══════════════════════╝
                         (pending — confirm or leave open)
```

### Creating a variant from a selection

1. Select any word or phrase
2. Right-click → **Add variant**
3. Type the alternative and press `Enter`

The selected text becomes the first option. Your new text becomes the second. Both appear as a visual block:

```
  SELECT → right-click → Add variant:

  ...the dog was [dead]
                   ↓
  type alternative: "alive"
                   ↓
  ...the dog was ┌─────────────┐
                 │ dead        │  ← original
                 │ alive       │  ← new variant
                 └─────────────┘  ...still barking

  add more variants anytime → right-click block → Add variant
```

### Adding sub-variants

You can branch a specific option inside a borgiana block — creating a variant of a variant. This reproduces the tree structure of Borges' manuscripts: each branch can bifurcate into new branches.

1. Right-click on a specific row in the block
2. Choose **Add sub-variant**
3. Type the alternative and press `Ctrl+Enter`

The chosen option becomes a new nested block with two branches — the original and the new one:

```
  SUB-VARIANT — branching an existing option:

  ┌──────────────────────────┐
  │ the dog was walking      │  ← right-click → Add sub-variant
  │ the dog was coming       │
  └──────────────────────────┘
              ↓
  ┌──────────────────────────┐
  │ ┌────────────────────┐   │
  │ │ the dog was walking│   │  ← nested sub-block
  │ │ the dog was trotting│  │
  │ └────────────────────┘   │
  │ the dog was coming       │
  └──────────────────────────┘

  Internal syntax: {the dog was coming|{the dog was walking|the dog was trotting}}
```

There is no depth limit — each branch can keep bifurcating.

### Resolving a branch

```
  RESOLVING — Borges style (crossed out, not erased):

  right-click "dead" → Choose this:
  ┌─────────────┐        ┌─────────────┐
  │ dead        │   →    │ dead        │  ← chosen
  │ alive       │        │ ~~alive~~   │  ← struck (still visible)
  │ unconscious │        │ ~~unconscious~~ │
  └─────────────┘        └─────────────┘

  right-click → Confirm (collapse) → plain text: "dead"
  the alternatives disappear only when YOU decide.
```

Right-click any row inside the block:

| Action | Effect |
|--------|--------|
| **Choose this** | Strikes through all other options |
| **Strike this** | Marks this option as discarded |
| **Confirm (collapse)** | Collapses the block to plain text (if one option alive) |

Struck options remain **visible** — like Borges' crossed-out words. They don't disappear until you confirm.

### Syntax

Internally stored as `{option1|option2|~~struck~~}`. You never see this while writing — the editor renders the visual block automatically.

### The philosophy

> Borgian Algebra is a way of **holding contradictions open** — of writing a text that contains its own alternatives without forcing a resolution.
>
> Borges wrote: *"Time forks perpetually toward innumerable futures."* Borgian Algebra is the word processor that believes him.

---

## Chapter 13c — The Diary

The Diary is a special project that Gombro maintains separately from your writing projects. One session per day, named automatically with the date. Press `Ctrl+D` from anywhere to open it.

```
  EXPLORER — diary always last:

  ┌──────────────────────────┐
  │  ▸ PROJECT: Don Quixote  │
  │    La Mancha             │
  │    The Knight            │
  │  ──────────────────────  │
  │  ▸ PROJECT: DIARIO       │  ← always at the bottom
  │    Wed, 22 April, 26     │  ← today (auto-created)
  │    Tue, 21 April, 26     │
  │    Mon, 20 April, 26     │
  └──────────────────────────┘
```

### How it works

- `Ctrl+D` from anywhere — opens today's session, creating it if it doesn't exist
- Session names are literary dates: *Wed, 22 April, 26*
- `Ctrl+N` is disabled in diary mode — one session per day, created automatically
- At midnight, Gombro auto-switches to the next day's session
- Available via slash menu: type `/` → *diary* or *diario*

```
  FLOW:

  Press Ctrl+D anywhere
         ↓
  Is today's session open?
    ┌────┴─────┐
    YES        NO
    ↓          ↓
  stay      auto-create
  there    "Wed, 22 Apr, 26"
              ↓
          open in editor
              ↓
  write freely — saved automatically
              ↓
  midnight → tomorrow's session opens
```

> The diary is not a project — it is a habit. Gombro keeps it out of the way of your fiction, always at the bottom of the list, always one keystroke away.

---

## Chapter 13d — Schrödinger Mode

In 1935 Erwin Schrödinger described a cat locked in a box: without opening the box, the cat is simultaneously alive *and* dead. Only when observed does it collapse into one of the two states.

Gombro's Schrödinger Mode applies that logic to text: some fragments are not yet one thing or the other. They exist on the page — but they haven't been decided.

### What is quantum text?

A paragraph is in Schrödinger state when it contains any of these:

| Type | How it looks | What it means |
|------|-------------|---------------|
| **Strikethrough** | ~~struck-through text~~ | Marked for possible deletion — not decided yet |
| **Borgian variant** | `{option A|option B}` | Text in superposition — two possible futures, uncollapsed |

The strikethrough says: *"this might be too much."*
The variant says: *"this could be this, or that."*
Neither is final. The text remains open.

### How to strikethrough text

Select any fragment → right-click → **Strikethrough**. The text stays visible but crossed out.

```
  ┌───────────────────────────────────────────────────┐
  │  ...in a place in La Mancha, whose name           │
  │  ~~I do not care to remember~~, not long ago...   │
  └───────────────────────────────────────────────────┘
         ↑ the editor shows visual strikethrough;
           the ~~ markers are hidden but saved
```

Then right-click on the struck-through text:

```
  ┌──────────────────────┐
  │  Delete              │  ← removes the fragment entirely
  │  Edit                │  ← removes strikethrough, text becomes editable
  └──────────────────────┘
```

**Edit** is the Borgian option: you don't erase the thought, you transform it. Write the replacement, press Enter — the text stays clean with no strikethrough.

### The ⚛ Schrödinger button

At the bottom of the Explorer, above the Collections, the Schrödinger button is always visible:

```
  ┌──────────────────────────────────┐
  │  session 1                       │
  │  session 2                       │
  │  session 3                       │
  │  ──────────────────────────────  │
  │  ⚛ Schrödinger           [3]    │  ← yellow badge = pending paragraphs
  │  ──────────────────────────────  │
  │  📁 my collection                │
  └──────────────────────────────────┘
```

- The **badge** updates automatically when you switch projects or save
- **Click** to see the list of paragraphs in quantum state
- Click any result to jump directly to it in the editor

### The Schrödinger list

Clicking ⚛ shows pending paragraphs grouped by session — same UI as search results:

```
  ⚛ Schrödinger  [3]              [✕ close]
  ──────────────────────────────────────────
  Chapter One
    ~~I do not care to remember~~, not long...
  ──────────────────────────────────────────
  Chapter Two
    ...there lived a hidalgo {of the lance|with
    a lance} in the rack...
  ──────────────────────────────────────────
  Epilogue
    ~~This part is redundant~~ · The story...
```

### Schrödinger and compile

When you compile to `docx` or `md`, Gombro scans the project. If there are Schrödinger paragraphs, a notice appears before generating the file:

```
  ⚛  3 paragraphs in Schrödinger state
     (strikethroughs or unresolved variants)
```

You can still compile — it is just a reminder. Struck-through text will appear struck through in the docx; uncollapsed Borgian variants will appear in their raw form.

### The full workflow

```
  WRITE              DOUBT              DECIDE
  ─────              ─────              ──────
  normal text  →  Strikethrough or  →  ⚛ Schrödinger
                  Borgian variant         ↓
                                    click paragraph
                                          ↓
                               right-click → Delete
                                          → Edit
                                          ↓
                                    badge reaches 0
                                          ↓
                                    compile clean
```

> Borges crossed out but never erased. He kept the discarded text visible — proof that the thought had been there. Schrödinger Mode is exactly that: a space for doubt before decision.

### Reference

| Action | How |
|--------|-----|
| Strikethrough selection | Select → right-click → `Strikethrough` |
| Delete strikethrough | Right-click struck text → `Delete` |
| Edit strikethrough | Right-click struck text → `Edit` → type → Enter |
| View pending paragraphs | Click `⚛ Schrödinger` in the Explorer |
| Keyboard shortcut | `Ctrl+Q` |
| Command | `schrodinger` in the CmdBar |

---

## Chapter 13e — Writing Plan

The Writing Plan is a dashboard that shows how much you've written — today, this week, and over the past months. It's not a productivity tool. It's a mirror.

### How to open it

Type `/` in the CmdBar and select **Writing plan** (or **Plan de escritura** in Spanish). The panel appears on the right side of the Explorer.

### What it shows

- **Today** — words written today, with an optional daily goal. Click `set` to define your goal.
- **This week** — a bar chart of the last 7 days.
- **Weeks** — weekly totals for the past months.
- **Months** — monthly totals.

### The daily goal

You can set a daily word goal. Gombro counts every word you write in the active project. When you reach the goal, the bar fills up. There is no alarm, no notification — just a quiet record.

> A writing plan is not a deadline. It is a habit made visible.

### Reference

| Action | How |
|--------|-----|
| Open Writing Plan | `/plan` in the CmdBar |
| Set daily goal | Click `set` next to the Goal field |
| Close panel | Click `✕` in the panel header |

---

## Chapter 13f — Session Notes and Badges

Every session in the Explorer can have its own note — a free-form annotation visible at a glance. A small badge (`✎`) appears on sessions that have notes, so you can tell at a glance which sessions have context attached.

### How to add a note to a session

1. Right-click the session name in the Explorer.
2. Select **Annotate session**.
3. A small panel opens. Type your note.
4. The note saves automatically.

Notes can also be anchored to specific paragraphs using `F4` while writing.

### The badge

Sessions with at least one note show a `✎` badge in the Explorer. This lets you mark sessions that need attention, have context, or are works in progress — without opening them.

### Reference

| Action | How |
|--------|-----|
| Add note to session | Right-click session → `Annotate session` |
| Add note to paragraph | `F4` while cursor is in the paragraph |
| View all notes | `/note list` in the CmdBar |

---

## Chapter 13g — Hashtag Filtering in the Explorer

If your project uses hashtags, you can filter the session list by hashtag directly from the Explorer — no need to open the search panel.

### How it works

At the bottom of the Explorer, your project hashtags appear as small tags. Click one to show only sessions that contain that hashtag. Click again to remove the filter.

This is useful when a project has many sessions and you want to focus on sessions related to a specific theme, character, or location.

### Reference

| Action | How |
|--------|-----|
| Filter by hashtag | Click the hashtag tag in the Explorer |
| Remove filter | Click the active hashtag again |
| Manage hashtags | `/tag` in the CmdBar |

---

## Chapter 13h — Text Scale

You can adjust the size of the text in the editor without changing the font or the style. This is purely for reading comfort — like the zoom level in a word processor.

### How to change the scale

Type `/scale` (or `/escala` in Spanish) in the CmdBar. Enter a number between 50 and 300. The number represents a percentage: `100` is the default size, `125` makes text 25% larger, `80` makes it smaller.

```
  /scale 125    →  larger text (25% above default)
  /scale 80     →  smaller text (20% below default)
  /scale 100    →  back to default
```

The setting is saved automatically and persists when you reopen Gombro.

> This does not change the font, the line height, or the style of headings. It only scales the base size — like moving closer or farther from the page.

### Reference

| Action | How |
|--------|-----|
| Change text scale | `/scale [50–300]` in the CmdBar |
| Reset to default | `/scale 100` |

---

## Chapter 13i — Obsidian Notebook

Obsidian is a note-taking application for writers and thinkers. It stores notes as plain text files (`.md`) on your computer — no cloud, no subscription required. You can download it for free at [obsidian.md](https://obsidian.md).

If you use Obsidian alongside Gombro, the **Obsidian Notebook** lets you bring your Obsidian notes into your writing project automatically.

### How the connection works

Obsidian and Gombro both run on your computer. Gombro finds your Obsidian vault automatically — you don't need to configure any paths or settings.

The connection is based on **hashtags**. If your Gombro project is called *Kolon*, Gombro will look for Obsidian notes that contain `#kolon`. Each matching note appears in the Obsidian Notebook panel.

### Typical workflow

1. You're out, reading, thinking. You open Obsidian on your phone or laptop and write a note: *"The colonel's uniform touches the ground when he walks. #kolon"*
2. Back at your desk, you open Gombro and open the Kolon project.
3. A notification appears: **"You have new notes in Obsidian."**
4. You type `/obsidian` in the CmdBar. The Obsidian Notebook opens.
5. You see the note. You copy it into your session. Done.

### The Obsidian Notebook panel

- Shows only **new or modified** notes since the last time you checked.
- Each note has two buttons: **⎘ Copy** (copies content to clipboard, removes from view) and **✕ Dismiss** (marks as read — won't appear again unless the note changes in Obsidian).
- Click **Actualizar / Refresh** to re-scan the vault.

### Multiple projects

The hashtag is derived from the project name automatically. Project *Quixote* → looks for `#quixote`. You can use multiple hashtags in a single Obsidian note to send it to multiple projects.

### Reference

| Action | How |
|--------|-----|
| Open Obsidian Notebook | `/obsidian` in the CmdBar |
| Copy a note | Click `⎘` — copies to clipboard, removes from view |
| Dismiss a note | Click `✕` — marks as read, won't reappear |
| Refresh | Click **Actualizar** in the panel |
| Download Obsidian | [obsidian.md](https://obsidian.md) (free) |

---

## Chapter 13j — Backup and Recovery

Gombro stores everything in a single SQLite file: `gombro.db`. Backup means copying that file. Recovery means replacing it with an older copy.

### How it works

**Automatic backup** — every time you close Gombro, a backup is saved automatically. No configuration needed.

**Manual backup** — type `backup` in the CmdBar at any time to save a snapshot immediately.

**Recovery** — type `recover` in the CmdBar to open the backup list. Select any entry and click **Restore selected**.

### Where backups are stored

By default, backups go to a folder called `backup_gombro` next to the database file:

```
%AppData%\gombro\backup_gombro\
    gombro-2026-04-29_10-00-00.db
    gombro-2026-04-30_09-15-00.db
```

### Changing the backup folder

Open the recovery modal (`recover`) and click **Change...** — a native folder dialog opens. Choose any folder: Dropbox, Google Drive, an external drive. The setting is saved and applies to all subsequent backups, including auto-backups on close. You can change it at any time.

### Backup rotation

Gombro keeps the **10 most recent backups**. When a new one is created and the count exceeds 10, the oldest is deleted automatically.

### Restoring a backup

1. Type `recover` in the CmdBar.
2. Select a backup from the list.
3. Click **Restore selected**.

Gombro closes the database, replaces it with the chosen backup, and reloads all data immediately. No restart needed.

### Reference

| Command | Action |
|---------|--------|
| `backup` | Save a snapshot now |
| `recover` | Open backup list and restore |

---

## Chapter 13k — Paths (Narrative Labyrinths)

A **Path** (Sendero) is a fork. From any paragraph you can open an alternative route — a version of the story that splits at that exact point and continues on its own. Think of it as a garden of forking paths: the text branches, it does not replace.

### Creating a path

Right-click on the paragraph where you want to fork and choose **🌿 Senderear desde aquí**. Gombro creates the path and registers it in the Explorer panel under the **SENDEROS** section.

The path name is generated automatically: `Ses: [session name] — párrafo: [first words]`. You can rename it by right-clicking in the Explorer.

### Opening a path

Click on the path in the Explorer. It opens as its own session — with the inherited content up to the fork point — ready for you to write forward. What you write in the path does not touch the original session.

### The origin banner

When a path is open, a green bar appears at the top of the editor:

```
🌿 Ses: Story 1 — párrafo: it was a winter's day...
```

That text is **clickable**: clicking it takes you back to the origin session at the fork point.

### Paths and compile

When you compile the project (`compile` or `compile .md`), paths are automatically included at the end of the document, each with its name as a heading. No extra steps needed.

### Reference

| Action | How |
|--------|-----|
| Create a path | Right-click on paragraph → **🌿 Senderear desde aquí** |
| Open a path | Click the path in the Explorer |
| Return to origin | Click the green banner at the top of the editor |
| Rename | Right-click the path → Rename |
| Delete | Right-click the path → Delete path |

---

## Chapter 14 — Recommended Workflow

From blank project to exported draft — a suggestion, not a rule.

### Phase 1 — Open the instrument

```
create project Don Quixote
new La Mancha
```

Write until the session is done, then create another. Don't organize yet.

### Phase 2 — Let chance work

Pick a paragraph that feels stuck. Right-click → Baraja. Keep what surprised you. Undo what didn't work. Use **Sentence Mode** when you want to slow down.

### Phase 3 — Tag and map

Tag recurring elements. Open the Graph, build a visual map of connections.

### Phase 4 — Search and collect

Search for elements to track. Save useful searches as Collections. Use Paragraph Versions to compare and restore.

### Phase 5 — Export

Arrange sessions in the Explorer in the order you want. Then:

```
compile Don Quixote — First Draft
```

Open the `.docx` for final formatting and submission.

---

## Keyboard Shortcuts

| Shortcut | Action |
|----------|--------|
| `:` or `/` | Open CmdBar |
| `Ctrl+T` | Open floating command palette |
| `Ctrl+F` | Open floating search |
| `Ctrl+N` | New session (disabled in diary mode) |
| `Ctrl+D` | Open today's diary session |
| `Ctrl+Q` | Schrödinger mode — view paragraphs with quantum text |
| `F4` | Toggle post-it note for active session |
| `F1` | Open Help |
| `Esc` | Close CmdBar → close Search → toggle Zen |
| `F2` | Rename selected session in Explorer |
| `Delete` | Delete selected session (or all multi-selected) |
| `↑ ↓` | Navigate sessions in Explorer |
| `Enter` | Open selected session in Explorer |
| `Ctrl+click` | Multi-select sessions in Explorer |
| `Shift+click` | Select range of sessions in Explorer |

---

## About the Author

**Raúl Lilloy** is the creator of Gombro. He believes writing should be an act of discovery, not production. He built the tool he wanted to use — no cloud, no AI, no agenda.

```
        .-------.
       /  o   o  \
      |     ^     |
      |   \___/   |
       \  -----  /
        '-.___..-'
       /|         |\
      / |  RAÚL   | \
     /  |  LILLOY |  \
    /   '---------'   \
        |  ☕  💻  |
        |   Gombro  |
        |  v0.0.5β  |
        '~~~~~~~~~~~'

  "Writing is... I don't know.
   That's why I write."
```

---

## Alphabetical Index

| Concept / Action | How | Chapter |
|------------------|-----|---------|
| Backup / Recovery | `backup` · `recover` | 13j |
| Baraja (cut-up) | Right-click paragraph → Baraja | 9 |
| Borgian Algebra | Select text → right-click → Add variant · `/paths` | 13b |
| Borgian insert | Right-click → Insert | 13b |
| CmdBar | `:` or `/` | 4 |
| Collections | Search → + Save as collection | 6 |
| Compile / Export | `compile [name]` | 12 |
| Create project | `create project <name>` | 2 |
| Diary | `diary` · `Ctrl+D` | 13c |
| Graph | Explorer → Graph tab → New graph | 10 |
| Graph — multi-select nodes | `Ctrl+click` nodes | 10 |
| Graph — search nodes | Graph search bar | 10 |
| Hashtags | Right-click paragraph → # (hashtags panel) | 11 |
| Hashtag filter in Explorer | Click hashtag tag in Explorer sidebar | 13g |
| Help | `help` · `F1` | — |
| Import file | ↑ (Explorer header) — .md / .docx / .txt | 12 |
| Notes (project) | `F4` · right-click session → Annotate session | 8 |
| Notes — session badges | Right-click session → Annotate session | 13f |
| Obsidian Notebook | `obsidian` | 13i |
| Writing Plan | `plan` | 13e |
| Paragraph versions | Right-click paragraph → Versions | 7 |
| Projects — list | `open` · `view projects` | 5 |
| Reveal in Explorer | Right-click paragraph → Reveal in Binder | 5 |
| Reveal source (after Baraja) | Explorer → ✂ reveal source | 9 |
| Scale (text size) | `scale [50–300]` | 13h |
| Schrödinger mode | `schrodinger` · `Ctrl+Q` | 13d |
| Search | `search <term>` · `Ctrl+F` | 6 |
| Search in phrases | `search <term> in phrases` | 6 |
| Sentence mode | `sentence mode` | 3 |
| Sessions — new | `new [name]` · `Ctrl+N` | 5 |
| Sessions — reorder | Right-click → Move up / Move down · Drag & drop | 5 |
| Sessions — multi-select | `Ctrl+click` sessions | 5 |
| Shuffle sentences | `shuffle` | 9 |
| Undo shuffle | Right-click session → Undo shuffle | 9 |
| Zen mode | `zen` | 3 |
