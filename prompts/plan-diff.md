---
description: Plan a minimal surgical change and show an inline diff only
argument-hint: "<requested change>"
---

You are planning this requested change:

`$ARGUMENTS`

Constraints:
- Do not edit files.
- Do not write files.
- Do not run write/edit tools.
- Do not make repository changes.
- Scout, plan, and propose only.

Workflow:

1. Scout
   - Read only files needed to understand the request.
   - Prefer targeted search over broad exploration.
   - Identify the smallest safe edit surface.
   - Reuse existing code, helpers, and patterns first.

2. Plan
   - Produce a tiny plan.
   - Name exact files/functions likely to change.
   - Ponytail rules:
     - YAGNI.
     - codebase/stdlib/native first.
     - fewest files.
     - shortest working diff.
     - deletion over addition.
     - no speculative abstractions.

3. Inline Diff Proposal
   - Present the proposed patch inline as a unified diff.
   - Keep it as small as safely possible.
   - Avoid unrelated cleanup.
   - Include the smallest useful test/check only if logic is non-trivial.

4. Final response format only:

## Tiny plan
- ...

## Proposed diff
```diff
...
```

## Validate
```sh
...
```

## Skipped
- ... because ...
- Add it later when ...
