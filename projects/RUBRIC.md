# Project Plan Rubric

Each criterion is scored **1–4**. A plan is **accepted** when every row scores **3 or higher**.

| Score | Level | Meaning |
|---|---|---|
| **4** | Exemplary | Above bar; model answer for future cohorts |
| **3** | Proficient | Meets bar; plan accepted, project starts |
| **2** | Developing | Revise and resubmit before starting |
| **1** | Insufficient | Idea needs a rethink, not a polish |

---

## Scoring matrix

| # | Criterion | 1 — Insufficient | 2 — Developing | 3 — Proficient *(accept)* | 4 — Exemplary |
|---|---|---|---|---|---|
| 1 | **Concept Selection** | Concepts not named, or all 5 listed without labels | Fewer than 3 concepts named, or basic/expert labels misapplied (e.g., 3 basic + 0 expert) | Exactly 3 of 5 concepts named with the correct **2 basic + 1 expert** split | The 3 concepts compound into a coherent project identity (e.g., GraphRAG × Engineering Rigor × Multimodal naturally reinforce each other) |
| 2 | **Basic Depth (×2)** | Both basic concepts vague ("we'll add monitoring") | One concrete, one vague | Both name a specific stack/pattern *and* the integration point | Both also commit to a small testable behavior (e.g., "5 eval cases in CI catching budget violations") |
| 3 | **Expert Depth (×1)** | No expert concept identified, or it's no deeper than the basic ones | Expert is *"we'll use [framework]"* — nothing custom | Names a non-trivial custom commitment beyond off-the-shelf framework use (e.g., custom planner with replanning on N tool failures) | Custom commitment **plus** a named baseline to evaluate against (e.g., "vs. plain ReAct on the same task suite") |
| 4 | **Problem Fit** | Generic pitch ("AI for healthcare") | Domain named but user/workflow vague ("clinics," "small businesses") | Specific named user/stakeholder, specific named pain, specific named workflow | Adds evidence the pain is real — user interview, observed behavior, or market signal |
| 5 | **Why Agentic** | Problem is solvable by a single prompt; agentic plumbing is unjustified | "We want to build an agent" with no justification of necessity | One clear sentence justifying why an agent loop is needed instead of a prompt or script | Names the specific failure mode of a non-agentic approach this design avoids |
| 6 | **Architecture Sketch** | None, or just a name with no structure | Agents named but loop structure or stop conditions missing | Diagram or numbered list naming: agents, roles, tools each can call, control flow, and stop conditions (~6–10 lines pseudocode + I/O box) | Adds explicit state model and I/O contract; could be handed to another team to build |
| 7 | **Scope (MVP vs Stretch)** | No scope discussion, or proposed scope is clearly impossible | MVP and stretch blended together, or MVP too ambitious for the team's remaining time | MVP cleanly separated from stretch goals; MVP achievable for the team as constituted in the remaining timeline | Tiered as **MVP / MVP+1 / MVP+2**, each a defined buildable unit; team capacity explicitly checked against timeline |
| 8 | **Success Criteria** | No success criteria stated | Criteria stated but none measurable ("works well", "users like it") | At least one *measurable* criterion (e.g., "agent stays under budget on 9/10 test cases") | Multiple measurable criteria spanning at least one quality metric **and** one cost/efficiency metric |
| 9 | **Risk + First Probe** | No risks named | Risk named but no probe, or generic risk ("we might run out of time") | Top single risk named **with** a concrete first-week experiment to test it | Top **2** risks, each with a probe **and** a kill criterion (when to pivot) |
| 10 | **Deliverables** | No deliverable plan stated | Some named (e.g., repo) but others missing or vague | Names: (a) code repo, (b) demo format, (c) LinkedIn post topic, (d) Medium article topic — all tied to chosen role × niche from Assignment 1 | Adds rough publishing dates aligned with the cohort timeline |

---

## Group rule

A group of **N** people delivers roughly **MVP + (N−1) stretch goals** of scope. The basic/expert labels apply per-project, not per-person — one expert concept covered well is enough for a group.

## Mentor review process

- **All rows ≥ 3** → plan accepted, project starts.
- **1–2 rows at 2** → returned with notes; team revises and resubmits.
- **Any row at 1, or 3+ rows at 2** → the idea needs a rethink, not a polish.

## Self-check before submission

Before sending the plan to a mentor, score yourself honestly. If you can't justify a 3 in your own head for every row, the plan isn't ready — keep iterating. Mentor time is for plans you believe in, not for triage.
