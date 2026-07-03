# OpenClaw Showcase

![Status](https://img.shields.io/badge/status-public--showcase-blue)
![Focus](https://img.shields.io/badge/focus-agentic%20workflow-purple)
![Review](https://img.shields.io/badge/review-human--approved-green)
![Runtime](https://img.shields.io/badge/runtime-closed--source-lightgrey)

**OpenClaw Showcase** is a public-safe portfolio repository for a closed-source agent-harness platform. It demonstrates how I structure AI-assisted work through scoped tasks, run logs, QA review, safety boundaries, and human approval gates.

OpenClaw is the platform I use to build and evaluate an agent harness. This repository does **not** expose the private runtime, working repo, raw logs, credentials, local configuration, or operational memory. Instead, it shows the workflow discipline around OpenClaw: how work is scoped, traced, reviewed, and prepared for public-safe presentation.

Built by **Drew Baker**, this showcase reflects my applied AI/ML trajectory and my interest in AI operations, agent workflow design, evaluation, and public-data geospatial AI concepts.

---

## Start Here

Recommended first read:

1. [Disclaimer](DISCLAIMER.md) — what this showcase is and is not.
2. [Security posture](SECURITY-POSTURE.md) — why the active runtime stays private.
3. [Safety boundaries](docs/safety-boundaries.md) — what can and cannot be shown publicly.
4. [Agentic studio workflow](docs/agentic-studio-workflow.md) — how scoped AI-assisted work moves through review.
5. [Sanitized run receipt](examples/sanitized-run-receipt.md) — a concrete example of traceability.
6. [BurnLens case study](case-studies/burnlens/README.md) — the public-data GeoAI concept used as the showcase artifact.
7. [Workflow map](diagrams/workflow-map.md) — Mermaid diagrams of the operating model.

---

## How the Documents Fit Together

This repository is intentionally small. Each file has a specific role:

- `DISCLAIMER.md` sets expectations for readers before they interpret the showcase.
- `SECURITY-POSTURE.md` explains the responsible-use position behind keeping operational authority private.
- `docs/safety-boundaries.md` turns that posture into practical public-safe rules.
- `docs/agentic-studio-workflow.md` explains the issue-to-approval workflow.
- `examples/sanitized-run-receipt.md` shows what traceability looks like without raw logs.
- `case-studies/burnlens/README.md` applies the workflow to a bounded public-data GeoAI concept.
- `diagrams/workflow-map.md` visualizes the same model for quick review.

Together, these files show the public layer of OpenClaw: not the private runtime, but the operating discipline around agent-assisted work.

---

## What OpenClaw Is

OpenClaw is the platform I use for building an agent harness: a structured environment for coordinating AI-assisted work through repeatable processes rather than loose one-off prompting.

The core idea is to design an operating harness around AI work:

```text
Issue → Branch → Work Session → Run Log → QA Review → Human Approval → Merge / Publish Decision
```

This showcase focuses on the workflow layer:

- How work is broken into scoped tasks.
- How agent-assisted work is routed through issue and branch discipline.
- How outputs are reviewed before they are treated as complete.
- How run logs and traceability records help explain what happened.
- How human approval gates prevent agent output from becoming public or authoritative too early.

---

## What This Repository Demonstrates

This repository demonstrates my ability to design and communicate an AI operations workflow with practical controls around agentic work.

Key areas shown here include:

- **Agent harness design** — building structure around AI-assisted work instead of relying on ad hoc prompts.
- **GitHub-based workflow control** — using issue, branch, pull request, and review patterns to organize work.
- **Run logs and traceability** — documenting what a work session attempted, what changed, what was reviewed, and what remains uncertain.
- **QA review discipline** — separating output quality from process quality.
- **Human approval gates** — keeping final judgment, publication, and scope expansion under human control.
- **Public-safe artifact preparation** — turning internal project work into material that can be shown without exposing sensitive runtime details.

---

## Why This Matters

AI-assisted work can produce polished outputs quickly, but polished output is not the same thing as reliable process.

OpenClaw is my attempt to treat AI work as an operations problem:

- What was the task?
- What was the allowed scope?
- What files or artifacts were involved?
- What evidence supports the result?
- What review happened?
- What risks remain?
- Who approved the final output?

This showcase is designed to make that process visible.

---

## Repository Contents

```text
openclaw-showcase/
├─ README.md
├─ DISCLAIMER.md
├─ SECURITY-POSTURE.md
├─ docs/
│  ├─ agentic-studio-workflow.md
│  └─ safety-boundaries.md
├─ examples/
│  └─ sanitized-run-receipt.md
├─ case-studies/
│  └─ burnlens/
│     └─ README.md
└─ diagrams/
   └─ workflow-map.md
```

---

## Featured Case Study: BurnLens

**BurnLens** is a public-data wildfire planning concept focused on geospatial decision support.

In this showcase, BurnLens is presented as a bounded portfolio case study. The goal is to demonstrate how an agentic workflow can support a public-data research artifact through scoping, evidence tracking, QA review, limitation-setting, and public-safe presentation.

BurnLens is used here to explore questions like:

- How can public geospatial data be organized into a decision-support narrative?
- How can an AI-assisted workflow avoid overclaiming?
- How should limitations be documented before a technical concept is shown publicly?
- How can a project move from internal research notes toward a portfolio-safe artifact?

This aligns with my broader AI/ML graduate trajectory and my interest in GeoAI, disaster planning, and trustworthy decision-support systems.

[View the BurnLens case study](case-studies/burnlens/README.md)

---

## Workflow Model

The OpenClaw workflow is designed around controlled progression:

```text
1. Define the task
2. Create or reference an issue
3. Work on a branch or isolated artifact
4. Record a run log
5. Review the output
6. Review the process
7. Require human approval
8. Merge, publish, revise, or reject
```

The important point is that AI-assisted work does not become final just because it looks complete. It has to pass through review and approval.

[View the workflow map](diagrams/workflow-map.md)

---

## Run Logs and Traceability

A central part of the OpenClaw process is the run log.

A run log records the basic receipt for an AI-assisted work session:

- Goal of the run
- Related issue or artifact
- Inputs used
- Files or documents changed
- Checks performed
- QA review status
- Known limitations
- Human approval status
- Next action

This makes the workflow easier to inspect after the fact. It also helps distinguish between a successful artifact and a successful process.

[View a sanitized run receipt](examples/sanitized-run-receipt.md)

---

## QA Review

OpenClaw uses QA review as a separate step from creation.

A review can ask:

- Did the output answer the actual task?
- Did the workflow stay inside the approved scope?
- Were limitations documented?
- Are claims supported by evidence?
- Is this safe to show publicly?
- Does this require human approval before release?

This helps prevent common failures in AI-assisted work: overclaiming, scope drift, unsupported conclusions, and premature publication.

---

## Human Approval Gate

The OpenClaw workflow keeps important decisions human-owned.

Human approval is required before:

- Publishing public-facing artifacts.
- Expanding tool authority.
- Treating a draft as final.
- Presenting a case study as portfolio-ready.
- Changing safety boundaries.
- Exposing runtime or configuration details.

The goal is not to remove the human from the loop. The goal is to make the loop clearer, more traceable, and more useful.

---

## What This Repository Does Not Include

This repository intentionally does **not** include:

- Closed-source OpenClaw runtime code.
- Private repo history.
- Raw operational logs.
- Runtime configuration.
- Secrets, tokens, credentials, or environment files.
- Private memory files.
- Internal issue numbers or private task history.
- Discord/session details.
- Local machine paths.
- Unredacted bug reports.
- Any material that would expose unsafe operational details.

Some runtime behavior and bug-fix lessons may be discussed at a high level when they are useful for explaining process design. Those notes are sanitized and framed as workflow lessons, not as live operational details.

---

## Status

OpenClaw Showcase is an evolving portfolio project.

This initial version focuses on:

- A security posture summary.
- A workflow overview.
- A safety-boundary explanation.
- A sanitized run receipt.
- A BurnLens case study.
- A workflow diagram.

Future versions may add deeper case-study artifacts, more diagrams, public-safe QA examples, and additional notes on agent workflow evaluation.

---

## Built By

**Drew Baker**  
Applied AI/ML graduate student and technical writer focused on AI operations, agent workflow design, geospatial AI concepts, and trustworthy decision-support systems.

This repository is intended to show how I think about AI-assisted work: not just what the model produced, but how the work was scoped, reviewed, traced, and approved.