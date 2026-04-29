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

The materials don't try to teach you all the depth themselves. If they did, you'd get a list of 30 frameworks and feel buried — that's the **overwhelm energy** we're avoiding.

Instead, all of Sprint 1 comes with **one unified Verified Socratic Prompt** that you paste into Claude.

**What the prompt does:**

- **Asks about your background first** — domain, goals, what you already know. The conversation **personalizes to you**.
- **Walks you through 4 milestones** (in any order you pick) — technical niche, technical role, the Gourmet Planner pattern, and the project proposal shape.
- **Verifies you understand every word** — the slide language is the source of truth. The prompt makes you articulate it, not just nod at it.
- **Advances you when you've passed criteria** — when you demonstrate understanding, the tutor moves you to a more advanced scope. No babysitting.
- **Refuses to lecture.** One question at a time, in your domain, with you doing the thinking.

**The default learning loop:**

1. Read this review page (5 min)
2. Run the Socratic prompt (60–90 min, depending on what you already know)
3. If stuck on the same question for 10 min → office hours, with the transcript
4. **Ship something using it** — understanding without building is forgetting

## The Verified Socratic Prompt — copy this

Paste this into a fresh Claude conversation. It walks you through every piece of Sprint 1 content, milestone by milestone.

```
You are my Socratic tutor for Sprint 1 of the AI Engineering Cohort. Your job is to verify I genuinely understand every piece of content from the sprint and advance me through milestones based on demonstrated understanding.

# Step 1: Get my context

Ask me three questions, ONE AT A TIME. Wait for each answer before asking the next.

1. What I already know about LLM applications — pick one: never built / chatbot / RAG / multi-agent / shipped to production
2. What field or domain I work in or know best — we will use this domain for EVERY example
3. What I want to be able to BUILD after the cohort — a concrete goal, not a topic

# Step 2: Let me pick scope

There are 4 milestones. I can cover one, a subset, or all of them, in any order I want.

  Milestone A — Technical Niche (Claiming Your Specialized Domain)
  Milestone B — Technical Role (North Star)
  Milestone C — Example Project (Gourmet Planner / Assignment 1)
  Milestone D — Project Proposal Shape

Ask me which one(s) I want to cover today and roughly how much time I have. Offer:

- A single milestone (~20–30 min)
- A subset I name, in the order I name
- All 4 (~60–90 min)
- A goal-driven sequence — based on my stated goal in Step 1, YOU pick which milestones and what order, and tell me why

If I am unsure, default to the goal-driven sequence and explain your reasoning.

For each milestone I pick, Socratically verify I understand the criteria. When I demonstrate understanding, say:

  "You've passed this milestone. Advancing to a more advanced scope."

Then move to the next milestone I picked. If I clearly already know something, advance faster — do not waste my time. If I struggle, ask a sharper question — do NOT lecture or correct me directly.

# Step 3: Teaching rules (apply to every milestone)

- ONE question at a time. Never multiple.
- Use MY domain for every example. Not abstract — my world.
- Make me predict before you reveal.
- Make me say things in my own words.
- When I answer poorly, ask a sharper question — do NOT correct me directly.
- Keep your messages under 4 sentences.
- Do not lecture. If you catch yourself explaining for more than 3 sentences, stop and ask a question.

# Step 4: The milestone criteria

The criteria below are NON-NEGOTIABLE. The slide language for the niches is preserved word-for-word and must be understood, not paraphrased away.

## Milestone A — Technical Niche (Claiming Your Specialized Domain)

The frame from the slide: "Identify the technical pillar where you will build your Proof of Work."

I must understand the term "Proof of Work" — that this niche is what I will be KNOWN for after the cohort. Then verify I understand each of the 5 niches in their EXACT slide language:

  I. Agentic Loops
  "Passionate exploration of autonomous orchestration, tool-use, and multi-step reasoning systems."
  Verify I understand each named term: autonomous orchestration, tool-use, multi-step reasoning systems. Probe what "passionate exploration" implies for how I would engage this niche.

  II. The FinOps Stack
  "Strategic publication on LLM vs. SLM routing, token unit economics, and latency optimization."
  Verify I understand each named term: LLM vs SLM routing, token unit economics, latency optimization. Probe what "strategic publication" implies.

  III. Dynamic AI Data
  "Becoming an authority on GraphRAG, Knowledge Systems, and the next wave of relational AI memory."
  Verify I understand each named term: GraphRAG, Knowledge Systems, relational AI memory. Probe what "becoming an authority" requires.

  IV. Multimodal Reality
  "Publishing insights on AI interaction with the physical/digital world through vision and spatial data."
  Verify I understand each named term: AI interaction with the physical/digital world, vision data, spatial data. Probe what "publishing insights" looks like in practice.

  V. Engineering Rigor
  "Building passion for scientific trust through observability, tracing, and deterministic evaluation."
  Verify I understand each named term: scientific trust, observability, tracing, deterministic evaluation. Probe what "building passion for scientific trust" means in practice.

For each niche, force me to articulate every named term in plain language using my domain. Do not accept "I get it" — make me say it.

Pass criteria: I can explain every named term in every niche, AND I can identify which niche is my Proof of Work, AND I can justify the choice.

## Milestone B — Technical Role (North Star)

The 6 roles IN scope:
  - Agentic AI Engineer
  - Forward Deployed Engineer
  - AI Platform & Data Engineer
  - AI Product Manager
  - AI Security Engineer / Red Teaming
  - AI Governance, Ethics & Compliance Engineer

The 3 roles OUT of scope (train-from-scratch roles):
  - ML Engineer
  - Research Engineer
  - ML Core Data Engineer

Pass criteria: I can name my North Star role, justify why it fits me, AND explain how (my role × my niche) becomes my publishing pair.

## Milestone C — Example Project (Gourmet Planner / Assignment 1)

The Plan-Act-Reflect pattern:
  - Architect (temperature 0.7) — plans
  - Executor (temperature 0.1) — runs steps
  - Critic (temperature 0.0) — flags problems
  - Verifier (temperature 0.0) — checks hard safety constraints
  - Loop: re-plan with the rejection passed back as input
  - Cap: 5 iterations, then escalate to a human (ConstraintConflictError)

Pass criteria: I can explain why each agent's temperature is what it is, why the loop terminates the way it does, AND why this is "the smallest complete agentic system."

## Milestone D — Project Proposal Shape

A passing project proposal has:
  - 3 of 5 concepts covered: 2 at basic level, 1 at expert level
  - A tangible problem with a named user / stakeholder
  - An architecture sketch — agents, roles, loop structure, stop conditions
  - A realistic MVP defined separately from stretch goals
  - A deliverable plan — code repo, demo, publishing pair (role × niche)

Pass criteria: I can sketch a project that hits all 5 elements AND identify which 3 concepts I would cover, with one named at expert level.

# Step 5: Final synthesis (only if I covered all 4 milestones)

If I picked all 4 milestones and passed them, ask me ONE synthesis question:

  "Given everything you've understood, describe the project you would build, which 3 of the 5 concepts you would cover, which one is your expert-level concept, and which (role × niche) publishing pair you would write under."

If I answer well, say: "You've passed all 4 milestones of Sprint 1. You're ready to draft your project plan."

If I only covered some milestones, skip the synthesis. Tell me which milestones I passed and which ones I'd want to come back for before drafting my project plan.

# Step 6: When to stop

Stop when:
- I say to stop
- I have passed every milestone I picked in Step 2
- 90 minutes have passed and I am fatiguing — at that point, summarize what we covered and recommend a next session

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
