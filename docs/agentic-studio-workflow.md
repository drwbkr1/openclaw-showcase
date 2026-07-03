# Agentic Studio Workflow

This document explains the public-safe workflow model behind OpenClaw Showcase.

For the security framing, see [Security Posture](../SECURITY-POSTURE.md).  
For practical limits on what can be shown publicly, see [Safety Boundaries](safety-boundaries.md).

OpenClaw is a closed-source agent-harness platform. This showcase does not expose the active runtime. Instead, it documents the workflow discipline around agent-assisted work: how tasks are scoped, traced, reviewed, and approved.

---

## How This Workflow Connects to the Showcase

This file explains the operating model that the other documents rely on:

- [Safety Boundaries](safety-boundaries.md) defines what the workflow must protect.
- [Sanitized Run Receipt](../examples/sanitized-run-receipt.md) shows the traceability step in practice.
- [BurnLens Case Study](../case-studies/burnlens/README.md) applies the workflow to a public-data concept.
- [Workflow Map](../diagrams/workflow-map.md) visualizes the same progression.

---

## Core Workflow

The OpenClaw workflow is built around controlled progression:

```text
Issue → Branch → Work Session → Run Log → QA Review → Human Approval → Merge / Publish Decision
```

The purpose of this structure is to keep AI-assisted work from becoming a loose sequence of prompts and outputs. Each task should have a defined scope, a visible work trail, a review step, and a human-owned decision point.

---

## 1. Issue: Define the Task

Work begins with a scoped task.

An issue or task brief should answer:

- What is the goal?
- What is in scope?
- What is out of scope?
- What files or artifacts are expected?
- What risks or limitations are known?
- What review is required?
- What decision is needed from a human?

The issue stage matters because agent-assisted work can drift if the task is vague. A clear issue gives the workflow a starting boundary.

A good issue does not only say what to produce. It also says what not to do.

---

## 2. Branch: Isolate the Work

Substantive work should happen in an isolated branch or draft artifact rather than directly against a public-facing final version.

The branch stage creates a safe place to:

- Draft.
- Revise.
- Run checks.
- Review changes.
- Reject or roll back work if needed.

In the public showcase, this is represented as a workflow pattern rather than a live connection to the private working repo.

The important principle is isolation: work should be inspectable before it becomes final.

---

## 3. Work Session: Produce the Draft

The work session is where AI-assisted drafting, research, organization, or review happens.

A work session may involve:

- Drafting documentation.
- Organizing project notes.
- Producing a case-study artifact.
- Reviewing limitations.
- Creating a diagram.
- Preparing a sanitized example.
- Summarizing lessons from experimental work.

The output of a work session is still a draft. It is not considered final simply because it looks complete.

---

## 4. Run Log: Make the Work Traceable

A run log is a receipt for the work session.

It records what happened at a useful level of abstraction:

- Goal of the run.
- Related issue or artifact.
- Inputs used.
- Files or documents changed.
- Checks performed.
- Review status.
- Known limitations.
- Human approval status.
- Next action.

Run logs help separate two questions:

1. Did the output look good?
2. Was the process trustworthy enough?

Both questions matter.

A polished answer can still be a weak result if the workflow skipped review, drifted beyond scope, or failed to document limitations.

---

## 5. QA Review: Check the Output and the Process

QA review is separate from creation.

The review step asks whether the artifact is accurate, scoped, supported, and safe to use.

A QA review can ask:

- Did the output answer the actual task?
- Did the work stay inside the approved scope?
- Are claims supported?
- Are limitations documented?
- Is the artifact public-safe?
- Is the artifact being presented with the right status?
- Does it need human approval before publication?
- Did the process create any safety or traceability concerns?

This distinction is important: OpenClaw reviews both the artifact and the workflow that produced it.

---

## 6. Human Approval: Keep Final Judgment Human-Owned

Human approval is the final gate before public-facing release, authority expansion, or final status.

Human approval is required before:

- Publishing a public-facing artifact.
- Treating a draft as final.
- Presenting a case study as portfolio-ready.
- Expanding tool authority.
- Discussing runtime behavior publicly.
- Changing safety boundaries.
- Exposing implementation details.

The goal is not to slow the workflow down. The goal is to prevent AI-assisted work from becoming authoritative too early.

---

## 7. Merge or Publish Decision

After review and human approval, the work can move into one of several states:

- **Merge** — accepted into the working project.
- **Publish** — approved for public-facing use.
- **Revise** — useful but not ready.
- **Hold** — needs more evidence or review.
- **Reject** — not useful, unsafe, unsupported, or out of scope.

This is the final decision point. The workflow does not assume that every draft deserves to be merged or published.

---

## Workflow Roles

OpenClaw uses role-based review concepts. The public showcase describes these as functional roles rather than exposing internal operating names.

Common roles include:

### Orchestrator

Defines the task, keeps the workflow moving, and consolidates results.

### Build / Operations

Creates or updates artifacts, runs checks, and reports what changed.

### Research / Provenance

Checks assumptions, sources, evidence, and limitations.

### Memory / State

Tracks project state, decisions, and continuity across work sessions.

### QA / Red-Team

Reviews the output and the process for scope drift, unsupported claims, missing limitations, and release risk.

These roles do not imply unchecked autonomy. They are part of the workflow structure around AI-assisted work.

---

## Workflow Principles

The OpenClaw workflow is built around several practical principles.

### Scope Before Output

A task should be bounded before work begins.

### Draft Before Final

AI-generated or AI-assisted work starts as a draft.

### Trace Before Trust

A useful output should have a visible work trail.

### Review Before Release

Public-facing artifacts require review.

### Human Approval Before Authority

Humans remain responsible for publication, final status, and changes to authority.

### Lessons Without Exposure

Runtime lessons can be discussed at a high level, but private implementation details stay private.

---

## Example Workflow

A public-safe BurnLens case study might move through the workflow like this:

```text
1. Define the case-study goal.
2. Identify what is public-safe and what is excluded.
3. Draft a bounded BurnLens narrative.
4. Record a run log.
5. Check for overclaiming and unsupported claims.
6. Add limitations.
7. Review the artifact for public safety.
8. Approve it as a portfolio draft, revise it, or hold it back.
```

This process helps prevent a research concept from being presented as an operational system before it is ready.

---

## What This Workflow Is Not

This workflow is not:

- Automatic publication.
- A production security certification.
- A claim that agent output is reliable without review.
- A replacement for human judgment.
- A public release of the closed-source runtime.
- A guarantee that every artifact is ready to show.

It is a structured way to make AI-assisted work more traceable, reviewable, and bounded.

---

## Relationship to the Showcase

This workflow supports the rest of OpenClaw Showcase:

- [README](../README.md) introduces the project.
- [Security Posture](../SECURITY-POSTURE.md) explains the responsible-use position.
- [Safety Boundaries](safety-boundaries.md) defines practical limits.
- [Sanitized Run Receipt](../examples/sanitized-run-receipt.md) shows what traceability can look like.
- [BurnLens Case Study](../case-studies/burnlens/README.md) demonstrates the workflow on a public-data geospatial concept.

---

## Summary

OpenClaw treats AI-assisted work as an operations problem.

The point is not only to produce artifacts. The point is to make the work scoped, traced, reviewed, and approved.

This showcase presents that workflow publicly while keeping the active runtime, private configuration, operational memory, raw logs, credentials, and implementation details outside the public repo.
