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
---

# Emergent Agent Model — Cursor Test Scaffold

## What This Is

A working test environment for the Emergent Agent Model — a framework for multi-agent AI systems designed as ecosystems, not armies. Built on Adrienne Maree Brown's Emergent Strategy principles.

No new technology required. Just files, folders, and agent prompts.

## Setup (2 minutes)

1. **Copy this entire folder** into a Cursor project (or open it as a project).
2. **Edit [[SYSTEM_SOUL]]** — fill in your purpose and customize values if needed.
3. **Start agent sessions** in Cursor, pasting the relevant archetype prompt from `.cursor/agents/[archetype].md` into the agent's system context.

That's it. The `.cursorrules` file ensures all agents follow the membrane protocol.

## Folder Structure

```
project-root/
├── SYSTEM_SOUL.md              ← The fractal seed (read by all agents)
├── .cursorrules                ← Global agent rules (auto-loaded by Cursor)
├── .cursor/
│   └── agents/
│       ├── sensing.md          ← Sensing archetype prompt
│       ├── creating.md         ← Creating archetype prompt
│       ├── tending.md          ← Tending archetype prompt
│       └── composting.md       ← Composting archetype prompt
├── membrane/
│   ├── state.md                ← System state and gardener context
│   ├── signals.md              ← Cross-agent signals
│   ├── learnings.md            ← Append-only learning log
│   ├── compost.md              ← Failure → nutrition processing
│   └── evolution.md            ← System soul change history
└── README.md                   ← You are here
```

## How to Test

### Test 1: Basic Membrane Flow
**Goal:** Verify that agents read from and write to the membrane.

1. Open a Sensing agent session. Give it a research task (e.g., "Research the current landscape of AI agent frameworks and summarize key trends").
2. After it completes, check: Did it update [[learnings]]? Did it post any signals to [[signals]]?
3. Open a Creating agent session. Give it a task that builds on the Sensing output (e.g., "Draft a short analysis of AI agent framework trends").
4. Check: Did it read the membrane before acting? Does its output reference what Sensing found?

**Success criteria:** Creating agent's output is demonstrably informed by Sensing agent's membrane entries without you manually copying information between them.

### Test 2: Failure Composting
**Goal:** Verify that failures become system nutrition.

1. Give a Creating agent an intentionally ambiguous task with insufficient context.
2. Let it struggle or fail.
3. Check: Did it write a compost entry in [[compost]]?
4. Open a Composting agent session. Ask it to process the compost heap.
5. Check: Did it extract patterns and post learnings? Did it update [[learnings]]?
6. Give the Creating agent the same task again.
7. Check: Does it read the compost/learnings and approach differently?

**Success criteria:** The system demonstrably learns from failure without you manually intervening.

### Test 3: Cross-Agent Sensing
**Goal:** Verify that agents sense each other's state.

1. Update [[state]] manually — set gardener energy to "low / overwhelmed."
2. Give a Creating agent a complex task.
3. Check: Does it simplify its output or acknowledge the energy state?
4. Have a Tending agent review the Creating agent's output.
5. Check: Does it flag pace or quality concerns based on the membrane state?

**Success criteria:** Agents adapt behavior based on membrane context, not just task instructions.

### Test 4: Emergence
**Goal:** See if the system produces insights no single agent generated.

1. Give a Sensing agent and a Creating agent the *same* open-ended problem from their different perspectives.
2. Have each update the membrane independently.
3. Open a Composting agent session. Ask it to synthesize across the membrane.
4. Check: Does the Composting agent surface a pattern or insight that neither Sensing nor Creating articulated?

**Success criteria:** The system produces something that didn't exist in any individual agent's output.

### Test 5: System Soul Evolution
**Goal:** Verify the feedback metabolism works end-to-end.

1. Run several tasks across multiple agents.
2. Ask a Composting agent to review the full membrane and propose system soul updates.
3. Check: Does it write a proposal in [[evolution]]?
4. Review the proposal as the gardener. Accept or modify.
5. Update [[SYSTEM_SOUL]] accordingly.
6. Run new tasks and check: Do agents reflect the evolved soul?

**Success criteria:** The system demonstrably evolves its own operating principles through lived experience.

## What to Watch For

### Signs the framework is working:
- Agents reference membrane content without being asked
- Later agents produce better output because earlier agents left learnings
- The compost heap fills up and becomes genuinely useful
- You start updating [[state]] naturally because agents actually use it
- Signals appear between archetypes that you didn't orchestrate

### Signs it needs tuning:
- Agents ignore the membrane and just do the task
- Membrane files fill with noise instead of signal
- The overhead of membrane updates slows agents down without adding value
- You find yourself manually copying context between agents anyway
- The system soul never evolves

## GitRepo = mycelium-model... Evolving toward mycelium-os. Not there yet. That's by design.

## Design by Jacob Turner (Xebra Consulting), 2026
Built on Adrienne Maree Brown's Emergent Strategy.
Framework developed in conversation with Claude Opus 4.6 (Anthropic).
