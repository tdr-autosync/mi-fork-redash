# Documentation contract

Follow this contract when modifying `AGENTS.md`, agent contracts, or documentation.
Check changed claims against implementation evidence and report checks actually
performed.

When editing a Markdown document, remove `Status`, `Purpose`, `Scope`,
`Last validated` and `Validation targets` frontmatter. Preserve useful meaning in
the body and other useful custom fields, such as `Owner`. Keep `_harness`
provenance in Harness template state before removing its marker. Reconcile old
requirements to generate or refresh this metadata. Untouched documents may stay
deferred; metadata cleanup is part of each edited document's coherent change.

Keep essential applicable working instructions in root or nested `AGENTS.md`.
Admit new text only when it changes a useful agent decision and cannot readily be
discovered. Preserve necessary non-obvious constraints. Put detailed agent rules
in owning contracts; the default home for new documentation contracts is
`docs/contracts/documentation.md`. Preserve useful existing owners and paths.

Route activities in a `## Agent contracts` section of the applicable `AGENTS.md`.
Introduce it once with “Before starting an activity below, read and follow its
linked contract:”. Use bullets beginning with the triggering activity, followed by
the contract link. Include only existing, applicable contracts; never link to a
deferred or absent target.

Keep direct activity links while readable within the configured entrypoint
character budget. If routing becomes unwieldy, an optional `docs/contracts.md`
may own activity-to-contract routing; its entrypoint trigger must say when to
consult it. Choose extraction by readability and budget, without a fixed contract
count. Do not generate an index, surface map, metadata, or exhaustive inventory
without a concrete need.

Keep other documentation human-facing. Link from contracts to the authoritative
explanation of domain facts instead of copying those facts into agent rules.
Agents may read human documentation. Do not move useful human docs into contracts
or create empty wrapper contracts merely to organize folders.

Before removing or relocating guidance, inspect custom knowledge and incoming
references. Preserve useful rules, facts, metadata, and unrelated content with
their owners; repair incoming links in the same change. Defer the whole affected
improvement if preservation and repairs cannot fit the configured file or
entrypoint character ceiling. Preserve independent progress and meaningful
organization. Keep generation provenance in Harness state. Verify routing and
repeat-run convergence without recreating removed navigation or rewriting
unchanged bookkeeping.
