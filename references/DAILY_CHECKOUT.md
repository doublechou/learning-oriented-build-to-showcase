# Daily Checkout

Use only when the user explicitly indicates that today's build session is finished.

A pause, sleep, closing the app, or returning the next calendar day does not retroactively redefine the previous session. If checkout was missed, reconcile the boundary explicitly when the user returns.

## Produce One Daily Session Handoff

Use the heading:

**Daily Session Handoff --- Day X**

Keep it concise and semantic. Capture information a coding agent cannot reliably infer from Git alone.

Include only relevant categories:

### Completed

Meaningful work actually completed or validated.

### Learned / Practiced

First-time concepts the learner understood or personally practiced. Distinguish these from work merely delegated.

### Product / Architecture / UX Decisions

Decisions, rationale, tradeoffs, and intentionally rejected alternatives.

### Debugging / Technical Reasoning

Transferable lessons, root causes, or important implementation context.

### Human--Agent Collaboration

Meaningful boundaries between learner decisions and delegated implementation.

### Portfolio / Showcase Evidence

Potential story material, screenshots, interactions, commits, failures, before/after evidence, or AI/HCI insights worth preserving.

### Open Questions

Only unresolved questions that could affect later work.

### Recommended Next Step

A repository-aware recommendation, not a blind copy of the old roadmap.

## Repository Documentation Sync

The learner can pass the handoff to the coding agent.

The coding agent should combine:

- repository/Git state = implementation truth;
- handoff = semantic context.

It should then determine which persistent Markdown documents require updates. Do not make the learner manually choose documentation files.

The agent should show the documentation diff before commit/push when the user's workflow requires approval.

## Day Boundary Rule

At the next session, determine the new day from repository logs plus the last completed checkout.

If work began before checkout was formally recorded, preserve the actual session history rather than forcing features into arbitrary roadmap-day labels.
