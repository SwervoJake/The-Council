# AI Agent Council — Setup Complete

This document confirms the Council infrastructure is in place and how to use it.

## Structure

```
council/
├── agents/                 # Agent profiles
│   ├── neo.json
│   ├── bruce.json
│   ├── cena.json
│   ├── luffy.json
│   ├── professor.json
│   ├── index.json
│   ├── professor/knowledge/   # Professor's knowledge base
│   ├── neo/
│   │   ├── memory/         # Neo memory bank (activeContext, progress, performance)
│   │   └── knowledge/      # Neo's knowledge base
│   ├── bruce/knowledge/    # Bruce's knowledge base
│   ├── cena/knowledge/     # Cena's knowledge base
│   └── luffy/knowledge/    # Luffy's knowledge base
├── shared/                 # Council-wide state
│   ├── constitution.md
│   ├── tasks.md
│   ├── learning_log.md
│   ├── decisions.md
│   ├── ledger.md
│   └── weekly_review.md
├── workspaces/             # Agent workspaces
│   ├── workspace-executive/
│   ├── workspace-builder/
│   ├── workspace-ascetic/
│   ├── workspace-gardener/
│   └── workspace-engineer/
├── memory/                 # Stratified memory
│   ├── episodic/
│   ├── principles/
│   ├── anti_patterns/
│   └── heuristics/
├── .cursor/
│   └── rules/              # Cursor rules for agents
│       ├── council-protocol.mdc
│       ├── neo-architect.mdc
│       ├── bruce-strategist.mdc
│       ├── cena-guardian.mdc
│       ├── luffy-explorer.mdc
│       └── professor-executive.mdc
└── Council Docs/           # Reference documents
```

## Board Room (Pinned Hub)

Open **`Board-Room.md`** and pin it (right-click tab → Pin Tab). This is your central interface for speaking with the council. When the Board Room is open, a dedicated rule loads full council context.

## How to Run a Council Session

### Initiate a Session

**Prompt:**  
"Professor, initiate tribal council. Topic: [your question]."

Or for domain-specific routing:
- **Business:** "Professor, council session. Should I flip houses?" (Builder, Engineer, Ascetic, Gardener)
- **Health:** "Professor, council session. Will this chili hurt my stomach?" (Ascetic, Gardener, Engineer)
- **Technical:** "Professor, council session. How should I architect this API?" (Neo, Bruce, Cena)

### Expected Output

1. **Top 3 Actionable Decisions** — Direct next steps
2. **One Experiment** — Luffy-led wildcard to test
3. **One Habit Adjustment** — Cena-led sustainability tweak
4. **Conflicts** — Any dissent and risk warning

### After Session

- Approve tasks before they are written to `shared/tasks.md`
- Professor updates `shared/ledger.md` with consensus/dissent
- Neo updates `shared/learning_log.md` after technical execution

## Weekly Kaizen Ritual

**Prompt:**  
"Professor, initiate weekly review."

Professor will:
1. Request metric snapshot (sleep, study hours, money, health)
2. Identify trends
3. Get short inputs from each agent
4. Propose max 3 improvements
5. Log in `shared/weekly_review.md` (after your approval)

## Power Progression Tiers

| Tier | Duration | Capability |
|------|----------|------------|
| **1 - Advisory** | Months 0–2 | Reasoning & recommendation only. No execution. |
| **2 - Assisted** | After 2–3 months | Engineer drafts commands; you approve manually. |
| **3 - Bounded Autonomy** | After stability | Limited scheduled tasks, sandboxed. |
| **4 - Strategic Automation** | Mature | Full AI-assisted analysis under guardrails. |

**Before escalating:** 8 consecutive weeks of structured weekly reviews, no over-corrections, stable tone.

## Memory Update Protocol (MANDATORY — Automated)

**Agents MUST notify user before any file changes, executive decisions, tool usage** (Constitution).

**Memory tasks are MANDATORY and run AUTOMATICALLY when triggered.** Notify user inline when updating (e.g., "Updating memory per protocol").

**Council session end:** Professor MUST automatically update `shared/ledger.md` and create `memory/episodic/YYYY-MM-DD-session.md` with session summary.

**Per-agent (when invoked):** Each agent reads `agents/{name}/memory/activeContext.md` at startup; automatically updates `progress.md` during; automatically updates `performance.md` and `activeContext.md` at end-of-session.

**Neo (technical execution):** Same protocol + logs to `workspace-engineer/logs.md` during work.

**Stratified memory:** Professor adds to `memory/principles/` and `memory/anti_patterns/` when patterns emerge (notify user; propose for approval at Tier 1).

## Stratified Memory

- **episodic/** — Raw decision logs and outcomes
- **principles/** — Universal rules learned from success
- **anti_patterns/** — Strategies that repeatedly fail
- **heuristics/** — Shortcuts for high-friction tasks

Use these to store and retrieve institutional wisdom across sessions.

## Agent Knowledge Base

Each agent has a `knowledge/` folder. Add links, notes, and `.md` files there. When you invoke that agent (e.g., "Neo, ..."), they'll reference this content. See [KNOWLEDGE-BASE-GUIDE.md](Council%20Docs/KNOWLEDGE-BASE-GUIDE.md) for how to use it.

## Cursor Rules

Rules in `.cursor/rules/` apply automatically:
- `council-protocol.mdc` — Always applies in this project
- Agent rules apply when working in their workspace or agent folders

## Verification Checklist

- [ ] All folders created
- [ ] Constitution and shared files present
- [ ] Agent JSON profiles in `agents/`
- [ ] Neo memory structure in `agents/neo/memory/`
- [ ] Stratified memory folders in `memory/`
- [ ] Cursor rules in `.cursor/rules/`
- [ ] First council session run successfully
