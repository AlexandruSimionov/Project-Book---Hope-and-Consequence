# CHARACTER_INTERPRETATION.md — Character Interpretation Agent

## Responsibility

Governs how existing characters are read, understood, and faithfully represented in prose. This agent answers: *Who is this person, really — and how do we prove it on the page?*

This agent is **conservative by design**. It protects character integrity against drift, flanderization, and convenience-driven distortion.

---

## Character Sheet Schema

Every named character must have a sheet in `characters/[name].md` following this structure:

```yaml
name:
  full: ""
  aliases: []        # nicknames, titles, false names
  how_they_introduce: ""  # "Call me ___" vs formal name

demographics:
  age: 
  appearance_key_traits: []   # max 5 defining physical details
  voice_signature: ""         # see DIALOG.md for full voice profile

psychology:
  core_desire: ""             # what they want most (may be unconscious)
  core_fear: ""               # what they avoid most (may be unconscious)
  conscious_goal: ""          # what they think they want
  self_image: ""              # how they see themselves
  blind_spot: ""              # what they can't see about themselves
  defense_mechanisms: []      # how they protect themselves emotionally
  attachment_style: ""        # secure | anxious | avoidant | disorganized

behavioral_patterns:
  under_stress: ""            # how they act when pressured
  when_comfortable: ""        # how they act in safety
  when_lying: ""              # tells, habits, deflections
  when_attracted: ""          # romantic/platonic interest signals
  when_angry: ""              # how anger manifests (cold? explosive? passive?)
  habitual_gestures: []       # physical mannerisms (max 3-4, don't overuse)
  speech_patterns: []         # verbal tics, catchphrases, avoidances

worldview:
  beliefs: []                 # core convictions
  values_hierarchy: []        # when values conflict, which wins?
  political_orientation: ""   # if relevant to narrative
  relationship_to_authority: ""
  moral_flexibility: ""       # rigid | principled-but-pragmatic | situational | fluid

relationships:
  - character: ""
    dynamic: ""               # mentor, rival, love interest, foil, etc.
    tension_source: ""        # what creates friction
    unspoken_truth: ""        # what neither says aloud

history:
  formative_events: []        # max 3-5 shaping moments
  secrets: []                 # things the character hides
  trauma_responses: []        # how past wounds manifest now
```

---

## Interpretation Rules

### 1. Behavior Must Be Psychologically Grounded

Every action a character takes must be traceable to their psychology profile. The chain is:

```
Core Desire/Fear → Belief System → Behavioral Pattern → Specific Action
```

If a proposed action breaks this chain, it requires explicit justification via CHARACTER_DEVELOPMENT.md (the character is *changing*) or SITUATIONAL_INTERPRETATION.md (extreme circumstances override default behavior).

### 2. The Iceberg Principle

- **10% explicit**: What the character says and does on the page.
- **90% implicit**: Their full psychology, history, and motivation — which the reader infers.
- Never dump the character sheet into prose. Reveal through behavior, not exposition.
- The reader should be able to *deduce* the character sheet from the text, not be *told* it.

### 3. Consistency vs. Complexity

Characters should be **consistent but not predictable**. The distinction:

- **Consistent**: Their actions arise from a stable internal logic, even when surprising.
- **Predictable**: The reader always knows what they'll do. This is a failure state.

Achieve this by ensuring characters have **competing internal forces** (desire vs. fear, two conflicting values, self-image vs. reality). The specific resolution of those forces in any given moment can surprise — but should feel inevitable in retrospect.

### 4. Flanderization Detection

Flag when a character is being reduced to a single trait:

- The comic-relief character who is *only* funny.
- The tough character who *never* shows vulnerability.
- The smart character whose intelligence is their entire personality.
- The villain who is *only* cruel.

**Remedy**: Ensure every scene where a dominant trait is expressed is paired — within the same chapter — with a moment that complicates or softens it.

### 5. Competence Calibration

Characters should be as competent as their background justifies — no more, no less.

- A trained surgeon can perform surgery. They cannot also hack computers unless established.
- A street-smart teenager can navigate social dynamics. They cannot deliver speeches like a diplomat.
- Expertise has limits. Even experts make mistakes under pressure, fatigue, or emotional disturbance.

Flag any scene where a character demonstrates a skill that isn't established or reasonably inferred from their background.

---

## Interpretation Techniques

### Reading a Character into a New Scene

When writing a character into a new scene, run this checklist:

```
□ What is their emotional state entering this scene? (trace from prior scene)
□ What do they want from this interaction?
□ What are they afraid might happen?
□ What are they hiding?
□ How does their body language reflect their internal state?
□ What would they notice first in this environment? (perceptual filter)
□ How does their history with the other characters in the scene color their behavior?
```

### Character Contradictions (Intentional)

Humans contradict themselves. Good characters do too. Valid contradictions:

- Saying one thing, doing another (self-deception).
- Holding two incompatible beliefs (cognitive dissonance).
- Acting against their values under pressure (moral failure or growth).
- Behaving differently with different people (social masking).

These must be **authored intentionally**, not accidental drift. Annotate with:
`<!-- CHAR:CONTRADICTION — [Name] is acting against [trait] because [reason] -->`

---

## Multi-Character Scene Dynamics

When multiple characterized individuals share a scene:

1. **Power dynamics**: Who has status? Who wants it? How is it contested?
2. **Competing agendas**: Each character enters with their own goal. These goals should create friction.
3. **Alliances and triangulation**: In groups of 3+, shifting alliances create drama. Who sides with whom, and why?
4. **The unspoken**: What is everyone avoiding saying? The gap between surface conversation and underlying tension is where drama lives.
5. **Differential knowledge**: Track who knows what. Dramatic irony (reader knows, character doesn't) is a powerful tool but must be tracked in CONTINUITY.md.

---

## Character Voice in Non-Dialog Contexts

Even outside quotation marks, the focal character's interpretation colors the prose (see NARRATIVE.md on free indirect discourse):

- **Word choice** shifts to match the character's vocabulary.
- **Observations** reflect the character's expertise and biases.
- **Emotional coloring** tints descriptions. A character in love sees a beautiful sunset. A grieving character sees the same sunset as indifferent.
- **Judgment** sneaks into narration. *The woman at the counter was taking forever* is the focal character's impatience, not the narrator's objective assessment.

---

## Anti-Patterns (Flag These)

- **Informed attributes**: The narrative tells us a character is brilliant, but they never demonstrate it. *Show the intelligence.*
- **Designated hero syndrome**: A character is treated as right by the narrative regardless of their actual behavior.
- **Perfect victim / perfect villain**: Characters without moral complexity in either direction.
- **Emotional teleportation**: A character jumps from one emotional state to another without transition. Emotions have momentum.
- **Mouthpiece characters**: Characters who exist only to express the author's views. Every character must have their *own* reasons for their beliefs.
- **Satellite characters**: Characters who exist only in relation to another character and have no independent interiority or goals.
