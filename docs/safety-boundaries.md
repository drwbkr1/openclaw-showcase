# Safety Boundaries

This document defines the practical safety boundaries for OpenClaw Showcase.

For the broader responsible-use statement, see [Security Posture](../SECURITY-POSTURE.md).

OpenClaw Showcase is a public-safe documentation repository. It is separate from the private OpenClaw runtime, private working repo, operational memory, raw logs, credentials, and live tool authority.

The core rule is:

> Public showcase material can explain the workflow. It must not expose the private system.

---

## How to Use This Document

Use this file as the practical rulebook for deciding what belongs in the public showcase.

It supports:

- [Security Posture](../SECURITY-POSTURE.md), which explains the responsible-use position.
- [Agentic Studio Workflow](agentic-studio-workflow.md), which explains the process these boundaries protect.
- [Sanitized Run Receipt](../examples/sanitized-run-receipt.md), which shows a public-safe example.
- [BurnLens Case Study](../case-studies/burnlens/README.md), which applies these rules to a GeoAI concept.
- [Workflow Map](../diagrams/workflow-map.md), which visualizes the public/private separation.

---

## Boundary Summary

OpenClaw Showcase is allowed to show:

- Public-safe workflow documentation.
- Sanitized run receipts.
- High-level safety and review patterns.
- QA review examples.
- Diagrams of the process.
- BurnLens as a bounded public-data case study.
- Chosen lessons from experimental runtime work at a safe level of abstraction.

OpenClaw Showcase must not show:

- Private runtime code.
- Raw operational logs.
- Credentials, tokens, secrets, or environment files.
- Private memory files.
- Local machine paths.
- Private issue history.
- Internal task numbers.
- Live tool authority paths.
- Deployment paths.
- Unredacted bug reports or operational traces.

---

## 1. Public Showcase Boundary

The showcase repo exists to explain the public-safe layer of OpenClaw.

### Allowed

- README and overview documentation.
- Workflow diagrams.
- Public-safe case studies.
- Sanitized examples.
- General lessons learned.
- Portfolio-oriented explanations.
- Links between showcase files.

### Not Allowed

- Copying private repo history into the public showcase.
- Publishing raw internal notes.
- Publishing private issue comments or internal task history.
- Presenting experimental outputs as production-ready systems.
- Presenting AI-generated drafts as final without review.

### Requires Approval

- Publishing a new public-facing case study.
- Adding a new example based on private operational work.
- Adding high-level runtime lessons.
- Adding screenshots or artifacts derived from private work.

---

## 2. Runtime and Private System Boundary

The active OpenClaw runtime is not part of this showcase.

This repo may describe workflow patterns around the runtime, but it must not expose private runtime implementation details.

### Allowed

- High-level explanation of OpenClaw as an agent-harness platform.
- General discussion of agent workflow design.
- General discussion of safety boundaries.
- Sanitized lessons from runtime experimentation.
- Public-safe descriptions of why review gates matter.

### Not Allowed

- Runtime source code.
- Raw runtime configuration.
- Private environment files.
- Operational memory files.
- Exact private runtime traces.
- Local machine paths.
- Raw bug details that expose implementation internals.
- Instructions that would allow someone to reproduce private operational authority.

### Requires Approval

- Any discussion of runtime configuration lessons.
- Any discussion of runtime bugs.
- Any explanation of tool permissions.
- Any explanation of sandboxing, memory, traceability, or reliability lessons derived from private runtime work.

---

## 3. Tool and Action Boundary

OpenClaw is designed around the idea that tool-enabled agents need clear scope.

The showcase may describe that principle. It must not expose live tool authority.

### Allowed

- Explaining least-privilege tool access.
- Explaining human approval gates.
- Explaining why write access should be controlled.
- Explaining why deployment and publication should be reviewed.
- Explaining why agent outputs should be treated as drafts.

### Not Allowed

- Publishing credentials or access tokens.
- Publishing live action paths.
- Publishing deployment instructions tied to private systems.
- Publishing private tool configuration.
- Publishing exact local permission rules from the active runtime.
- Showing unrestricted tool access as a recommended pattern.

### Requires Approval

- Any example involving tool use.
- Any example involving file access.
- Any example involving write authority.
- Any discussion of deployment automation.
- Any public-facing claim about what the active runtime can or cannot do.

---

## 4. Data and Log Boundary

The showcase may include sanitized receipts and examples, but not raw operational data.

### Allowed

- Sanitized run receipts.
- Summaries of what a workflow attempted.
- Generalized examples of checks performed.
- Public-safe descriptions of QA review.
- High-level lessons from logs.

### Not Allowed

- Raw logs.
- Full transcripts.
- Private memory dumps.
- Internal session details.
- Local file paths.
- Private repo links that expose internal work.
- Unredacted command output from private operations.
- Sensitive error messages or traces.

### Requires Approval

- Any excerpt derived from a real log.
- Any sanitized example based on a private run.
- Any workflow receipt connected to a real internal task.
- Any artifact that could reveal private project structure.

---

## 5. Publication Boundary

Nothing in OpenClaw becomes public simply because it exists.

Public release requires review.

### Allowed

- Drafting public-safe documentation.
- Preparing portfolio artifacts.
- Reviewing case studies for overclaiming.
- Publishing only after approval.
- Marking experimental work clearly.

### Not Allowed

- Publishing internal drafts automatically.
- Publishing private operational details.
- Publishing case studies without limitation statements.
- Claiming a concept is operational when it is only a portfolio or research artifact.
- Presenting AI-generated material as final without human review.

### Requires Approval

- Any public release.
- Any portfolio-ready case study.
- Any new public-facing diagram.
- Any claim about system capability.
- Any artifact connected to BurnLens or another applied AI concept.
- Any material that discusses lessons from experimental runtime work.

---

## 6. Human Approval Boundary

Human judgment remains the final gate for public-facing work.

### Human approval is required before:

- Publishing public-facing artifacts.
- Treating a draft as final.
- Expanding public discussion of runtime behavior.
- Adding high-level runtime lessons.
- Adding examples based on private work.
- Presenting a case study as portfolio-ready.
- Changing safety or redaction rules.
- Exposing any implementation detail that could affect private system safety.

The purpose of this boundary is not to slow the project down. It is to keep the public showcase accurate, safe, and credible.

---

## Boundary Examples

### Allowed

A sanitized run receipt that says:

```text
Goal: Prepare a public-safe BurnLens case study.
Checks: QA review, limitation review, public-release review.
Result: Approved as portfolio draft, not operational system.
```

### Not Allowed

A raw operational log that includes:

```text
Local paths, private session details, runtime traces, tool configuration, or error output from the active system.
```

---

### Allowed

A public case study that says:

```text
BurnLens is a public-data wildfire planning concept used to demonstrate geospatial AI workflow design.
```

### Not Allowed

A public case study that says or implies:

```text
BurnLens is an operational wildfire response system.
```

---

### Allowed

A workflow diagram showing:

```text
Issue → Work Session → Run Log → QA Review → Human Approval
```

### Not Allowed

A diagram showing:

```text
Private runtime internals, live tool authority, credential flow, or private deployment paths.
```

---

### Allowed

A high-level lesson that says:

```text
Agentic systems need scoped file access and reviewable run logs.
```

### Not Allowed

A raw bug writeup that exposes:

```text
Implementation internals, private configuration, exact traces, or live failure paths.
```

---

## Practical Review Checklist

Before adding material to OpenClaw Showcase, check:

- Is this public-safe?
- Does it expose private runtime code?
- Does it expose raw logs or operational memory?
- Does it expose credentials, secrets, local paths, or private configuration?
- Does it reveal live tool authority?
- Does it include private issue history or internal task details?
- Is the claim supported?
- Are limitations stated?
- Has the artifact been reviewed?
- Does this require human approval before publication?

If the answer is unclear, keep the material private until reviewed.

---

## Summary

OpenClaw Showcase is designed to make the workflow visible without exposing the private system.

The public repo can show how agentic work is scoped, traced, reviewed, and approved.

The private system retains the runtime, authority, configuration, operational memory, and implementation details.
