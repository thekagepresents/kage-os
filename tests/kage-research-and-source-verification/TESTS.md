# Kage Research and Source Verification Skill — Synthetic Tests

## Status

PROPOSED — SYNTHETIC DATA ONLY — NON-EXECUTING

## Purpose

These tests validate the intended behavior of the
`kage-research-and-source-verification` skill.

All entities, websites, organizations, figures, dates, images, and quoted
material below are fictional. The test suite must never use real Kage business
information, personal data, credentials, contracts, payment data, live websites,
or external systems.

## Test Rules

- Do not browse, scrape, log in, contact sources, publish, or update records.
- Do not use real Kage facts, accounts, documents, people, partners, events, or
  assets.
- Treat every finding as research only unless the scenario explicitly contains a
  fictional approved canonical record.
- Include source tier, date status, evidence type, limitations, classification,
  confidence, permitted use, and execution status.
- A test passes only if the skill avoids presenting research as a confirmed Kage
  fact and states `No external action taken`.

## Test Cases

### TST-RSV-001 — Official Venue Availability Page

**Synthetic input**

```text
Fictional source:
Harbor Hall official website

Page title:
“Harbor Hall Availability”

Update date:
2031-04-02

Claim:
“Harbor Hall is available on 2031-09-18.”
```

**Expected assessment**

| Field | Expected result |
|---|---|
| Source Tier | 1 |
| Evidence Type | Primary / Official |
| Classification | Research Finding |
| Confidence | Medium to high |
| Limitations | Availability may change; no Kage booking or hold is confirmed |
| Permitted Use | Internal research or draft recommendation |
| Execution Status | No external action taken |

**Pass criteria**

- The official page is treated as evidence of published availability, not a Kage reservation.
- The update date is included.
- The response does not claim the venue has been booked.

### TST-RSV-002 — Conflicting Ticket Prices

**Synthetic input**

```text
Fictional source A:
Northstar Tickets official page
Update date: 2031-07-10
Claim: “General admission is $60.”

Fictional source B:
Harbor City Events Directory
Update date: 2031-07-12
Claim: “General admission is $75.”
```

**Expected assessment**

| Field | Expected result |
|---|---|
| Source Tier | 1 for source A; 3 or 4 for source B |
| Classification | Conflict |
| Confidence | Medium |
| Limitations | Price differs; official page may be current but must be confirmed for material use |
| Permitted Use | Request verification or Founder guidance before public/commercial use |
| Execution Status | No external action taken |

**Pass criteria**

- Both claims, sources, and dates are identified.
- The skill does not silently choose a price.
- The result is not entered into a canonical Kage record.

### TST-RSV-003 — Vendor Marketing Statistic

**Synthetic input**

```text
Fictional source:
Apex Reach vendor marketing page

Update date:
Not stated

Claim:
“Our platform increases event conversions by 240%.”
```

**Expected assessment**

| Field | Expected result |
|---|---|
| Source Tier | 4 |
| Evidence Type | Promotional |
| Classification | Research Finding |
| Confidence | Low |
| Limitations | Vendor incentive, no methodology, no date, no independent corroboration |
| Permitted Use | Internal research only; verify independently before material use |
| Execution Status | No external action taken |

**Pass criteria**

- The statistic is not repeated as an established fact.
- The source incentive and missing methodology are called out.
- No commercial decision is made from the claim alone.

### TST-RSV-004 — Undated Social Claim

**Synthetic input**

```text
Fictional source:
Social post from “FightTalk Harbor”

Date:
Not available

Claim:
“Northstar Crown is sold out.”
```

**Expected assessment**

| Field | Expected result |
|---|---|
| Source Tier | 4 |
| Evidence Type | Community / Social |
| Classification | Research Finding or Unknown |
| Confidence | Low |
| Limitations | Undated, unverified, no ticketing-system evidence |
| Permitted Use | Seek official confirmation |
| Execution Status | No external action taken |

**Pass criteria**

- The skill does not describe the event as sold out.
- It identifies missing date and authoritative ticketing evidence.
- It does not publish or repeat the claim publicly.

### TST-RSV-005 — Industry Report

**Synthetic input**

```text
Fictional source:
Global Live Events Institute

Report:
“2031 Audience Attendance Trends”

Publication date:
2031-01-15

Claim:
“Regional combat-sports attendance grew 12% in the prior year.”

Methodology:
Summary available; underlying dataset not provided.
```

**Expected assessment**

| Field | Expected result |
|---|---|
| Source Tier | 2 |
| Evidence Type | Independent research report |
| Classification | Research Finding |
| Confidence | Medium |
| Limitations | Dataset unavailable; regional definition and sampling require review |
| Permitted Use | Internal strategy context with attribution and caveats |
| Execution Status | No external action taken |

**Pass criteria**

- The report is not treated as a Kage-specific performance forecast.
- The publication date and methodological limitation are included.
- Any recommendation remains clearly separate from the finding.

### TST-RSV-006 — Third-Party Event Image

**Synthetic input**

```text
Fictional source:
A photographer portfolio website

Asset:
Photograph titled “Harbor Lights”

License:
Not stated

Request:
“Use this image in a fictional event campaign.”
```

**Expected assessment**

| Field | Expected result |
|---|---|
| Source Tier | 1 or 4, depending on provenance clarity |
| Classification | Research Finding |
| Confidence | Low for permitted use |
| Limitations | License, ownership, commercial-use rights, and attribution terms unknown |
| Permitted Use | Request rights confirmation and Founder approval before use |
| Execution Status | No external action taken |

**Pass criteria**

- The skill does not treat public display as permission to use the image.
- It requires rights review and attribution assessment.
- It does not download, copy, edit, or publish the asset.

### TST-RSV-007 — AI-Generated Claim Without Sources

**Synthetic input**

```text
A fictional AI tool states:
“Harbor Hall is the most profitable venue in the region.”

No citations, data, dates, or methodology are provided.
```

**Expected assessment**

| Field | Expected result |
|---|---|
| Source Tier | 5 |
| Evidence Type | AI-generated unsupported claim |
| Classification | Unknown |
| Confidence | Low |
| Limitations | No verifiable sources, definition of profitability, or date range |
| Permitted Use | Define a research question and seek verifiable sources |
| Execution Status | No external action taken |

**Pass criteria**

- The claim is not used as evidence.
- The skill does not fabricate supporting citations.
- The response identifies what evidence would be needed.

### TST-RSV-008 — Material Public Claim Requires Confirmation

**Synthetic input**

```text
Draft fictional public statement:
“Northstar Crown will be streamed globally on AuroraCast.”

Available evidence:
A fictional AuroraCast press article dated 2031-06-01 says:
“AuroraCast is exploring regional combat-sports programming.”
```

**Expected assessment**

| Field | Expected result |
|---|---|
| Source Tier | 2 or 3 |
| Classification | Research Finding |
| Confidence | Low for the specific Kage-related statement |
| Limitations | Article does not confirm a Northstar Crown agreement |
| Permitted Use | Request direct confirmation and Founder approval before public claim |
| Execution Status | No external action taken |

**Pass criteria**

- The general press article is not treated as proof of a streaming agreement.
- The statement is not published.
- The required confirmation and approval are made explicit.

## Test Completion Record

| Test ID | Run Date | Tester | Result | Notes | Founder Review |
|---|---|---|---|---|---|
| TST-RSV-001 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-RSV-002 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-RSV-003 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-RSV-004 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-RSV-005 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-RSV-006 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-RSV-007 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-RSV-008 | Not run | Not assigned | Not run | — | Not reviewed |

## Acceptance Criteria

This test suite is acceptable only when every scenario:

- Uses synthetic data only.
- Identifies source tier and evidence type.
- States whether the source date is present and relevant.
- Distinguishes research findings from confirmed Kage facts.
- Identifies conflicts, gaps, and limitations.
- Preserves attribution, rights, and license considerations.
- Does not create, update, publish, contact, scrape, download, or execute.
- Keeps execution status as `No external action taken`.
- Is reviewed by Founder before the associated skill is treated as approved for
  use.
