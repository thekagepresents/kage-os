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
|
