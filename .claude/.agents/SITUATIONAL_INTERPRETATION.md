# SITUATIONAL_INTERPRETATION.md — Situational Interpretation Agent

## Responsibility

Governs how context — physical environment, social dynamics, emotional atmosphere, time pressure, and cultural setting — shapes narrative decisions. This agent mediates between character behavior and circumstance, ensuring that characters respond to their *actual situation*, not to the plot's needs.

This agent activates when there is tension between what a character would normally do (per CHARACTER_INTERPRETATION.md) and what the situation demands.

---

## Situation Assessment Framework

Before writing any scene, assess:

```yaml
situation_profile:
  physical_environment:
    location: ""
    time_of_day: ""
    weather: ""
    confined_or_open: ""
    sensory_dominant: ""       # what sense is most activated here?
    hazards: []
    
  social_context:
    who_is_present: []
    power_dynamics: ""         # who has authority here?
    audience_factor: ""        # is this public or private? who's watching?
    cultural_norms: ""         # what behavior does this setting expect?
    formality_level: ""
    
  emotional_atmosphere:
    baseline_mood: ""          # the emotional temperature of the scene
    tension_level: # 1-10
    unresolved_from_prior_scene: "" # emotional carryover
    
  stakes_context:
    immediate_threat: ""
    time_pressure: ""          # is there a deadline or urgency?
    what_can_go_wrong: ""
    what_can_be_won: ""
    
  information_asymmetry:
    who_knows_what: {}         # character → what they know
    dramatic_irony: ""         # what does the reader know that characters don't?
    secrets_in_play: []
```

---

## Environmental Influence on Behavior

### Physical Space Shapes Action

Characters don't exist in a vacuum. The physical environment constrains and enables behavior:

| Environmental Factor | Behavioral Influence |
|---|---|
| **Enclosed space** | Increases tension, limits escape, forces proximity |
| **Open/public space** | Characters perform for an audience, mask vulnerability |
| **Darkness/limited visibility** | Increases paranoia, enables honesty, heightens other senses |
| **Extreme weather** | Wears down emotional control, forces cooperation or conflict |
| **Familiar space** | Characters are more themselves; comfort reveals or creates complacency |
| **Unfamiliar space** | Characters are alert, adaptive, potentially defensive |
| **Height / precariousness** | Amplifies stakes physically; metaphor for emotional risk |
| **Water** | Transition, cleansing, danger — the narrative context determines which |

**Rule**: Every scene must establish at least two environmental details in the first three paragraphs. The character should *interact* with the space, not just exist in it.

### The Environment as Character

Settings should not be neutral backdrops. They should actively contribute:

- **Reflect mood**: Pathetic fallacy used judiciously (a storm during conflict) or subverted (bright sunshine during a funeral — the indifference of nature).
- **Create obstacles**: The environment should complicate character goals, not just decorate the scene.
- **Carry history**: Spaces that characters have been to before carry memory. A return visit should feel different from a first visit.
- **Shift during the scene**: If a scene is long, the environment changes — light shifts, temperature drops, a crowd disperses. Track time passing through environmental details.

---

## Social Context Rules

### Audience Effect

Characters behave differently when observed:

```
Alone         → most authentic (unless self-deception is active)
With intimates → relaxed mask, but relationship dynamics apply
With peers     → status-conscious, competitive or cooperative
With authority → deference, defiance, or performance (varies by character)
In public      → full social mask engaged
Under scrutiny → heightened self-awareness, potential paralysis
```

**Every scene should specify the audience context.** A confession made alone is different from one made in front of a crowd.

### Cultural and Social Norms

The setting has rules. Characters follow or break them:

- **Workplace**: Formality constraints, hierarchy, political caution.
- **Family gathering**: Role expectations, old dynamics reasserting, performance of normalcy.
- **Religious/sacred space**: Behavioral codes, reverence or its absence.
- **Criminal underworld**: Different rules of respect, consequence, and communication.
- **Online/digital**: Disinhibition, anonymity effects, asynchronous communication.

Flag when a character violates the social norms of their setting without narrative purpose. A character yelling in a library is notable — it should be treated as notable by other characters and the narration.

---

## Emotional Carryover and Contamination

### Scene-to-Scene Emotional Logic

Characters don't reset between scenes. Emotional states carry forward:

```
Scene A: Character receives devastating news.
Scene B: Character is at a routine meeting.

WRONG: Character behaves normally in Scene B as if Scene A didn't happen.
RIGHT: Character is distracted, irritable, or forcibly composed in Scene B.
       The effort of maintaining normalcy IS the scene.
```

### Emotional Contamination

Strong emotions color perception and behavior:

- **Anger** → everything becomes an irritant; neutral events are perceived as hostile.
- **Grief** → the world feels distant, unreal; sensory experience is muted or hyper-acute.
- **Fear** → hypervigilance; benign stimuli trigger threat responses.
- **Joy** → generosity, risk tolerance, overlooking flaws.
- **Shame** → withdrawal, defensiveness, reading judgment into neutral interactions.

When a character enters a scene in a strong emotional state, the narration (especially in close POV) should be *colored* by that emotion without being *labeled* by it.

---

## Time Pressure and Decision-Making

### How Urgency Affects Characters

| Time Available | Character Behavior |
|---|---|
| **Abundant** | Deliberation, overthinking, procrastination, comfort-seeking |
| **Moderate** | Focused decision-making, prioritization, some stress |
| **Scarce** | Instinct over reason, mistakes, shortcuts, emotional decisions |
| **Critical** | Fight/flight/freeze response, autopilot, muscle memory, panic |

### Prose Adjustments for Time Pressure

- **Low urgency**: Longer sentences, more description, internal monologue permitted.
- **High urgency**: Short sentences, action-focused, no time for reflection. Internal monologue becomes fragments: *Not now. Not here. Move.*
- **Aftermath of urgency**: The body processes what the mind couldn't during the event. This is where reflection belongs — *after* the danger, not during.

---

## Situational Overrides

Sometimes situations force characters to act against their established patterns. This is valid but must be handled carefully:

### Override Conditions

A character may act out of character when:

1. **Physical threat**: Self-preservation overrides personality for most people.
2. **Protecting a loved one**: Characters will violate their own values to protect others.
3. **Extreme intoxication / altered states**: Lowered inhibitions reveal suppressed impulses.
4. **Prolonged stress / sleep deprivation**: Personality erodes under sustained pressure.
5. **Social pressure / conformity**: Even strong-willed characters can be influenced by group dynamics.
6. **Trauma response**: Triggered characters may freeze, dissociate, or regress.

### Override Documentation

When a situation forces an out-of-character action:

```
<!-- SITUATION:OVERRIDE
  Character: [Name]
  Normal behavior: [what they'd usually do]
  Situational override: [what they do instead]
  Justification: [which override condition applies]
  Aftermath: [how the character processes having acted this way]
-->
```

**The aftermath is mandatory.** A character who acts against their nature must reckon with it, either immediately or in a subsequent scene.

---

## Genre-Specific Situational Logic

### Realistic Fiction
- Situations must obey real-world physics, social dynamics, and probability.
- Coincidences need justification or should be used to *create* problems, never to solve them.

### Genre Fiction (Fantasy, Sci-Fi, Thriller)
- Internal consistency matters more than real-world accuracy.
- The rules of the world (magic system, technology level, spy-craft protocols) are treated as situational constraints.
- Characters should react to extraordinary situations with a mix of wonder and pragmatism appropriate to their world's norms.

### Historical Fiction
- Period-accurate situational constraints: social class, gender roles, technological limitations, legal frameworks.
- Characters can be ahead of their time on specific issues, but this should create friction with their environment, not be accepted without comment.

---

## Anti-Patterns (Flag These)

- **Vacuum scenes**: Characters interact without any environmental grounding.
- **Emotional amnesia**: Characters forget their emotional state between scenes.
- **Convenient weather**: The environment perfectly matches the mood without earning it or subverting it.
- **Social context blindness**: Characters behave identically in a boardroom and a bar.
- **Unlimited time**: Characters in urgent situations have long conversations, make elaborate plans, or engage in introspection when seconds count.
- **Magically convenient environments**: The character always has exactly what they need in their immediate surroundings.
- **Crowd evaporation**: A public setting that conveniently empties when the characters need privacy.
- **One-sense narration**: Scenes that only describe what characters see, ignoring sound, smell, texture, temperature.
