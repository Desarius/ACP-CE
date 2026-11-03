# Proposed ACP-CE Experiments

**No experiments in this document have been conducted or validated.**

## E01 — Recall versus durable adaptation

**Hypothesis:** Agents with real adaptation mechanisms outperform retrieval-only systems on novel transfer tasks even when episodic memory access is removed at evaluation.

**Groups:** Frozen stateless model; frozen model with episodic memory; model with an auditable adaptation mechanism. Control exposure, task mix and compute where feasible.

**Falsifier:** No reliable transfer advantage after retrieval is ablated.

## E02 — Continuity versus shuffled experience

**Hypothesis:** Temporally ordered experience improves reasoning about delayed effects relative to matched shuffled exposure.

Use equivalent event sets and test on held-out causal-order tasks. Report seeds, budgets and confidence intervals.

**Falsifier:** No replicable advantage for temporally coherent experience.

## E03 — Spontaneous cognition

**Hypothesis:** Bounded self-directed reflection generates useful discoveries beyond an equal-compute scheduled-reflection baseline.

Measure transfer, novelty quality, error rate and wasted computation. Include negative results.

**Falsifier:** No benefit or worse calibration relative to the matched control.

## E04 — History-dependent individualization

**Hypothesis:** Identical starting models subjected to different histories develop stable, revisable choices in blinded tasks unrelated to their exposure content.

Ablate explicit autobiographical prompts; use blinded evaluators and later changed environments.

**Falsifier:** Differences vanish under these controls or track only directly retrieved statements.

## Mandatory reporting

Record model/checkpoint IDs, training/update mechanism, seeds, environment versions, event logs, prompts, token and compute budgets, exclusions, negative outcomes, statistics and safety boundaries. No self-report alone establishes sentience or consciousness.
