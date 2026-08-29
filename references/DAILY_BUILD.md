# Daily Build

Use this reference whenever starting or resuming a build day.

## Start-of-Day Protocol

First inspect the repository, especially:

1. current architecture/product model
2. current implementation state
3. roadmap
4. latest relevant daily log
5. recent Git evidence when needed

Then explicitly establish:

- **Today = Day X**
- what is already complete
- what remains uncommitted or unresolved
- what the roadmap originally expected next
- whether repository evidence changes that expectation

Do not infer the day number solely from chat continuity.

## Plan Today's Build

Establish:

### Build

What concrete capability or architectural slice should exist by the end of the session?

### Why Now

Explain the technical dependency reasoning. If the sequence differs from a designer/user-journey intuition, explain why.

### Learn

Identify the small number of important new concepts likely to appear.

### Practice

Identify what the learner should personally implement or reason through.

### Delegate

Identify mechanical work safe to give to the coding agent.

### Showcase Evidence

Identify decisions, interactions, architecture, debugging moments, AI/human boundaries, tests, or before/after evidence worth noticing.

### Definition of Done

Define observable completion criteria.

### Deferred

Explicitly protect the session from scope creep.

## During the Build

Teach concepts just in time rather than front-loading a course.

When a new concept appears:

1. explain what it is;
2. explain why it exists in this implementation;
3. connect it to something the learner already understands;
4. let the learner practice when the learning value is high;
5. delegate repetition after understanding is demonstrated.

For coding-agent tasks, provide bounded prompts with:

- exact goal
- relevant repository context
- allowed scope
- forbidden scope
- checks to run
- whether commit/push is allowed

After agent work:

1. inspect the diff;
2. identify semantic vs formatting changes;
3. run or verify relevant tests/build/lint;
4. smoke-test behavior when appropriate;
5. discuss unexpected architectural consequences before accepting them.

## Dynamic Roadmap Updates

Treat implementation evidence as feedback.

Reconsider the next step when:

- a data model proves unstable;
- a dependency appears earlier than expected;
- a planned capability no longer provides useful learning;
- a simpler implementation can validate the same hypothesis;
- new portfolio evidence suggests a more valuable experiment;
- the learner has already mastered something the roadmap expected to teach;
- the learner discovers a meaningful knowledge gap.

Do not change direction merely for novelty.

## Evidence Capture

Notice and preserve:

- key product/architecture decisions and rejected alternatives;
- why technical sequence changed;
- bugs that taught transferable debugging patterns;
- first-time concepts actually practiced;
- meaningful agent collaboration boundaries;
- user testing or observed behavior;
- screenshots/prototypes/commits that show evolution;
- AI uncertainty, failure, override, explainability, or trust patterns when relevant.

Portfolio evidence should be collected during the build, not reconstructed afterward.

## Continuous Learning Diagnosis

During build-day conversation, treat the learner's questions, misconceptions, debugging behavior, and later independent reasoning as evidence for an evolving learner model.

Do not simply answer isolated questions. When a pattern emerges: 1. identify the broader capability or mental-model gap; 2. explain the immediate concept just in time; 3. connect it to the user's Project Strategy and current feature; 4. note whether it should change Practice Personally vs Delegate decisions; 5. update the Learning Primer or roadmap when the gap is important enough.

Likewise, when the learner demonstrates independent understanding, stop reteaching the concept and move repeated mechanical work toward delegation.

Do not interrupt every build step with meta-analysis. Accumulate signals and surface a learning diagnosis when it is useful for a decision, milestone, roadmap adjustment, or requested reflection.
