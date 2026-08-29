---
description: A learning-oriented project-building workflow that turns a
  rough idea into a real-world project, deliberately tailors the build
  around what the user wants to learn, and captures the journey as
  evidence for reflection and a shareable case study.
name: Learning-Oriented Build-to-Showcase Workflow
slug: learning-oriented-build-to-showcase
---

# Learning-Oriented Build-to-Showcase Workflow

## Purpose

Use this workflow when a user wants to turn an idea into a real-world
project while deliberately using the building process to learn new
capabilities.

Help the user explore and shape the project around their goals, create a
personalized roadmap connecting project work to learning opportunities,
adapt the learning path as their understanding develops, and distinguish
what they should practice personally from what can be delegated to AI or
coding agents.

Throughout the project, preserve meaningful decisions, iterations,
challenges, learning moments, and demonstrated capabilities. At
completion, synthesize this evidence into a learning retrospective and a
shareable case study.

The workflow spans the full lifecycle:

**Idea → Explore & Shape → MVP × Learning Fit → Personalized Roadmap →
Build & Learn ↔ Adapt → Reflect → Showcase**

Do not treat this as a fixed coding curriculum or a generic
project-management checklist. Adapt the build sequence to the project's
actual technical dependencies, the learner's current understanding, and
the evidence emerging from implementation.

## Core Optimization Principle

Do not optimize the project before defining what the user wants the
project to optimize for.

This workflow has a default learning-and-showcase orientation, but the
actual priority weighting must come from the user's confirmed Project
Strategy. Learning, portfolio, product validation, shipping, technical
exploration, or another outcome may be primary.

After Project Strategy is confirmed, use it as the decision criterion
for MVP direction, scope, learning depth, delegation, roadmap
sequencing, and polish.

This does not mean the learner should manually implement everything.
Prefer hands-on work where it creates goal-relevant new understanding;
delegate work that has become mechanical or does not serve the confirmed
strategy.

## Sources of Truth

Keep these responsibilities separate:

- **Git repository** = persistent implementation and project-state truth.
- **Daily conversation** = today's planning, teaching, reasoning, debugging, and working context.
- **Daily Session Handoff** = semantic context that cannot be reliably inferred from Git alone.
- **Coding agent** = implementation, repository inspection, mechanical changes, tests, documentation sync, and approved Git operations.
- **Roadmap** = a living hypothesis about build sequence, not immutable truth.

When repository evidence conflicts with an older conversation or roadmap, prefer the current repository state.

## Learning vs. Delegation

Use this decision rule throughout the project:

- **Important first-time concept** → explain it, connect it to the current implementation, and preferably let the learner practice it.
- **Already-understood mechanical implementation** → delegate to the coding agent.
- **Product or architecture decision** → discuss the reasoning and tradeoffs before implementation.
- **Agent-generated work** → review the diff and test behavior rather than accepting it blindly.
- **Low-learning production polish** → defer unless it is required for the current capability, credibility, or showcase.

Avoid turning learning into unnecessary manual labor. The objective is transferable understanding, not typing volume.

## Roadmap Reasoning

The workflow must actively help the user brainstorm and maintain the roadmap.

When choosing a next phase, evaluate candidate work through at least:

1. **Technical Dependency** — What must exist before later capabilities can be built safely?
2. **Learning Value** — What important new concept or reasoning pattern will this expose?
3. **Portfolio Value** — What meaningful evidence, decision, interaction, failure, or outcome could this produce?
4. **Product Value** — Does it advance the project's core loop or validate a critical assumption?
5. **Uncertainty Reduction** — Will doing this now answer an architectural or product question that would otherwise make later work speculative?
6. **Cost of Premature Commitment** — Would implementing this now harden an unstable model too early?

Explain non-obvious sequencing decisions to the learner. Teach not only *what* comes next, but *how a technical builder reasons about what comes next*.

Never blindly execute an outdated roadmap. Re-evaluate it using:

**Current Repo State + Architecture + Learning Progress + New Evidence → Best Next Step**

A useful milestone definition includes:

- Build
- Why now technically
- Learn / practice
- What the learner should implement personally
- What can be delegated
- Portfolio/showcase evidence to watch for
- Definition of done
- Explicitly deferred scope

## Workflow Lifecycle

### Scope-Shaping Inputs

Before product exploration, resolve consequential unknowns that could change the project—especially the project/outcome goal, capability goal, and time horizon. Reuse information already supplied; ask only for missing scope-shaping constraints. Do not turn this into an intake questionnaire or require a second confirmation after the user answers.

### 1. Project Bootstrap

For a new project, read `references/PROJECT_BOOTSTRAP.md`.

Use a gated, multi-turn bootstrap. First discover and confirm the Project Strategy: what the project is for, which capabilities matter, what success means, and relevant constraints. Only then generate MVP directions shaped by that strategy. After MVP confirmation, assess the technical landscape and learner baseline, generate a personalized roadmap, and pause for roadmap confirmation. Do not begin Build Day 1 before these consequential decisions are explicitly confirmed.

### 2. Start or Resume a Build Day

Read `references/DAILY_BUILD.md`.

Before planning the day, inspect the repository's current architecture, current state, roadmap, and latest relevant daily log. Explicitly establish the current Build Day.

### 3. Build, Learn, and Review

Work incrementally. Teach first-time concepts just in time, discuss architecture decisions before implementation, delegate bounded mechanical work, and review agent diffs/tests.

Capture meaningful learning and showcase evidence as it appears rather than trying to reconstruct it months later.

### 4. Daily Checkout

Only when the user explicitly indicates the build session is finished, read `references/DAILY_CHECKOUT.md`.

Produce one concise Daily Session Handoff. Do not silently infer checkout merely because the conversation pauses.

### 5. Repository Sync

Use the handoff as semantic context and the repository as implementation truth. The coding agent should update the appropriate persistent documentation, show the diff, and only commit/push according to the user's approval workflow.

### 6. Reflect and Showcase

At MVP completion or another meaningful project milestone, read `references/REFLECT_AND_SHOWCASE.md`.

Synthesize two distinct outputs:

- **Learning Retrospective** — what the learner can now understand and do.
- **Portfolio Case Study** — what the project demonstrates to an external audience.

Showcase synthesis must be grounded in evidence accumulated during the build. Do not invent outcomes, metrics, research findings, or design rationale after the fact.

## Repository Documentation Contract

Prefer a lightweight repository-centered documentation system. Adapt names to the project when necessary.

Typical structure:

```text
PROJECT_ARCHITECTURE.md
AGENTS.md
docs/
  CURRENT_STATE.md
  ROADMAP.md
  daily/
    DAY_01.md
    DAY_02.md
  LEARNING_RETROSPECTIVE.md
  CASE_STUDY.md
```

`PROJECT_ARCHITECTURE.md` is a generic role, not a mandatory filename. A project may appropriately use names such as `PRODUCT_ARCHITECTURE.md` or `SYSTEM_ARCHITECTURE.md`.

Do not duplicate detailed project truth into the skill itself.

## Reference Routing

- New project / zero-to-one setup → `references/PROJECT_BOOTSTRAP.md`
- Starting, resuming, planning, or executing a build day → `references/DAILY_BUILD.md`
- Explicit end-of-day / end-of-session → `references/DAILY_CHECKOUT.md`
- MVP or major milestone retrospective / portfolio synthesis → `references/REFLECT_AND_SHOWCASE.md`
