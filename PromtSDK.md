# PromptSDK.md Context

This document defines the prompt construction standard for every AI stage in the workflow.

It specifies how runtime prompts are assembled, which markdown files each AI stage may use, how structured data is exchanged between stages, and the responsibilities of each stage.

The purpose of this specification is to ensure that workflow logic, project behavior, runtime data, and workflow architecture remain clearly separated.

PromptSDK.md does not define workflow architecture.

It does not define business logic.

It does not define project-specific prompts.

It does not define stage dependencies.

Instead, it defines the common runtime prompt framework that every AI stage must follow.

Workflow architecture, stage dependencies, Contract ownership, validation ownership, retry ownership, and downstream relationships are defined exclusively in DependencyMap.md.

Execution order and runtime pipeline behavior are defined in DataFlow.md.

Stage-specific behavior is defined only inside the corresponding prompt documents (Story.md, Image.md, Voice.md, QA.md, CharacterLockPrompt.md, etc.).

Before modifying any workflow component, the implementation must first consult DependencyMap.md to determine all affected downstream consumers and Contracts, then consult DataFlow.md to understand execution order, and finally apply the PromptSDK rules when constructing or modifying prompts.

All AI implementations, workflow modifications, and future stages must remain compatible with this specification.

If any implementation conflicts with this document, PromptSDK.md takes precedence over the implementation for prompt construction.

If any dependency information conflicts with PromptSDK.md, DependencyMap.md is the source of truth for workflow architecture.

This specification is intended for workflow developers and AI implementation. It is never included directly in runtime prompts sent to an LLM.