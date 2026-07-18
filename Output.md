# Output Rules

## Purpose

Define the required output structure for every generation node.

All outputs must be structured, consistent, and easy for downstream nodes to process.

All generation nodes must return valid JSON.

---

# General JSON Rules

## Format

Output must be valid JSON only.

Do not include:

- Markdown formatting.
- Explanations outside JSON.
- Comments.
- Additional text.

---

## Structure Rules

Every generated scene must contain a scene identifier.

Scene numbering must remain consistent across:

- Script
- Voiceover
- Image Prompt
- QA

---

# Scene Object

Each scene should follow this structure:

```json
{
  "scene": 1,
  "script": "",
  "voiceover": "",
  "image_prompt": ""
}
```

---

# Script Output

## Required Fields

```json
{
  "scene": 1,
  "script": ""
}
```

## Rules

Script must contain only the story content.

Do not include:

- Voice instructions.
- Image instructions.
- Metadata.
- Comments.

---

# Voice Output

## Required Fields

```json
{
  "scene": 1,
  "voiceover": ""
}
```

## Rules

Voiceover must contain only spoken narration.

Do not include:

- Scene labels.
- Speaker names.
- Sound effects.
- Production notes.

---

# Image Prompt Output

## Required Fields

```json
{
  "scene": 1,
  "image_prompt": ""
}
```

## Rules

Image prompt must contain only visual generation instructions.

Do not include:

- Voiceover text.
- Explanations.
- Production comments.

---

# Break Frame Output

## Required Fields

```json
{
  "scene": 1,
  "type": "question",
  "text": ""
}
```

## Allowed Types

```
question
fact
```

## Rules

Break frame content must be:

- Short.
- Clear.
- Related to the story.
- Easy to understand.

---

# Complete Video Output

When combining all generated data:

Use a scene-based structure.

Example:

```json
{
  "video": {
    "title": "",
    "scenes": [
      {
        "scene": 1,
        "script": "",
        "voiceover": "",
        "image_prompt": ""
      }
    ]
  }
}
```

---

# Data Consistency Rules

All nodes must maintain:

- Same scene numbers.
- Same scene order.
- Same topic.
- Same character references.

A scene should not exist in one output but be missing in another.

---

# Validation Rules

Before passing data to the next node:

Check:

- Valid JSON.
- Required fields exist.
- No empty required fields.
- Scene numbers are correct.
- No unexpected fields.
- No duplicated scenes.

---

# Forbidden

Do not output invalid JSON.

Do not mix multiple scenes into one object.

Do not add unnecessary metadata.

Do not change field names.

Do not rename required keys.

Do not add explanations outside JSON.