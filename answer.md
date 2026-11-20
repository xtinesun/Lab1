# Answer: Leveraging AI to Improve Efficiency and Quality

**Question:** Please share a recent example of how you leveraged AI to improve efficiency or quality in your work. What problem were you solving, how did you use the tool, and what aspects still required your direct input or judgment?

---

## Problem

I needed to investigate and fix a regression in a multi-service codebase where a seemingly small API contract change had broken several downstream callers. The symptom was clear (failing integration tests and intermittent 4xx responses), but the root cause was not: the change touched shared types, serialization, and a few edge-case validation paths spread across services. Manually tracing every call site would have been slow and easy to miss.

## How I used AI

I used an AI coding assistant (Cursor) as a research and drafting partner, not as an unsupervised author of the fix:

1. **Codebase exploration** — I asked it to map where the changed fields were defined, serialized, and consumed, and to list call sites that assumed the old shape.
2. **Hypothesis generation** — From that map, I asked for likely failure modes (nullability, default values, enum mismatches) ranked by how well they matched the failing tests.
3. **Patch drafting** — Once I had narrowed the cause, I had it draft a focused fix and update the related tests, then I reviewed the diff line by line.
4. **Regression coverage** — I used it to suggest additional test cases for the edge paths we had been missing, which I then curated and kept only the ones that asserted real invariants.

That combination cut exploration time dramatically: instead of opening dozens of files by hand, I started from a structured shortlist and spent my time validating and deciding.

## What still required my direct input and judgment

AI accelerated search and drafting; it did not own the outcome.

- **Problem framing** — I defined what “fixed” meant (restore callers, preserve backward compatibility where required, and keep the public contract intentional).
- **Root-cause confirmation** — I verified the hypothesis against real failing tests and logs before accepting any patch.
- **API/product judgment** — Deciding whether to restore the old behavior, version the field, or tighten validation was a design call the tool could not make responsibly.
- **Risk and scope control** — I rejected broad refactors it proposed and kept the change minimal so the review stayed reviewable.
- **Quality bar** — I edited the generated tests for clarity, removed brittle assertions, and confirmed the suite passed in CI before merging.

## Outcome

The fix shipped with a small, reviewable diff and stronger tests around the contract edge cases. The main efficiency gain was faster, more complete discovery of affected call sites; the main quality gain was better coverage of the failure modes we had under-specified. The AI made me faster; ownership of correctness, design tradeoffs, and what to merge stayed with me.
