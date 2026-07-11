# Enterprise Playability Knowledge Base

This repository captures the working body of knowledge for Enterprise Playability (EP), including the Viper Method and guidance for using playability, gamification, motivation, and personas. The first ISS application, Viper Command, is referenced as an example of an EP application.

The repo is intentionally Markdown-first. Chat is the discovery space; this repository is the stabilized shared memory.

This README is the entrypoint for guidance work in the EP knowledge base. For the broader three-folder workspace, start with [`../ep-command.md`](../ep-command.md). For Command application work, start with [`../viper/viper-command/README.md`](../viper/viper-command/README.md). For CRANK blog work, start with [`../ratchet.agency/src/blog/README.md`](../ratchet.agency/src/blog/README.md).

## Start Here

For first-time readers working on EP guidance, read the repository in this order:

1. Read [Enterprise Playability (EP) – A Working Primer](playability-guide/enterprise-playability.md) for the broader EP framework.
2. Read [Persona-Driven UCD and Jobs to Be Done](persona-guide/persona-driven-ucd-and-jtbd.md) to understand how we use User-Centered Design, personas, and Jobs to be Done.
3. Read [Viper: A Short Tour](viper-method-guide/Viper-A-Short-Tour.md) for the core method language.
4. Refer to [Primary Persona: Scott](../viper/viper-command/persona-scott.md) to understand who Command is built for.
5. See [Viper Command Design Brief](../viper/viper-command/design-brief.md) for details on the design of Command.
6. Read [Viper Command Conceptual Domain Model](../viper/viper-command/conceptual-domain-model.md) for the high-level domain model of Command.
7. Use [YTHO](../ratchet.agency/src/blog/ytho-md.md) to understand and preserve why important project decisions were made.

This order introduces the philosophy, the design method, the first application, the founding persona, the domain language, and the decision history.

## Repository structure

```text
enterprise-playability-guide/
  README.md
  YTHO.md
  decision-records/
    0001-discover-promote-commit-workflow.md
  motivation-guide/
    tomo.md
  persona-guide/
    persona-driven-ucd-and-jtbd.md
    persona-universality.md
  playability-guide/
    enterprise-playability.md
    gamestorming.md
  viper-method-guide/
    Viper-A-Short-Tour.md
    Viper-Method-Principles-and-Mechanics.md
  ../viper/viper-command/
    design-brief.md
    persona-scott.md
    conceptual-domain-model.md
    story-beats.md
    ui-language.md
  ../ratchet.agency/src/blog/
    README.md
    reducing-the-cost-of-reorientation.md
    ytho-md.md
  assets/
    wireframes/
    diagrams/
```

## Working Principles

Nothing becomes truth until it is promoted into this repository.

Conversation is where ideas are explored, challenged, and refined. The repository is where accepted understanding is preserved. Every document in this repository represents the team's best current understanding and should be updated as that understanding evolves.

Before ending substantial work, leave the relevant Markdown documents in a state that lets a future session resume without reading previous chat history. Capture useful discoveries, decisions, definitions, constraints, and open questions where they belong.

Because this repository is public, our default operating model is transparent by design. Significant decisions, their rationale, and the concepts that guide Enterprise Playability should be captured here so that others can understand not only *what* we believe, but *why* we believe it.

## Why We Made These Decisions

See [YTHO](YTHO.md) for the decision records explaining why this repository and its documents are organized the way they are.

## Working agreement

- Trunk-based workflow: commit directly to `main` unless the team later discovers a need for branches.
- No CI/CD initially. Add automation only when publishing or validation needs create real demand.
- Markdown documents are first-class project artifacts.
- Major decisions should be captured in a YTHO/ADR-style record when doing so preserves shared understanding.

## Current focus

Command is the first EP application and the first demand-pulled probe for the broader ISS/Viper Platform body of knowledge. Its immediate purpose is to help the founding team maintain a shared model of reality while navigating formation decisions and tasks.
