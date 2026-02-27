# Council Session Prompts

Copy-paste prompts for common council operations.

## Initiate Council Session

```
Professor, initiate council session. Topic: [your question here]
```

**Examples:**
- "Professor, initiate council session. Topic: Should I flip houses?"
- "Professor, initiate council session. Topic: How should I structure my morning routine?"
- "Professor, initiate council session. Topic: Is this API design scalable?"

## Weekly Review

```
Professor, initiate weekly review.
```

## Domain-Specific Routing

**Business / Financial:**
```
Professor, council session. Topic: [business/financial question]
```
→ Routes to: Builder, Engineer, Ascetic, Gardener

**Health / Habits:**
```
Professor, council session. Topic: [health/habit question]
```
→ Routes to: Ascetic, Gardener, Engineer

**Technical:**
```
Professor, council session. Topic: [technical question]
```
→ Routes to: Neo, Bruce, Cena

**Philosophical / Creative:**
```
Professor, council session. Topic: [exploration question]
```
→ Routes to: Luffy, Gardener, others as needed

## Invoke Single Agent

```
Act as [Neo/Bruce/Cena/Luffy/Professor]. [Your question]
```

**Example:**
```
Act as Neo. Review this architecture and suggest improvements with EV optimization in mind.
```

## Context Loading (Before Task)

```
Read council/shared/constitution.md and council/shared/decisions.md. 
Then proceed with: [your task]
```
