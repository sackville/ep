# Command UI Language

This document extracts the fixed visual vocabulary from the Command Design Brief.

## Tone

Warm tech tree. Legible enough to orient in seconds, alive enough to want to look at.

## Regions

| Region | Meaning |
|---|---|
| Wake | Settled, dated history. |
| Today seam | Boundary between measured past and undated dependency structure. |
| Frontier | Available, queued, locked, or undefined work. |
| Exogenous track | External forces outside the team's control. |
| Headcount band | Team size over measured time. |

## Color rule

Hue means ownership and nothing else.

State is encoded through fill, border, badge, fog, and other non-hue treatments.

## Node states

| State | Meaning |
|---|---|
| Researched | Settled. Lives in the wake. |
| Available | Actionable now. |
| Locked | Visible but not reachable. |
| Process-undefined | Exists, but its governing process has not been chosen. |
| Orphan | No one owns the unblocking. |
| Recursive | Collapses a sub-graph. |

## Signature mechanics

### Interior fog

Process-undefined nodes hide their outgoing structure until the process is authored as data.

### Cascade

Settling a node lights downstream relationships and reveals what has become available.
