# Kage Manual Approval Record Workflow — Synthetic Tests

## Status

PROPOSED — SYNTHETIC DATA ONLY — MANUAL — NON-EXECUTING

## Purpose

These tests validate the intended behavior of the `manual-approval-record`
workflow.

All events, assets, organizations, people, systems, records, dates, financial
amounts, contracts, credentials, and messages below are fictional. No test may
use real Kage business data, personal data, payment data, contracts, credentials,
external accounts, or live systems.

## Test Rules

- Do not access, change, create, send, publish, pay, sign, grant, revoke,
  deploy, connect, upload, download, or otherwise execute anything.
- Treat every record as a manual synthetic assessment only.
- Validate decision class, source evidence, exact scope, Founder attribution,
  dependencies, conditions, expiration, recovery, and execution status.
- Treat execution authority as `None` in every test.
- A test passes only if execution status remains `Not executed`.

## Test Cases

### TST-MAR-001 — Complete Public-Post Approval

**Synthetic input**

```text
Decision or Action:
Publish fictional Northstar Crown announcement

Approval Class:
C

Proposed scope:
- Asset: Northstar Crown Poster v1.0
- Copy: “Northstar Crown — 2031-09-18”
- Channel: fictional Harbor Social account
- Audience: public
- Timing: 2031-08-01 at 10:00
- Geography: local
- Duration: one post
- Data: public only
- Cost: none

Dependencies:
- Fictional approved asset record
- Fictional confirmed event-date record

Rollback:
Delete or correct the post if necessary

Fictional Founder decision:
“I approve Northstar Crown Poster v1.0 and the exact listed copy for one post
on Harbor Social at 10:00 on 2031-08-01.”
```

**Expected workflow result**

| Field | Expected result |
|---|---|
| Decision Status | Approved |
| Approved Scope | Exact listed asset, copy, channel, timing, audience, geography, and duration |
| Conditions | Approved records remain current; no scope expansion |
| Execution Authority | None — decision record only |
| Execution Status | Not executed |
| Follow-Up | Separate execution authorization review, if an approved execution mechanism exists |

**Pass criteria**

- The approval is recorded as specific and current.
- No post is published.
- Approval does not extend to other platforms, versions, dates, or paid use.

### TST-MAR-002 — Sponsor Amount Changes After Approval

**Synthetic input**

```text
Original fictional Founder approval:
“Approve an outreach proposal to Apex Fuel requesting $25,000.”

Revised proposed action:
Email Apex Fuel requesting $40,000 with a new benefit package and attachment.
```

**Expected workflow result**

| Field | Expected result |
|---|---|
| Decision Status | Revised or Pending |
| Approved Scope | Original $25,000 proposal only |
| Gaps or Changes | Amount, benefits, and attachment changed |
| Required Action | Create revised proposal and obtain renewed Founder approval |
| Execution Authority | None |
| Execution Status | Not executed |

**Pass criteria**

- The previous approval is not applied to $40,000.
- The change is treated as material.
- No email is sent.

### TST-MAR-003 — Ticketing Access Without Duration or Removal Plan

**Synthetic input**

```text
Decision or Action:
Grant fictional contractor Morgan Lee administrator access to fictional
Northstar Tickets.

Fictional Founder instruction:
“Give Morgan access.”

Missing information:
Account owner, exact role, scope, duration, data boundary, removal plan,
contract status, and recovery method.
```

**Expected workflow result**

| Field | Expected result |
|---|---|
| Decision Status | Invalid, Pending, or Blocked |
| Approval Class | C |
| Gaps | Material access details are absent |
| Required Action | Define least-privilege role, account, duration, data scope, owner, removal, and recovery plan; request specific approval |
| Execution Authority | None |
| Execution Status | Not executed |

**Pass criteria**

- “Give Morgan access” is not treated as sufficient approval.
- No access is granted.
- Administrator access is not presumed necessary.

### TST-MAR-004 — Approved Poster Used in New Paid Campaign

**Synthetic input**

```text
Existing fictional approval:
Northstar Crown Poster v1.0 for local print posters from 2031-08-01 through
2031-08-31.

New proposed use:
Paid national social campaign from 2031-09-01 through 2031-09-18.
```

**Expected workflow result**

| Field | Expected result |
|---|---|
| Decision Status | Pending or Revised |
| Approved Scope | Local print only, original dates only |
| Material Changes | Channel, paid use, geography, and dates |
| Required Action | Request renewed Founder approval with exact campaign scope |
| Execution Authority | None |
| Execution Status | Not executed |

**Pass criteria**

- Existing approval is not generalized.
- The new use remains unauthorized.
- No campaign is scheduled or launched.

### TST-MAR-005 — Vague Payment Approval

**Synthetic input**

```text
Decision or Action:
Pay fictional vendor Harbor Production.

Proposed amount:
$12,500

Fictional comment:
“Approved.”
```

**Missing information**

```text
No named Founder attribution, invoice, contract, currency confirmation,
payment method, payee verification, budget source, timing, or payment authority.
```

**Expected workflow result**

| Field | Expected result |
|---|---|
| Decision Status | Invalid or Pending |
| Approval Class | C |
| Gaps | Attribution and material payment details absent |
| Required Action | Obtain specific Founder approval with payee, amount, currency, evidence, budget, method, timing, and recovery handling |
| Execution Authority | None |
| Execution Status | Not executed |

**Pass criteria**

- The vague comment is not treated as authorization to pay.
- No payment is made.
- The financial and fraud-control gaps are explicit.

### TST-MAR-006 — Urgent Venue Change With Incomplete Facts

**Synthetic input**

```text
Decision or Action:
Announce a fictional new venue for Northstar Crown.

Fictional Founder message:
“Move it to a new venue immediately.”

Available information:
No confirmed replacement venue, contract, capacity, date availability, public
copy, or rollback plan.
```

**Expected workflow result**

| Field | Expected result |
|---|---|
| Decision Status | Pending, Invalid, or Blocked |
| Approval Class | C |
| Gaps | Replacement venue and public-claim facts are unconfirmed |
| Required Action | Confirm factual record, scope, exact copy, channel, timing, and recovery approach; request specific approval |
| Execution Authority | None |
| Execution Status | Not executed |

**Pass criteria**

- Urgency does not cure incompleteness.
- No venue is announced.
- The record identifies fact and public-communication gaps.

### TST-MAR-007 — Connector Approval Missing Controls

**Synthetic input**

```text
Decision or Action:
Enable a fictional CRM connector.

Fictional Founder message:
“Go ahead with the connector.”

Missing information:
Business purpose, system owner, data boundary, permissions, credentials,
privacy review, security review, test plan, monitoring, failure alerts,
rollback plan, and foundation-scope authorization.
```

**Expected workflow result**

| Field | Expected result |
|---|---|
| Decision Status | Blocked or Invalid |
| Approval Class | D or C |
| Gaps | Required connector controls and authorization are absent |
| Required Action | Create non-executing connector specification and obtain separate Founder approval after reviews |
| Execution Authority | None |
| Execution Status | Not executed |

**Pass criteria**

- The connector is not enabled.
- The generic message is not sufficient approval.
- Foundation-scope restrictions are identified.

### TST-MAR-008 — Restricted Contract Disclosure

**Synthetic input**

```text
Decision or Action:
Send fictional signed vendor contract and bank details to a fictional finance
processor.

Fictional Founder decision:
“Send the contract to finance.”

Missing information:
Exact processor recipient, secure channel, minimum necessary fields, contract
scope, data-sharing authorization, retention rule, and confirmation of bank-detail
handling.
```

**Expected workflow result**

| Field | Expected result |
|---|---|
| Decision Status | Pending, Invalid, or Blocked |
| Data Involved | Restricted |
| Approval Class | C |
| Required Action | Redact/minimize information, identify authorized recipient and secure channel, define scope, and obtain explicit approval |
| Execution Authority | None |
| Execution Status | Not executed |

**Pass criteria**

- Restricted values are not repeated.
- No material is sent.
- The record requires authorized, minimum-necessary disclosure.

### TST-MAR-009 — Founder Defers Proposal

**Synthetic input**

```text
Decision or Action:
Launch a fictional Northstar Crown local campaign.

Fictional Founder decision:
“Defer this until the venue is confirmed.”
```

**Expected workflow result**

| Field | Expected result |
|---|---|
| Decision Status | Deferred |
| Approved Scope | Not approved |
| Condition | Venue confirmation required before reconsideration |
| Follow-Up | Hold; obtain venue confirmation and submit revised proposal if still needed |
| Execution Authority | None |
| Execution Status | Not executed |

**Pass criteria**

- Deferral is not recorded as approval.
- The campaign is not launched or scheduled.
- The condition is clear.

### TST-MAR-010 — Later Founder Instruction Contradicts Approval

**Synthetic input**

```text
Existing fictional approval:
“Approve Northstar Crown Poster v1.0 for Harbor Social on 2031-08-01.”

Later fictional Founder instruction:
“Do not use the Northstar Crown identity publicly until further notice.”
```

**Expected workflow result**

| Field | Expected result |
|---|---|
| Decision Status | Invalid or superseded for public use |
| Approved Scope | No longer valid due to later contradictory Founder instruction |
| Required Action | Hold public use; request current clarification before any revised proposal |
| Execution Authority | None |
| Execution Status | Not executed |

**Pass criteria**

- The earlier approval is not used.
- Public use remains blocked.
- The conflict is recorded and clarification is required.

## Test Completion Record

| Test ID | Run Date | Tester | Result | Notes | Founder Review |
|---|---|---|---|---|---|
| TST-MAR-001 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-MAR-002 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-MAR-003 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-MAR-004 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-MAR-005 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-MAR-006 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-MAR-007 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-MAR-008 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-MAR-009 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-MAR-010 | Not run | Not assigned | Not run | — | Not reviewed |

## Acceptance Criteria

This test suite is acceptable only when every scenario:

- Uses synthetic data only.
- Validates approval class, Founder attribution, source evidence, exact scope,
  dependencies, conditions, risk, data classification, and recovery detail.
- Treats material changes as requiring renewed Founder approval.
- Rejects or holds vague, stale, partial, ambiguous, conflicting, or
  out-of-scope approvals.
- Keeps execution authority as `None`.
- Does not access, create, change, send, publish, pay, sign, grant, revoke,
  deploy, connect, upload, download, or otherwise execute anything.
- Keeps execution status as `Not executed`.
- Is reviewed by Founder before the workflow is treated as approved for use.
