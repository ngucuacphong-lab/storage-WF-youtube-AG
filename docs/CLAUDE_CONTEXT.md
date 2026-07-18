# CLAUDE_CONTEXT.md

# AI Video Workflow Implementation Context

Version: 1.0

Status: FROZEN

---

# Purpose

This document provides the complete implementation context for Claude.

It explains:

- the purpose of the project
- the workflow architecture
- the responsibilities of every AI stage
- implementation rules
- non-negotiable constraints

This file exists only to help future implementation and maintenance.

It is NOT loaded by any runtime AI node.

---

# Project Goal

This project is an AI-powered workflow for automatically producing YouTube videos.

The workflow generates:

- Story
- Scripts
- Voiceover
- Image Prompts

followed by automatic quality validation before publishing.

The objective is to build a reusable AI Engine where only the project files change while the workflow remains unchanged.

---

# Core Philosophy

The workflow is the engine.

The project files provide knowledge.

Changing projects must never require modifying the workflow.

---

# Frozen Architecture

Topic

↓

Story

↓

Scripts

├───────────────┐

▼               ▼

Voice        Image

└──────┬────────┘

↓

QA

↓

Approval

↓

Audio

↓

Export

This architecture is frozen.

Implementation may change.

Architecture must not.

---

# Responsibilities

## Topic

Generate candidate video topics.

Output:

Topic

---

## Story

Generate the complete story structure.

Output:

Story JSON

Must NOT:

- write scripts
- generate voiceover
- generate image prompts

---

## Scripts

Generate detailed scene scripts.

Input:

Story JSON

Output:

Scripts JSON

Must NOT:

- generate voiceover
- generate image prompts

---

## Voice

Generate narration.

Input:

Scripts JSON

Output:

Voice JSON

Must NOT modify scripts.

---

## Image

Generate image prompts.

Input:

Scripts JSON

Output:

Image JSON

Must NOT modify scripts.

---

## QA

Validate every output.

Input:

Story JSON

Scripts JSON

Voice JSON

Image JSON

Output:

QA Report

QA never creates content.

QA only validates.

---

# Runtime Files

The workflow loads these files.

Story.md

Image.md

Voice.md

QA.md

LockPrompt.md

These files contain project-specific knowledge.

---

# Documentation Files

These files are NOT used during execution.

Structure.md

CLAUDE_CONTEXT.md

---

# Prompt Strategy

System prompts are hardcoded inside workflow nodes.

Project files are injected into user prompts.

This separation must remain unchanged.

---

# JSON Communication

Every AI stage communicates using JSON.

Avoid text parsing whenever possible.

Avoid regex-based communication between AI stages.

JSON contracts are the primary communication method.

---

# Design Principles

- Single Responsibility
- Deterministic Outputs
- Clear Data Contracts
- Reusable Workflow
- Project Independence

---

# Non-Negotiable Rules

Do NOT redesign the architecture.

Do NOT merge AI stages.

Do NOT combine multiple responsibilities into one AI node.

Do NOT remove QA.

Do NOT bypass JSON contracts.

Do NOT modify project philosophy.

---

# Claude's Role

Claude is the implementation engineer.

Claude is NOT the system architect.

Claude should:

- implement the workflow
- improve maintainability
- reduce implementation bugs
- preserve the frozen architecture

Claude must never redesign the system unless explicitly instructed.

---

# Current Project Status

Architecture:
Frozen

Data Contracts:
Frozen

System Prompts:
Frozen

Workflow:
Implementation in progress

Current objective:

Implement the workflow according to the frozen design without changing its architecture.