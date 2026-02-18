---
type: state
created: [DATE]
status: active
tags:
  - thread/emergent-agent-model
related:
  - "[[SYSTEM_SOUL]]"
  - "[[signals]]"
  - "[[garden]]"
  - "[[purpose]]"
---

# Membrane — System State

> This file is the ambient awareness layer. Agents read it to understand what's happening across the ecosystem. Update it when context shifts.

---

## Current Context

**Gardener focus:** [What are you currently focused on?]
**Gardener energy:** [High / Medium / Low — be honest with yourself]
**Active threads:** [What's currently in motion?]

## System Health

**Coherence:** [Are agents aligned with the system soul? Any drift detected?]
**Pace:** [Is the system moving at the speed of trust, or outpacing the gardener?]
**Open questions:** [Unresolved things the system is holding]

## Recent Shifts

| When | What changed | Noted by |
|---|---|---|
| [DATE] | System initialized. Scaffold set up. | Gardener |

---

## Live Views (Dataview)

> These queries generate live views in Obsidian with the Dataview plugin. They are convenience layers — all underlying data lives in standard YAML frontmatter.

### Active Threads Across the System

```dataview
TABLE type AS "Type", status AS "Status", archetype AS "Archetype"
FROM ""
WHERE status = "active"
SORT type ASC
```

### Growing Items

```dataview
LIST
FROM ""
WHERE contains(tags, "season/growing")
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

*Agents: Update this file when you notice a shift in context, energy, or priority. Don't wait to be asked.*
