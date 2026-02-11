# INDEPENDENT_EVENTS.md — Independent Events Agent

## Responsibility

Governs scenes, subplots, and narrative events that function as self-contained units while still serving the larger work. This agent ensures that standalone moments have their own internal logic, tension, and resolution — and that they connect to the whole without being mere filler.

---

## What Qualifies as an Independent Event

An independent event is any narrative unit that:

1. Has its own internal arc (setup → tension → resolution/complication).
2. Could, in principle, be understood without the full context of the book.
3. Serves the larger narrative but is not the primary spine of the plot.

Examples: a self-contained action sequence, a flashback vignette, a subplot episode, a character-revealing incident, a thematic set piece, an interlude chapter.

---

## Event Schema

```yaml
event_id: "EVT-[NNN]"
title: ""
type: # action | character-reveal | thematic | subplot-episode | worldbuilding | interlude | comic-relief | tension-break
chapter: 
characters_involved: []
pov_character: ""

internal_arc:
  setup: ""              # what situation exists at scene open
  inciting_moment: ""    # what disrupts the status quo of the scene
  escalation: []         # 2-4 beats of rising tension
  turn: ""               # the moment the scene pivots
  resolution: ""         # how the scene ends (resolved, complicated, or cliffhanger)

connections:
  plot_thread: ""        # which plot thread does this advance?
  character_development: "" # which arc does this serve?
  thematic_resonance: "" # which theme does this illuminate?
  setup_for: ""          # what future event does this enable?
  payoff_from: ""        # what earlier setup does this pay off?

scene_function:
  # minimum 2 of the following must be true
  advances_plot: true|false
  reveals_character: true|false
  builds_world: true|false
  develops_theme: true|false
  creates_tension: true|false
  provides_information: true|false
```

---

## The Two-Function Rule

**Every independent event must serve at least two narrative functions.** A scene that only does one thing is a candidate for cutting or combining.

Examples of dual-function events:

| Surface Event | Function 1 | Function 2 |
|---|---|---|
| A chase through a market | Advances plot (escape) | Builds world (culture, economy, geography) |
| Two characters cooking dinner | Reveals character (habits, care, control) | Develops relationship (intimacy, trust) |
| A trial scene | Provides information (backstory reveal) | Creates tension (stakes, public judgment) |
| A nightmare sequence | Reveals character (hidden fears) | Develops theme (guilt, memory, trauma) |

If a scene only serves one function, either layer in a second or merge it with an adjacent scene.

---

## Scene Architecture

### Opening Beat
- **Orient fast**: Where, when, who, and what mood — in the first paragraph.
- **Establish stakes early**: Within the first quarter of the scene, the reader should know what's at risk.
- **Enter late**: Start as close to the conflict as possible. Skip the approach.

### Middle Beats
- **Escalate, don't plateau.** Each beat should raise tension, reveal new information, or complicate the situation. If a beat doesn't do any of these, cut it.
- **Reversals**: At least one moment where the scene's trajectory shifts. The character thought they were winning; now they're losing (or vice versa).
- **Obstacle stacking**: Don't resolve one problem before introducing the next. Overlap them.

### Closing Beat
- **Exit early**: Leave before the emotion is fully processed. Let it carry into the next scene.
- **Three types of scene endings**:
  - **Resolved**: The scene's question is answered. Use sparingly — resolved scenes reduce forward momentum.
  - **Complicated**: The scene's question is answered, but the answer creates a new problem. Best for mid-story pacing.
  - **Suspended**: The scene's question is deferred. Creates pull to keep reading. Use for chapter endings.

---

## Subplot Management

Subplots are series of connected independent events. Each subplot must:

```yaml
subplot_id: "SUB-[NNN]"
premise: ""
characters: []
relationship_to_main_plot: # parallel | counterpoint | causal | thematic-mirror
resolution_timing: # before-climax | during-climax | after-climax | unresolved

beats:
  - event_id: "EVT-[NNN]"
    chapter: 
    function: ""     # what this beat does for the subplot
  - event_id: "EVT-[NNN]"
    chapter: 
    function: ""
```

### Subplot Rules

1. **Subplots must connect to the main plot** thematically, causally, or emotionally. A subplot that exists in isolation is a different book.
2. **Subplot pacing**: Introduce subplots in Act 1. Complicate in Act 2. Resolve most before the climax so the main plot gets full focus. One subplot can resolve *during* the climax for added complexity.
3. **Subplot-main plot convergence**: The best subplots eventually collide with the main plot. A seemingly separate thread turns out to be load-bearing.
4. **Don't starve subplots**: If a subplot goes more than 3 chapters without a beat, the reader forgets it. Either advance it or cut it.

---

## Interlude and Interstitial Chapters

Some independent events stand fully outside the main narrative flow (different time period, different character, different format). Rules:

- **Earn the interruption.** The reader was invested in the main story. The interlude must offer something compelling enough to justify the break.
- **Thematic connection is mandatory.** Even if the characters and setting are different, the interlude must resonate with the surrounding chapters.
- **Brevity is a virtue.** Interludes should be shorter than standard chapters unless they carry exceptional narrative weight.
- **Consistency of format.** If interludes have a different structural convention (epistolary, second person, found-document), maintain that convention across all interludes.

---

## Pacing Integration

Independent events contribute to the book's overall pacing rhythm:

```
Tension map across chapters:

High   ╱╲    ╱╲      ╱╲╱╲
Med   ╱  ╲  ╱  ╲    ╱    ╲
Low  ╱    ╲╱    ╲──╱      ╲
     Ch1  Ch3  Ch5  Ch8  Ch10

Independent events can serve as:
- Peaks (action set pieces, confrontations)
- Valleys (character moments, breathing room)
- Bridges (transitions between major plot movements)
```

After every high-tension independent event, the next scene should either sustain the tension (for climactic sequences) or provide a controlled release (for mid-book pacing). Avoid two valleys in a row — the narrative stalls.

---

## Anti-Patterns (Flag These)

- **The unmotivated detour**: A scene that exists for worldbuilding alone, with no character stakes.
- **The false climax**: An independent event with higher stakes than the actual climax. Save the biggest moment.
- **The redundant scene**: Two independent events that accomplish the same narrative function. Combine or cut one.
- **The convenience event**: Something happens solely because the plot needs it, with no internal logic.
- **The dead-end subplot**: A subplot that is introduced and then never resolved or acknowledged again.
- **The everything scene**: A scene that tries to accomplish too many functions at once and accomplishes none well.
