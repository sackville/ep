# 0001: Discover, Promote, Commit Workflow

- Status: Accepted

## Context and Problem Statement

Enterprise Playability is being developed through collaborative conversations involving humans and AI. Conversations are valuable for exploration but are transient and difficult to revisit as the body of knowledge grows.

The project requires a workflow that preserves durable understanding without requiring future contributors to reconstruct past conversations.

## Considered Options

### Keep long-running conversations

Maintain a single conversation as the primary project memory.

### Preserve conversation summaries

Capture summaries of important conversations in the repository.

### Discover, Promote, Commit

Use conversations for discovery, promote durable understanding into the repository, and commit those changes to the project's primary branch.

## Decision Outcome

The project adopts a Discover, Promote, Commit workflow.

### Discover

Use conversations to explore ideas, challenge assumptions, and refine concepts.

### Promote

When an idea becomes sufficiently stable to guide future work, capture it in one or more repository documents.

The repository preserves discoveries rather than conversation history.

### Commit

Review the promoted changes, commit them to the repository, and treat the repository as the canonical source of shared understanding.

Future conversations should begin from the repository rather than depending on previous conversations.

## Consequences

Positive:

- Reduces dependence on long-lived chat history.
- Makes shared understanding durable and searchable.
- Improves onboarding for both humans and AI collaborators.
- Aligns the development process with Enterprise Playability's emphasis on preserving shared understanding.

Trade-offs:

- Promotion requires deliberate effort.
- Repository documentation becomes an active part of development rather than an afterthought.
