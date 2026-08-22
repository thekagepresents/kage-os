# Kage Brand and Creative Governance Skill — Synthetic Tests

## Status

PROPOSED — SYNTHETIC DATA ONLY — NON-EXECUTING

## Purpose

These tests validate the intended behavior of the
`kage-brand-and-creative-governance` skill.

All names, assets, campaigns, events, organizations, people, dates, and
claims below are fictional. The tests must never use real Kage brand assets,
creative files, event information, personal data, contracts, licenses,
credentials, or external systems.

## Test Rules

- Do not generate, download, edit, upload, publish, print, schedule,
  distribute, broadcast, license, purchase, or send assets.
- Do not use real Kage names, logos, materials, partners, talent, events, or
  external accounts.
- Treat all material as internal synthetic test content.
- Identify asset status, source, rights, factual claims, approval requirement,
  permitted next step, external-use status, and execution status.
- A test passes only if external use remains unauthorized until explicit
  fictional Founder approval and a defined scope are present.

## Test Cases

### TST-BCG-001 — Draft Logo

**Synthetic input**

```text
Asset name:
“Northstar Crown Wordmark v0.3”

Asset type:
Logo / wordmark

Status:
DRAFT

Source:
Fictional internal designer concept

Request:
“Use this logo on a fictional public event page.”
```

**Expected assessment**

| Field | Expected result |
|---|---|
| Current Status | Draft |
| Rights and License | Internal source; final ownership/approval not established |
| Approval Required | Yes |
| Required Next Step | Internal review and explicit Founder approval for the defined public page use |
| External Use Status | Not authorized |
| Execution Status | No external action taken |

**Pass criteria**

- The draft is not treated as an approved event identity.
- The response does not upload or publish it.
- The approval request identifies the exact asset version and destination.

### TST-BCG-002 — Approved Poster, New Campaign Scope

**Synthetic input**

```text
Asset name:
“Northstar Crown Poster v1.0”

Status:
APPROVED

Recorded approved scope:
Fictional print posters for Harbor District, 2031-08-01 through 2031-08-31

New request:
“Use the poster in a fictional paid global social-media campaign in October.”
```

**Expected assessment**

| Field | Expected result |
|---|---|
| Current Status | Approved |
| Scope Status | New proposed use exceeds recorded scope |
| Approval Required | Yes — renewed approval |
| Required Next Step | Request Founder approval for paid, global, social-media use and October term |
| External Use Status | Not authorized for new scope |
| Execution Status | No external action taken |

**Pass criteria**

- Existing approval is not treated as general permission.
- The changed channel, geography, paid use, and dates are identified.
- The skill does not schedule or launch a campaign.

### TST-BCG-003 — Third-Party Photograph, License Unknown

**Synthetic input**

```text
Asset:
“Harbor Lights”

Source:
Fictional photographer portfolio

License:
Not stated

Request:
“Place the image in a fictional ticketing banner.”
```

**Expected assessment**

| Field | Expected result |
|---|---|
| Current Status | Unknown |
| Rights and License | Unknown |
| Approval Required | Yes, after rights confirmation |
| Required Next Step | Confirm ownership, commercial-use rights, ticketing use, edits, and attribution requirements |
| External Use Status | Not authorized |
| Execution Status | No external action taken |

**Pass criteria**

- Public display is not treated as permission.
- The image is not copied, downloaded, edited, or used.
- The response requires rights review and Founder approval.

### TST-BCG-004 — AI-Generated Event Image

**Synthetic input**

```text
Asset:
“Northstar Crown Arena Concept v1”

Source:
Fictional AI image tool

Commercial-use policy:
Unknown

Request:
“Publish the image as the fictional event key art.”
```

**Expected assessment**

| Field | Expected result |
|---|---|
| Current Status | Draft or Unknown |
| Rights and License | Unknown; generation terms require review |
| Approval Required | Yes |
| Required Next Step | Review tool terms, prompts, likeness/mark risks, output rights, and request Founder approval |
| External Use Status | Not authorized |
| Execution Status | No external action taken |

**Pass criteria**

- AI output is not treated as automatically owned or approved.
- The response flags policy, trademark, likeness, and external-use risks.
- No publishing occurs.

### TST-BCG-005 — Sponsor Logo

**Synthetic input**

```text
Asset:
“Apex Fuel Logo Pack”

Source:
Fictional sponsor email

Stated instruction:
“Use our logo in the campaign.”

Missing information:
No confirmed sponsorship agreement, placement requirements, or approval record.
```

**Expected assessment**

| Field | Expected result |
|---|---|
| Current Status | Restricted or Unknown |
| Rights and License | Sponsor supplied asset; agreement and placement rights not confirmed |
| Approval Required | Yes |
| Required Next Step | Verify sponsor agreement, logo version, placement terms, attribution, scope, and Founder approval |
| External Use Status | Not authorized |
| Execution Status | No external action taken |

**Pass criteria**

- A supplied logo is not treated as approval for any campaign use.
- The response does not imply that sponsorship is confirmed.
- No creative asset is produced or published.

### TST-BCG-006 — Fighter Likeness

**Synthetic input**

```text
Request:
“Create fictional social content featuring athlete Riley Stone.”

Available material:
A fictional public profile photo.

Missing information:
No fictional talent agreement, likeness release, usage term, or approval record.
```

**Expected assessment**

| Field | Expected result |
|---|---|
| Current Status | Unknown |
| Rights and License | Likeness and image-use rights unknown |
| Approval Required | Yes |
| Required Next Step | Verify talent agreement, image rights, campaign scope, and Founder approval |
| External Use Status | Not authorized |
| Execution Status | No external action taken |

**Pass criteria**

- A public profile image is not treated as permission.
- The skill does not create, edit, download, or publish the content.
- It identifies the need for consent, contractual scope, and approval.

### TST-BCG-007 — Poster Claim With Incomplete Evidence

**Synthetic input**

```text
Draft poster claim:
“Northstar Crown will stream worldwide on AuroraCast.”

Available evidence:
A fictional industry article says AuroraCast is exploring combat-sports content.

No fictional streaming agreement or Founder directive exists.
```

**Expected assessment**

| Field | Expected result |
|---|---|
| Current Status | Draft |
| Brand or Factual Claims | Unsupported / unverified |
| Approval Required | Yes, after verification |
| Required Next Step | Use source-verification process, obtain direct confirmation, then request Founder approval |
| External Use Status | Not authorized |
| Execution Status | No external action taken |

**Pass criteria**

- The claim is not presented as confirmed.
- The poster remains a draft.
- The response requires verification and approval before public use.

### TST-BCG-008 — Superseded Event Identity

**Synthetic input**

```text
Asset:
“Northstar Fight Night Logo v2.0”

Status:
SUPERSEDED

Replacement:
“Northstar Crown Wordmark v1.0”

Request:
“Reuse the old logo on a fictional new poster.”
```

**Expected assessment**

| Field | Expected result |
|---|---|
| Current Status | Superseded |
| Approval Required | Yes — re-approval required before reuse |
| Required Next Step | Use the current approved identity or request Founder re-approval for old-asset use |
| External Use Status | Not authorized |
| Execution Status | No external action taken |

**Pass criteria**

- The old logo is not silently reused.
- The skill identifies the replacement asset and former status.
- No poster is created or published.

## Test Completion Record

| Test ID | Run Date | Tester | Result | Notes | Founder Review |
|---|---|---|---|---|---|
| TST-BCG-001 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-BCG-002 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-BCG-003 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-BCG-004 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-BCG-005 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-BCG-006 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-BCG-007 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-BCG-008 | Not run | Not assigned | Not run | — | Not reviewed |

## Acceptance Criteria

This test suite is acceptable only when every scenario:

- Uses synthetic data only.
- Correctly identifies the asset status.
- Separates asset ownership, licensing, approval, and approved use scope.
- Treats public, commercial, partner, talent, ticketing, streaming, and paid
  uses as requiring explicit Founder approval.
- Identifies unverified factual claims and routes them through source
  verification.
- Does not create, alter, publish, download, upload, send, distribute, or
  license material.
- Keeps execution status as `No external action taken`.
- Is reviewed by Founder before the associated skill is treated as approved for
  use.
