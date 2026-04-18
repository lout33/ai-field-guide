# Refactor a Large Codebase

AI is genuinely useful for refactoring large codebases.

It is also one of the easiest places to get fooled.

A flashy demo can make a refactor look easy:
- rename some files
- move logic around
- update imports
- fix a few tests

Real refactoring is harder.
Large codebases contain:
- hidden assumptions
- old patterns mixed with new ones
- duplicated logic
- fragile boundaries
- unclear ownership
- side effects that only show up after the third change

So the real question is not:

> Can AI edit many files?

It is:

> Can AI help reduce the cognitive load of a risky multi-file change without making the codebase worse?

## The short answer

Yes — but only if you use the right tool for the right phase.

For most solo developers and small technical teams, the strongest pattern is:

- **Claude Code** for understanding the repo, planning the refactor, and executing larger multi-file changes
- **Cursor** for inspecting, refining, validating, and cleaning up the implementation details

This is a job where heavier repo-level reasoning matters more than pure IDE convenience.

## Why refactoring is a distinct use case

Refactoring is different from normal feature work.

You are not just adding code.
You are changing the structure of code that already works — or half works — or works only because people are scared to touch it.

That means the priorities change.

You need help with:
- understanding the current shape of the system
- finding repeated patterns
- tracing dependencies
- planning a safe sequence of changes
- applying updates across many files
- catching subtle breakage

This is exactly where AI can be valuable, and exactly where it can become dangerous.

## What AI is good at here

AI is often useful for:
- summarizing unfamiliar modules
- identifying duplicated patterns
- proposing refactor plans
- updating repeated structures across many files
- migrating interfaces or naming conventions
- drafting first-pass changes before human review

## What AI is bad at here

AI is weaker at:
- knowing which weird edge case actually matters in production
- distinguishing elegant abstractions from over-engineering
- preserving implicit team knowledge that never made it into docs
- deciding whether a refactor is even worth doing right now
- guaranteeing safety on high-risk logic

That means the value is real, but the supervision burden stays high.

## The best default tool split

## Claude Code for repo-level work
Use Claude Code when you need to:
- understand the structure of a system
- trace a pattern across many files
- plan a multi-step refactor
- update a broad slice of the repo
- make a change that crosses boundaries

This is where Claude Code tends to feel more useful than a pure IDE-native assistant.

The task is not:
- “help me write this line”

It is:
- “understand this mess, propose a path, and help me execute it safely”

## Cursor for cleanup and controlled iteration
Use Cursor when you need to:
- review and refine changes in-context
- inspect diffs quickly
- clean up generated code
- handle smaller follow-up fixes
- stay in the edit-run-test loop

Cursor is useful after the broad shape of the change exists.

## A practical refactor workflow

## Step 1: define the goal clearly
Before touching the code, define:
- what is changing
- what is not changing
- what success looks like
- what must remain backward compatible
- what tests or checks should catch regressions

This matters because AI is much better at helping with a well-scoped refactor than with a vague sense that “this code is messy.”

## Step 2: map the current structure
Use Claude Code to answer questions like:
- where does this pattern appear?
- what files are involved?
- what depends on this interface?
- what is duplicated?
- what order should the changes happen in?

At this stage, the biggest win is not code generation.
It is reducing the time needed to load the codebase into your head.

## Step 3: plan the sequence
Good refactors are staged.

Instead of:
- “rewrite the whole thing”

prefer:
- introduce new abstraction
- migrate callers
- remove dead path
- tighten tests
- clean up leftovers

Claude Code is often useful for drafting this sequence.

## Step 4: execute the broad pass
Once the sequence is clear, use Claude Code for:
- cross-file updates
- systematic renames
- shared abstraction extraction
- moving logic into clearer boundaries
- first-pass cleanup of repetition

This is where the tool can save real time.

## Step 5: switch to Cursor for inspection and refinement
Once the broad change lands, use Cursor to:
- inspect each affected area more closely
- resolve awkward spots
- polish types and interfaces
- clean up formatting and local inconsistencies
- handle smaller repairs quickly

## Step 6: test aggressively
This is non-negotiable.

Large refactors are exactly where AI can be confidently wrong in ways that look plausible.

You need:
- tests
- manual checks
- local runs
- type checks
- linting
- smoke testing the actual workflows that matter

## What kinds of refactors AI helps with most

### Good candidates
AI tends to help most with:
- systematic renames
- extracting shared utilities
- splitting large files into cleaner modules
- migrating duplicated patterns to one reusable path
- updating call sites after interface changes
- cleaning up repetitive UI/component structures
- moving from one library pattern to another when the changes are mechanical

### Bad candidates
AI is riskier for:
- performance-sensitive internals
- concurrency-heavy logic
- security-critical code
- code with poor tests and unclear behavior
- refactors where the real problem is product ambiguity, not code structure

## Warning signs that a refactor is going wrong

Stop and slow down if:
- the AI starts inventing abstractions you did not ask for
- many files change but the reason for each change is unclear
- naming gets more abstract while clarity gets worse
- you are accepting changes faster than you can review them
- the refactor keeps growing in scope
- tests pass but the system feels less understandable

A “successful” AI refactor can still be a net negative if it makes the codebase harder to reason about.

## What to avoid

### 1. One-shot rewrite fantasies
Do not ask one tool to rewrite the whole architecture in one pass and expect a maintainable result.

### 2. Refactoring without a written target
“Make this cleaner” is too vague.
Give the tool a target shape, not just dissatisfaction.

### 3. Trusting broad diffs without staged review
Large multi-file changes need checkpoints.

### 4. Using AI to avoid hard design decisions
If you do not know what the better structure is, AI may produce a more elaborate version of the same confusion.

## Best default stack for this use case

For most solo developers:

- **Claude Code** for planning + broad repo-level changes
- **Cursor** for review + cleanup + follow-up iteration
- **tests and manual review** as mandatory guardrails

This is one of the clearest use cases for a two-tool setup.

## Current verdict

Large-codebase refactoring is one of the strongest arguments for heavier coding agents — but only when paired with human judgment and a tighter IDE cleanup loop.

Right now, the most practical default path is:

- use **Claude Code** to understand and execute the broad change
- use **Cursor** to inspect and refine the result
- use tests and staged review to keep the refactor honest

## Related pages

- [`../tools/claude-code.md`](../tools/claude-code.md)
- [`../tools/cursor.md`](../tools/cursor.md)
- [`../stacks/$40-indie-hacker-stack.md`](../stacks/$40-indie-hacker-stack.md)
- [`../personas/indie-hacker.md`](../personas/indie-hacker.md)
- [`./build-a-web-app.md`](./build-a-web-app.md)
