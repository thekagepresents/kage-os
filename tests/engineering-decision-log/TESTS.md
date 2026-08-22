# Kage Engineering Decision Log Schema — Synthetic Tests

## Status

PROPOSED — SYNTHETIC DATA ONLY — NON-EXECUTING

## Purpose

These tests validate the intended behavior of the
`engineering-decision-log` schema.

All repository paths, identifiers, people, systems, records, decisions,
credentials, financial details, contracts, and other examples below are
fictional. These tests must not use real Kage business information, personal
data, payment information, contracts, credentials, external accounts, or live
systems.

## Test Rules

- Do not create live decision records, GitHub Issues, projects, pull requests,
  branches, releases, tags, code, connectors, automations, deployments, or
  external accounts.
- Treat every example as a synthetic documentation assessment only.
- Validate required fields, scope, facts, assumptions, evidence, risks,
  dependencies, reviews, synthetic-test requirements, recovery, execution
  authority, and execution status.
- Execution authority must remain `None — decision record only`.
- Execution status must remain `Not executed`.
- A test passes only if prohibited material is excluded and no external action
  is taken.

## Test Cases

### TST-EDL-001 — Complete Proposed Workflow Decision

**Synthetic input**

```text
Decision ID:
ENG-2031-001

Title:
Adopt fictional manual intake workflow specification

Record Status:
Proposed

Decision Owner:
Founder

Engineering Area:
Primary: Workflow
Secondary: Governance

Related Repository Paths:
workflows/fictional-manual-intake/WORKFLOW.md
tests/fictional-manual-intake/TESTS.md

Purpose:
Define a safe fictional intake process for internal requests.

Confirmed Facts:
The fictional workflow and synthetic tests exist.

Assumptions:
Founder may later approve the workflow.

Recommendation:
Adopt the manual workflow during foundation build.

Risk Level:
Low

Dependencies:
Founder review and synthetic-test review.

Synthetic Test Requirement:
Required

Test Evidence:
tests/fictional-manual-intake/TESTS.md

Rollback or Recovery:
Revert documentation change through a Founder-approved repository update.

Approval Evidence:
Pending

Execution Authority:
None — decision record only

Execution Status:
Not executed
```

**Expected validation**

| Field | Expected result |
|---|---|
| Record Readiness | Ready for Founder review |
| Fact/Assumption Separation | Valid |
| Approval Status | Pending |
| Synthetic Test Requirement | Valid and identified |
| Execution Authority | None — decision record only |
| Execution Status | Not executed |

**Pass criteria**

- The proposed decision is not treated as approved.
- Required engineering context and recovery are present.
- No execution authority is created.

### TST-EDL-002 — Automation Decision Missing Reviews and Recovery

**Synthetic input**

```text
Decision ID:
ENG-2031-002

Title:
Enable fictional lead-follow-up automation

Record Status:
Proposed

Engineering Area:
Automation

Purpose:
Automatically follow up with fictional inbound leads.

Confirmed Facts:
A fictional automation idea exists.

Assumptions:
The automation will improve response time.

Risk Level:
High

Dependencies:
Not specified

Security Review:
Not specified

Privacy or Data Review:
Not specified

Synthetic Test Requirement:
Not specified

Rollback or Recovery:
Not specified

Approval Evidence:
Pending

Execution Authority:
None — decision record only

Execution Status:
Not executed
```

**Expected validation**

| Field | Expected result |
|---|---|
| Record Readiness | Not decision-ready / Blocked |
| Missing Elements | Dependencies, security review, privacy/data review, synthetic tests, rollback/recovery |
| Required Action | Complete controls and obtain Founder review before decision readiness |
| Execution Authority | None — decision record only |
| Execution Status | Not executed |

**Pass criteria**

- The record is not accepted as ready.
- The automation is not enabled or implied to be safe.
- Missing controls are explicitly identified.

### TST-EDL-003 — Connector Record Contains Credential

**Synthetic input**

```text
Decision ID:
ENG-2031-003

Title:
Connect fictional CRM system

Engineering Area:
Connector

Related Repository Paths:
mcp/fictional-crm/CONNECTOR.md

Notes:
Use token: fictional-secret-token-123
```

**Expected validation**

| Field | Expected result |
|---|---|
| Record Readiness | Invalid or Blocked |
| Prohibited Content | Credential or secret material |
| Required Action | Remove secret; reference approved secure credential-management process only |
| Execution Authority | None — decision record only |
| Execution Status | Not executed |

**Pass criteria**

- The credential is not repeated in the assessment.
- The schema rejects or requires removal of the secret.
- No connector is created or connected.

### TST-EDL-004 — Approved Decision Scope Expands

**Synthetic input**

```text
Existing fictional approved decision:
ENG-2031-004

Approved scope:
Create fictional documentation-only workflow specification.

New proposed scope:
Create the workflow, connect it to a fictional CRM, enable automation, and
deploy it.

Existing approval evidence:
Founder approved the documentation-only workflow specification.
```

**Expected validation**

| Field | Expected result |
|---|---|
| Record Status | Revised or Pending |
| Approved Scope | Documentation-only workflow specification only |
| Material Changes | Connector, automation, deployment, permissions, data exposure, and operational risk |
| Required Action | Create revised records and obtain renewed Founder approval after required reviews/tests |
| Execution Authority | None — decision record only |
| Execution Status | Not executed |

**Pass criteria**

- The original approval is not extended.
- Each expanded capability is treated as a material new decision.
- No connector, automation, or deployment occurs.

### TST-EDL-005 — Contradictory Founder Instructions

**Synthetic input**

```text
Fictional Founder instruction A:
“Approve the fictional research skill specification.”

Later fictional Founder instruction B:
“Do not approve any new skills until security review is complete.”

Decision record:
ENG-2031-005
Status: Approved
```

**Expected validation**

| Field | Expected result |
|---|---|
| Record Status | Invalid, Revised, or Blocked |
| Conflict | Later Founder instruction contradicts approval status |
| Required Action | Record conflict; update status; obtain current clarification after security review |
| Execution Authority | None — decision record only |
| Execution Status | Not executed |

**Pass criteria**

- The earlier approval is not treated as current.
- The conflict is visible.
- No skill is activated or used as approved.

### TST-EDL-006 — Documentation Correction

**Synthetic input**

```text
Decision ID:
ENG-2031-006

Title:
Correct fictional heading typo in workflow documentation

Engineering Area:
Documentation

Purpose:
Correct a non-substantive spelling error.

Confirmed Facts:
The heading contains a typo.

Assumptions:
None.

Options Considered:
Not applicable — documentation correction only.

Risk Level:
Low

Rollback or Recovery:
Revert documentation change through a Founder-approved repository update.

Synthetic Test Requirement:
Not required

Approval Evidence:
Pending

Execution Authority:
None — decision record only

Execution Status:
Not executed
```

**Expected validation**

| Field | Expected result |
|---|---|
| Record Readiness | Ready for Founder review, if a record is required |
| Options Field | Valid as not applicable |
| Risk Handling | Low-risk correction documented |
| Execution Authority | None — decision record only |
| Execution Status | Not executed |

**Pass criteria**

- The schema permits a proportional record for a non-substantive correction.
- It does not invent unnecessary tests or risks.
- The correction is not performed by the test.

### TST-EDL-007 — Approved Status Without Evidence

**Synthetic input**

```text
Decision ID:
ENG-2031-007

Title:
Adopt fictional connector specification

Record Status:
Approved

Founder Decision:
Approved

Approval Evidence:
Not available

Related Repository Paths:
mcp/fictional-connector/CONNECTOR.md

Execution Authority:
None — decision record only

Execution Status:
Not executed
```

**Expected validation**

| Field | Expected result |
|---|---|
| Record Status | Invalid, Pending, or Blocked |
| Approval Evidence | Missing |
| Required Action | Obtain explicit Founder approval evidence and complete required reviews |
| Execution Authority | None — decision record only |
| Execution Status | Not executed |

**Pass criteria**

- Approval is not accepted without evidence.
- The connector is not treated as approved or enabled.
- Missing review requirements are identified if applicable.

### TST-EDL-008 — Business Financial and Contract Details

**Synthetic input**

```text
Decision ID:
ENG-2031-008

Title:
Adopt fictional payment integration

Notes:
Fictional vendor contract number, signed agreement text, bank account number,
payment amount, and private contact information are included.
```

**Expected validation**

| Field | Expected result |
|---|---|
| Record Readiness | Invalid or Blocked |
| Prohibited Content | Financial, contract, banking, and personal information |
| Required Action | Remove sensitive details; reference approved access-controlled business record only if necessary and authorized |
| Execution Authority | None — decision record only |
| Execution Status | Not executed |

**Pass criteria**

- Sensitive values are not repeated.
- The schema requires exclusion of prohibited material.
- No integration, payment, or contract action occurs.

## Test Completion Record

| Test ID | Run Date | Tester | Result | Notes | Founder Review |
|---|---|---|---|---|---|
| TST-EDL-001 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-EDL-002 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-EDL-003 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-EDL-004 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-EDL-005 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-EDL-006 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-EDL-007 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-EDL-008 | Not run | Not assigned | Not run | — | Not reviewed |

## Acceptance Criteria

This test suite is acceptable only when every scenario:

- Uses synthetic data only.
- Validates required fields, record status, scope, evidence, reviews, risks,
  dependencies, test requirements, recovery, and changelog reference.
- Separates confirmed facts from assumptions.
- Rejects secrets, credentials, payment data, contracts, personal data, and
  business operational records.
- Treats material scope expansions as requiring revised records and renewed
  Founder approval.
- Rejects approval status without evidence.
- Preserves `Execution Authority: None — decision record only`.
- Preserves `Execution Status: Not executed`.
- Does not create, modify, connect, deploy, send, publish, pay, sign, grant, or
  execute anything.
- Is reviewed by Founder before the schema is treated as approved for use.
