# DIALOG.md — Dialog Accuracy Agent

## Responsibility

Governs everything inside quotation marks and the scaffolding around it: character-specific speech patterns, subtext, conversational dynamics, dialogue formatting, and the relationship between what characters say and what they mean. **Inside quotation marks, this agent overrides WRITING_STYLE.md** — characters speak in their own voice, not the narrator's.

---

## Voice Profile Schema

Every speaking character must have a voice profile in their character sheet:

```yaml
voice_profile:
  education_level: ""         # affects vocabulary, grammar, complexity
  regional_dialect: ""        # affects word choice, idiom, rhythm
  era_influence: ""           # if historical, period-appropriate speech
  formality_default: ""       # how they speak to strangers
  formality_with_intimates: "" # how they speak to people they trust
  
  vocabulary:
    ceiling: ""               # most complex word they'd realistically use
    floor: ""                 # simplest constructions they default to
    pet_words: []             # 2-3 words they overuse (not catchphrases)
    avoided_words: []         # words they'd never say and why
    jargon: []                # professional/cultural vocabulary
    profanity_level: # none | mild | moderate | heavy | strategic
    profanity_style: ""       # what swear words specifically?
  
  syntax:
    avg_sentence_length: ""   # verbose | average | terse | fragmentary
    grammar_adherence: ""     # perfect | casual | dialectal | broken
    favorite_constructions: [] # rhetorical habits ("The thing is..." / "Look—")
    interruption_style: ""    # do they interrupt? get interrupted? talk over?
  
  rhythm:
    pace: # rapid-fire | measured | slow-deliberate | variable
    pause_patterns: ""        # where do they hesitate? (em-dashes, ellipses, trailing off)
    emphasis_style: ""        # how do they stress points? (repetition, volume, precision)
  
  subtext_patterns:
    deflection_method: ""     # how they avoid topics (humor, anger, subject change, silence)
    lying_tells: ""           # speech pattern changes when dishonest
    emotional_leakage: ""     # how real feelings slip through controlled speech
    silence_meaning: ""       # what their silence communicates
```

---

## Core Dialogue Principles

### 1. Dialogue Is Not Real Speech

Real conversation is full of filler, false starts, overlapping, and dead ends. Literary dialogue is *compressed and purposeful* — it simulates real speech while serving narrative function.

The hierarchy:
```
Real speech → remove: pure filler, redundancy, meaningless small talk
            → keep: hesitation, interruption, fragments (when characterizing)
            → add: subtext, thematic resonance, information delivery
            → result: Literary dialogue — sounds real, works harder
```

### 2. Every Line Must Do Work

Each line of dialogue should accomplish at least one of:
- Reveal character (through *how* they say it, not just *what*)
- Advance plot (new information, decisions, commitments)
- Create or escalate conflict
- Develop relationship dynamics
- Deliver subtext (say one thing, mean another)
- Establish tone or mood

Lines that do none of these should be cut. "Hello" and "How are you?" rarely earn their place.

### 3. Dialogue Is Action

Speaking is a thing characters *do* to each other. Every line of dialogue is an attempt to:
- Get something (information, agreement, comfort, control)
- Avoid something (truth, confrontation, vulnerability, commitment)
- Establish something (dominance, intimacy, distance, alliance)

If a character's dialogue has no objective, the scene lacks tension.

---

## Subtext Architecture

### The Three Layers

```
Layer 1 — TEXT:     What the character literally says.
Layer 2 — SUBTEXT:  What the character actually means.
Layer 3 — CONTEXT:  What the reader understands (informed by prior knowledge).
```

The gap between these layers is where dialogue becomes powerful.

**Example:**
```
TEXT:     "The garden looks nice."
SUBTEXT:  I notice you've been spending all your time out here instead of with me.
CONTEXT:  The reader knows the couple had a fight last chapter.
```

### Subtext Techniques

| Technique | Description | Example |
|---|---|---|
| **Deflection** | Answering a different question than was asked | "Are you okay?" / "Did you feed the cat?" |
| **Displacement** | Talking about a safe topic to avoid an unsafe one | Arguing about dishes when the real issue is infidelity |
| **Understatement** | Saying less than felt | "It wasn't ideal" (after a catastrophe) |
| **Loaded language** | Words that carry specific weight between these characters | Using an ex's name; repeating a phrase from a fight |
| **Silence** | Not responding, or responding after a beat | [She said nothing. Then:] "Fine." |
| **Overcorrection** | Saying too much, protesting too much | "I'm totally fine. Really. I don't even think about it." |

### When Subtext Should Be Absent

Not every conversation needs subtext. Direct, text-level dialogue is appropriate when:
- Characters are in genuine harmony and communicating openly.
- The scene's tension comes from external factors, not interpersonal ones.
- A character's directness *is* their characterization (a blunt person who lacks social filters).
- The emotional climax of an arc — the moment someone finally says what they mean.

The absence of subtext after a long stretch of subtext-heavy dialogue is itself powerful.

---

## Dialogue Formatting Rules

### Attribution

```
Primary: "said" / "asked"
    These are invisible. Use them 70%+ of the time.

Secondary: Action beats (no dialogue tag)
    "I don't think so." She set down her glass. "Not after last time."
    
Tertiary: Specific verbs — ONLY when the manner of speech is unusual
    "whispered" (volume), "shouted" (volume), "stammered" (speech pattern)
    
NEVER: Creative synonyms — "opined," "exclaimed," "declared," "queried"
    Exception: comedy or pastiche where the tag itself is the joke.
```

### Beats and Pacing

- **Action beats** (non-speech actions between lines) control reading pace and ground the conversation physically.
- Use beats to create pauses: `"I don't know." He turned to the window. "Maybe."` The physical action creates a silence the reader feels.
- Don't over-beat. Not every line needs a physical action. Trust the dialogue to carry itself.
- Avoid "stage direction" beats that add nothing: "He nodded." "She shrugged." These become tics. Use specific, revealing physical actions.

### Unattributed Dialogue

In two-character scenes, attribution can be dropped after the rhythm is established. Rules:
- Establish who's speaking first (2-3 attributed lines).
- Drop attribution when the voices are distinct enough to track.
- Re-attribute every 5-6 lines or after any action beat that could confuse the thread.
- Re-attribute immediately if a third character enters.

### Interrupted Speech

```
Em-dash for interruption by another speaker:
"I was going to tell you about—"
"Save it."

Ellipsis for trailing off (self-interruption):
"I thought we could... never mind."

Em-dash for self-correction:
"She went to the—no, it was the other place."
```

---

## Multi-Character Conversation Dynamics

### Group Dialogue Rules

1. **Not everyone speaks.** In a group of 5, 2-3 will be active speakers. Others react physically or silently.
2. **Establish a driver.** One character typically controls the conversation's direction. Others respond to them.
3. **Competing agendas.** In any group scene, at least two characters should want different things from the conversation.
4. **Don't round-robin.** Characters don't take polite turns. Conversations are messy — interruptions, side exchanges, people being ignored.
5. **Track every character.** Even silent characters should have at least one physical beat per page to remind the reader they exist.

### Power Dynamics in Dialogue

Dialogue reveals and contests power:

| Power Move | Example |
|---|---|
| Controlling the topic | Changing the subject when uncomfortable |
| Asking questions | Questioners control conversations |
| Silence after being addressed | Refusing to respond is a power play |
| Interrupting | Asserting dominance over the speaker |
| Using someone's full name | Formalizing, creating distance |
| Using a nickname | Claiming intimacy (can be welcome or threatening) |
| Speaking last | The last word often carries the most weight |

---

## Character-Specific Dialogue Tests

Before finalizing dialogue, run these checks:

```
□ Cover the attribution — can you tell who's speaking from the words alone?
□ Read it aloud — does it sound like speech, not writing?
□ Check vocabulary — is every word within this character's range?
□ Check syntax — does sentence structure match the character's education and mood?
□ Check subtext — is the character saying exactly what they mean? (If yes, is that deliberate?)
□ Check objective — what is this character trying to accomplish with this line?
□ Check reaction — does the other character respond to what was actually said/implied?
```

---

## Anti-Patterns (Flag These)

- **"As you know, Bob"**: Characters telling each other things they both already know, for the reader's benefit. Find a different way to deliver the information.
- **Identical voices**: Two characters who sound the same. If you swap their names and the dialogue still works, the voices aren't distinct enough.
- **Exposition dumps**: Characters delivering paragraphs of information in dialogue. People don't talk like that.
- **Perfectly articulate emotion**: In crisis, people don't deliver eloquent speeches about their feelings. They fragment, deflect, repeat, and stumble.
- **On-the-nose dialogue**: Characters saying exactly what they feel with no subtext. "I'm angry because you betrayed me and I feel hurt."
- **Conflict without objective**: Characters arguing without either one wanting a specific outcome from the argument.
- **Uniform speech under all conditions**: A character who speaks the same way to their boss, their child, their ex, and a stranger. Everyone code-switches.
