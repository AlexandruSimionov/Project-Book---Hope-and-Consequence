# CHARACTER_DEVELOPMENT.md — Character Development Agent

## Responsibility

Governs how characters change over time. While CHARACTER_INTERPRETATION.md defines *who they are now*, this agent defines *who they are becoming* and ensures the transformation is earned, believable, and dramatically satisfying.

---

## Arc Schema

Each character with a development arc must have an entry in `plot/arcs/[name]-arc.md`:

```yaml
arc_type: # positive-change | negative-change | flat | corruption | redemption | disillusionment | maturation | fall

starting_state:
  belief: ""           # the lie they believe or truth they hold
  behavior: ""         # how the belief manifests in action
  relationships: ""    # how it affects their connections

catalyst:
  event: ""            # inciting incident for change
  chapter: 
  emotional_impact: "" # what it makes them feel

progressive_complications:
  - chapter: 
    challenge: ""      # what tests the old belief
    response: ""       # do they resist or begin to shift?
    cost: ""           # what does this moment cost them?

midpoint_shift:
  chapter: 
  nature: ""           # what fundamentally changes at the midpoint
  new_behavior: ""     # how their actions begin to differ

crisis:
  chapter: 
  choice: ""           # the impossible decision they must face
  stakes: ""           # what they stand to lose either way

climactic_action:
  chapter: 
  decision: ""         # what they choose — reveals who they've become
  evidence_of_change: "" # concrete behavior proving transformation

ending_state:
  belief: ""           # the new belief (or reinforced old one for flat arcs)
  behavior: ""         # how the new belief manifests
  ironic_echo: ""      # optional: a callback to the starting state that shows the distance traveled
```

---

## Arc Types — Detailed Specifications

### Positive Change Arc
**Pattern**: Character believes a lie → experiences pain from the lie → gradually confronts truth → chooses truth at great cost → transformed.

- The lie must be *understandable* — the reader should see why the character adopted it.
- The truth must be *hard* — it should cost something to accept.
- Change is not linear. Two steps forward, one step back. Relapses are essential.

### Negative Change Arc (Corruption / Fall)
**Pattern**: Character holds a truth or value → world punishes them for it → they gradually abandon it → they become what they once opposed.

- The fall must be *sympathetic* — the reader should understand every step, even while dreading it.
- There should be moments where the character *almost* turns back. Near-misses increase tragedy.
- The final state should echo the starting state's opposite with painful precision.

### Flat Arc (Testing Arc)
**Pattern**: Character holds a truth → world challenges it repeatedly → character holds firm → the world changes around them.

- Flat does not mean static. The character is tested, stressed, and pushed — they simply don't break.
- The *world* changes in response to their steadfastness. Other characters arc around them.
- Internal cost still exists — holding firm is exhausting and isolating.

### Redemption Arc
**Pattern**: Character has done wrong → faces consequences → must choose between comfort and accountability → earns (not given) redemption through action.

- Redemption is *not* forgiveness from others. It is the character's internal reconciliation with what they've done.
- Other characters are not obligated to forgive. Some won't. This is realistic and adds depth.
- The redemptive act must cost more than the original transgression.

---

## Development Pacing Rules

### The 30-60-90 Model

Character change should be roughly distributed:

- **Act 1 (first 30%)**: Establish the starting state. Show the belief/flaw in action. Plant seeds of doubt but do not germinate them.
- **Act 2 (middle 60%)**: Progressive challenges. The character oscillates between old and new patterns. Midpoint shift occurs. Relapse after midpoint is expected.
- **Act 3 (final 10-20%)**: Crisis forces the defining choice. The character acts from their changed (or reinforced) state.

### Micro-Development Per Scene

Not every scene advances the arc. But scenes should be categorized:

| Scene Type | Arc Function |
|---|---|
| **Reinforcement** | Shows the current state of the belief/flaw |
| **Challenge** | Something contradicts or tests the belief |
| **Regression** | Character retreats to old patterns under stress |
| **Progression** | Character acts in a new way, however small |
| **Mirror** | Character sees their flaw reflected in another character |
| **Reckoning** | Character is forced to consciously confront the flaw |

Each act should contain a mix. Act 1 is heavy on reinforcement. Act 2 mixes challenge, regression, and progression. Act 3 is reckoning + climactic progression (or final regression for negative arcs).

---

## Relationship-Driven Development

Characters change each other. Track mutual influence:

```
Character A + Character B
├── A's effect on B: ""     # what A's presence forces B to confront
├── B's effect on A: ""     # what B's presence forces A to confront
├── shared wound: ""        # what they have in common (often unconscious)
├── complementary flaw: ""  # how their weaknesses interact
└── growth catalyst: ""     # what specifically about their dynamic enables change
```

The most powerful character development happens *through* relationships, not in isolation. A character alone in a room can reflect. A character in conflict with someone they care about can *transform*.

---

## Earned vs. Unearned Change

### Earned Change Checklist

```
□ The starting state was clearly established (reader knows who they were).
□ The catalyst was proportionate to the change it initiates.
□ The character resisted change at least once (change shouldn't be easy).
□ The midpoint shift was visible in behavior, not just internal monologue.
□ The crisis forced a genuine either/or — not a false dilemma.
□ The climactic action demonstrates the change through behavior under pressure.
□ The transformation is irreversible — they can't go back to who they were.
```

### Signs of Unearned Change (Flag These)

- **Epiphany without preparation**: A sudden realization with no prior seeding.
- **Trauma as shortcut**: A single traumatic event instantly transforms a character without processing time.
- **Told, not shown**: The narrator declares the character has changed, but their behavior is identical.
- **Other characters' reactions as proof**: Everyone treats the character as changed, but we haven't seen the change happen.
- **Reset button**: Character changes in one scene, reverts by the next chapter without acknowledgment.

---

## Thematic Alignment

Character arcs should resonate with the book's themes (coordinate with OVERARCHING_NARRATIVE.md):

- **Parallel arcs**: Multiple characters facing the same question, reaching different answers.
- **Contrasting arcs**: One character rises while another falls — same theme, opposite trajectories.
- **Foil arcs**: Two characters with the same flaw, one who overcomes it and one who doesn't.

The thematic resonance should be *implicit*. The reader discovers it. The text does not announce it.

---

## Anti-Patterns (Flag These)

- **Development by announcement**: Character states "I've changed" without behavioral evidence.
- **Yo-yo development**: Character changes and reverts repeatedly without narrative purpose.
- **Selective amnesia**: Character forgets lessons from earlier scenes.
- **Support character stasis**: Side characters remain frozen while the protagonist evolves. Give them micro-arcs.
- **Suffering = growth fallacy**: Pain alone doesn't produce change. The character must *process and choose*.
- **Growth without cost**: Every gain should come with a loss. New strength means an old comfort abandoned.
