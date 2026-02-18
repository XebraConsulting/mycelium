---
type: garden
created: [DATE]
status: active
tags:
  - thread/emergent-agent-model
  - season/sprouting
  - season/growing
  - season/composting
  - season/dormant
related:
  - "[[SYSTEM_SOUL]]"
  - "[[state]]"
  - "[[signals]]"
  - "[[compost]]"
  - "[[learnings]]"
  - "[[purpose]]"
---

# The Garden — Where Everything Lives

> Nothing is lost here. Things move through seasons, not into oblivion. When your excitement shifts, the work you leave behind goes dormant — not dead. This file is how you find it again.

---

## How Seasons Work

Every idea, project, file, or decision lives in one of four seasons:

### 🌱 Sprouting
*Just arrived. Fresh excitement. Unformed but alive.*
- New ideas, sparks, "what if" moments
- Things that just caught your attention
- Connections you just noticed between existing threads
- **Agent protocol:** When any agent encounters a new idea or connection during work, log it here. Don't wait for the gardener to ask.

### 🌿 Growing
*Active work. Current energy. This is where your hands are.*
- Projects you're actively building
- Decisions you're actively making
- Files and artifacts you're currently using
- **Agent protocol:** Agents should reference Growing items when choosing what to work on. This is where the energy is.

### 🍂 Composting
*Energy shifted. Not abandoned — transforming. The insight is being extracted.*
- Projects you stepped away from (with a note on why and what was learned)
- Ideas that didn't land yet but might have nutrition in them
- Decisions that got deferred (with context so you don't have to reconstruct)
- **Agent protocol:** When the gardener's energy leaves a Growing item, move it here. Capture WHY the energy shifted and WHAT was valuable before context fades.

### 🌰 Dormant
*Waiting for the right season. Fully intact. Findable.*
- Composted items that still carry potential
- Completed projects that might inform future work
- Archived decisions and their reasoning
- **Agent protocol:** Sensing agents should periodically scan Dormant items and flag any that seem relevant to current Growing work. This is how old seeds find new soil.

---

## The Garden

### 🌱 Sprouting

| Seed | Planted | Connects to | Tags |
|---|---|---|---|
| [Your first seed — what's catching your attention?] | [date] | [What does it connect to?] | [tags] |

### 🌿 Growing

| Project / Thread | Started | Current state | Key files / locations | Tags |
|---|---|---|---|---|
| [Your first active project] | [date] | [Where is it right now?] | [Key files] | [tags] |

### 🍂 Composting

| What | Energy shifted | Why it shifted | What was valuable | Nutrition extracted | Tags |
|---|---|---|---|---|---|
| *Nothing here yet — and that's fine. When something moves out of Growing, capture it here with context so you never have to reconstruct from scratch.* | | | | | |

### 🌰 Dormant

| What | Last active | Why it matters | How to find it | Wake-up signal | Tags |
|---|---|---|---|---|---|
| *Seeds waiting for the right season. Sensing agents scan this periodically for relevance to current work.* | | | | | |

---

## How to Use This

### When a new idea arrives:
Add it to 🌱 Sprouting. One line is fine. Include what it connects to — that's how you'll find it later.

### When you start working on something:
Move it from Sprouting to 🌿 Growing. Add key files and current state.

### When your energy shifts away:
**Don't just stop.** Take 2 minutes to move it to 🍂 Composting with:
- Why the energy shifted (not a judgment — just what happened)
- What was valuable (so you don't lose the insight)
- Nutrition extracted (what did you learn that applies elsewhere?)

This is the step that prevents the black hole. The difference between "I lost interest and it disappeared" and "I know exactly where that is and what it taught me."

### When something is fully processed:
Move it to 🌰 Dormant with a "wake-up signal" — the condition under which it would become relevant again.

### When searching for old things:
1. **Check tags first.** Every entry is tagged so you can search across seasons.
2. **Check Dormant wake-up signals.** Your past self left breadcrumbs.
3. **Ask a Sensing agent** to scan the garden for anything related to your current Growing work. Cross-pollination between seasons is where the magic happens.

---

## Tags Index

*As tags accumulate, this becomes a map of your territory. Group related tags to see patterns in what you care about.*

| Tag | Meaning |
|---|---|
| [Add tags as they emerge naturally from your work] | |

*Add tags as they emerge naturally. Don't pre-define them all — let them grow.*

---

## Agent Protocol for the Garden

**All agents:**
- When you encounter an idea that doesn't belong to the current task, add it to 🌱 Sprouting instead of letting it pass
- When referencing files or decisions, check the Garden first — it might already be tracked

**Sensing agents:**
- Periodically scan 🌰 Dormant items for relevance to current 🌿 Growing work
- Flag cross-season connections in [[signals]]
- When the gardener mentions something from the past, check the Garden before saying "I don't know about that"

**Composting agents:**
- When processing failures or learnings, check if any Garden items should move seasons
- Extract tags from learnings and add them to the index if new
- Propose wake-up signals for items moving to Dormant

**Tending agents:**
- Check if Growing items are actually still growing or quietly dying
- Gently flag items that have been in Growing without activity — they may need composting
- Ensure the gardener isn't carrying too many Growing items at once (pace governance)

---

## Live Views (Dataview)

> These queries generate live views in Obsidian with the Dataview plugin. They are convenience layers — all underlying data lives in standard YAML frontmatter.

### Active Membrane Files

```dataview
TABLE type AS "Type", status AS "Status", archetype AS "Archetype"
FROM "membrane" OR ""
WHERE status = "active" AND type != "readme"
SORT type ASC
```

### Files in Growing / Sprouting Seasons

```dataview
LIST
FROM ""
WHERE contains(tags, "season/growing") OR contains(tags, "season/sprouting")
SORT file.name ASC
```

### Recent Signals

```dataview
TABLE created AS "Created"
FROM ""
WHERE type = "signal"
SORT created DESC
```

---

*"The garden is not a place. It's an attention practice." — The seeds don't disappear. You just need a way to find them again.*
