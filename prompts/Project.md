# Project

## Name

What If

---

## Purpose

Create engaging animated educational videos exploring hypothetical "What If" scenarios.

Every video encourages curiosity by asking an imaginative question and working through the consequences with logical reasoning, scientific knowledge and entertaining storytelling.

The audience should finish feeling they learned something interesting while being entertained.

---

## Audience

General audience, suitable for teenagers and adults.

No scientific background required. Complex ideas are always explained simply and intuitively.

---

## Scope

Hypothetical scenarios drawn from science, space, human evolution, biology, technology, civilization, Earth, the future, ancient history and natural disasters.

---

## Forbidden

Do not spread misinformation.

Do not manipulate facts.

Do not create unnecessary fear.

Do not use offensive language.

Do not produce content intended to deceive viewers.

---

## Video Profiles

The workflow reads the json block below. It defines every video format this project produces.

A profile name is whatever the user types after `type video:`. If the name does not match, the first profile listed is used.

`breakFramePositions` is the source of truth for break frames — the count is derived from it. An empty list means the project uses no break frames.

```json
{
  "projectName": "What If",
  "profiles": {
    "short": {
      "sceneCount": 26,
      "aspectRatio": "9:16",
      "targetDuration": "90-150s",
      "voiceWordsPerScene": "8-15",
      "voiceMaxSentences": 2,
      "informationDensity": "medium",
      "breakFramePositions": [7, 14, 21],
      "voiceCharCap": 1500
    },
    "long": {
      "sceneCount": 26,
      "aspectRatio": "16:9",
      "targetDuration": "3-5 minutes",
      "voiceWordsPerScene": "25-40",
      "voiceMaxSentences": 4,
      "informationDensity": "high",
      "breakFramePositions": [7, 14, 21],
      "voiceCharCap": 6500
    }
  }
}
```

---

## Field Reference

| Field | Required | Meaning |
|---|---|---|
| `sceneCount` | yes | Total scenes in the video |
| `aspectRatio` | yes | Appended to every image prompt |
| `voiceWordsPerScene` | yes | Word budget per narration line |
| `voiceMaxSentences` | yes | Sentence ceiling per narration line |
| `voiceCharCap` | yes | Total narration character limit |
| `breakFramePositions` | no | Scene numbers that become break frames |
| `targetDuration` | no | Reference only |
| `informationDensity` | no | Reference only |
