# Inbound Pipeline (GitHub Project v2)

Project URL:
- <https://github.com/users/VictorAOPS/projects/1>

## Mission Fit

This pipeline operationalizes the hub mission:
- Industrial Intelligence
- Data-Driven OpEx
- Ethical, human-centered execution

## Core Intake Flow

1. README CTA -> `issues/new` (prefill or form)
2. Issue is created with labels (`intent/inbound` or `request/project`)
3. `inbound-auto-add-to-project` adds the issue to Project v2
4. `inbound-pipeline-sync` updates `Pipeline` based on labels/state

## Pipeline Stages

- New
- Qualified
- In Progress
- Waiting
- Closed/Won

## Stage Definitions

- New: New inbound request, pending triage.
- Qualified: Intake has enough context to start.
- In Progress: Active collaboration/execution.
- Waiting: External dependency or missing input.
- Closed/Won: Engagement completed or outcome closed.

## SLA + Qualification Gate

- SLA: first response target in **24-48h**.
- Gate to move to **Qualified** (all required):
  - Goal
  - Context
  - Target KPI
  - Constraints and available data

## Labels (Canonical)

- `source/*` -> traffic origin (README, LinkedIn, other)
- `intent/*` -> collaboration intent
- `request/*` -> request type (project/role/other)
- `domain/*` -> technical domain
- `outcome/*` -> close reason / conversion result

Operational stage labels:
- `qualified`
- `in_progress`
- `waiting`

## Pipeline Sync Rules (Automation)

- `intent/inbound` OR `request/project` -> `New`
- `qualified` -> `Qualified`
- `in_progress` -> `In Progress`
- `waiting` -> `Waiting`
- Issue closed OR any `outcome/*` label -> `Closed/Won`

Workflows:
- `.github/workflows/inbound-auto-add-to-project.yml`
- `.github/workflows/inbound-pipeline-sync.yml`

## Project Fields (Recommended)

Keep `Pipeline` as the primary status field, plus:
- `Type`: `Collab`, `Research`, `Project`, `Role`, `Feedback`
- `Theme`: `DataOps`, `Smart Mfg`, `Applied AI`, `OpEx`, `Ethics/ESG`
- `Value`: `High`, `Medium`, `Low`
- `Urgency`: `Now`, `Soon`, `Later`
- `Next Step Date` (date)
- `Outcome`: `Won Project`, `Won Collab`, `Won Interview`, `No Fit`, `No Response`, `Later`

## Project Views (Recommended)

- `Pipeline` (board grouped by `Pipeline`)
- `By Theme` (table grouped by `Theme`)
- `Waiting` (filter `Pipeline=Waiting`, sort `Next Step Date`)
- `High Value` (filter `Value=High`)
- `Closed Outcomes` (filter `Pipeline=Closed/Won`, group by `Outcome`)

## NDA-Friendly Policy

- Public issues stay high-level (problem framing, expected outcomes, next steps).
- Sensitive architecture/data details are handled privately under NDA.
