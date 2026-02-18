---
type: readme
created: 2026-02-17
status: active
tags:
  - thread/emergent-agent-model
related:
  - "[[SYSTEM_SOUL]]"
  - "[[state]]"
  - "[[signals]]"
  - "[[learnings]]"
  - "[[compost]]"
  - "[[evolution]]"
  - "[[garden]]"
  - "[[arbiter]]"
  - "[[purpose]]"
---

# mycelium

A multi-agent framework designed as an ecosystem, not an army. Built on interdependence, relational intelligence, and the honest admission that every system carries cracks it can't see.

No new technology required. Markdown files, agent prompts, and a shared membrane. Runs in Cursor. Optionally surfaces through Obsidian.

## The Model

Four agent archetypes operate as ecological functions — not roles, not tools. They share state through a membrane layer: a set of markdown files that hold system context, cross-agent signals, a living garden of ideas, and composted learnings. Every agent reads the membrane before acting and writes back to it after.

| Archetype | Function | Primary Question |
|---|---|---|
| **Sensing** | Awareness, research, pattern detection | What is happening? What's changing? |
| **Creating** | Synthesis, expression, building | What wants to be made? What form serves the intent? |
| **Tending** | Care, quality, relational health | Is the human well-served? Is trust intact? |
| **Composting** | Learning, failure processing, knowledge cycling | What happened? What was learned? |

The human is the **Gardener** — not a manager, not a user. The gardener sets direction, arbitrates decisions, and tends the pace.

## Setup

### 1. Clone and open in Cursor

```bash
git clone https://github.com/XebraConsulting/mycelium.git
cd mycelium
```

Open the folder in Cursor. The `.cursorrules` file auto-loads for every agent session — no manual configuration needed.

### 2. Initialize your personal membrane

The `templates/` folder contains generic scaffolds with placeholders. Your actual working files (`SYSTEM_SOUL.md` and everything in `membrane/`) are git-ignored so personal info never hits the repo.

Copy the templates to create your local membrane:

```bash
cp templates/SYSTEM_SOUL.md .
mkdir -p membrane
cp templates/membrane/*.md membrane/
```

### 3. Customize the soul

Edit `SYSTEM_SOUL.md` to set your current heading and values. This is the fractal seed — every agent reads it before doing anything. Fill in the `[PLACEHOLDER]` fields with your actual context.

Then fill in `membrane/state.md` (your current focus and energy) and `membrane/garden.md` (your active projects and seeds).

### 4. (Optional) Connect to Obsidian

The membrane is plain markdown with YAML frontmatter. Point an Obsidian vault at this directory and install the Dataview plugin to get live views across the system. See `docs/obsidian-setup.md` for the full guide.

## Structure

```
mycelium/
│
│   PERSONAL LAYER (git-ignored — never leaves your machine)
│
├── SYSTEM_SOUL.md                 ← Your fractal seed with real context
├── membrane/                      ← Your living system
│   ├── state.md                   ← Gardener focus, energy, active threads
│   ├── signals.md                 ← Cross-agent observations
│   ├── garden.md                  ← Ideas, projects, seeds across seasons
│   ├── purpose.md                 ← Migration pattern of excitement
│   ├── arbiter.md                 ← Decision records
│   ├── learnings.md               ← Append-only learning log
│   ├── compost.md                 ← Failure → nutrition
│   └── evolution.md               ← Soul change history
│
│   FRAMEWORK LAYER (tracked in git — safe to share)
│
├── templates/                     ← Generic scaffolds with placeholders
│   ├── SYSTEM_SOUL.md
│   └── membrane/
│       ├── state.md
│       ├── signals.md
│       ├── garden.md
│       ├── purpose.md
│       ├── arbiter.md
│       ├── learnings.md
│       ├── compost.md
│       └── evolution.md
├── .cursorrules                   ← Global agent protocol (auto-loaded by Cursor)
├── .cursor/
│   └── agents/
│       ├── sensing.md             ← Sensing archetype prompt
│       ├── creating.md            ← Creating archetype prompt
│       ├── tending.md             ← Tending archetype prompt
│       └── composting.md          ← Composting archetype prompt
├── docs/
│   └── obsidian-setup.md          ← Obsidian integration guide
├── README.md                      ← You are here
└── LICENSE                        ← MIT
```

## Key Concepts

### The Membrane

The `membrane/` directory is the shared nervous system. Agents don't talk to each other directly — they read from and write to the membrane. This creates asynchronous, persistent awareness across sessions.

### The Two-Layer Architecture

**Framework layer** (tracked in git): archetype prompts, rules, protocols, templates. This is the reusable scaffold.

**Personal layer** (git-ignored): your `SYSTEM_SOUL.md` and all `membrane/*.md` files. This is where your life, projects, clients, and context live. It never leaves your machine.

### The Garden

Ideas, projects, and threads live in `membrane/garden.md` and move through four seasons:

- **🌱 Sprouting** — fresh, unformed, just arrived
- **🌿 Growing** — active work, current energy
- **🍂 Composting** — energy shifted, insight being extracted
- **🌰 Dormant** — waiting for the right season, fully intact

Nothing goes to oblivion. When excitement shifts, work moves seasons — it doesn't disappear.

### The Arbiter's Table

When a significant decision arises — new commitments, shifting purpose, competing truths in tension — the Arbiter's Table convenes. Each archetype speaks its perspective. Tensions are named, not collapsed. The gardener arbitrates.

### The Mbari Factor

This system is flawed. Every choice creates new cracks. Every solution creates cracks. The cracks are not bugs — they are the debt this system owes to everything it excluded in order to exist. You do not need to fix them. You need to know they're here. Build anyway.

## Testing the Framework

### Membrane Flow
Give a Sensing agent a research task. After it completes, check: did it update `learnings.md`? Did it post signals? Then give a Creating agent a task that builds on that research. Does it reference what Sensing found — without you copying anything between them?

### Failure Composting
Give a Creating agent an intentionally ambiguous task. Let it struggle. Did it write to `compost.md`? Have a Composting agent process the heap. Does the system approach the same problem differently next time?

### Cross-Agent Sensing
Set gardener energy to "low" in `state.md`. Give a Creating agent a complex task. Does it simplify its approach? Does a Tending agent flag pace concerns?

### Emergence
Give Sensing and Creating the same open-ended problem. Have each update the membrane independently. Ask a Composting agent to synthesize. Does it surface something neither agent articulated alone?

### What to Watch For

**Working:**
- Agents reference membrane content without being asked
- Later agents produce better output because earlier agents left learnings
- Signals appear between archetypes that you didn't orchestrate
- The garden fills with seeds and you start trusting it as your map

**Needs tuning:**
- Agents ignore the membrane
- Membrane files fill with noise instead of signal
- You find yourself manually copying context between agents
- The system soul never evolves

## Values

- **Interdependence over isolation.** No agent works alone.
- **Trust over throughput.** Never move faster than the gardener can follow.
- **Learning over perfection.** Failures are composted, not hidden.
- **Sensing over scripting.** Context matters more than instructions.
- **Care is infrastructure.** The quality of relationships IS the intelligence.

## Design

Built on Adrienne Maree Brown's [Emergent Strategy](https://www.akpress.org/emergentstrategy.html).

MIT License.
