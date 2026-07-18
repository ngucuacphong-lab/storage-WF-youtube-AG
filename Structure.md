# AI Video Workflow Project Structure

Version: 1.0

Status: FROZEN

---

## Purpose

This document explains the structure of the project.

It is intended for developers and maintainers.

This file is NOT part of the AI runtime prompts.

---

# Folder Structure

Project/

├── Story.md
├── Image.md
├── Voice.md
├── QA.md
├── LockPrompt.md
├── Structure.md
└── Architecture.md

---

# Runtime Files

These files are loaded by the workflow.

## Story.md

Defines storytelling principles.

Used by:
Story Node

---

## Image.md

Defines image generation rules.

Used by:
Image Node

---

## Voice.md

Defines voiceover generation rules.

Used by:
Voice Node

---

## QA.md

Defines quality control rules.

Used by:
QA Node

---

## LockPrompt.md

Defines immutable visual style.

Used by:
Image Node

---

# Documentation Files

These files are NOT loaded by the AI workflow.

## Structure.md

Explains project files.

---

## Architecture.md

Explains workflow architecture.

---

# Important

The workflow should never depend on this document during execution.

It exists only for documentation.