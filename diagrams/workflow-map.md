# Workflow Map

This document visualizes the public-safe workflow model behind OpenClaw Showcase.

OpenClaw is a closed-source agent-harness platform. This showcase does not expose the active runtime, private repository, raw logs, credentials, local configuration, operational memory, or live tool authority.

These diagrams show the public workflow pattern: how AI-assisted work is scoped, traced, reviewed, limited, and approved.

---

## How to Read These Diagrams

The diagrams are a visual companion to the written documents:

- [Agentic Studio Workflow](../docs/agentic-studio-workflow.md) explains the process in prose.
- [Safety Boundaries](../docs/safety-boundaries.md) defines the limits the diagrams represent.
- [Sanitized Run Receipt](../examples/sanitized-run-receipt.md) shows the traceability step as a concrete example.
- [BurnLens Case Study](../case-studies/burnlens/README.md) applies the workflow to a public-data concept.

GitHub renders Mermaid diagrams directly in Markdown, so this file is designed to be readable in the repository view.

---

## 1. Core OpenClaw Workflow

```mermaid
flowchart LR
    A[Task / Issue] --> B[Branch or Draft Workspace]
    B --> C[Work Session]
    C --> D[Run Log]
    D --> E[QA Review]
    E --> F[Human Approval]
    F --> G{Decision}

    G -->|Approved| H[Merge or Publish]
    G -->|Needs Work| I[Revise]
    G -->|Not Ready| J[Hold]
    G -->|Unsafe or Unsupported| K[Reject]

    I --> C
    J --> A
```

### What this shows

OpenClaw work does not move directly from prompt to publication. It passes through task scoping, traceability, QA review, and human approval before any merge or public release decision.

---

## 2. Workflow With Safety Gates

```mermaid
flowchart TD
    A[Define Work] --> B{Scope Clear?}
    B -->|No| B1[Clarify Task]
    B1 --> A

    B -->|Yes| C[Draft Artifact]

    C --> D{Public-Safe?}
    D -->|No| D1[Remove Private or Sensitive Material]
    D1 --> C

    D -->|Yes| E[Create Run Receipt]

    E --> F{Claims Supported?}
    F -->|No| F1[Revise Claims or Add Limitations]
    F1 --> C

    F -->|Yes| G[QA Review]

    G --> H{Review Passed?}
    H -->|No| H1[Revise or Hold]
    H1 --> C

    H -->|Yes| I[Human Approval]

    I --> J{Approved?}
    J -->|Yes| K[Portfolio Draft / Publish Decision]
    J -->|No| L[Hold / Revise / Reject]
```

### What this shows

The workflow checks more than whether an artifact reads well. It checks whether the work is scoped, public-safe, supported, reviewed, and approved.

---

## 3. Human Approval Boundary

```mermaid
flowchart LR
    A[AI-Assisted Draft] --> B[Traceability Record]
    B --> C[QA Review]
    C --> D{Human Approval Gate}

    D -->|Approved| E[Public-Safe Artifact]
    D -->|Needs Revision| F[Revise Draft]
    D -->|Not Approved| G[Keep Private]

    F --> B
```

### Human approval is required before

- Publishing public-facing artifacts.
- Treating a draft as final.
- Presenting a case study as portfolio-ready.
- Expanding tool authority.
- Discussing runtime behavior publicly.
- Changing safety boundaries.
- Exposing implementation details.

---

## 4. Role-Based Review Loop

```mermaid
flowchart TD
    A[Orchestrator] --> B[Build / Operations]
    A --> C[Research / Provenance]
    A --> D[Memory / State]
    A --> E[QA / Red-Team]

    B --> F[Draft or Artifact]
    C --> F
    D --> F

    F --> E
    E --> G{Review Verdict}

    G -->|Approved| H[Human Approval Gate]
    G -->|Approved with Notes| I[Revise and Recheck]
    G -->|Blocked| J[Hold or Redesign]

    I --> B
    H --> K[Merge / Publish Decision]
```

### Public-facing role labels

OpenClaw uses role-based workflow concepts. This showcase describes them by function:

| Role | Public Function |
|---|---|
| Orchestrator | Defines the task, coordinates the run, and consolidates results. |
| Build / Operations | Creates artifacts, runs checks, and reports changes. |
| Research / Provenance | Reviews assumptions, sources, and limitations. |
| Memory / State | Tracks continuity, decisions, and current project state. |
| QA / Red-Team | Reviews output and process for risk, scope drift, and overclaiming. |

These roles are workflow functions. They do not imply unchecked autonomy or public runtime exposure.

---

## 5. Public Showcase Boundary

```mermaid
flowchart LR
    subgraph Private_System[Private System Boundary]
        A[Closed-Source Runtime]
        B[Private Working Repo]
        C[Operational Memory]
        D[Raw Logs]
        E[Credentials / Secrets]
        F[Runtime Configuration]
        G[Live Tool Authority]
    end

    subgraph Public_Showcase[Public Showcase Boundary]
        H[README]
        I[Security Posture]
        J[Safety Boundaries]
        K[Workflow Documentation]
        L[Sanitized Run Receipt]
        M[BurnLens Case Study]
        N[Workflow Diagrams]
    end

    Private_System -. Sanitized lessons only .-> Public_Showcase
```

### What this shows

The public showcase explains the workflow. It does not expose the private runtime, private operating environment, credentials, raw logs, or live authority paths.

---

## 6. BurnLens Showcase Path

```mermaid
flowchart TD
    A[BurnLens Concept] --> B[Public-Data Framing]
    B --> C[Case Study Draft]
    C --> D[Run Receipt]
    D --> E[Claim Discipline Review]
    E --> F[Limitation Review]
    F --> G{Public-Safe?}

    G -->|Yes| H[Portfolio Draft]
    G -->|Needs Edits| I[Revise Framing]
    G -->|No| J[Keep Internal]

    I --> C

    H --> K[Human Approval Required]
    K --> L{Approved?}
    L -->|Yes| M[Showcase Artifact]
    L -->|No| N[Hold or Revise]
```

### What this shows

BurnLens is handled as a bounded public-data wildfire planning concept. The workflow prevents it from being presented as an operational emergency-response system, live monitoring tool, predictive risk model, or production-ready GeoAI platform.

---

## 7. Draft Status Lifecycle

```mermaid
stateDiagram-v2
    [*] --> Scoped
    Scoped --> Drafted
    Drafted --> Logged
    Logged --> Reviewed
    Reviewed --> RevisionNeeded
    Reviewed --> ApprovalNeeded
    Reviewed --> Blocked

    RevisionNeeded --> Drafted
    ApprovalNeeded --> Approved
    ApprovalNeeded --> Held
    ApprovalNeeded --> Rejected

    Approved --> PortfolioReady
    Held --> Drafted
    Rejected --> [*]
    PortfolioReady --> [*]
```

### What this shows

An artifact can have several states before it becomes portfolio-ready. The workflow allows revision, holding, or rejection instead of assuming every AI-assisted draft should be published.

---

## 8. Traceability Receipt Model

```mermaid
flowchart TD
    A[Work Session] --> B[Run Receipt]

    B --> C[Goal]
    B --> D[Scope]
    B --> E[Inputs Used]
    B --> F[Outputs Produced]
    B --> G[Checks Performed]
    B --> H[QA Review]
    B --> I[Limitations]
    B --> J[Human Approval Status]
    B --> K[Next Action]

    C --> L[Reviewable Process]
    D --> L
    E --> L
    F --> L
    G --> L
    H --> L
    I --> L
    J --> L
    K --> L
```

### What this shows

A run receipt is not a raw log. It is a public-safe process record that makes the work easier to understand and review.

---

## 9. Key Operating Principle

```mermaid
flowchart LR
    A[Polished Output] --> B{Enough?}
    B -->|No| C[Need Scope]
    B -->|No| D[Need Traceability]
    B -->|No| E[Need QA Review]
    B -->|No| F[Need Limitations]
    B -->|No| G[Need Human Approval]

    C --> H[Trustworthy Process]
    D --> H
    E --> H
    F --> H
    G --> H
```

### Core idea

A polished artifact is not enough.

OpenClaw Showcase emphasizes the process around the artifact:

```text
Scoped → Traced → Reviewed → Limited → Approved
```

---

## Relationship to Other Showcase Files

- [OpenClaw Showcase README](../README.md)
- [Security Posture](../SECURITY-POSTURE.md)
- [Safety Boundaries](../docs/safety-boundaries.md)
- [Agentic Studio Workflow](../docs/agentic-studio-workflow.md)
- [Sanitized Run Receipt](../examples/sanitized-run-receipt.md)
- [BurnLens Case Study](../case-studies/burnlens/README.md)

---

## Summary

These diagrams present OpenClaw as an AI operations workflow, not as an uncontrolled automation system.

The public showcase highlights the visible process:

```text
Task → Draft → Trace → Review → Approve
```

The private system retains the runtime, configuration, credentials, operational memory, raw logs, and live tool authority.
