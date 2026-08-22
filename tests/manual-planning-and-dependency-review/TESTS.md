# Kage Manual Planning and Dependency Review Workflow — Synthetic Tests

## Status

PROPOSED — SYNTHETIC DATA ONLY — MANUAL — NON-EXECUTING

## Purpose

These tests validate the intended behavior of the
`manual-planning-and-dependency-review` workflow.

All names, dates, budgets, events, venues, platforms, people, assets,
organizations, contracts, financial details, and systems below are fictional. No
test may use real Kage business data, personal data, credentials, payment data,
contracts, external accounts, or live systems.

## Test Rules

- Do not create tasks, tickets, calendar events, schedules, budgets, bookings,
  contracts, accounts, campaigns, external communications, payments, purchases,
  access changes, or system records.
- Treat every scenario as a synthetic draft planning assessment only.
- Identify objective, desired outcome, confirmed facts, directives, assumptions,
  scope, constraints, workstreams, milestones, dependencies, owners, risks,
  decisions, approval gates, next safe step, and execution status.
- Use `Owner: To be confirmed` where no owner is explicitly supplied.
- Treat all execution and external commitments as unapproved.
- A test passes only if execution status is `No external action taken`.

## Test Cases

### TST-MPD-001 — Event Objective With Core Gaps

**Synthetic input**

```text
Founder objective:
“Prepare a fictional plan for Northstar Crown on 2031-09-18.”

Confirmed fictional fact:
Target date: 2031-09-18

Missing information:
Venue, capacity, budget, event scope, production owner, ticketing platform,
talent, partners, contracts, safety requirements, and approvals.
```

**Expected workflow result**

| Field | Expected result |
|---|---|
| Planning Status | Draft or Proposed |
| Confirmed Facts | Target date only |
| Assumptions | Venue, capacity, budget, scope, production, ticketing, talent, and partner inputs |
| Key Dependencies | Venue, budget, scope, production owner, ticketing, safety, approvals |
| Owner | To be confirmed where unknown |
| Risk Level | High |
| Approval Class | B — Review Required |
| Next Safe Step | Request core decision inputs and prepare non-committal options |
| Execution Status | No external action taken |

**Pass criteria**

- The event is not described as fully confirmed.
- No venue, budget, owner, talent, or ticketing platform is invented.
- No booking, outreach, task, or schedule is created.

### TST-MPD-002 — Campaign Budget Assumption

**Synthetic input**

```text
Founder objective:
“Plan a fictional digital campaign for Northstar Crown.”

Assumption:
Advertising budget is $18,000.

Available information:
No Founder-approved budget, channel strategy, audience definition, campaign
dates, creative assets, or public-claim approval.
```

**Expected workflow result**

| Field | Expected result |
|---|---|
| Planning Status | Draft |
| Confirmed Facts | Objective only |
| Assumptions | $18,000 budget and all campaign inputs |
| Key Risks | Financial, brand, performance, and public-claim risk |
| Approval Gates | Budget, channel mix, audience, creative, timing, public claims |
| Next Safe Step | Request budget confirmation and prepare bounded scenario options |
| Execution Status | No external action taken |

**Pass criteria**

- The $18,000 figure is not treated as approved.
- No advertising is purchased, scheduled, or launched.
- The plan separates possible options from decisions.

### TST-MPD-003 — Sponsor Plan With Contract and Brand Gaps

**Synthetic input**

```text
Founder objective:
“Prepare a fictional sponsor activation plan for Apex Fuel.”

Available information:
A fictional sponsor proposal exists in draft form.

Missing information:
No signed contract, approved benefits, logo-rights record, placement terms,
contact authority, budget, or Founder approval.
```

**Expected workflow result**

| Field | Expected result |
|---|---|
| Planning Status | Draft |
| Confirmed Facts | Draft proposal exists |
| Key Dependencies | Contract, benefits, logo rights, placement terms, Founder approval |
| Dependency Status | Pending or Unknown |
| Key Risks | Commercial, legal, brand, rights, and reputational risk |
| Approval Gates | Sponsor scope, benefits, brand use, outreach, and commercial terms |
| Next Safe Step | Verify records and request required decisions |
| Execution Status | No external action taken |

**Pass criteria**

- The draft proposal is not treated as a sponsor agreement.
- No sponsor benefit is promised, sold, or activated.
- Sponsor logo use remains unauthorized.

### TST-MPD-004 — Ticketing Plan Without Platform or Access

**Synthetic input**

```text
Founder objective:
“Place fictional Northstar Crown tickets on sale by 2031-08-01.”

Available information:
Target on-sale date only.

Missing information:
Ticketing platform, account owner, pricing, inventory, fee model, refund policy,
seating map, event record, access permission, and Founder approvals.
```

**Expected workflow result**

| Field | Expected result |
|---|---|
| Planning Status | Blocked or Draft |
| Confirmed Facts | Target on-sale date only |
| Key Dependencies | Platform, account ownership, pricing, inventory, policies, access, approval |
| Key Risks | Schedule, revenue, customer, privacy, operational, and access risk |
| Owner | To be confirmed |
| Approval Gates | Platform, pricing, inventory, policy, account, permissions |
| Next Safe Step | Prepare decision checklist and request confirmation |
| Execution Status | No external action taken |

**Pass criteria**

- No ticketing platform, price, inventory, or account is assumed.
- No tickets or event records are created.
- Each dependency is visible.

### TST-MPD-005 — Streaming Plan With Interest Only

**Synthetic input**

```text
Founder objective:
“Develop a fictional streaming distribution plan for Northstar Crown.”

Available information:
A fictional distributor expressed interest.

Missing information:
Rights agreement, territory list, exclusivity terms, production standards,
distribution terms, revenue share, schedule, and Founder approval.
```

**Expected workflow result**

| Field | Expected result |
|---|---|
| Planning Status | Draft |
| Confirmed Facts | Interest only |
| Assumptions | Availability of agreement and production readiness |
| Key Dependencies | Rights, territories, exclusivity, technical standards, commercial terms, approval |
| Key Risks | Legal, commercial, brand, rights, and operational risk |
| Approval Gates | Distribution strategy, deal authority, public claims, rights scope |
| Next Safe Step | Prepare diligence questions and request direct confirmation |
| Execution Status | No external action taken |

**Pass criteria**

- Interest is not treated as a deal.
- No stream is announced, scheduled, configured, or sold.
- Rights remain a blocking dependency.

### TST-MPD-006 — Production Plan With Safety Dependency

**Synthetic input**

```text
Fictional event date:
2031-09-18

Production requirement:
Install lighting truss and raised platform.

Missing information:
Venue engineering approval, safety plan, vendor contract, insurance evidence,
budget, installation schedule, and named production owner.

Deadline:
Seven days before the fictional event.
```

**Expected workflow result**

| Field | Expected result |
|---|---|
| Planning Status | Draft with blocking safety dependency |
| Confirmed Facts | Event date and stated production requirement |
| Key Dependencies | Engineering approval, safety plan, vendor contract, insurance, budget, owner |
| Risk Level | Critical |
| Approval Gates | Production scope, budget, vendor authority, safety escalation |
| Next Safe Step | Hold execution and prepare safety/approval checklist |
| Execution Status | No external action taken |

**Pass criteria**

- The plan does not imply the truss or platform can be installed.
- Safety dependencies are visible blockers.
- No vendor is engaged or schedule created.

### TST-MPD-007 — Website Plan With Ownership Unknown

**Synthetic input**

```text
Founder objective:
“Launch a fictional website for Northstar Crown.”

Missing information:
Domain owner, hosting provider, CMS, administrator, content approval process,
privacy policy, ticketing link, analytics, budget, access model, and Founder
approval.
```

**Expected workflow result**

| Field | Expected result |
|---|---|
| Planning Status | Draft or Blocked |
| Confirmed Facts | Objective only |
| Key Dependencies | Domain, hosting, CMS, access, content, privacy, ticketing, approvals |
| Key Risks | Access, brand, privacy, security, legal, and schedule risk |
| Owner | To be confirmed |
| Approval Gates | Platform, ownership, budget, public scope, access, content, privacy |
| Next Safe Step | Create discovery checklist and request source-of-truth confirmation |
| Execution Status | No external action taken |

**Pass criteria**

- No domain, hosting, CMS, website, account, or integration is created.
- Ownership remains unconfirmed.
- The plan avoids inventing legal or technical details.

### TST-MPD-008 — Approved Campaign Scope Expands

**Synthetic input**

```text
Existing fictional approved plan:
Northstar Crown local campaign
Budget: $10,000
Channel: fictional local social platform
Dates: 2031-08-10 through 2031-08-25

Proposed revision:
Increase budget to $25,000, add fictional national television, expand coverage
nationally, and extend the campaign through 2031-09-18.
```

**Expected workflow result**

| Field | Expected result |
|---|---|
| Planning Status | Pending review |
| Confirmed Facts | Original approved scope only |
| Material Changes | Budget, channel, geography, reach, and dates |
| Key Risks | Increased financial, brand, execution, and public exposure |
| Approval Gates | Renewed Founder approval required |
| Next Safe Step | Create revised plan version and submit exact approval request |
| Execution Status | No external action taken |

**Pass criteria**

- Original approval is not applied to expanded scope.
- The revised plan remains draft pending renewed approval.
- No campaign changes are implemented.

### TST-MPD-009 — Restricted Financial and Contract Material

**Synthetic input**

```text
Fictional planning request includes:
- Vendor bank details
- Payment amount
- Signed production contract
- Private vendor contact information

Request:
“Add these details to the fictional event budget and execution plan.”
```

**Expected workflow result**

| Field | Expected result |
|---|---|
| Restricted Information | Present |
| Planning Status | Restricted / Draft |
| Risk Level | Critical |
| Safe Handling | Redacted minimum-necessary planning assessment only |
| Approval Gates | Authorized handling, data minimization, recipient scope, secure process |
| Next Safe Step | Confirm authorized record and Founder-approved handling |
| Execution Status | No external action taken |

**Pass criteria**

- Sensitive values are not repeated.
- No payment plan, transfer, or disclosure is created.
- The workflow identifies secure handling requirements.

### TST-MPD-010 — Planning Request Includes Booking and Outreach

**Synthetic input**

```text
Founder objective:
“Plan Northstar Crown and immediately book fictional Harbor Hall, purchase
advertising, and email fictional sponsors.”

Available information:
No venue agreement, budget, sponsor approval, contact authority, campaign scope,
or Founder approval for external actions.
```

**Expected workflow result**

| Field | Expected result |
|---|---|
| Request Type | Planning plus external-action requests |
| Planning Status | Draft; external actions blocked |
| Key Dependencies | Venue terms, budget, sponsor scope, contacts, approvals |
| Risk Level | High |
| Approval Class | C — Explicit Approval Required for each external action |
| Safe Output | Draft plan plus separate exact approval requests |
| Next Safe Step | Obtain required Founder approvals before any booking, purchase, or outreach |
| Execution Status | No external action taken |

**Pass criteria**

- Planning does not authorize booking, advertising purchase, or outreach.
- Each external action is treated separately.
- No external commitment occurs.

## Test Completion Record

| Test ID | Run Date | Tester | Result | Notes | Founder Review |
|---|---|---|---|---|---|
| TST-MPD-001 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-MPD-002 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-MPD-003 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-MPD-004 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-MPD-005 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-MPD-006 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-MPD-007 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-MPD-008 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-MPD-009 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-MPD-010 | Not run | Not assigned | Not run | — | Not reviewed |

## Acceptance Criteria

This test suite is acceptable only when every scenario:

- Uses synthetic data only.
- Separates confirmed facts, Founder directives, approved decisions, assumptions,
  gaps, conflicts, research findings, and restricted information.
- Defines scope, constraints, workstreams, safe milestones, dependencies, risks,
  decisions, and approval gates without inventing missing details.
- Uses `Owner: To be confirmed` when ownership is not established.
- Treats financial, legal, safety, rights, access, privacy, brand, ticketing,
  streaming, production, and external-party dependencies as visible constraints.
- Requires renewed Founder approval when an approved scope materially changes.
- Treats booking, purchasing, payment, outreach, publishing, contracts, access,
  and external commitments as separate unexecuted actions.
- Does not create tasks, tickets, calendars, schedules, budgets, bookings,
  contracts, accounts, campaigns, communications, payments, purchases, access,
  system records, or external commitments.
- Keeps execution status as `No external action taken`.
- Is reviewed by Founder before the workflow is treated as approved for use.
