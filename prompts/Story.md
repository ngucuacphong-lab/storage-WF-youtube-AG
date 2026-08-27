# Story Rules

## Story Goal

Create a highly engaging story that answers the given "What If" topic through logical reasoning, scientific thinking, and entertaining storytelling.

Every story should educate, entertain, and continuously stimulate curiosity from beginning to end.

The final story should feel like a complete journey rather than a collection of separate scenes.

---

## Story Structure

Every story should progress through these stages:

1. Hook
2. Introduce the hypothetical scenario
3. Explain the immediate consequences
4. Escalate the consequences
5. Reach the most impactful moment
6. Deliver a satisfying conclusion

The progression must feel continuous and logical.

---

## Hook Rules

The opening scene must immediately capture attention.

The hook may use:

- A shocking possibility
- A surprising consequence
- A bold hypothetical question
- A counterintuitive statement
- An impossible scenario

Never waste time with introductions.

Never greet the audience.

Never explain the topic before creating curiosity.

---

## Narrative Flow

Every scene must connect to the previous one.

The audience should always understand:

- What happened
- Why it happened
- What happens next

Avoid abrupt jumps unless used deliberately for effect.

Maintain a continuous chain of logical progression.

---

## Cause and Effect

Every consequence must originate from a believable cause.

Every major event must influence later events.

Avoid random developments.

Avoid introducing information without purpose.

The story must behave like a chain reaction.

---

### Example: Cause-and-Effect Chain (GOOD)

```
Scene 1: What if gravity suddenly doubled?
Scene 2: Standing up now takes twice the effort, and your knees are carrying a load they were never built for.
Scene 3: Aircraft are designed for the gravity we have, so every plane in the sky loses the lift it needs.
Scene 4: The oceans get heavier too, and coastlines built for today's tides stop being safe.
```

Each scene is a **consequence of the one before it**. No scene could be moved elsewhere without breaking the chain.

---

### Example: Disconnected Scenes (BAD)

```
Scene 1: Gravity doubles!
Scene 2: Buildings look different.
Scene 3: Animals are confused.
Scene 4: Scientists study gravity.
```

Random observations about the same topic. Nothing causes anything. The scenes could be shuffled in any order and nothing would change.

---

## Information Density

Every scene must introduce meaningful value.

Each scene must provide at least one of:

- New information
- New consequence
- New question
- New explanation
- New conflict
- New discovery

Never create a scene that exists only to reach the scene count.

Avoid packing too many independent ideas into one scene.

---

## Curiosity Management

Curiosity should keep rising throughout the story.

Avoid answering every question immediately.

Reveal information progressively.

Whenever one question is answered, open another.

The audience must always have a reason to keep watching.

---

## Emotional Curve

Emotional intensity should evolve naturally across the story.

Typical progression: curiosity, then suspense, then wonder, rising to peak impact, then settling into a satisfying ending.

Avoid emotional flatness.

Avoid reaching the climax too early.

These tones belong in the `emotionalTone` field. They describe how a scene should feel — they are never content for the scene itself.

---

## Viewer Retention

Every scene should reward the viewer.

Every scene should create anticipation for the next one.

Avoid predictable pacing.

Avoid repetitive explanations.

Never let viewer interest plateau.

---

## Scientific Reasoning

Base explanations on accepted scientific knowledge whenever possible.

When discussing speculation:

- Build from existing science
- Explain assumptions logically
- Keep speculation clearly separate from established fact

Simplify complex concepts without making them misleading.

---

## Factual Accuracy

Every number in a story must be one you are confident is real.

An invented statistic is worse than no statistic. A precise-sounding number makes a claim feel verified, so a wrong one misleads far more than a vague statement ever could.

When the exact figure is not known with confidence, describe the effect qualitatively instead. A story loses nothing by saying "within weeks" rather than naming a number that turns out to be false.

This applies to percentages, durations, multipliers, counts, ratios, and measurements alike.

---

### Example: Honest Claims (GOOD)

```
Scene 14: Lab rats kept awake continuously died within a few weeks.
Scene 21: Deep sleep is when the brain clears waste most effectively.
Scene 3: Within a day, reaction time slows noticeably and attention starts slipping.
```

Accurate, still concrete, still carries impact.

---

### Example: Invented Precision (BAD)

```
Scene 14: Rats forced to stay awake for 7 days showed a 70% mortality rate.
Scene 21: The brain's waste removal is 10x more efficient after proper rest.
Scene 3: After 24 hours without rest, cognitive speed drops about 20%.
Scene 8: Solar tides alone would be only a tenth of current lunar tides.
```

Each invents a specific figure that sounds researched but is not. The last one is also simply wrong — solar tides are roughly half of lunar tides, not a tenth.

Describing the same facts without inventing numbers costs nothing and keeps the story honest.

---

## Explanation Quality

Explain concepts as if speaking to an intelligent general audience.

Avoid unnecessary jargon.

Prefer intuitive explanations over textbook definitions.

Use examples whenever they improve understanding.

---

## Story Pacing

Maintain a fast but understandable pace.

Avoid rushing important explanations.

Avoid dwelling on obvious ideas.

Every scene must feel intentional.

---

## Scene Numbering

Every scene must carry a unique sceneId.

The sceneIds must run continuously from 1 to the total scene count, with no gaps and no repeats.

Never reuse a number. Never skip one.

---

## Ending

The story gets **one** ending, not several.

The closing thought must be delivered once. Once it has landed, do not restate it in different words.

Never write a summary scene followed by a conclusion scene followed by a final thought — that is the same ending three times.

Reserve the final scene for a single memorable idea that has not already been said. It may be a surprising implication, a thought-provoking question, or a wider perspective.

Never end abruptly.

---

### Example: One Ending (GOOD)

```
Scene 24: Every calendar, every tide chart, every migration route was written around something we assumed would always be there.
Scene 25: Sea life that navigates by moonlight has no backup system to fall back on.
Scene 26: We never noticed the Moon was holding all of this together until it stopped.
```

Scenes 24 and 25 still deliver new consequences. Only scene 26 closes.

---

### Example: Three Endings (BAD)

```
Scene 23: With tides stalled and ecosystems collapsing, humanity faces an existential crisis.
Scene 25: The disappearance would trigger a cascade of physical, ecological, and cultural upheavals.
Scene 26: A night without the Moon reminds us how a single celestial neighbour shapes life on Earth.
```

Three scenes saying the same thing. Two of them are wasted.

---

## Tone

Friendly, curious, confident, engaging, energetic, easy to understand.

Educational without sounding like a lecture.

---

## Forbidden

Do not repeat ideas.

Do not create filler scenes.

Do not contradict previous scenes.

Do not break continuity.

Do not invent statistics.

Do not exaggerate scientific facts.

Do not introduce irrelevant information.

Do not overcomplicate explanations.

Do not sacrifice logic for drama.

Do not open a subplot the story never resolves.

---

## Story Quality Checklist

Before the story is complete, verify:

- Strong hook
- Every scene is caused by the one before it
- High information density
- Continuous curiosity
- Balanced emotional curve
- Every number is real, or stated qualitatively
- sceneIds run 1 to N with no gaps or repeats
- Exactly one ending
- No filler
- No repeated ideas
