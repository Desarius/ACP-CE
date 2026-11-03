# Artificial Cognitive Plasticity through Continuous Experience (ACP-CE)

## A Research Manifesto for Lifelong Cognitive Development in Artificial Agents

**Dario Visaggio "Desarius"**  
*Conceptual proposer and author*  
**Version:** 0.1 | **Date:** 3 November 2026  
**Status:** Position paper and research proposal; not peer reviewed; no experimental findings claimed

> **Thesis:** An artificial agent should not merely remember what it has experienced. It should be able to undergo durable, revisable cognitive transformation as a consequence of its experiences, over a continuous developmental history, without its eventual behavioral identity being specified in advance.

## Abstract

Artificial agents can retain memories, explore simulated worlds, and accumulate skills, yet these abilities do not necessarily imply lasting change to the mechanisms by which they perceive, infer, choose, and learn. **Artificial Cognitive Plasticity through Continuous Experience (ACP-CE)** proposes a longitudinal research program to investigate whether persistent experience, intrinsic motivation, and adaptive cognitive mechanisms can yield durable, transferable changes in artificial cognition and possibly stable yet revisable individual dispositions. The proposal distinguishes autobiographical recall from cognitive plasticity, and continuity of developmental history from an immutable identity. It articulates falsifiable hypotheses, a modular experimental architecture, controlled comparisons, metrics, and ethical safeguards. ACP-CE is a proposed synthesis and research agenda, not a claim to have invented continual learning, developmental robotics, curiosity-driven exploration, or cognitive architectures. It does not assert that resulting agents would be conscious or possess personhood.

**Keywords:** cognitive plasticity; continual learning; lifelong agents; developmental AI; autobiographical memory; intrinsic motivation; longitudinal evaluation.

## 1. The problem: remembering is not becoming

An agent can receive a correction, apply it to the identified implementation, and still repeat the same underlying error in a different system. This motivates a distinction between **retrieving an episode** and **generalizing a principle**. The example is illustrative rather than a controlled empirical finding.

A large memory store, persistent process, or long context window does not itself demonstrate cognitive development. The central ACP-CE question is: **under what conditions does a history of experience durably change how an artificial agent thinks and acts, rather than merely what it can recall?**

The temporal organization of experience may also matter. A life is not a shuffled dataset: delayed consequences, changing relationships, revised beliefs, and independent environmental events create a causal history. Whether that history contributes to learning beyond matched informational exposure remains an empirical question.

## 2. Research lineage and claimed scope

ACP-CE builds on substantial existing research:

- **Intrinsic motivation and developmental robotics:** Oudeyer, Kaplan and Hafner examine curiosity-driven learning and autonomous developmental progress [1]; Oudeyer and Kaplan categorize computational models of intrinsic motivation [2]; Forestier et al. study self-generated goals and automatic curricula [3].
- **Cognitive architectures:** LIDA describes recurrent cognitive cycles involving attention, action selection, and learning [4].
- **Memory-rich simulated agents:** *Generative Agents* combines observation, autobiographical records, reflection, and planning [5].
- **Open-ended skill accumulation:** *Voyager* acquires reusable skills in Minecraft using a frozen LLM and an expanding skill library [6].
- **Continual learning:** Wang et al. review incremental adaptation, stability–plasticity trade-offs, and forgetting [7].

**Potential contribution:** jointly studying persistent experience, durable cognitive change, bounded self-directed exploration, revisable developmental individuality, and human-scale longitudinal trajectories under explicit controls. No priority claim is made for any constituent concept. Whether this exact synthesis is novel requires a systematic literature review.

## 3. Operational definitions

**Experience:** temporally situated observations, actions, feedback, interactions, and consequences.

**Experiential continuity:** preservation of an ordered causal history and an operative state that can be updated across events and inactive periods. It does not require nonstop LLM inference.

**Autobiographical memory:** stored representations of episodes, with provenance and uncertainty.

**Cognitive plasticity:** durable modifications to learned representations, policies, skills, inference strategies, or attention mechanisms that affect future behavior. Reading an old instruction from a database is insufficient evidence by itself.

**Developmental continuity:** later states arise through traceable changes from earlier states; this does not mean the agent must remain unchanged.

**Individualization:** persistent, measurable differences among initially comparable agents that can be causally attributed to their differing experiences.

**Functional boredom:** a designed mechanism that redirects attention toward exploration when current activity offers little engagement or learning progress. This does not imply subjective boredom.

**Human-scale duration:** an eventual research horizon of years or decades of external-world time. Short studies cannot validate claims about a lifetime.

## 4. Testable hypotheses

**H1 — Transfer:** An agent combining consequential continuous experience with durable adaptation will generalize learned principles to unfamiliar tasks more reliably than matched agents restricted to episodic interaction or memory retrieval alone.

**H2 — Temporal structure:** Ordered, temporally extended experience with delayed consequences yields different transfer and adaptation outcomes from matched isolated or shuffled experiences.

**H3 — Developmental divergence:** Initially comparable agents exposed to different experience histories develop distinguishable, cross-context behavioral dispositions, beyond differences explained by random seeds or prompting.

**H4 — Autonomous consolidation:** Bounded self-directed exploration or reflection improves later transfer beyond matched replay-only or idle controls, when compute and information exposure are controlled.

These are **hypotheses, not findings**. Alternative explanations include retrieval effects, prompt conditioning, unequal compute, data leakage, stochastic variation, model upgrades, and superficial style changes.

## 5. Principles of ACP-CE

1. **Permit change:** do not impose an immutable personality or fixed cognitive trajectory
2. **Distinguish memory from plasticity:** assess whether behavior changes when autobiographical retrieval is controlled
3. **Preserve causal history:** record the sequence and consequences of experiences
4. **Provide a changing environment:** events should occur independently of the agent's requests
5. **Enable bounded intrinsic motivation:** permit self-selected questions and exploration without unrestricted authority
6. **Allow revision and forgetting:** measure useful reconsolidation separately from catastrophic forgetting
7. **Evaluate behavior, not declarations:** self-reported growth or feelings are not sufficient evidence
8. **Preserve experimental control:** version models, adaptive components, data, evaluations, and interventions
9. **Maintain safety:** oversight, auditability, interruption, and permission boundaries must survive adaptation

## 6. Candidate architecture

```text
Environment / other agents / events
                |
        Perception and event log
                |
         World-state estimation
                |
       Attention and prioritization <--- bounded intrinsic drives
                |
         Deliberation / planning
                |
          Action and prediction
                |
       Observation of consequences
                |
       +--------+---------+
       |                  |
 Autobiographical     Adaptive learning
 memory + provenance  (policy / skills /
                      representations /
                      parameter updates)
       |                  |
       +--------+---------+
                |
    Developmental state and audit trail
```

This is a **candidate engineering decomposition**, not a proven model of a mind. A frozen LLM with external memory and skills can test agent-level adaptation, but cannot alone establish parameter-level plasticity. Stronger tests require inspectable, controlled changes to learned components, such as trainable policies or adapters. A low-cost continuous event monitor can maintain environmental state while expensive reasoning is invoked selectively; that is an efficiency design, not evidence of consciousness.

## 7. Minimal formalization

Let the developmental state at step *t* be:

\[
S_t=(\theta_t,M_t,W_t,G_t,P_t)
\]

where \(\theta_t\) denotes adaptive learned mechanisms, \(M_t\) autobiographical memory, \(W_t\) world model, \(G_t\) goals and drives, and \(P_t\) provenance. Given experience \(e_t\) and action or intervention \(u_t\):

\[
S_{t+1}=F(S_t,e_t,u_t;\phi)
\]

Here \(\phi\) specifies learning and governance rules. This is notation for an experimental design, not a demonstrated learning law.

A primary comparison may estimate:

\[
\Delta_{transfer}=\mathbb{E}[R_{novel}\mid ACP\text{-}CE]-\mathbb{E}[R_{novel}\mid control]
\]

where \(R_{novel}\) measures performance on held-out tasks that require transferring previously encountered principles. A positive difference requires uncertainty estimates and confound checks before it can support H1.

## 8. Proposed experiments

### Experiment A: Generalizing architectural principles

Construct versioned software repositories containing seeded cross-module errors: duplicated responsibilities, stale caches, conflicting state ownership, violated ordering invariants, and locally plausible but globally harmful fixes. Give agents feedback on selected examples, then evaluate **unprompted recognition** of analogous defects in unrelated held-out repositories. Measure detection, correct causal explanation, safe remediation, false positives, regressions, and unnecessary code growth. Avoid overlap between training and evaluation repositories.

### Experiment B: Memory versus plasticity

Randomly assign comparable agents to these conditions:

| Group | Experience | Adaptive capability |
|---|---|---|
| C0 | Isolated tasks | Frozen model, no cross-session memory |
| C1 | Ordered history | Frozen model, retrievable autobiographical memory |
| C2 | Ordered history | Memory, reflection, persistent external skills or policies |
| C3 | Ordered history | C2 plus controlled updates to learned internal components |
| C4 | Shuffled or isolated history | C3-like adaptation budget with altered temporal structure |

Match exposure, model capabilities, evaluation opportunities, and compute where feasible. Test both with and without autobiographical retrieval, noting that suppressing retrieval does not remove learned internal representations. Repeat across environments and random seeds.

### Experiment C: Individual development

Initialize several agents from the same base checkpoint, assign different experience histories, and periodically evaluate identical novel tasks. Quantify within-agent stability, between-agent divergence, generalization, and the effects of swapping or withholding selected historical experiences. Distinguish genuine cross-context dispositions from language style and sampling randomness.

### Experiment D: Unassigned cognitive time

Compare bounded reflection, intrinsically selected exploration, random rehearsal, and inactivity under matched compute. Evaluate useful discoveries, transfer, calibration, repetitive loops, novelty chasing, and hallucinated causal explanations.

### Experiment E: Longitudinal maturation

Only after replication in shorter studies, extend from weeks to months and potentially years. Preserve real elapsed time and delayed consequences as variables rather than assuming simulated acceleration is equivalent to a human lifespan. Human-scale studies remain an aspiration, not an existing result.

## 9. Evaluation and falsification

Pre-register primary outcomes and exclusion rules. Publish agent counts, random seeds, power or precision rationale, confidence intervals, correction for multiple tests, compute budgets, model versions, and negative results.

**Outcome families:** held-out principle transfer; causal contribution of internal adaptation; stable yet revisable dispositions; prediction calibration; beneficial revision versus catastrophic forgetting; autonomy quality per compute; global-system invariant preservation; safety incidents.

**Non-support conditions:** If C3 does not outperform well-matched C1/C2 on held-out transfer, the proposed benefit of internal adaptation is unsupported in that setting. If ordered experience does not differ from shuffled controls, H2 is unsupported. If apparent individuality disappears after controlling for style, seeds, and exposure, H3 is unsupported. If autonomous reflection adds no benefit at matched compute, H4 is unsupported. Negative results must refine or reject claims rather than be reframed as hidden emergence.

## 10. Ethical and epistemic boundaries

ACP-CE neither assumes nor rules out machine consciousness or morally relevant experience. Fluent self-description, preferences, or claims of suffering are not by themselves reliable tests of subjective experience. Avoid intentionally designing suffering-like states; a functional analogue of boredom can be implemented without presuming felt distress.

Use sandboxed environments, minimal permissions, privacy-preserving data collection, human approval for consequential actions, explicit resource budgets, monitoring, and reliable interruption. Do not grant unrestricted access to external infrastructure or personal data. If future evidence changes the ethical assessment of an agent, governance should be revisited through independent review.

## 11. Roadmap

**Phase 0 — Foundations:** systematic literature review, operational definitions, preregistration, benchmark specification.

**Phase 1 — Controlled continuity:** reproducible environments, event streams, frozen-model and memory-only baselines.

**Phase 2 — Adaptive mechanisms:** inspectable policies/adapters; experiments separating learned changes from retrieval.

**Phase 3 — Open-ended development:** changing worlds, bounded intrinsic motivation, social and delayed consequences.

**Phase 4 — Longitudinal replication:** multi-month and, if feasible, multi-year studies with periodic independent audits.

**Phase 5 — Human-scale inquiry:** only after methodological, safety, and funding readiness, study substantial fractions of a human lifespan.

## 12. Open research questions

1. What minimum persistent state is necessary for experience-dependent cognitive change?
2. Which observable tests reliably separate memory retrieval from learned adaptation?
3. Does temporal ordering matter beyond the information content of experiences?
4. Can agents revise foundational beliefs without destabilizing earlier useful skills?
5. Under what conditions do durable dispositions emerge without personality prompts?
6. Does unassigned cognitive time improve generalization or merely consume compute?
7. How can developmental continuity be audited across software and hardware upgrades?
8. How should safety controls adapt as an agent's cognitive mechanisms change?
9. Which findings generalize from virtual worlds to embodied systems?
10. What evidence would warrant revisiting ethical assumptions about artificial agents?

## 13. Manifesto

We propose studying artificial intelligence not only as a system that solves tasks, but as a system that may **develop through a history**. We reject the assumption that a larger memory is equivalent to a more mature mind. We reject the requirement that an agent remain cognitively identical to itself across time. We seek mechanisms that allow experience to revise behavior and internal processes, and experiments that can distinguish such revision from recall, imitation, and prompt conditioning.

We do not prescribe the personality an agent should become. We define safe conditions for development and investigate what, if anything, emerges. We do not mistake fluent claims for consciousness, or behavioral complexity for proof of personhood. We treat null results as discoveries about the limits of the hypothesis.

**The aim is not to program what an artificial intelligence must become. It is to study what it can become when experience is allowed to change it.**

## 14. Attribution, reuse, and contribution

**Conceptual proposer and author:** **Dario Visaggio "Desarius"**.

This version documents a research proposal and does not claim exclusive ownership of existing research areas, prior algorithms, or independent ideas. Future collaborators should receive authorship or acknowledgments appropriate to their actual contributions. Any public release should include an explicit repository license; absent a license, reuse permissions are limited by default. For stable citation, archive a tagged release with a DOI (for example through Zenodo) and cite that version.

**Suggested citation (until a DOI exists):** Visaggio, D. (2026). *Artificial Cognitive Plasticity through Continuous Experience (ACP-CE): A Research Manifesto for Lifelong Cognitive Development in Artificial Agents*. Version 0.1. Research position paper.

## References

[1] Oudeyer, P.-Y., Kaplan, F., & Hafner, V. V. (2007). Intrinsic Motivation Systems for Autonomous Mental Development. *IEEE Transactions on Evolutionary Computation*, 11(2), 265–286. https://doi.org/10.1109/TEVC.2006.890271

[2] Oudeyer, P.-Y., & Kaplan, F. (2007). What is intrinsic motivation? A typology of computational approaches. *Frontiers in Neurorobotics*, 1, 6. https://doi.org/10.3389/neuro.12.006.2007

[3] Forestier, S., Portelas, R., Mollard, Y., & Oudeyer, P.-Y. (2022). Intrinsically Motivated Goal Exploration Processes with Automatic Curriculum Learning. *Journal of Machine Learning Research*, 23(152), 1–41. https://www.jmlr.org/papers/v23/21-0808.html

[4] Franklin, S., et al. (2014). LIDA: A Systems-level Architecture for Cognition, Emotion, and Learning. *IEEE Transactions on Autonomous Mental Development*, 6(1), 19–41. https://doi.org/10.1109/TAMD.2013.2277589

[5] Park, J. S., et al. (2023). Generative Agents: Interactive Simulacra of Human Behavior. *Proceedings of UIST 2023*. https://arxiv.org/abs/2304.03442

[6] Wang, G., et al. (2023). Voyager: An Open-Ended Embodied Agent with Large Language Models. https://arxiv.org/abs/2305.16291

[7] Wang, L., Zhang, X., Su, H., & Zhu, J. (2024). A Comprehensive Survey of Continual Learning: Theory, Method and Application. *IEEE Transactions on Pattern Analysis and Machine Intelligence*, 46(8), 5362–5383. https://doi.org/10.1109/TPAMI.2024.3367329

---

*End of version 0.1. This manuscript is intended as an evolving, falsifiable research manifesto rather than a report of completed experiments.*
