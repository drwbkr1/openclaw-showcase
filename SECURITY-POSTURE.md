# Security Posture

OpenClaw Showcase is a public-safe portfolio repository for a closed-source agent-harness platform. It documents selected workflow patterns, safety boundaries, and review practices without exposing the active runtime or private operating environment.

The active OpenClaw runtime is not included in this showcase. It remains closed-source because the project is experimental, designed for a personal/solo operator context, and not ready for public release as a runnable system.

This repository is a documentation and portfolio artifact. Its purpose is to show how I think about AI operations, agent workflow design, traceability, QA review, and human-in-the-loop approval.

---

## How This File Fits

This file explains the security posture behind the showcase.

It should be read with:

- [Disclaimer](DISCLAIMER.md), which sets the overall public-use expectation.
- [Safety Boundaries](docs/safety-boundaries.md), which turns this posture into practical rules.
- [Agentic Studio Workflow](docs/agentic-studio-workflow.md), which shows how scoped work moves through review.
- [Workflow Map](diagrams/workflow-map.md), which visualizes the public/private boundary.

---

## Responsible Use Position

OpenClaw is treated as an agent-harness experiment, not as a production security product.

The main security principle is simple:

> Documentation may be public; operational authority stays private.

Tool-enabled agents can create real risk if they are given broad file access, write permissions, live credentials, deployment authority, or uncontrolled action paths. OpenClaw is designed around the idea that agentic work should be scoped, logged, reviewed, and approved before it becomes authoritative or public-facing.

This showcase only presents the public-safe layer of that work.

---

## What Is Public Here

This repository may include:

- High-level workflow documentation.
- Sanitized examples of run receipts.
- Public-safe diagrams.
- Safety-boundary summaries.
- QA and review patterns.
- BurnLens as a bounded public-data wildfire planning concept.
- Chosen lessons from experimental runtime work, described at a high level.

The goal is to demonstrate process discipline without exposing implementation details that would create unnecessary risk.

---

## What Is Not Included

This repository intentionally excludes:

- Closed-source runtime code.
- Private repo history.
- Raw operational logs.
- Secrets, tokens, credentials, or environment files.
- Private memory files.
- Discord/session details.
- Local machine paths.
- Internal issue numbers or private task history.
- Unredacted operational traces.
- Sensitive implementation details that would expose live authority paths.

High-level runtime configuration lessons may be discussed when they help explain safety or workflow design. Raw configuration files and operational details are not included.

---

## Public-Safe Rules

The showcase follows these rules:

- Keep the public repo separate from the private working environment.
- Publish sanitized documentation only.
- Do not expose secrets, credentials, raw logs, or operational memory.
- Do not expose private runtime code.
- Do not expose live tool authority, action paths, or deployment paths.
- Keep capability expansion gated.
- Keep public-facing artifacts under human review.
- Treat AI-generated outputs as drafts until reviewed.
- Document limitations before presenting a case study as portfolio-ready.
- Discuss runtime lessons only at a safe level of abstraction.

These rules are intended to keep the showcase useful without making the private system more exposed.

---

## Human-in-the-Loop Approval

OpenClaw is not designed around automatic publication or unchecked agent authority.

Human approval is required before:

- Publishing public-facing artifacts.
- Treating a draft as final.
- Expanding tool authority.
- Exposing implementation details.
- Presenting a case study as portfolio-ready.
- Changing safety boundaries.

The goal is not to remove human judgment from the process. The goal is to make the process around AI-assisted work clearer, more traceable, and easier to review.

---

## Chosen Lessons from Experiment

Some parts of OpenClaw involve experimental runtime behavior, including sandboxing, tool permissions, traceability, memory, runtime reliability, and configuration boundaries.

Those lessons may appear in this showcase when they are useful for explaining the design of the workflow. They are presented as sanitized lessons, not as raw incidents, live bug reports, or operational traces.

A useful public lesson might be:

- “Agent work needs scoped file access.”
- “Runtime behavior should be logged in a reviewable way.”
- “Human approval should gate publication and authority expansion.”
- “A polished output is not the same thing as a reliable process.”
- “Experimental agent systems need clear boundaries between documentation, runtime, credentials, and deployment authority.”

The showcase focuses on those transferable lessons rather than the private mechanics of the active runtime.

---

## Relationship to Other Showcase Files

This security posture supports the rest of the showcase:

- [README](README.md) introduces the project.
- [Agentic studio workflow](docs/agentic-studio-workflow.md) explains the operating model.
- [Safety boundaries](docs/safety-boundaries.md) describes how scope is limited.
- [Sanitized run receipt](examples/sanitized-run-receipt.md) shows traceability without raw logs.
- [BurnLens case study](case-studies/burnlens/README.md) demonstrates public-safe artifact preparation.

---

## Summary

OpenClaw Showcase is meant to demonstrate responsible AI workflow design, not expose the active system.

The public repo shows the process: task structure, run logs, QA review, safety boundaries, human approval, and portfolio-safe presentation.

The private runtime retains the authority: tools, configuration, credentials, operational memory, and implementation details stay outside the showcase.
