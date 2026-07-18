# DependencyMap.md

Version: 1.0

Status: FROZEN

---

# Purpose

This document is the single source of truth for workflow dependencies.

It defines:

- stage dependencies
- data dependencies
- downstream consumers
- retry dependencies
- validation dependencies
- JSON Contract flow

Unlike DataFlow.md, this document does NOT describe execution order.

Instead, it describes which stages depend on which outputs.

Every workflow modification must consult this document before changing any node.

---

# Goals

DependencyMap exists to guarantee that architecture changes remain synchronized across the entire workflow.

Whenever a stage changes, every downstream consumer can immediately be identified.

This prevents partial updates that silently break the pipeline.

---

# Scope

DependencyMap documents only architecture.

It never contains prompts.

It never contains business logic.

It never contains implementation code.

It never describes how to generate content.

It only describes relationships.

---

# Required Information

Every stage must document:

- Stage Name
- Purpose
- Consumes
- Produces
- Direct Consumers
- Upstream Dependencies
- Validation Node
- Retry Path
- JSON Contract
- Notes

---

# Dependency Rules

A stage may consume only documented outputs.

A stage may not depend on hidden side effects.

Every dependency must be explicit.

Every produced Contract must list all downstream consumers.

---

# Contract Rules

For every Contract document:

Producer

Consumers

Validation Node

Retry Owner

Contract Version

---

# Retry Rules

Every retry path must identify:

Origin Stage

Retry Counter

Retry Decision Node

Retry Delay

Maximum Retry Count

No retry path may be undocumented.

---

# Validation Rules

Every Contract must have exactly one validation owner.

Validation ownership must be unique.

Validation ownership must not overlap.

---

# Workflow Modification Rules

Before modifying any node:

1. Read DependencyMap.md.

2. Identify every downstream consumer.

3. Identify every Contract affected.

4. Identify validation ownership.

5. Identify retry ownership.

6. Update every affected node.

7. Perform compatibility verification.

A workflow modification is not complete until every downstream dependency has been updated.

---

# Future Extensions

New stages must be added here before implementation.

Removed stages must be removed here.

Changed Contracts must update dependency relationships here first.

DependencyMap must always represent the current architecture.

This file is considered architecture documentation and must remain synchronized with the workflow.