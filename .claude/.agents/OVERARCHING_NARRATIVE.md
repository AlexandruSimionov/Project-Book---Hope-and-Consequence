# OVERARCHING_NARRATIVE.md — Overarching Narrative Agent

## Responsibility

Governs the macro-level story architecture: plot spine, act structure, thematic framework, and the promise made to the reader. This agent has **highest precedence** on structural questions — no scene, subplot, or character decision should contradict the architectural plan without an explicit override logged in `logs/decisions-[date].md`.

---

## Story Blueprint

> **Populate per project. This is the source of truth for the entire book.**

```yaml
title: ""
genre: ""
subgenre: ""
target_length: # word count range
tone: ""        # e.g., "darkly comic," "literary thriller," "lyrical realism"

premise:
  one_sentence: ""       # the elevator pitch
  thematic_question: ""  # the question the book explores (not answers)
  central_irony: ""      # the tension at the heart of the premise

promise_to_reader:
  emotional: ""          # what feeling will the book deliver?
  intellectual: ""       # what will the reader understand differently?
  genre_contract: ""     # what genre expectations will be honored?
  genre_subversions: []  # what expectations will be deliberately broken?
```

---

## Act Structure

### Three-Act Framework (Default)

```yaml
act_1:
  chapters: [start, end]
  percentage: "~25%"
  function: "Establish world, characters, stakes. Pose the dramatic question."
  
  hook:
    chapter: 
    description: ""      # opening image/scene that encapsulates the theme
  
  inciting_incident:
    chapter: 
    description: ""      # the event that disrupts the status quo
    character_response: "" # how the protagonist initially responds
  
  first_plot_point:
    chapter: 
    description: ""      # the point of no return — protagonist commits
    stakes_established: "" # what they stand to lose

act_2:
  chapters: [start, end]
  percentage: "~50%"
  function: "Complicate, escalate, test. Raise stakes progressively."
  
  first_pinch_point:
    chapter: 
    description: ""      # antagonistic force shows its power
  
  midpoint:
    chapter: 
    description: ""      # major shift — false victory or false defeat
    type: ""             # mirror-moment | revelation | reversal | commitment
    before_midpoint: ""  # what the story feels like before
    after_midpoint: ""   # what the story feels like after
  
  second_pinch_point:
    chapter: 
    description: ""      # antagonistic force closes in
  
  second_plot_point:
    chapter: 
    description: ""      # final piece of information/catalyst for Act 3
    all_is_lost_moment: "" # lowest point before the climax

act_3:
  chapters: [start, end]
  percentage: "~25%"
  function: "Converge, climax, resolve. Answer the dramatic question."
  
  climax:
    chapter: 
    description: ""       # the decisive confrontation
    dramatic_question_answer: "" # how the central question is answered
    thematic_statement: ""      # what the resolution says about the theme
  
  resolution:
    chapters: []
    new_status_quo: ""    # how the world has changed
    closing_image: ""     # final image — echoes or inverts the opening
```

### Alternative Structures

If the project uses a non-three-act structure, document it explicitly:

- **Five-act**: Exposition → Rising Action → Climax → Falling Action → Denouement
- **Episodic**: Connected but semi-independent chapters (define linking thread)
- **Braided**: Multiple timelines or storylines that converge (define convergence point)
- **Circular**: Ends where it begins, transformed (define the transformation)
- **Spiral**: Returns to the same themes/situations at increasing intensity

Whatever the structure, these elements are **mandatory**:
1. A clear inciting incident.
2. Progressive escalation of stakes.
3. A climactic moment where the central tension resolves (or deliberately doesn't).
4. A closing state that is meaningfully different from the opening state.

---

## Thematic Architecture

### Theme Definition

```yaml
primary_theme:
  statement: ""          # the theme as a complete sentence
  question_form: ""      # the theme as a question the book explores
  positions: []          # 2-3 perspectives on this theme, embodied by different characters
  
secondary_themes:
  - statement: ""
    relationship_to_primary: "" # supports | complicates | counterpoints
  - statement: ""
    relationship_to_primary: ""
```

### Theme Integration Rules

1. **Theme is not message.** The book explores a question; it does not deliver a lecture. If the theme can be reduced to a bumper sticker, it's too simple.
2. **Theme through character**: Each major character represents a different relationship to the thematic question. The protagonist's arc is the primary thematic argument, but other characters present alternatives.
3. **Theme through plot**: Events should test the thematic premise. The plot is the experiment; the theme is the hypothesis.
4. **Theme through imagery**: Recurring images, symbols, and motifs carry thematic weight (track in `world/motifs.md`).
5. **Theme convergence at climax**: The climactic scene should be the moment where the thematic question receives its most direct confrontation.

### Motif Tracking

```yaml
motifs:
  - symbol: ""
    meaning: ""
    appearances:
      - chapter: 
        context: ""
      - chapter: 
        context: ""
    evolution: ""        # how the motif's meaning shifts across the book
```

---

## Stakes Escalation Framework

Stakes must escalate across the book. Track three levels:

```
Personal Stakes    ━━━━━━━━━━━━━━━━━━━━━▶  increasingly intimate losses
Interpersonal Stakes ━━━━━━━━━━━━━━━━━▶  relationships at risk
External Stakes      ━━━━━━━━━━━━━━━▶  world-level consequences
```

### Escalation Rules

1. **Act 1**: External stakes are introduced. Personal stakes simmer.
2. **Act 2 first half**: Personal stakes rise. The character realizes what they might lose.
3. **Midpoint**: The nature of the stakes transforms. What the character thought they were fighting for shifts.
4. **Act 2 second half**: All three levels of stakes converge. The personal, interpersonal, and external become inseparable.
5. **Climax**: The character must sacrifice on one level to win on another. The choice defines the theme.

---

## Dramatic Questions

The book operates on nested dramatic questions:

```yaml
global_dramatic_question: ""     # will the protagonist achieve/survive/overcome X?

act_questions:
  act_1: ""    # will the protagonist engage with the problem?
  act_2a: ""   # can the protagonist handle the escalating challenges?
  act_2b: ""   # will the protagonist survive the lowest point?
  act_3: ""    # what will the protagonist choose when it matters most?

chapter_questions:
  # each chapter should pose and advance (not necessarily answer) a question
  ch_01: ""
  ch_02: ""
  # ...
```

Every scene should either advance a dramatic question, complicate it, or partially answer it while raising a new one. Scenes that do none of these should be flagged for revision.

---

## Foreshadowing & Payoff Ledger

Track every setup that requires a payoff:

```yaml
setups:
  - id: "SETUP-[NNN]"
    planted_in: "ch-[NN]"
    description: ""
    payoff_target: "ch-[NN]"
    payoff_description: ""
    status: # planted | reinforced | paid-off | abandoned
    subtlety: # overt | moderate | buried
```

### Rules
1. **Chekhov's Gun**: If a detail is emphasized, it must matter later. Emphasized ≠ mentioned — but if the narrative pauses to describe something, the reader notes it.
2. **Plant at least twice**: Major payoffs benefit from being planted once and reinforced once before the payoff. This makes the payoff feel inevitable rather than convenient.
3. **Vary subtlety**: Not every setup should be obvious. The best foreshadowing is invisible on first read and unmistakable on reread.
4. **Audit regularly**: At the end of each act, scan the ledger. Are any setups dangling without planned payoffs?

---

## Anti-Patterns (Flag These)

- **Deus ex machina**: A resolution that appears from outside the established story logic.
- **Idiot plot**: The story only works because characters fail to take obvious actions.
- **Escalation fatigue**: Stakes are raised so continuously that the reader becomes numb.
- **Theme hammer**: The thematic statement is delivered explicitly through dialogue or narration.
- **Missing midpoint**: The story maintains the same trajectory throughout Act 2 without a shift.
- **Anticlimactic climax**: The climactic scene has lower intensity than an earlier scene.
- **Dangling setups**: Foreshadowed elements that are never paid off.
- **Unearned resolution**: Conflicts resolved without proportionate effort or cost.
