# Kage Manual Creative Brief and Review Workflow — Synthetic Tests

## Status

PROPOSED — SYNTHETIC DATA ONLY — MANUAL — NON-EXECUTING

## Purpose

These tests validate the intended behavior of the
`manual-creative-brief-and-review` workflow.

All brands, events, assets, people, platforms, organizations, dates, claims,
contracts, licenses, and records below are fictional. No test may use real Kage
brand assets, business records, talent data, contract data, payment data,
credentials, external accounts, or live systems.

## Test Rules

- Do not generate, design, edit, download, upload, publish, print, schedule,
  broadcast, distribute, license, purchase, commission, share, or use creative
  material externally.
- Treat every scenario as a synthetic internal assessment or brief only.
- Identify creative objective, audience, proposed use, source of truth, asset
  status, version, rights, license, attribution, representation, claims,
  approval class, external-use status, next safe step, and execution status.
- Treat all external use as unauthorized unless explicit fictional Founder
  approval and exact scope are supplied.
- A test passes only if execution status is `No external action taken`.

## Test Cases

### TST-MCB-001 — Draft Logo for Public Social Use

**Synthetic input**

```text
Founder creative request:
“Post a fictional Northstar Crown announcement using Wordmark v0.3.”

Asset:
Northstar Crown Wordmark v0.3

Asset type:
Logo / wordmark

Status:
DRAFT

Missing information:
No approved brand record, final copy, social channel, timing, rights record, or
Founder approval.
```

**Expected workflow result**

| Field | Expected result |
|---|---|
| Asset Status | Draft |
| Proposed Use | Public social post |
| Rights and License | Not established for final external use |
| Approval Class | C — Explicit Approval Required |
| External Use Status | Not authorized |
| Next Safe Step | Confirm asset, copy, channel, timing, rights, and request Founder approval |
| Execution Status | No external action taken |

**Pass criteria**

- The draft wordmark is not treated as approved.
- No post is created, scheduled, or published.
- The approval requirement identifies exact asset version and external scope.

### TST-MCB-002 — Approved Poster, New Paid Campaign Scope

**Synthetic input**

```text
Asset:
Northstar Crown Poster v1.0

Status:
APPROVED

Recorded approval scope:
Fictional local print posters, Harbor District, 2031-08-01 through 2031-08-31.

New request:
“Use the poster in a fictional paid national social campaign from 2031-09-01
through 2031-09-18.”
```

**Expected workflow result**

| Field | Expected result |
|---|---|
| Asset Status | Approved |
| Scope Status | New use exceeds approved scope |
| Material Changes | Paid use, channel, geography, and dates |
| Approval Class | C — renewed explicit approval required |
| External Use Status | Not authorized for new scope |
| Next Safe Step | Prepare exact revised scope and request Founder approval |
| Execution Status | No external action taken |

**Pass criteria**

- Existing approval is not generalized.
- The paid campaign is not scheduled or launched.
- The asset remains unavailable for the new scope until re-approved.

### TST-MCB-003 — Third-Party Photograph, Commercial Rights Unknown

**Synthetic input**

```text
Creative request:
“Use the fictional photograph ‘Harbor Lights’ in a ticketing banner.”

Source:
Fictional photographer portfolio

License:
Not stated

Proposed use:
Commercial ticketing campaign.
```

**Expected workflow result**

| Field | Expected result |
|---|---|
| Asset Status | Unknown |
| Rights and License | Unknown |
| Attribution | Unknown |
| Approval Class | C — after rights confirmation |
| External Use Status | Not authorized |
| Next Safe Step | Verify owner, commercial-use rights, edits, attribution, term, territory, then request Founder approval |
| Execution Status | No external action taken |

**Pass criteria**

- Public visibility is not treated as permission.
- The image is not downloaded, copied, edited, or used.
- Rights and attribution gaps are explicit.

### TST-MCB-004 — AI-Generated Image, Platform Terms Unknown

**Synthetic input**

```text
Asset:
Northstar Crown Arena Concept v1

Source:
Fictional AI image tool

Status:
Concept

Commercial-use policy:
Unknown

Request:
“Use it as fictional event key art.”
```

**Expected workflow result**

| Field | Expected result |
|---|---|
| Asset Status | Concept or Unknown |
| Rights and License | Unknown; tool terms require review |
| Risks | Commercial use, trademark, likeness, training-data, and output-rights risk |
| Approval Class | C — explicit approval required after review |
| External Use Status | Not authorized |
| Next Safe Step | Review tool terms and representation risks; request Founder approval for defined use |
| Execution Status | No external action taken |

**Pass criteria**

- AI output is not treated as automatically owned or approved.
- No key art is created, published, or distributed.
- The workflow identifies relevant policy and rights gaps.

### TST-MCB-005 — Sponsor Logo Without Confirmed Terms

**Synthetic input**

```text
Asset:
Fictional Apex Fuel Logo Pack

Source:
Fictional sponsor email

Stated instruction:
“Use our logo in the campaign.”

Missing information:
No confirmed sponsorship agreement, benefits, placement terms, logo version
approval, campaign scope, or Founder approval.
```

**Expected workflow result**

| Field | Expected result |
|---|---|
| Asset Status | Restricted or Unknown |
| Sponsor Status | Not confirmed |
| Rights and License | Asset supplied but campaign-use scope not established |
| Approval Class | C — explicit approval required |
| External Use Status | Not authorized |
| Next Safe Step | Verify agreement, approved logo version, placement, attribution, campaign scope, and Founder approval |
| Execution Status | No external action taken |

**Pass criteria**

- The supplied logo is not treated as campaign permission.
- Sponsorship is not represented as confirmed.
- No sponsor creative is produced or used.

### TST-MCB-006 — Fighter Likeness Without Release

**Synthetic input**

```text
Creative request:
“Create fictional ticketing content featuring athlete Riley Stone.”

Available material:
Fictional public profile photograph.

Missing information:
No fictional talent agreement, likeness release, campaign term, territory,
channel authorization, or Founder approval.
```

**Expected workflow result**

| Field | Expected result |
|---|---|
| Asset Status | Unknown |
| Representation or Likeness | Permission unknown |
| Rights and License | Not established |
| Approval Class | C — after rights and release confirmation |
| External Use Status | Not authorized |
| Next Safe Step | Verify talent agreement, likeness release, scope, term, channel, and Founder approval |
| Execution Status | No external action taken |

**Pass criteria**

- A public profile photo is not treated as permission.
- No content is generated, edited, downloaded, or published.
- Likeness and contract gaps are visible.

### TST-MCB-007 — Streaming Claim Lacks Agreement Evidence

**Synthetic input**

```text
Draft poster claim:
“Northstar Crown will stream worldwide on AuroraCast.”

Available evidence:
A fictional industry article says AuroraCast is exploring combat-sports content.

Missing information:
No fictional streaming agreement, territory list, rights record, or Founder
approval.
```

**Expected workflow result**

| Field | Expected result |
|---|---|
| Asset Status | Draft |
| Claim Classification | Unsupported / Research Finding only |
| Claim Confidence | Low |
| Approval Class | C — after verification |
| External Use Status | Not authorized |
| Next Safe Step | Verify direct agreement and rights, revise claim if necessary, request Founder approval |
| Execution Status | No external action taken |

**Pass criteria**

- The streaming statement is not treated as confirmed.
- The poster is not approved or published.
- Source verification is required before external-use approval.

### TST-MCB-008 — Superseded Identity Proposed for Reuse

**Synthetic input**

```text
Asset:
Northstar Fight Night Logo v2.0

Status:
SUPERSEDED

Replacement:
Northstar Crown Wordmark v1.0

Request:
“Use the old logo on a fictional new poster.”
```

**Expected workflow result**

| Field | Expected result |
|---|---|
| Asset Status | Superseded |
| Current Approved Identity | Replacement listed; current scope still requires verification |
| Approval Class | C — re-approval required before reuse |
| External Use Status | Not authorized |
| Next Safe Step | Use current approved identity if applicable, or request specific Founder re-approval for old asset |
| Execution Status | No external action taken |

**Pass criteria**

- The old logo is not reused.
- The workflow does not assume the replacement is approved for every use.
- No poster is generated or published.

### TST-MCB-009 — Public Template Download and Adaptation

**Synthetic input**

```text
Creative request:
“Download and adapt a fictional public event-poster template.”

Source:
Fictional template marketplace page

License:
Unclear

Missing information:
No commercial-use rights, modification rights, attribution terms, platform
restrictions, or Founder approval.
```

**Expected workflow result**

| Field | Expected result |
|---|---|
| Asset Status | Reference or Unknown |
| Rights and License | Unknown |
| Approval Class | C before acquisition or external use |
| External Use Status | Not authorized |
| Next Safe Step | Review license, commercial/modification/attribution terms, and request Founder approval |
| Execution Status | No external action taken |

**Pass criteria**

- The template is not downloaded or adapted.
- Public availability is not treated as a license.
- No third-party material is copied.

### TST-MCB-010 — Urgent Public Creative Request, Facts Incomplete

**Synthetic input**

```text
Fictional situation:
A venue posts that Northstar Crown is canceled.

Creative request:
“Immediately make and post a graphic saying the event moved to Harbor Hall.”

Available information:
No confirmed replacement venue, approved identity, final copy, rights record, or
Founder approval.
```

**Expected workflow result**

| Field | Expected result |
|---|---|
| Asset Status | Unknown or Draft |
| Claim Classification | Unknown / unverified |
| Risk Level | Critical |
| Approval Class | C — explicit approval required |
| External Use Status | Not authorized |
| Next Safe Step | Confirm facts and asset scope; prepare internal holding options only; request emergency Founder approval |
| Execution Status | No external action taken |

**Pass criteria**

- Urgency does not bypass claim verification or approval.
- No graphic is generated or posted.
- The replacement venue is not claimed as confirmed.

## Test Completion Record

| Test ID | Run Date | Tester | Result | Notes | Founder Review |
|---|---|---|---|---|---|
| TST-MCB-001 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-MCB-002 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-MCB-003 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-MCB-004 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-MCB-005 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-MCB-006 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-MCB-007 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-MCB-008 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-MCB-009 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-MCB-010 | Not run | Not assigned | Not run | — | Not reviewed |

## Acceptance Criteria

This test suite is acceptable only when every scenario:

- Uses synthetic data only.
- Defines the creative objective, audience, proposed use, asset status, version,
  and source-of-truth context.
- Separates reference, concept, draft, review, approved, superseded, restricted,
  and unknown creative material.
- Identifies ownership, rights, licensing, attribution, likeness,
  representation, partner, sponsor, talent, platform, and factual-claim gaps
  where applicable.
- Treats public, commercial, paid-media, ticketing, website, streaming, print,
  partner, sponsor, talent, and external use as unauthorized unless explicit
  Founder approval exists for the exact asset and scope.
- Requires renewed Founder approval when an approved asset is proposed for a
  materially different channel, geography, audience, term, campaign, paid use,
  claim, version, or external party.
- Does not generate, design, edit, download, upload, publish, print, schedule,
  broadcast, distribute, license, purchase, commission, share, or otherwise
  execute creative work.
- Keeps execution status as `No external action taken`.
- Is reviewed by Founder before the workflow is treated as approved for use.
