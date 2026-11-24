# Code review

Review only when the requester asks for code review. Finishing implementation or
opening or updating a PR does not trigger a review.

## Independent review

From the repository root, start one independent review with `codex review` using
its custom-instructions prompt (or `codex review -` with the prompt on stdin).
Include the requester's natural-language request, available ticket/specification
requirements or their readable sources, and an explicit instruction to read and
follow this guide at its actual repository path. The independent conversation
does not inherit the implementation chat. Pass relevant context explicitly.

Use native review behavior for the requested scope, within or outside a PR. Use
the custom prompt on its own: do not combine it with `--base`, `--commit`, or
`--uncommitted`. For example, fill in the request, requirements and actual guide
path before running:

```sh
codex review - <<'REVIEW'
Read and follow docs/contracts/code-review.md.
Review request: <requester's request, including any target/base/commit>.
Available requirements: <requirements and/or readable sources; say if unavailable>.
Review code quality and alignment with these requirements. Return findings only;
do not fix files or publish findings externally. If requirements are unavailable,
explicitly report that requirements alignment could not be assessed.
REVIEW
```

If already executing inside the independent `codex review` conversation, perform
the review directly; do not launch another reviewer. Inspect the requested code,
applicable repository guidance and available requirements. Check actionable
correctness, performance, security and maintainability risks and requirements
mismatches. Use existing domain documentation for repository facts.

If the CLI or independent review cannot start, report the actual limitation and
stop the review. Do not substitute a review in the implementation conversation.
This execution path targets Codex; no other host adapter is supplied.

## Results

Return actionable findings with locations and consequences to the requester.
Do not fix code, change review guidance, create follow-ups or publish externally
as part of reviewing. If no findings exist, say so. If ticket/specification
requirements are unavailable, continue with code-quality review and explicitly
state that requirements alignment could not be assessed. Do not claim complete
requirements coverage from a code-quality review alone.

## Repository review criteria

Owners can ask an agent to add or refine criteria here in plain language. When
asked to change criteria, update this section in place; future independent
reviews read this same guide. Keep domain facts with their existing owners and
link to them. Preserve useful custom criteria during maintenance.
