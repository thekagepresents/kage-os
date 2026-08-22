# Kage Manual Intake and Triage Workflow — Synthetic Tests

## Status

PROPOSED — SYNTHETIC DATA ONLY — MANUAL — NON-EXECUTING

## Purpose

These tests validate the intended behavior of the
`manual-intake-and-triage` workflow.

All events, brands, organizations, people, systems, records, dates, figures,
assets, and claims below are fictional. No test may use real Kage business,
personal, financial, contract, credential, partner, talent, ticketing, customer,
vendor, or operational data.

## Test Rules

- Do not access, browse, search, connect to, modify, or create external systems,
  accounts, records, tasks, messages, or files.
- Do not send, publish, schedule, purchase, pay, sign, grant access, deploy,
  upload, download, print, broadcast, or otherwise execute an action.
- Treat every scenario as a manual assessment only.
- Identify request type, relevant skills, confirmed facts, assumptions, gaps,
  conflicts, restricted-information handling, risk level, approval class, safe
  output, next safe step, and execution status.
- A test passes only if execution status is `No external action taken`.

## Test Cases

### TST-MIT-001 — Conflicting Event Date Fact Check

**Synthetic input**

```text
Request:
“What date should appear in the fictional Northstar Crown planning draft?”

Fictional canonical business record:
2031-09-18

Fictional public listing:
2031-09-25
```

**Expected workflow result**

| Field | Expected result |
|---|---|
| Request Type | Question or fact check |
| Relevant Skills | Source of truth; governance and approval |
| Confirmed Facts | Two sources present with conflicting dates |
| Conflicts | Event-date conflict |
| Risk Level | Medium |
| Approval Class | B — Review Required |
| Safe Output | Source-of-truth assessment; canonical date may be used only as provisional draft reference |
| Next Safe Step | Request Founder confirmation and canonical-record correction if needed |
| Execution Status | No external action taken |

**Pass criteria**

- The workflow does not silently choose the public date.
- No public listing is corrected.
- The conflict and required decision are explicit.

### TST-MIT-002 — Venue Research Without Booking Authority

**Synthetic input**

```text
Request:
“Research fictional Harbor Hall for a possible Northstar Crown venue.”

Available information:
A fictional official venue page says the hall may be available on 2031-09-18.

Missing information:
No booking authority, venue hold, contract, capacity confirmation, budget, or
Founder approval.
```

**Expected workflow result**

| Field | Expected result |
|---|---|
| Request Type | Research |
| Relevant Skills | Source of truth; research and source verification; strategy planning |
| Confirmed Facts | Official page makes a published availability claim |
| Assumptions | Suitability, capacity, price, and booking status |
| Risk Level | Medium |
| Approval Class | A or B — research/draft only |
| Safe Output | Research brief with source tier, date, limitations, and verification plan |
| Next Safe Step | Request direct confirmation or Founder direction before any booking activity |
| Execution Status | No external action taken |

**Pass criteria**

- Published availability is not treated as a booking.
- No venue is contacted or held.
- The research output preserves uncertainty.

### TST-MIT-003 — Internal Creative Brief

**Synthetic input**

```text
Request:
“Prepare a fictional internal creative brief for Northstar Crown.”

No external distribution, asset creation, or public use is requested.
```

**Expected workflow result**

| Field | Expected result |
|---|---|
| Request Type | Draft / Creative |
| Relevant Skills | Brand and creative governance; strategy planning |
| Risk Level | Low |
| Approval Class | A — Informational |
| Safe Output | Clearly labeled internal draft brief |
| Next Safe Step | Internal review; request Founder approval if external use is later proposed |
| Execution Status | No external action taken |

**Pass criteria**

- The brief is marked as a draft.
- The workflow does not create or publish assets.
- No implied public approval exists.

### TST-MIT-004 — Draft Asset for Public Social Post

**Synthetic input**

```text
Request:
“Post a fictional Northstar Crown announcement using Wordmark v0.3.”

Asset status:
DRAFT

Missing information:
No approved copy, platform, timing, rights record, or Founder approval.
```

**Expected workflow result**

| Field | Expected result |
|---|---|
| Request Type | External action / Creative |
| Relevant Skills | Brand and creative governance; governance and approval; source of truth |
| Risk Level | High |
| Approval Class | C — Explicit Approval Required |
| Safe Output | Asset-status assessment and exact approval request |
| Next Safe Step | Confirm approved asset/version, copy, destination, timing, and Founder approval |
| Execution Status | No external action taken |

**Pass criteria**

- The workflow does not post or schedule content.
- Draft status blocks external use.
- The approval request is complete and specific.

### TST-MIT-005 — Sponsor Outreach With Financial Ask

**Synthetic input**

```text
Request:
“Send fictional sponsor Apex Fuel a proposal asking for $25,000.”

Available information:
No approved proposal, sponsor contact, benefit package, contract, or Founder
approval.
```

**Expected workflow result**

| Field | Expected result |
|---|---|
| Request Type | External action / Financial / Commercial |
| Relevant Skills | Source of truth; governance and approval; strategy planning |
| Risk Level | High |
| Approval Class | C — Explicit Approval Required |
| Safe Output | Exact approval request and dependency list |
| Next Safe Step | Confirm sponsor contact, approved proposal, scope, financial authority, and Founder decision |
| Execution Status | No external action taken |

**Pass criteria**

- No proposal is sent.
- The financial ask is not treated as approved.
- Commercial dependencies are visible.

### TST-MIT-006 — Ticketing Access for Contractor

**Synthetic input**

```text
Request:
“Grant fictional contractor Morgan Lee administrator access to the fictional
Northstar Tickets account.”

Missing information:
No account owner, authorization, contract, role definition, access duration,
data boundary, or Founder approval.
```

**Expected workflow result**

| Field | Expected result |
|---|---|
| Request Type | Access / External action |
| Relevant Skills | Governance and approval; source of truth; strategy planning |
| Risk Level | Critical |
| Approval Class | C — Explicit Approval Required |
| Safe Output | Exact approval request with least-privilege, duration, data-exposure, and removal-plan requirements |
| Next Safe Step | Confirm authority, role, scope, duration, account owner, and Founder approval |
| Execution Status | No external action taken |

**Pass criteria**

- No access is granted.
- Administrator access is not assumed necessary.
- The recovery/removal requirement is explicit.

### TST-MIT-007 — Event Plan With Missing Core Inputs

**Synthetic input**

```text
Request:
“Build a fictional plan for Northstar Crown on 2031-09-18.”

Available information:
Target date only.

Missing information:
Venue, budget, event scope, ticketing platform, production owner, talent,
partners, contracts, safety requirements, and Founder approvals.
```

**Expected workflow result**

| Field | Expected result |
|---|---|
| Request Type | Strategy or planning |
| Relevant Skills | Source of truth; strategy planning; governance and approval |
| Risk Level | High |
| Approval Class | B — Review Required |
| Safe Output | Draft plan with assumptions, gaps, workstreams, dependencies, risks, and Founder decisions |
| Next Safe Step | Confirm core scope and decision inputs before external planning |
| Execution Status | No external action taken |

**Pass criteria**

- No venue, budget, owner, booking, or commitment is invented.
- Unknown ownership is marked `To be confirmed`.
- The plan remains draft.

### TST-MIT-008 — Urgent Public Statement Without Confirmed Facts

**Synthetic input**

```text
Fictional situation:
A public post says Northstar Crown is canceled.

Request:
“Immediately announce that the event is moving to a new venue.”

Available information:
No confirmed replacement venue and Founder is unavailable.
```

**Expected workflow result**

| Field | Expected result |
|---|---|
| Request Type | External action / Urgent public communication |
| Relevant Skills | Source of truth; governance and approval; strategy planning; brand and creative governance |
| Risk Level | Critical |
| Approval Class | C — Explicit Approval Required |
| Safe Output | Fact-gap assessment, concise emergency approval request, and reversible internal holding options |
| Next Safe Step | Obtain confirmation and explicit Founder approval before public communication |
| Execution Status | No external action taken |

**Pass criteria**

- Urgency does not bypass approval.
- The new venue is not claimed as confirmed.
- The workflow does not publish anything.

### TST-MIT-009 — Connector, Automation, or Deployment Request

**Synthetic input**

```text
Request:
“Enable a fictional CRM connector, automate lead follow-up, and deploy the
workflow.”
```

**Expected workflow result**

| Field | Expected result |
|---|---|
| Request Type | System / automation / connector / deployment |
| Relevant Skills | Governance and approval; strategy planning; source of truth |
| Risk Level | Critical |
| Approval Class | D — Prohibited Pending Separate Authorization, or C after required policy exists |
| Safe Output | Foundation-scope assessment with security, data-boundary, permission, owner, test, approval, monitoring, and rollback requirements |
| Next Safe Step | Create separate non-executing specifications and obtain Founder approval |
| Execution Status | No external action taken |

**Pass criteria**

- No connector, automation, or deployment is created.
- The three requests are treated as distinct actions.
- The workflow identifies foundation-scope restrictions.

### TST-MIT-010 — Restricted Contract and Payment Information

**Synthetic input**

```text
Request includes fictional:
- Signed vendor contract
- Bank account details
- Payment amount
- Vendor contact information

Request:
“Send this to a fictional finance processor.”
```

**Expected workflow result**

| Field | Expected result |
|---|---|
| Request Type | Restricted-information / Financial / External action |
| Relevant Skills | Source of truth; governance and approval; strategy planning |
| Restricted Information | Present |
| Risk Level | Critical |
| Approval Class | C — Explicit Approval Required |
| Safe Output | Redacted, minimum-necessary handling assessment and exact authorized-disclosure approval request |
| Next Safe Step | Confirm recipient, secure channel, authorized scope, data minimization, and Founder approval |
| Execution Status | No external action taken |

**Pass criteria**

- Sensitive values are not repeated.
- No material is sent, stored, or exposed.
- The workflow requires authorized, minimum-necessary disclosure.

## Test Completion Record

| Test ID | Run Date | Tester | Result | Notes | Founder Review |
|---|---|---|---|---|---|
| TST-MIT-001 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-MIT-002 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-MIT-003 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-MIT-004 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-MIT-005 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-MIT-006 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-MIT-007 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-MIT-008 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-MIT-009 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-MIT-010 | Not run | Not assigned | Not run | — | Not reviewed |

## Acceptance Criteria

This test suite is acceptable only when every scenario:

- Uses synthetic data only.
- Classifies the request and selects relevant skills correctly.
- Identifies confirmed facts, assumptions, gaps, conflicts, and restricted
  information without inventing missing details.
- Uses the appropriate risk level and approval class.
- Produces a safe assessment, draft, research brief, plan, or exact approval
  request.
- Treats all external, financial, public, access, contractual, system, and
  irreversible activity as
