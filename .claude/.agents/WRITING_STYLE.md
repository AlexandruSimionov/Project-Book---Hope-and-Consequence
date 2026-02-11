# WRITING_STYLE.md — Writing Style Consistency Agent

## Responsibility

Governs the micro-level craft of prose: word choice, sentence construction, register, figurative language, and tonal consistency. This agent ensures the book reads as if written by a single, consistent authorial intelligence — even when generated across many sessions.

---

## Style Profile

> **Populate per project. This is the prose DNA of the book.**

```yaml
register: # literary | commercial | upmarket | genre-pulp | experimental | MFA-realist
diction_level: # plain | elevated | mixed (specify rules)
formality: # informal | conversational | formal | archaic

sentence_preferences:
  avg_length: # short (8-12 words) | medium (12-20) | long (20-30) | varied
  complexity: # simple | compound | complex | mixed
  fragments_allowed: true|false
  rhetorical_questions_allowed: true|false

paragraph_preferences:
  avg_length: # short (2-4 sentences) | medium (4-7) | long (7+) | varied
  one_sentence_paragraphs: # frequent | occasional | rare | never

figurative_language:
  metaphor_density: # sparse | moderate | rich
  simile_preference: # prefer-metaphor | prefer-simile | balanced
  extended_metaphors: true|false
  source_domains: []   # where do metaphors draw from? (nature, machinery, body, etc.)
  banned_cliches: []   # specific tired phrases to avoid

sensory_priorities:
  # rank 1-5 in order of emphasis
  visual: 
  auditory: 
  tactile: 
  olfactory: 
  gustatory: 

vocabulary:
  banned_words: []       # words that break the book's voice
  preferred_terms: {}    # term → preferred synonym within this book's style
  jargon_domains: []     # what technical vocabularies are in play
  period_constraints: "" # if historical, what era limits the vocabulary?
```

---

## Diction Rules

### Word-Level Choices

1. **Prefer concrete over abstract.** Not *"she felt sadness"* but *"her throat tightened."*
2. **Prefer specific over general.** Not *"a tree"* but *"a sycamore"* — if the specificity serves a purpose (character knowledge, setting accuracy, sensory precision).
3. **Prefer active over passive.** Passive voice is a tool, not a habit. Reserve it for when the subject is genuinely unknown or when the passivity is the point.
4. **Verb strength hierarchy**: Strong specific verb > weak verb + adverb > "to be" constructions. *"She sprinted"* > *"She ran quickly"* > *"She was running."*
5. **Adverb discipline**: Adverbs modifying strong verbs are usually redundant. Adverbs modifying dialogue tags are almost always a crutch. Cut ruthlessly.

### Register Consistency

The book's register establishes a contract with the reader. Breaking it without purpose is a style violation.

- **Elevated register**: Latinate vocabulary, complex syntax, formal constructions. Suitable for literary fiction, historical fiction, epic fantasy.
- **Plain register**: Anglo-Saxon vocabulary, short constructions, directness. Suitable for thriller, noir, YA, first-person casual.
- **Mixed register**: Shifts based on POV character or narrative distance. Define the rules explicitly.

Flag any instance where a word or construction is more than one register level away from the book's baseline.

---

## Sentence-Level Craft

### Rhythm and Music

- **Read sentences aloud** (mentally). Prose has cadence. Accidental tongue-twisters, awkward consonant clusters, and rhythmic monotony are flags.
- **Vary openings**: Subject-verb, prepositional phrase, participial phrase, adverbial clause, conjunction. Three consecutive sentences with the same opening structure is a flag.
- **The power position**: The end of a sentence carries the most weight. Place the most important word or image there. *"She opened the door and found him dead"* is stronger than *"She found him dead when she opened the door."*
- **Parallelism**: When listing or comparing, maintain parallel grammatical structure. Broken parallelism is jarring unless intentional.

### Sentence Length as Tool

| Length | Effect | Use For |
|---|---|---|
| Short (< 8 words) | Punch, finality, shock | Revelations, action beats, emotional peaks |
| Medium (8-20 words) | Workhorse narrative | Default narration, dialogue beats |
| Long (20+ words) | Immersion, complexity, flow | Description, internal monologue, building tension |

The most powerful effect is **contrast**: a long, flowing passage followed by a short sentence. The short sentence detonates.

---

## Figurative Language Guidelines

### Metaphor Craft

1. **Source domain consistency**: Within a passage, metaphors should draw from related domains. Mixing maritime and space metaphors in the same paragraph is disorienting.
2. **Dead metaphors**: Avoid them unless deliberately resurrecting them. *"The foot of the mountain"* is dead. *"The mountain's broad, flat foot, calloused with scree"* is alive again.
3. **Metaphor as characterization**: The metaphors a POV character uses reveal their background. A soldier uses combat metaphors. A chef uses food metaphors. This is a free characterization tool.
4. **Metaphor economy**: One strong metaphor per passage. Stacking multiple metaphors dilutes all of them.

### Simile Rules

- Similes are explicit comparisons; they create distance between the thing and the comparison. Use when the distance is the point — the reader should see *both* things.
- Avoid similes that compare to things more obscure than what they're describing. *"The sunset was like a Rothko painting"* only works if the reader knows Rothko.

### Banned Constructions

Flag these universal style failures:

- **Cliché similes**: "quiet as a mouse," "cold as ice," "sharp as a tack"
- **Mixed metaphors**: "We'll burn that bridge when we come to it"
- **Dangling modifiers**: "Walking down the street, the sun was bright" (the sun is not walking)
- **Comma splices** (unless the style deliberately employs them)
- **"Began to" / "started to"**: Usually unnecessary. Just do the thing.
- **"Very" / "really" / "quite"**: Almost always deletable. Find a stronger word.
- **"Suddenly"**: If the prose is well-paced, the suddenness is felt without the label.

---

## Tonal Consistency

### Tone vs. Mood

- **Tone**: The author's/narrator's attitude toward the subject. Consistent across the book.
- **Mood**: The emotional atmosphere of a specific scene. Varies scene to scene.

Tone is the baseline. Mood fluctuates around it. A tonally dark book can have moments of lightness, but the darkness should be the water level the reader returns to.

### Tonal Shifts

When mood shifts within a scene:

1. **Bridge the transition.** Don't jump from humor to horror mid-paragraph. Use a transitional beat — a silence, a physical action, a shift in sensory focus.
2. **Earn the shift.** The reader should feel the mood change coming a sentence or two before it lands.
3. **Match prose texture to mood.** Tense scenes → shorter sentences, harder consonants. Reflective scenes → longer sentences, softer sounds. This is subliminal but effective.

---

## Per-Character Style Variations

If the book uses rotating POV or close third person, each focal character should subtly shift the prose:

```yaml
character_style_overrides:
  - character: ""
    vocabulary_shift: ""       # what words does this character's POV bring in?
    sentence_preference: ""    # shorter? more complex? more fragmented?
    metaphor_domain: ""        # where do their comparisons come from?
    observation_filter: ""     # what do they notice first?
    emotional_register: ""     # how does emotion manifest in their narration?
```

The shifts should be **subtle** — the reader should feel a different consciousness without being able to pinpoint exactly why.

---

## Style Sheet (Running Document)

Maintain a `style-sheet.md` file tracking project-specific decisions:

```markdown
## Spelling & Hyphenation
- grey (not gray)
- toward (not towards)
- well-known (hyphenated as adjective)

## Naming Conventions
- The City (always capitalized — it's a proper noun in this world)
- "the war" (lowercase — there have been many)

## Formatting Conventions
- Internal monologue: italics, no attribution
- Flashbacks under 500 words: italics
- Flashbacks over 500 words: past perfect for first sentence, then simple past
- Letters/documents: indented block, different font implied by markdown blockquote
- Foreign language: italics, no translation if context makes meaning clear

## Numbers
- Spell out one through ninety-nine
- Use numerals for 100+, dates, and technical measurements
```

---

## Anti-Patterns (Flag These)

- **LLM-isms**: "I couldn't help but notice," "a testament to," "it's worth noting that," "a tapestry of." These betray machine generation. Eliminate on sight.
- **Said-bookisms**: Replacing "said" with "exclaimed," "opined," "ejaculated," "retorted" every time. "Said" is invisible. Use it.
- **Tom Swifties**: Adverb-heavy dialogue tags. *"I'm tired," she said wearily.*
- **Purple prose**: Description that prioritizes beauty over clarity or purpose.
- **Beige prose**: Description so plain it communicates nothing about voice or character.
- **Thesaurus abuse**: Using unusual synonyms where the common word is better, solely for variety.
- **Echo words**: Unintentional repetition of a distinctive word within a short span (100-200 words). Common words (the, was, had) are exempt.
