---
name: to-spec
description: "Turn the current, confirmed grill-me feature discussion into a task spec under docs/specs: no interview, just synthesis of what you have already discussed."
disable-model-invocation: true
---

This skill takes the current conversation context and produces a task spec from a completed, user-confirmed `grill-me` discussion. Do NOT interview the user; just synthesize what you already know.

Do not use this skill as a general-purpose spec writer.

## Preconditions

The current conversation must contain all of the following:

- A completed `grill-me` discussion about a software feature.
- The user's explicit confirmation that the shared-understanding recap is correct.
- No open question that would block implementation or acceptance, unless the user has explicitly accepted the risk.

If a precondition is missing, do not create a `Ready` spec, invent requirements, or begin another interview. State the missing prerequisite and direct the user back to `grill-me`.

## Process

1. Explore the repository only when needed to verify vocabulary or a fact already relevant to the confirmed discussion. If a discovered contradiction would change the requirement or acceptance criteria, stop and return it to the user as a decision. Do not silently resolve it.

2. Create `docs/specs/` at the repository root if it does not exist. Write the task spec to `docs/specs/<feature-slug>.md`, using a short kebab-case slug derived from the feature name.

3. Do not overwrite an unrelated task spec. Update an existing document only when it is clearly the same feature; otherwise ask for a different feature name or explicit permission to update it.

4. Write the spec using this template:

```markdown
# <Feature name>

Status: Ready

## Problem Statement

The problem the user is facing, from the user's perspective.

## What to Build

The confirmed, user-visible behavior to deliver. Put a constraint here only when it directly qualifies that behavior.

## Out of Scope / Must Not Change

The behavior, interface, or data that this work must not alter, plus anything explicitly excluded from the task.

## Acceptance Criteria

- [ ] <An observable, decidable completion condition>
```

Do NOT add a long user-story list, speculative implementation plans, file paths, code snippets, or fixed sections for constraints and verification. If an acceptance criterion needs particular evidence, state that evidence beside the criterion itself.

After writing the document, report its path and that it is ready for a later implementation session. Do not automatically implement, split tickets, or create other documents.
