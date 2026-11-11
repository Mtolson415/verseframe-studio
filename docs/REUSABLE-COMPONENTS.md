# Reusable code, snippets, and APIs

## Purpose and current status
Use established libraries, official SDKs, and small sourced examples when they meet the project need. This file defines the review process; it does not claim that new components have been selected or tested.

## Source selection
Inspect existing project code first, then version-matched official documentation and owning repositories. Review community samples for license, dependencies, maintenance, and behavior. Prefer dependency managers and lockfiles to copying entire libraries.

## Component inventory
| Component or API | Owning source and exact version/commit | License and notices | Why selected / alternatives | Test evidence and status |
|---|---|---|---|---|
| Inventory pending | Not yet selected | Review required | Evaluate against project requirements | Candidate |

## Record template
Copy this section for each important reused component:

### Component name
- Source repository and official documentation:
- Exact version/tag/commit or image digest:
- License and required notices:
- Files using or adapting the component:
- Problem solved, alternatives, and reason selected:
- Changes from the upstream example:
- Minimal example, inputs, expected output, and exact containerized command:
- API schema/version, authentication, secret storage, and data destinations:
- Timeouts, retries/idempotency, rate limits, cost, and failure handling:
- Verification environment, image identity, date, and evidence:
- Success, invalid-input, and upstream-failure checks:
- Mocked versus live checks:
- Known limitations and update/deprecation procedure:

## Evidence vocabulary
Official means source ownership is established. Reviewed means source/license/behavior inspected. Executed means it ran in a recorded environment. Verified locally means relevant acceptance checks passed. Integrated means it passed this project's integration checks. Portable means the stated checks were reproduced on another recorded host.

## Learning and maintenance
Explain why a pattern works, when an alternative fits, and how to diagnose common errors. Keep minimal runnable examples with their tests. Record provenance in `docs/sources.md` when that file is introduced and preserve third-party notices where required. Never store real credentials in examples.

Back: [Documentation index](README.md) · [Project README](../README.md)
