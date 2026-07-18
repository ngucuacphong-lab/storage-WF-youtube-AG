# Data Flow Contract

Version: 1.0

Status: FROZEN

---


# Purpose

This document defines how data flows between AI stages.

It describes execution order, Contract flow, and runtime communication between stages.

Dependency ownership, downstream relationships, retry ownership, validation ownership, and architectural relationships are NOT defined here.

Those responsibilities belong exclusively to DependencyMap.md.

Every AI node must consume only the Contract produced by the previous stage.

No node may reconstruct missing information.

No node may infer hidden context.

Execution order must remain independent from workflow architecture..

---

# Pipeline

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

---

# Stage Inputs

## Story

Input

Topic

Video Profile

Output

Story Contract

---

## Scripts

Input

Story Contract

Output

Scripts Contract

---

## Voice

Input

Scripts Contract

Output

Voice Contract

---

## Image

Input

Scripts Contract

Output

Image Contract

---

## QA

Input

Story Contract

Scripts Contract

Voice Contract

Image Contract

Output

QA Contract

---

# Dependency Rules

Story depends only on Topic.

Scripts depends only on Story.

Voice depends only on Scripts.

Image depends only on Scripts.

QA depends on all previous contracts.

No node may skip a dependency.

---

# Communication Rules

AI stages communicate only through contracts.

Never through free-form text.

Never through hidden assumptions.

Every contract must declare its schema version.

---

# Validation Rules

Each node must validate its input contract before generation.

If validation fails:

- Stop generation.
- Return a structured error.
- Never guess missing fields.

---

# Backward Compatibility

Future contract versions must increment the schema version.

Older contracts must not be silently interpreted as newer versions.

---

# Forbidden

Nodes must NOT:

- Read downstream contracts.
- Modify upstream contracts.
- Merge responsibilities.
- Generate outputs outside their responsibility.