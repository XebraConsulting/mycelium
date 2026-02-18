---
type: setup-guide
created: 2026-02-17
status: active
tags:
  - thread/emergent-agent-model
  - tooling
related:
  - "[[SYSTEM_SOUL]]"
  - "[[garden]]"
  - "[[state]]"
---

# Obsidian Setup Guide — Emergent Agent Scaffold

> How to open this system in Obsidian and get the most out of the metadata layer.

---

## Quick Start

1. **Open this folder as an Obsidian vault.** File → Open Vault → Open folder as vault → select this project root.
2. **Install the recommended plugins** (see below).
3. **Start navigating.** Click any `[[wikilink]]` to jump between membrane files. Open the Graph View to see the whole system at a glance.

---

## Recommended Plugins

### Dataview (essential)

**What it does:** Turns YAML frontmatter into live, queryable views — like a database on top of your markdown files.

**Why it matters here:** [[garden]] and [[state]] contain Dataview query blocks that generate live tables of active threads, growing items, and recent signals. Without Dataview installed, those blocks render as plain code.

**Install:** Settings → Community Plugins → Browse → search "Dataview" → Install → Enable.

**Settings to adjust:**
- Enable "Enable JavaScript Queries" if you want to write advanced queries later.
- Enable "Enable Inline Queries" for quick inline lookups.

### Graph View (built-in)

**What it does:** Visualizes the relationships between files as an interactive graph.

**Why it matters here:** The `related` field in each file's frontmatter and the `[[wikilinks]]` throughout the body text create a web of connections. Graph View makes the mycelium visible — you can see how [[SYSTEM_SOUL]] connects to every membrane file, how the archetype prompts relate to their membrane outputs, and where clusters of connection are forming.

**How to use:** Click the graph icon in the left sidebar, or use `Cmd+G` (Mac) / `Ctrl+G` (Windows).

**Useful filters:**
- Color nodes by `type` to see soul, signal, compost, garden, etc. as different colors.
- Color by `archetype` to see which files belong to which agent function.
- Filter to show only `membrane/` files for a focused view of the living system.

### Templates (built-in)

**What it does:** Lets you create new files from templates with pre-filled frontmatter.

**Why it matters here:** As the membrane grows, you'll create new signal entries, compost entries, and garden seeds. Templates ensure consistent frontmatter and structure.

**Suggested templates to create:**

**Signal template:**
```yaml
---
type: signal
created: {{date:YYYY-MM-DD}}
archetype:
status: active
tags:
  - thread/emergent-agent-model
related: []
---
```

**Learning template:**
```yaml
---
type: learning
created: {{date:YYYY-MM-DD}}
archetype:
status: active
tags:
  - thread/emergent-agent-model
related: []
---
```

**Compost template:**
```yaml
---
type: compost
created: {{date:YYYY-MM-DD}}
archetype:
status: active
tags:
  - thread/emergent-agent-model
  - season/composting
related: []
---
```

**Setup:** Settings → Core Plugins → Templates → Enable. Set your template folder to a `/templates/` directory.

### Optional: Tag Wrangler

Useful if you want to rename, merge, or reorganize tags across the vault as your taxonomy evolves. Keeps the tag system clean without manual find-and-replace.

---

## Metadata Structure

Every `.md` file in this system carries YAML frontmatter with a consistent schema:

| Field | Purpose | Values |
|---|---|---|
| `type` | What kind of document this is | `soul`, `signal`, `learning`, `compost`, `seed`, `decision`, `state`, `evolution`, `purpose`, `garden`, `arbiter`, `archetype-prompt`, `readme`, `setup-guide` |
| `created` | When the file was created | `YYYY-MM-DD` format |
| `archetype` | Which agent function this file belongs to (if applicable) | `sensing`, `creating`, `tending`, `composting`, `gardener` |
| `status` | Current lifecycle state | `active`, `dormant`, `composting`, `sprouting` |
| `tags` | Categorization array | See Tag Taxonomy below |
| `related` | Wikilinks to connected files | Array of `"[[filename]]"` strings |

---

## Tag Taxonomy

Tags follow a consistent naming convention across the system:

### Thread Tags
`#thread/[project-name]` — Track work across files by project or initiative.
- `#thread/emergent-agent-model` — The core framework
- `#thread/ai-literacy-curriculum` — The curriculum design work

### Season Tags
`#season/sprouting` — Fresh, unformed, just arrived
`#season/growing` — Active work, current energy
`#season/composting` — Energy shifted, insight being extracted
`#season/dormant` — Waiting for the right season

### Archetype Tags
`#archetype/sensing` — Originated from the Sensing function
`#archetype/creating` — Originated from the Creating function
`#archetype/tending` — Originated from the Tending function
`#archetype/composting` — Originated from the Composting function
`#archetype/gardener` — Originated from the gardener (human)

### Special Tags
`#crack` — Things that don't resolve. The Mbari Factor. Tensions held, not collapsed.

### Domain Tags
These emerge organically from the [[garden]] tag index. Examples:
- `#curriculum`, `#framework`, `#liberation-tech`, `#client`, `#nonprofit`, `#tooling`, `#personal-os`, `#systems`, `#business`, `#methodology`

*Add new tags as they emerge naturally. The taxonomy grows with the work.*

---

## Wikilinks

Every file references related membrane files using `[[filename]]` syntax. These create bidirectional links in Obsidian — click to navigate, and the "Backlinks" panel shows you everywhere a file is referenced.

Key links in the system:
- [[SYSTEM_SOUL]] — The fractal seed. Referenced whenever values, purpose, or ethical boundaries are invoked.
- [[state]] — The ambient awareness layer. Current context.
- [[signals]] — Cross-agent communication channel.
- [[garden]] — Where everything lives across seasons.
- [[compost]] — Failure processed into nutrition.
- [[learnings]] — Append-only learning log.
- [[evolution]] — How the system soul has changed.
- [[arbiter]] — Decision protocol for competing truths.
- [[purpose]] — The migration pattern of excitement.

---

## Dataview Queries

Two files contain live Dataview query blocks:

**[[garden]]** — Live views of:
- All active membrane files across the system
- Files in Growing / Sprouting seasons
- Recent signals

**[[state]]** — Live views of:
- Active threads across the system
- Growing items
- Recent signals

These queries pull from the YAML frontmatter in every file. As new files are added with proper frontmatter, they automatically appear in these views.

---

## Portability

**The core system is plain markdown and YAML.**

Everything in this scaffold — the membrane files, the system soul, the archetype prompts, the Garden, the metadata — is stored as standard `.md` files with standard YAML frontmatter. Nothing here requires Obsidian.

**What works everywhere:**
- All file content, structure, and voice
- YAML frontmatter (readable by any tool that parses YAML — Hugo, Jekyll, Logseq, Dendron, Notion import, custom scripts, etc.)
- `[[wikilinks]]` are supported by Obsidian, Logseq, Dendron, Foam, and many other tools
- The tag taxonomy (`#thread/name`, `#season/state`, etc.) works in any system that supports tags

**What is Obsidian-specific:**
- Dataview query blocks (the ` ```dataview ` code fences in [[garden]] and [[state]]). These render as live tables in Obsidian but display as inert code blocks in other editors. They are convenience layers only — no data lives inside them.
- Graph View visualization. Other tools have their own graph features, or you can visualize the `related` field with custom tooling.

**If you move to another tool:**
- The markdown files transfer as-is.
- YAML frontmatter is universally parseable.
- Wikilinks may need format adjustment depending on the target tool (some prefer `[text](path)` style links).
- Dataview blocks can be removed or replaced with the target tool's equivalent query language.

The system's intelligence lives in the files and their relationships — not in any particular tool.

---

*"The medium is not the message. The membrane is the message. The tools just make it visible."*
