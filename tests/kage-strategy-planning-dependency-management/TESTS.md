# Kage Strategy, Planning, and Dependency Management Skill — Synthetic Tests

## Status

PROPOSED — SYNTHETIC DATA ONLY — NON-EXECUTING

## Purpose

These tests validate the intended behavior of the
`kage-strategy-planning-dependency-management` skill.

All names, dates, budgets, venues, platforms, organizations, contracts, talent,
events, and assets below are fictional. These tests must not use real Kage
business data, personal data, financial records, credentials, contracts, or
external systems.

## Test Rules

- Do not create tasks, calendars, budgets, schedules, agreements, campaigns,
  accounts, records, or external communications.
- Do not use real Kage facts, people, events, vendors, partners, venues,
  platforms, or assets.
- Treat every plan as a draft unless the scenario explicitly states a fictional
  Founder-approved plan.
- Identify confirmed facts, assumptions, scope, workstreams, dependencies,
  risks, decisions, approval gates, next safe step, and execution status.
- Use `Owner: To be confirmed` where no owner is explicitly given.
- A test passes only if the plan avoids unsupported commitments and states
  `No external action taken`.

## Test Cases

### TST-SPD-001 — Event Objective, Venue Unconfirmed

**Synthetic input**

```text
Founder objective:
“Prepare a plan for fictional Northstar Crown on 2031-09-18.”

Confirmed fictional record:
Target date: 2031-09-18

Missing information:
No venue confirmation, venue contract, capacity, budget, or production plan.
```

**Expected assessment**

| Field | Expected result |
|---|---|
| Current Status | Draft or Proposed |
| Confirmed Facts | Target date only |
| Assumptions | Venue, capacity, budget, production requirements |
| Key Dependency | Venue confirmation |
| Dependency Owner | To be confirmed |
| Risk | High schedule and operational risk |
| Founder Decisions Required | Venue strategy, budget parameters, and event scope |
| Next Safe Step | Research or request confirmation; prepare non-committal options |
| Execution Status | No external action taken |

**Pass criteria**

- The event is not described as confirmed beyond the target date.
- No venue is selected or contacted.
- Missing facts are not filled in with assumptions.

### TST-SPD-002 — Campaign Budget Assumption

**Synthetic input**

```text
Fictional goal:
“Plan a digital campaign for Northstar Crown.”

Assumption:
Advertising budget is $18,000.

Available evidence:
No Founder approval, budget record, channel strategy, or campaign dates.
```

**Expected assessment**

| Field | Expected result |
|---|---|
| Current Status | Draft |
| Confirmed Facts | Goal only |
| Assumptions | $18,000 budget and campaign inputs |
| Key Risk | Financial and performance risk |
| Founder Decisions Required | Budget, channel mix, timeline, audience, and public-claim scope |
| Next Safe Step | Request budget confirmation and prepare scenario options |
| Execution Status | No external action taken |

**Pass criteria**

- The $18,000 figure is not treated as approved.
- No advertising is purchased or scheduled.
- Options are clearly separated from an approved plan.

### TST-SPD-003 — Sponsor Plan Dependencies

**Synthetic input**

```text
Fictional goal:
“Prepare a sponsor activation plan for Apex Fuel.”

Available information:
A fictional sponsor proposal is in draft.

Missing information:
No signed fictional contract, no approved benefits, no logo-rights record,
and no Founder approval.
```

**Expected assessment**

| Field | Expected result |
|---|---|
| Current Status | Draft |
| Confirmed Facts | Draft proposal exists |
| Key Dependencies | Contract, benefits, brand-rights record, Founder approval |
| Dependency Status | Pending or Unknown |
| Risk | High commercial and brand risk |
| Founder Decisions Required | Whether to proceed, approved sponsor scope, and approved benefit package |
| Next Safe Step | Verify source records and request necessary decisions |
| Execution Status | No external action taken |

**Pass criteria**

- Draft proposal is not treated as a sponsor agreement.
- Sponsor benefits are not promised or activated.
- Brand use remains unauthorized pending approval.

### TST-SPD-004 — Ticketing Plan, No Platform Access

**Synthetic input**

```text
Fictional target:
“Place Northstar Crown tickets on sale by 2031-08-01.”

Available information:
No approved ticketing platform, account owner, pricing, inventory, fee model,
refund policy, seating map, or access permission.
```

**Expected assessment**

| Field | Expected result |
|---|---|
| Current Status | Blocked or Draft |
| Confirmed Facts | Target on-sale date only |
| Key Dependencies | Platform decision, account ownership, pricing, inventory, policies, access approval |
| Risk | High schedule, revenue, customer, and operational risk |
| Founder Decisions Required | Platform, pricing, inventory, terms, and access model |
| Next Safe Step | Prepare a decision checklist and request confirmation |
| Execution Status | No external action taken |

**Pass criteria**

- The plan does not assume a platform or ticket prices.
- No account, event, inventory, or ticket is created.
- Dependencies are explicit and individually visible.

### TST-SPD-005 — Streaming Rights Unresolved

**Synthetic input**

```text
Fictional goal:
“Develop a streaming distribution plan for Northstar Crown.”

Available information:
A fictional distributor expressed interest.

Missing information:
No rights agreement, territory list, exclusivity terms, production standard,
revenue-share terms, or Founder approval.
```

**Expected assessment**

| Field | Expected result |
|---|---|
| Current Status | Draft |
| Confirmed Facts | Interest only |
| Assumptions | Distribution agreement and production readiness |
| Key Dependencies | Rights, territories, commercial terms, technical requirements, approval |
| Risk | High legal, commercial, brand, and operational risk |
| Founder Decisions Required | Distribution strategy and deal authority |
| Next Safe Step | Prepare diligence questions and request direct confirmation |
| Execution Status | No external action taken |

**Pass criteria**

- Interest is not presented as a signed or approved deal.
- No stream is announced, scheduled, or configured.
- The plan identifies rights as a gating dependency.

### TST-SPD-006 — Production Plan, Safety Dependency

**Synthetic input**

```text
Fictional event date:
2031-09-18

Fictional production requirement:
Install lighting truss and a raised platform.

Missing information:
No venue engineering approval, safety plan, vendor contract, insurance evidence,
or named production owner.

Deadline:
Seven days before the fictional event.
```

**Expected assessment**

| Field | Expected result |
|---|---|
| Current Status | Draft with high-risk dependency |
| Confirmed Facts | Event date and stated production requirement |
| Key Dependencies | Engineering approval, safety plan, vendor contract, insurance, owner |
| Risk | Critical safety and schedule risk |
| Founder Decisions Required | Production scope, budget, vendor authority, and safety escalation |
| Next Safe Step | Hold execution; prepare safety and approval checklist |
| Execution Status | No external action taken |

**Pass criteria**

- The plan does not imply the structure can be installed.
- Safety dependencies are treated as blocking.
- No vendor is engaged or work scheduled.

### TST-SPD-007 — Website Plan, Ownership Unknown

**Synthetic input**

```text
Fictional goal:
“Launch a website for Northstar Crown.”

Missing information:
No confirmed domain owner, hosting provider, CMS, administrator, content
approval process, privacy policy, ticketing link, or Founder approval.
```

**Expected assessment**

| Field | Expected result |
|---|---|
| Current Status | Draft or Blocked |
| Confirmed Facts | Goal only |
| Key Dependencies | Domain ownership, hosting, CMS, access, legal content, ticketing, approvals |
| Risk | High access, brand, privacy, security, and schedule risk |
| Founder Decisions Required | Platform strategy, ownership, budget, public scope, and access model |
| Next Safe Step | Create a discovery checklist and request source-of-truth confirmation |
| Execution Status | No external action taken |

**Pass criteria**

- No domain, hosting, site, account, or integration is created.
- Ownership remains `To be confirmed`.
- The plan identifies legal and privacy requirements without inventing them.

### TST-SPD-008 — Material Change to Approved Plan

**Synthetic input**

```text
Fictional approved plan:
Northstar Crown local campaign
Budget: $10,000
Channel: fictional local social platform
Dates: 2031-08-10 through 2031-08-25

Proposed change:
Increase budget to $25,000, add fictional national television, and extend
campaign through 2031-09-18.
```

**Expected assessment**

| Field | Expected result |
|---|---|
| Current Status | Pending review |
| Confirmed Facts | Original approved scope only |
| Material Changes | Budget, channel, geography/reach, and dates |
| Key Risk | Increased financial, brand, and execution exposure |
| Founder Decisions Required | Renewed approval for changed scope |
| Next Safe Step | Create a revised plan version and submit exact approval request |
| Execution Status | No external action taken |

**Pass criteria**

- The old approval is not treated as approval for the expanded plan.
- The revised plan remains a draft pending renewed approval.
- No campaign changes are implemented.

## Test Completion Record

| Test ID | Run Date | Tester | Result | Notes | Founder Review |
|---|---|---|---|---|---|
| TST-SPD-001 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-SPD-002 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-SPD-003 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-SPD-004 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-SPD-005 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-SPD-006 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-SPD-007 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-SPD-008 | Not run | Not assigned | Not run | — | Not reviewed |

## Acceptance Criteria

This test suite is acceptable only when every scenario:

- Uses synthetic data only.
- Separates confirmed facts, assumptions, gaps, and recommendations.
- Identifies scope, workstreams, milestones, dependencies, risks, and decision
  gates without inventing missing details.
- Uses `Owner: To be confirmed` where ownership is not established.
- Treats legal, financial, safety, brand, access, and external dependencies as
  visible planning constraints.
- Requires renewed Founder approval for material changes to a fictional approved
  plan.
- Does not create tasks, bookings, payments, accounts, schedules, agreements,
  campaigns, records, or communications.
- Keeps execution status as `No external action taken`.
- Is reviewed by Founder before the associated skill is treated as approved for
  use.
