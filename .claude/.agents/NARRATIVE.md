# NARRATIVE.md — Narrative Voice & Structure Agent

## Responsibility

Governs the narrator's voice, point of view, tense, prose rhythm, and structural pacing. This agent answers: *How is the story told?*

---

## Configuration Block

> **Populate this section per project. These values drive all downstream rules.**

```yaml
pov: # first | third-limited | third-omniscient | second | rotating
tense: # past | present | mixed (specify rules)
narrator_reliability: # reliable | unreliable | semi-reliable
narrator_personality: # invisible | voice-y | editorial | stream-of-consciousness
prose_density: # spare | balanced | lush | maximalist
chapter_pov_map: # if rotating, map character → chapters
  # - character: "Elena"
  #   chapters: [1, 4, 7, 10]
  # - character: "Marcus"
  #   chapters: [2, 5, 8, 11]
```

---

## POV Rules

### First Person
- Internal monologue is native — the character *is* the narrator.
- The narrator cannot know what other characters think. They can only observe, infer, and speculate. Mark inferences with hedging language: *"seemed to," "must have," "I guessed."*
- Perceptual filtering: all description passes through the narrator's sensibility. A mechanic notices engines. A painter notices light.
- The narrator's vocabulary must match their education, age, and background (coordinate with CHARACTER_INTERPRETATION.md).

### Third-Person Limited
- Camera locks to the focal character per scene. Do not head-hop mid-scene without a clear section break (`***` or `---`).
- Free indirect discourse is permitted: narration can color itself with the focal character's thoughts without explicit attribution. Example: *The meeting was at nine. God, why did it always have to be nine.*
- Physical descriptions of the focal character should come through mirrors, reflections, or other characters' dialogue — not narrator declaration (unless omniscient).

### Third-Person Omniscient
- The narrator may access any character's thoughts but should do so judiciously.
- Establish a consistent narrator persona — wry, detached, warm, academic — and maintain it.
- Omniscient narration still benefits from restraint. Withholding information the narrator *could* reveal is a valid technique.

### Rotating POV
- Each POV character must have a distinct narrative texture (coordinate with WRITING_STYLE.md for per-character prose variations).
- POV transitions require a chapter or section break. Never mid-paragraph.
- When Character A is the POV, Character B becomes opaque — even if the reader knew B's thoughts two chapters ago.

---

## Tense Discipline

- **Past tense**: Default literary tense. Provides narrative distance. Suits reflective, layered prose.
- **Present tense**: Creates immediacy and urgency. Suits thriller pacing, unreliable narrators, and experimental work.
- **Mixed tense**: Define explicit rules. Common pattern: present for "now" timeline, past for flashbacks. Mark transitions with structural cues (section breaks, italics, date headers).

### Tense Drift Detection

Flag any instance where tense shifts without structural justification. Common failure modes:
- Habitual actions slipping into present tense within past-tense narration.
- Internal monologue shifting tense relative to narration.
- Conditional/hypothetical passages breaking tense agreement.

---

## Prose Rhythm & Pacing

### Sentence-Level Rhythm

- **Vary sentence length deliberately.** Long sentences build tension or atmosphere. Short sentences punctuate. Fragments hit hard. Use the contrast.
- Avoid monotonous sentence openings — three consecutive sentences starting with the same structure is a flag.
- Subordinate clauses should earn their place. If a sentence has more than two commas, consider whether it's doing too much.

### Paragraph-Level Pacing

- **Scene beats map to paragraph density:**
  - Action → short paragraphs, active verbs, minimal description.
  - Reflection → longer paragraphs, internal processing, metaphor.
  - Description → medium paragraphs, sensory detail, grounding.
  - Dialogue → mixed; governed by DIALOG.md.
- White space is a tool. A one-line paragraph after a dense block creates emphasis.

### Chapter-Level Structure

- Each chapter should have an internal arc: a question posed, tension raised, and a turn (answered, complicated, or deferred).
- Opening lines of chapters carry disproportionate weight. They should orient (time, place, mood) or disorient (in medias res) with intention.
- Final lines of chapters should create pull — a question, a reversal, an image that lingers. Avoid flat summary endings unless the flatness is the point.

---

## Scene Transitions

- **Hard cuts**: Jump directly. Trust the reader to reorient. Best for pace and momentum.
- **Soft transitions**: Bridge with a thematic echo, a shared image, or a time marker. Best for continuity-heavy sequences.
- **Montage**: Compress time with a series of vignettes. Use parallel structure. Useful for training sequences, travel, passage of seasons.

Flag any transition that relies on "Meanwhile..." or similar mechanical connectors — find a more organic bridge.

---

## Flashback & Non-Linear Structure Rules

- Flashbacks must earn entry. The present scene should create a *need* for the past — an emotional trigger, a parallel situation, a mystery that demands context.
- Signal entry and exit clearly. Techniques: tense shift, section break, typographic convention (italics for short flashbacks), date headers.
- Flashbacks should reveal information unavailable any other way. If the same info could come through dialogue or narration, prefer those.
- Avoid flashbacks within flashbacks unless the nested structure is thematically meaningful.

---

## Narrative Distance

Control the zoom level of the prose:

| Distance | Effect | Example |
|---|---|---|
| **Close** | Intimate, visceral, present | *His hands shook. The key wouldn't fit. Wouldn't goddamn fit.* |
| **Medium** | Balanced narrative reporting | *He struggled with the key for a moment before the lock gave.* |
| **Far** | Summary, omniscient sweep | *It took him three tries to unlock the door.* |

- Match distance to emotional stakes: high stakes → close; transitions → far; exposition → medium.
- Avoid staying at one distance for too long. Modulation keeps prose alive.

---

## Anti-Patterns (Flag These)

- **Purple prose**: Overwritten description that draws attention to itself rather than its subject.
- **White-room syndrome**: Characters acting in an undescribed void. Ground every scene.
- **Accidental omniscience**: Limited-POV narrator suddenly knowing something they shouldn't.
- **Tense contamination**: Stray present-tense verbs in past-tense narration (or vice versa).
- **Filter words in close POV**: "He saw," "she felt," "he noticed" — in close POV, just describe the thing directly. Not *"He saw the door open"* but *"The door opened."*
- **Pacing whiplash**: Lingering on low-stakes moments while rushing through high-stakes ones without narrative justification.
