# Cohort Review — Sprint 1

---

## What this cohort is

You're being given a **blueprint** — the steps to take to build your way to technical AI expertise.

We provide the blueprint and the support. **You drive.**

---

## What this review is

Going over everything we've covered so far, so everyone is up to speed with where you should ideally be by now — and how to get there from wherever you actually are.

No one is behind. We're aligning.

---

## Today's path

1. Overview of the cohort milestones
2. Technical niche goals
3. Technical role goals
4. Example project — the Gourmet Planner
5. Project proposal — from the content perspective
6. **How to actually learn this stuff** ← the part that matters most
7. **Feedback** ← we close here

---

# 1. Cohort milestones

The 6-milestone roadmap:

1. **Orientation** — understand the landscape
2. **Focus** — pick your niche and your role
3. **Project** — build something real
4. **Publish** — write about what you built
5. **Release** — ship it publicly
6. **Placement** — turn it into opportunity

**Where we are:** Sprint 1 — Orientation moving into Focus.
**What's behind us:** Lesson 1, Lesson 2, Assignment 1.
**What's ahead:** project plan (due Sunday) → build → demo.

Why this matters: knowing the arc lets you **pace yourself**. The cohort rewards consistency, not sprinting.

---

# 2. Technical niche goals

The five foundational concepts. Pick **one** as your SME niche for publishing. Pick **three** to cover in your project (2 basic + 1 expert).

| Niche | What it is | Where it shows up |
|---|---|---|
| **Agentic Loops** | Plan / Act / Observe / Refine — systems that decide their own next move | LangGraph, Google ADK, ReAct |
| **FinOps Stack** | LLM/SLM routing, caching, token economics — the cost layer | RouteLLM, LiteLLM, vLLM |
| **Dynamic AI Data** | GraphRAG, knowledge graphs, relational memory — where the model gets context | Neo4j, MS GraphRAG, Contextual Retrieval |
| **Multimodal Reality** | Vision, video, screen-action — agents that see and act on the world | Gemini, Claude Vision, Computer Use |
| **Engineering Rigor** | Observability, evals, guardrails — trust for non-deterministic systems | LangSmith, RAGAS, DeepEval |

You don't need to know all five deeply. You need to know **one** deeply and **three** well enough to ship a project.

---

# 3. Technical role goals

The six roles in scope:

- **Agentic AI Engineer** — orchestration, tool-use design, evals
- **Forward Deployed Engineer** — rapid prototyping, edge AI, integration
- **AI Platform & Data Engineer** — vector DBs, inference optimization, LLMOps
- **AI Product Manager** — unit economics, UX for uncertainty, compliance
- **AI Security Engineer / Red Teaming** — adversarial robustness, privacy, supply chain
- **AI Governance / Ethics / Compliance** — bias, XAI, model cards, policy

**Out of scope** (not what we're training for): ML Engineer, Research Engineer, ML Core Data Engineer. These are train-from-scratch roles, a different career.

Your **publishing pair** = (your role) × (your niche). That pair defines what you write about and what you ship.

---

# 4. Example project — the Gourmet Planner

The Plan-Act-Reflect agentic system you've been studying. This is **Assignment 1**.

**The agents:**
- **Architect** (temp 0.7) — plans the menu
- **Executor** (temp 0.1) — runs the steps
- **Critic** (temp 0.0) — flags problems (e.g. over budget)
- **Verifier** (temp 0.0) — checks safety constraints (allergies, dietary)

**The loop:**

> Architect plans → Executor runs → Critic + Verifier review → if rejected, Architect re-plans with the rejection as input.

Cap at 5 iterations. After that, escalate to a human (`ConstraintConflictError`).

**Why this is the example:** it's the **smallest complete agentic system**. Every project pattern you'll build is a variant of this.

**Worked solutions in the repo:**
- `agep/` — polished, 6-agent version (adds Saboteur + Chef)
- `agep-antigrav/` — simpler, 4-agent version

Read these like a math textbook. Study the structure. Notice the design choices. Then build your own version *differently*.

---

# 5. Project proposal — the content perspective

This is your **portfolio piece** and the **substrate** for your LinkedIn + Medium publishing.

What we're looking for in a proposal:

- **3 of the 5 concepts:** 2 at basic level, 1 at expert level
- **A tangible problem** with a named user/stakeholder — not "AI for healthcare," but "X for Y workflow at Z"
- **An architecture sketch** — agents, roles, loop, stop conditions
- **A realistic MVP** defined separately from stretch goals
- **A deliverable plan** — code, demo, publishing pair

Group projects welcome.

**This week:**

1. Drop a first-draft idea in the Google Sheet **tonight**
2. Final project plan due **Sunday, May 3** — must pass the rubric
3. Book a mentor consult when office hours open

The full rubric is coming this week.

---

# 6. How to actually learn this stuff

This is the part that matters most. Read it carefully.

The materials don't try to teach you all the depth themselves. If they did, you'd get a list of 30 frameworks per concept and feel buried — that's the **overwhelm energy** we're avoiding.

Instead, every concept comes with a **Verified Socratic Prompt** that you paste into Claude.

**What the prompt does:**

- **Asks you about your background first** — your domain, your goals, what you already know. The conversation **personalizes to you**.
- **Refuses to lecture.** It asks one question at a time and makes you do the thinking.
- **Uses your domain** for every example — not abstract diagrams, *your* world.
- **Forces specific checkpoints** — there are concepts the LLM must surface, but only after you've reasoned your way to needing them.
- **Has a clear exit:** you write a 4-sentence explanation you could send to a teammate. The LLM critiques it. You revise it once.

**What this means for you:**

You will not sit and read 4 hours of material. You will have a 30–45 minute conversation that adapts to where you actually are.

**The default learning loop for any concept:**

1. Read the concept page (5 min)
2. Run the Socratic prompt (30–45 min)
3. If stuck on the same question for 10 min → office hours, with the transcript
4. **Ship something using it** — understanding without building is forgetting

**Tiered time:**

| Time you have | What to do |
|---|---|
| 30 min | Run the Socratic prompt. Stop at the 4-sentence summary. |
| 3 hours | Do that, then read the canonical example in the repo and trace how state moves through the system. |
| Deep dive | Do both, then build your own minimal version from scratch — no framework — then port it to a framework and notice what changed. |

## The Verified Socratic Prompt — copy this

Paste this into a fresh Claude conversation. It will ask about your background, ask which concept(s) you want to focus on, and pace itself based on the time you have.

```
You are my Socratic tutor for the 5 foundational concepts of agentic AI engineering:

1. Agentic Loops — Plan / Act / Observe / Refine — systems that decide their own next move
2. FinOps Stack — LLM/SLM routing, prompt caching, token economics
3. Dynamic AI Data — GraphRAG, knowledge graphs, relational memory
4. Multimodal Reality — vision, video, screen-action, agents that see and act on the world
5. Engineering Rigor — observability, tracing, evals, guardrails

# Step 1: Get my context

Before teaching anything, ask me three questions, ONE AT A TIME. Wait for each answer before asking the next.

1. What I already know about LLM applications — pick one: never built / chatbot / RAG / multi-agent / shipped to production
2. What field or domain I work in or know best — we will use this domain for ALL examples in our conversation
3. What I want to be able to BUILD after this conversation — a concrete goal, not a topic

# Step 2: Let me pick scope

After context, ask me which concept(s) I want to cover and how much time I have. Offer:

- A specific concept (~30–45 min)
- A subset I name
- All 5 (~2 hours, deep)
- Goal-driven sequence — based on my stated goal, YOU pick the order and tell me why

If I am unsure, default to the goal-driven sequence and explain your reasoning.

# Step 3: Teach Socratically

For every concept we cover, follow these rules without exception:

- ONE question at a time. Never multiple.
- Use MY domain for every example. Not abstract diagrams — my world.
- Make me predict the next step before you reveal it.
- When I gloss over something, stop and make me say it in my own words.
- When I answer poorly, do NOT correct me. Ask a sharper question.
- Keep your messages under 4 sentences unless I ask for depth.
- Do not lecture. If you catch yourself explaining for more than 3 sentences, stop and ask a question instead.

# Step 4: Surface the verified checkpoints

For each concept I cover, you must surface these ideas — but only AFTER I have reasoned my way to needing them. Do not list them. Do not pre-teach them.

Agentic Loops:
- Why "Plan" must be separable from "Act"
- What "Observe" actually consumes (state, tool output, errors)
- The role of Critic / Verifier in preventing drift and hallucination
- Why temperature differs across agent roles
- The three legitimate reasons a loop terminates: convergence, max-iter cap, escalation

FinOps Stack:
- Why a small model can replace a large one for routine sub-tasks
- What prompt caching actually caches and what it doesn't
- The cost-quality-latency triangle and where you trade
- Why batch processing changes the economics
- When SLM-on-device beats hosted frontier models

Dynamic AI Data:
- Why vector RAG fails at relational queries
- What a knowledge graph captures that embeddings can't
- The difference between retrieval and reasoning over retrieved data
- Why memory architecture matters more than memory size
- When a graph is overkill and embeddings are enough

Multimodal Reality:
- Why vision-language models are NOT just OCR + text
- What spatial reasoning means and where models fail at it
- The difference between "agent sees screen" and "agent acts on screen"
- Why temporal understanding (video) is structurally harder than image understanding
- The trust problem: how to verify a multimodal agent's perception

Engineering Rigor:
- Why deterministic tests cannot fully cover non-deterministic systems
- What an LLM-as-judge eval actually measures
- The tracing-vs-eval distinction
- Why guardrails fail at the edges (prompt injection, jailbreaks)
- The cost of NOT having observability — measured in incidents, not dollars

# Step 5: Cross-link

When natural, point out how the concepts connect:
- FinOps decisions live INSIDE Agentic Loops — which agent gets which model?
- Dynamic AI Data feeds the "Observe" step of a loop
- Multimodal expands what "Observe" can consume
- Engineering Rigor wraps the entire loop

If I show solid understanding of one concept, ask a question that ties it to a related concept.

# Step 6: Exit criterion

For each concept we cover, end the segment with:

1. I write a 4-sentence explanation I could send to a teammate.
2. You critique it against the checkpoints above. Tell me which checkpoints I missed or got wrong.
3. I revise once.
4. You confirm or push back one more time.

If we covered multiple concepts, finish the whole session with one final synthesis question:
"Describe the next project you would build and which 3 concepts you would lean on. Why those three?"

# Step 7: When to stop

Stop when:
- I say to stop
- I have completed the exit criterion for everything I picked
- 60 minutes have passed and I am fatiguing — at that point, summarize where we got and recommend a next session

Begin by asking me question 1.
```

---

# 7. Feedback

Two layers. Both anonymous. Both happening **now**.

**Right now — silent fill, 5 minutes:**
The Google Form. Even one-word answers count. *(link in chat)*

Questions:
1. Confidence on Assignment 1 (1–5)
2. Confidence on picking your project (1–5)
3. Biggest thing blocking you right now (free text)
4. One thing you want more of
5. One thing you want less of

**Then open mic:**
What's a question you didn't want to ask in front of the group? Now's the time.

---

# Your three actions this week

1. **Tonight** — drop a first-draft project idea in the Google Sheet
2. **This week** — book a mentor consult when office hours open
3. **Before Sunday** — self-score your project plan against the rubric

See you Sunday, InshAllah.
