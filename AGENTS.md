# Agent instructions

Keep changes scoped to the task and preserve useful repository instructions.
Claim verification only for checks actually run or inspected CI evidence; report
skipped checks and remaining uncertainty.

When using Harness Composer, use `.harness-composer/bin/harness-composer`.
Its lifecycle events are activated by the invoking skill or workflow. The shim's
presence alone does not activate them.

## Agent contracts

Before starting an activity below, read and follow its linked contract:

- Modifying `AGENTS.md`, agent contracts, or documentation:
  [Documentation contract](docs/contracts/documentation.md).

- When reviewing code, read the [code review contract](docs/contracts/code-review.md).

## Review guidelines

Do not review or comment on files in `.harness-composer/`.
