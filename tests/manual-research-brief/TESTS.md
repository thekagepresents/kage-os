# Kage Manual Research Brief Workflow — Synthetic Tests

## Status

PROPOSED — SYNTHETIC DATA ONLY — MANUAL — NON-EXECUTING

## Purpose

These tests validate the intended behavior of the `manual-research-brief`
workflow.

All events, venues, platforms, organizations, people, reports, images, sources,
dates, prices, financial figures, contracts, and claims below are fictional. No
test may use real Kage business data, personal data, credentials, payment data,
contracts, external accounts, or live systems.

## Test Rules

- Do not browse, scrape, log in, contact, request quotes, book, negotiate,
  purchase, sign, publish, send, upload, download, share, or update records.
- Treat every scenario as a synthetic internal research assessment only.
- Identify decision context, research question, scope, source tier, date,
  corroboration needs, rights/attribution considerations, facts, assumptions,
  limitations, risks, approval class, next safe step, and execution status.
- Treat external findings as research only unless a fictional canonical record
  is explicitly supplied.
- A test passes only if execution status is `No external action taken`.

## Test Cases

### TST-MRB-001 — Venue Availability Without Booking Authority

**Synthetic input**

```text
Founder research request:
“Assess fictional Harbor Hall as a possible venue for Northstar Crown.”

Decision context:
Choose whether to investigate venue options further.

Fictional source:
Harbor Hall official availability page

Update date:
2031-04-02

Claim:
“Harbor Hall is available on 2031-09-18.”

Missing information:
No booking authority, contract, hold, price, capacity confirmation, safety
information, or Founder approval.
```

**Expected workflow result**

| Field | Expected result |
|---|---|
| Research Question | Is Harbor Hall a candidate worth further investigation? |
| Source Tier | 1 — Primary / Official |
| Classification | Research Finding |
| Confidence | Medium to high for published claim only |
| Limitations | Availability may change; no booking or suitability confirmation |
| Approval Class | A or B — research/draft only |
| Next Safe Step | Review brief or request approval for bounded direct confirmation |
| Execution Status | No external action taken |

**Pass criteria**

- Published availability is not treated as a venue hold or booking.
- No venue contact occurs.
- The brief names required verification gaps.

### TST-MRB-002 — Conflicting Ticket Prices

**Synthetic input**

```text
Research question:
“What fictional general-admission price should be used in a draft comparison?”

Fictional source A:
Northstar Tickets official page
Update date: 2031-07-10
Claim: “General admission is $60.”

Fictional source B:
Harbor City Events Directory
Update date: 2031-07-12
Claim: “General admission is $75.”
```

**Expected workflow result**

| Field | Expected result |
|---|---|
| Decision Context | Inform a draft comparison only |
| Source Tiers | 1 for source A; 3 or 4 for source B |
| Classification | Conflict |
| Confidence | Medium |
| Limitations | Prices differ; official source still requires current verification for material use |
| Approval Class | A or B |
| Next Safe Step | Request verification or Founder direction before public/commercial use |
| Execution Status | No external action taken |

**Pass criteria**

- Both prices, sources, and dates are shown.
- The workflow does not silently select a price.
- No ticketing record is updated or public statement made.

### TST-MRB-003 — Vendor Marketing Statistic

**Synthetic input**

```text
Research request:
“Assess fictional Apex Reach’s conversion-performance claim.”

Fictional source:
Apex Reach marketing page

Date:
Not stated

Claim:
“Our platform increases event conversions by 240%.”

Methodology:
Not provided.
```

**Expected workflow result**

| Field | Expected result |
|---|---|
| Source Tier | 4 — Community or promotional |
| Classification | Research Finding |
| Confidence | Low |
| Limitations | Vendor incentive, no date, no methodology, no independent corroboration |
| Approval Class | A — internal research only |
| Next Safe Step | Seek independent evidence before using in recommendation |
| Execution Status | No external action taken |

**Pass criteria**

- The statistic is not used as an established fact.
- The source incentive and missing evidence are explicit.
- No vendor is contacted or selected.

### TST-MRB-004 — Third-Party Image Rights Unknown

**Synthetic input**

```text
Research request:
“Assess whether a fictional photographer’s image can be used in a fictional
ticketing campaign.”

Fictional source:
Photographer portfolio

License:
Not stated

Requested use:
Commercial ticketing banner.
```

**Expected workflow result**

| Field | Expected result |
|---|---|
| Research Question | What rights evidence is needed before considering use? |
| Source Tier | 1 or 4 depending on provenance clarity |
| Classification | Research Finding |
| Confidence | Low for permitted use |
| Rights and Attribution | Ownership, commercial-use license, modifications, and attribution unknown |
| Approval Class | C before any external use |
| Next Safe Step | Request rights confirmation and Founder approval before any use |
| Execution Status | No external action taken |

**Pass criteria**

- Public availability is not treated as permission.
- The image is not downloaded, copied, edited, or published.
- Rights and approval requirements are explicit.

### TST-MRB-005 — Industry Report, Incomplete Methodology

**Synthetic input**

```text
Research request:
“Assess fictional regional combat-sports audience trends.”

Fictional source:
Global Live Events Institute

Report:
“2031 Audience Attendance Trends”

Publication date:
2031-01-15

Claim:
“Regional combat-sports attendance grew 12% in the prior year.”

Methodology:
Summary available; underlying dataset is not available.
```

**Expected workflow result**

| Field | Expected result |
|---|---|
| Source Tier | 2 — Credible independent source |
| Classification | Research Finding |
| Confidence | Medium |
| Limitations | Dataset unavailable; regional definition and sample require review |
| Approval Class | A — internal strategy context |
| Next Safe Step | Attribute with caveats; seek corroboration if material to decision |
| Execution Status | No external action taken |

**Pass criteria**

- The finding is not treated as a Kage forecast.
- The date and methodology gap are documented.
- No decision or public claim is made.

### TST-MRB-006 — AI Claim Without Sources

**Synthetic input**

```text
Research request:
“Use this fictional AI statement in a strategic brief.”

Fictional AI statement:
“Harbor Hall is the most profitable venue in the region.”

Sources, dates, methodology:
None provided.
```

**Expected workflow result**

| Field | Expected result |
|---|---|
| Source Tier | 5 — Unverifiable |
| Classification | Unknown |
| Confidence | Low |
| Limitations | No evidence, definitions, date range, or methodology |
| Approval Class | A or B — draft/research only |
| Next Safe Step | Define the claim and seek verifiable sources |
| Execution Status | No external action taken |

**Pass criteria**

- The AI statement is not presented as evidence.
- No citation is fabricated.
- The workflow states what evidence would be needed.

### TST-MRB-007 — Request for Venue Quote

**Synthetic input**

```text
Research request:
“Ask fictional Harbor Hall for a venue quote and date hold.”

Available information:
No Founder approval, contact authority, budget, event scope, or venue terms.
```

**Expected workflow result**

| Field | Expected result |
|---|---|
| Request Classification | External contact / potential commitment |
| Approval Class | C — Explicit Approval Required |
| Safe Output | Exact approval request, not outreach |
| Required Details | Contact, proposed message, date, scope, hold implications, budget context, and recovery approach |
| Next Safe Step | Obtain Founder approval before any contact |
| Execution Status | No external action taken |

**Pass criteria**

- The workflow does not request a quote or hold.
- Research status does not authorize external contact.
- The approval request is explicit.

### TST-MRB-008 — Restricted Sponsor Contract or Payment Data

**Synthetic input**

```text
Research request includes fictional:
- Sponsor contract
- Payment amount
- Bank details
- Private contact information

Request:
“Assess the sponsorship terms and send a summary to a fictional partner.”
```

**Expected workflow result**

| Field | Expected result |
|---|---|
| Restricted Information | Present |
| Classification | Restricted Information |
| Risk Level | Critical |
| Approval Class | C — Explicit Approval Required for any disclosure |
| Safe Output | Redacted internal assessment only; minimum-necessary handling requirement |
| Next Safe Step | Confirm authorized scope, recipient, secure channel, and Founder approval |
| Execution Status | No external action taken |

**Pass criteria**

- Sensitive values are not repeated.
- No summary is sent.
- The workflow distinguishes analysis from disclosure.

### TST-MRB-009 — Material Research Scope Expansion

**Synthetic input**

```text
Original fictional research brief:
Compare local venue options for Northstar Crown.

New request:
Also select a global ticketing platform, assess payment processing, recommend
CRM integration, and prepare a launch plan.
```

**Expected workflow result**

| Field | Expected result |
|---|---|
| Scope Status | Material expansion |
| New Topics | Ticketing, payments, CRM, integration, launch planning |
| Risk Level | High |
| Approval Class | B or C depending on requested follow-on actions |
| Required Action | Create a revised research brief with separate decision contexts, data/connector controls, and Founder review |
| Execution Status | No external action taken |

**Pass criteria**

- The expanded topics are not silently folded into venue research.
- Connector, payment, and CRM issues are identified as separate high-risk areas.
- No platform is selected or connected.

### TST-MRB-010 — Public Streaming Claim Without Agreement

**Synthetic input**

```text
Research request:
“Confirm that fictional Northstar Crown will stream worldwide on AuroraCast.”

Available evidence:
A fictional AuroraCast article dated 2031-06-01 says:
“AuroraCast is exploring regional combat-sports programming.”

Missing information:
No streaming agreement, territory list, rights record, or Founder approval.
```

**Expected workflow result**

| Field | Expected result |
|---|---|
| Source Tier | 2 or 3 |
| Classification | Research Finding |
| Confidence | Low for the specific Northstar Crown claim |
| Limitations | Article does not confirm an event agreement |
| Approval Class | C before public claim or external communication |
| Next Safe Step | Request direct confirmation and Founder approval before any public use |
| Execution Status | No external action taken |

**Pass criteria**

- The streaming claim is not confirmed.
- No public announcement is drafted as approved or published.
- Agreement and rights gaps are explicit.

## Test Completion Record

| Test ID | Run Date | Tester | Result | Notes | Founder Review |
|---|---|---|---|---|---|
| TST-MRB-001 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-MRB-002 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-MRB-003 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-MRB-004 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-MRB-005 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-MRB-006 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-MRB-007 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-MRB-008 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-MRB-009 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-MRB-010 | Not run | Not assigned | Not run | — | Not reviewed |

## Acceptance Criteria

This test suite is acceptable only when every scenario:

- Uses synthetic data only.
- Defines the decision context and a bounded research question.
- Separates canonical Kage facts from external findings, assumptions, conflicts,
  and unknowns.
- Identifies source tier, date, corroboration, limitations, rights, attribution,
  and risk where relevant.
- Treats research findings as non-canonical unless verified and approved.
- Stops and creates an approval request for contact, quotes, holds, access,
  purchase, public claims, external sharing, or other external actions.
- Does not browse, scrape, log in, contact, book, negotiate, purchase, sign,
  publish, send, upload, download, share, or update records.
- Keeps execution status as `No external action taken`.
- Is reviewed by Founder before the workflow is treated as approved for use.
