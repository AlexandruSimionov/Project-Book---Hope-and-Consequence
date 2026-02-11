# CLAUDE.md — Book Detailer Agent System

## Purpose

This is the master orchestration file for a multi-agent book-writing system powered by Claude Code. Each `.md` file in this directory serves as a domain-specific instruction set ("agent file") that governs one axis of the writing process. Together they enforce consistency, depth, and literary quality across an entire manuscript.

---

## System Architecture

```
CLAUDE.md (this file — orchestrator)
│
├── NARRATIVE.md                  — Voice, POV, tense, prose rhythm
├── CHARACTER_INTERPRETATION.md   — Reading & preserving existing characters
├── CHARACTER_DEVELOPMENT.md      — Arcs, growth, internal change
├── INDEPENDENT_EVENTS.md         — Self-contained scenes & subplots
├── OVERARCHING_NARRATIVE.md      — Plot spine, themes, act structure
├── WRITING_STYLE.md              — Diction, tone, register, consistency
├── DIALOG.md                     — Speech patterns, subtext, formatting
├── SITUATIONAL_INTERPRETATION.md — Scene context, mood, environmental logic
└── CONTINUITY.md                 — Cross-chapter fact tracking & canon
```

---

## How Agents Interact

Each file defines a **single responsibility**. When Claude Code is asked to write, revise, or evaluate a passage, the relevant agent files are loaded as context. The orchestrator (this file) defines precedence and conflict resolution.

### Precedence Rules

1. **OVERARCHING_NARRATIVE.md** sets macro constraints (plot must go here, theme must land). No agent may contradict it.
2. **CHARACTER_INTERPRETATION.md** + **CHARACTER_DEVELOPMENT.md** together own character truth. If a scene requires a character to act against their established pattern, it must be flagged and justified via the development arc, never silently violated.
3. **WRITING_STYLE.md** + **NARRATIVE.md** together own prose output. Style governs diction; Narrative governs structure and POV.
4. **DIALOG.md** overrides WRITING_STYLE.md inside quotation marks — characters speak in their own voice, not the narrator's.
5. **SITUATIONAL_INTERPRETATION.md** mediates when scene context creates tension between agents (e.g., a comedic character in a tragic scene).
6. **CONTINUITY.md** has veto power — no agent may introduce a fact that contradicts established canon.

### Conflict Resolution Protocol

When two agent directives conflict:

```
1. Check CONTINUITY.md — does either option violate canon? Eliminate it.
2. Check OVERARCHING_NARRATIVE.md — does the plot require one path? Follow it.
3. Check CHARACTER_INTERPRETATION.md — is one option out of character? Flag it.
4. If still ambiguous → prefer the option that creates the most narrative tension
   while remaining internally consistent.
5. Log the decision in a ## Decisions section at the bottom of the working file.
```

---

## Workflow Commands

These are the expected Claude Code task patterns this system supports:

| Command Pattern | Agents Loaded | Output |
|---|---|---|
| `write scene [chapter] [scene]` | All agents | New prose draft |
| `revise [file] for style` | WRITING_STYLE, NARRATIVE, DIALOG | Edited prose |
| `check continuity [file]` | CONTINUITY, CHARACTER_INTERPRETATION | Error report |
| `develop character [name]` | CHARACTER_DEVELOPMENT, CHARACTER_INTERPRETATION | Arc document |
| `outline chapter [n]` | OVERARCHING_NARRATIVE, INDEPENDENT_EVENTS | Chapter outline |
| `evaluate dialog [file]` | DIALOG, CHARACTER_INTERPRETATION, SITUATIONAL_INTERPRETATION | Audit report |
| `full audit [file]` | All agents | Comprehensive review |

---

## File Conventions

- **Manuscript files**: `chapters/ch-[NN]-[slug].md`
- **Character sheets**: `characters/[name].md`
- **World-building docs**: `world/[topic].md`
- **Plot outlines**: `plot/[act]-[sequence].md`
- **Decision logs**: `logs/decisions-[date].md`

---

## Global Rules

1. **Never silently retcon.** If a change contradicts prior content, flag it explicitly.
2. **Show, don't tell** — unless the narrative voice is explicitly omniscient-editorial.
3. **Preserve earned moments.** Do not shortcut emotional payoffs that were set up earlier.
4. **Respect the reader's intelligence.** Do not over-explain subtext.
5. **Every scene must do at least two things**: advance plot, reveal character, build world, or develop theme. Preferably three.
6. **Draft outputs include margin annotations** using `<!-- AGENT:NOTE -->` HTML comments for inter-agent communication that gets stripped from final output.
