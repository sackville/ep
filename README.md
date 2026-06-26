# Enterprise Playability Knowledge Base

This repository captures the working body of knowledge for Enterprise Playability (EP), the Viper Method, and the first ISS application, Command.

The repo is intentionally Markdown-first. Chat is the discovery space; this repository is the stabilized shared memory.

## Start Here

For first-time readers, read the repository in this order:

1. Read [Enterprise Playability (EP) – A Working Primer](philosophy/enterprise-playability.md) for the broader EP framework.
2. Read [Persona-Driven UCD and Jobs to Be Done – Synthesis for ISS](philosophy/persona-driven-ucd-and-jtbd.md) to understand how we use User-Centered Design, personas, and Jobs to be Done.
3. Read [Viper: A Short Tour](philosophy/viper.md) for the core method language.
4. Refer to [Primary Persona: Scott](command/persona-scott-decision-facilitator.md) to understand who Command is built for.
5. See [Command — Design Brief (MVP)](command/design-brief.md) for details on the design of Command.
6. Read [Command Conceptual Domain Model](command/conceptual-domain-model.md) for the high-level domain model of Command.
7. Use [YTHO](YTHO.md) to understand and preserve why important project decisions were made.

This order introduces the philosophy, the design method, the first application, the founding persona, the domain language, and the decision history.

## Repository structure

```text
ep/
  README.md
  YTHO.md
  philosophy/
    enterprise-playability.md
    gamestorming.md
    tomo.md
    viper.md
    persona-driven-ucd-and-jtbd.md
    persona-universality.md
    ytho.md
  command/
    design-brief.md
    persona-scott-decision-facilitator.md
    conceptual-domain-model.md
    story-beats.md
    ui-language.md
  blog/
    reducing-the-cost-of-reorientation.md
  assets/
    wireframes/
    diagrams/
```

## Working Principles

Nothing becomes truth until it is promoted into this repository.

Conversation is where ideas are explored, challenged, and refined. The repository is where accepted understanding is preserved. Every document in this repository represents the team's best current understanding and should be updated as that understanding evolves.

Because this repository is public, our default operating model is transparent by design. Significant decisions, their rationale, and the concepts that guide Enterprise Playability should be captured here so that others can understand not only *what* we believe, but *why* we believe it.

## Why We Made These Decisions

See [YTHO](YTHO.md) for the decision records explaining why this repository and its documents are organized the way they are.

## Working agreement

- Trunk-based workflow: commit directly to `main` unless the team later discovers a need for branches.
- No CI/CD initially. Add automation only when publishing or validation needs create real demand.
- Markdown documents are first-class project artifacts.
- Major decisions should be captured in a YTHO/ADR-style record when doing so preserves shared understanding.

## Current focus

Command is the first EP application and the first demand-pulled probe for the broader ISS/Viper body of knowledge. Its immediate purpose is to help the founding team maintain a shared model of reality while navigating formation decisions.
