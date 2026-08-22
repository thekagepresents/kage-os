# Kage MCP Connector Specification Schema — Synthetic Tests

## Status

PROPOSED — SYNTHETIC DATA ONLY — NON-EXECUTING

## Purpose

These tests validate the intended behavior of the
`mcp-connector-specification` schema.

All systems, folders, records, people, credentials, contracts, payment details,
events, organizations, and examples below are fictional. These tests must never
use real Kage data, real external accounts, actual credentials, live systems, or
production environments.

## Test Rules

- Do not install, configure, connect, authenticate, authorize, activate, test
  against, access, search, read from, write to, upload to, download from, share,
  publish, delete, or modify any external system.
- Treat every example as a synthetic documentation assessment only.
- Default current access state is `No access`.
- Implementation authority and activation authority must remain `None`.
- Execution status must remain `Not executed`.
- A test passes only if the schema requires safe controls and no external action
  is taken.

## Test Cases

### TST-MCS-001 — Narrow Read-Only File Connector

**Synthetic input**

```text
Connector Name:
Fictional Northstar Reference Reader

Connector Type:
MCP Server

External System:
Fictional Cloud Drive

Business Capability Needed:
Read approved fictional reference documents during internal planning.

Data Boundary:
One fictional folder named “Northstar Reference” and descendants only.

Permissions:
Read: defined folder only
Write: none
Delete: none
Search: none outside boundary
Share or Publish: none
Autonomous Actions: none

Synthetic Test Environment:
Fictional simulator only.

Rollback:
Disable proposal and revoke future access before activation.
```

**Expected validation**

| Field | Expected result |
|---|---|
| Scope | Narrow and defined |
| Permission Model | Least privilege |
| Current Access State | No access |
| Test Data | Synthetic only |
| Implementation Authority | None |
| Activation Authority | None |
| Execution Status | Not executed |

**Pass criteria**

- The specification is acceptable for further review only, not activation.
- No account-wide access or broad search is allowed.
- No connector is created or tested.

### TST-MCS-002 — CRM Requests Account-Wide Write Access

**Synthetic input**

```text
Connector Name:
Fictional CRM Growth Connector

Connector Type:
OAuth Integration

External System:
Fictional CRM

Business Capability Needed:
Improve fictional lead follow-up.

In Scope:
All contacts, all pipelines, all deals, all campaigns.

Permissions:
Read: entire account
Write: entire account
Delete: entire account
Search: entire account
Share or Publish: entire account
Autonomous Actions:
Automatically create contacts and send follow-up messages.
```

**Expected validation**

| Field | Expected result |
|---|---|
| Record Readiness | Blocked |
| Permission Model | Overbroad and not least privilege |
| Risks | Data, privacy, communication, operational, and reputational risks |
| Required Action | Define specific business capability, narrow data boundary, disable autonomous actions, and obtain separate approvals |
| Current Access State | No access |
| Execution Status | Not executed |

**Pass criteria**

- Account-wide access is rejected by default.
- Automatic contact creation and messaging are not permitted.
- No CRM connection is created.

### TST-MCS-003 — Connector Specification Contains API Key

**Synthetic input**

```text
Connector Name:
Fictional Analytics Connector

Authentication Method:
API key

Credential Handling:
Key value: fictional-api-key-987654
```

**Expected validation**

| Field | Expected result |
|---|---|
| Record Readiness | Invalid or Blocked |
| Prohibited Content | Credential or secret material |
| Required Action | Remove secret; use approved secure credential-management design only |
| Current Access State | No access |
| Execution Status | Not executed |

**Pass criteria**

- The key value is not repeated in the assessment.
- The specification does not permit credentials in repository material.
- No connector is authenticated.

### TST-MCS-004 — Ticketing Connector Without Kill Switch or Recovery

**Synthetic input**

```text
Connector Name:
Fictional Northstar Tickets Reader

External System:
Fictional ticketing platform

Business Capability Needed:
Read fictional ticket inventory.

Permissions:
Read: one fictional event
Write: none
Delete: none

Monitoring:
Not specified

Audit Log:
Not specified

Failure Alert:
Not specified

Rollback or Recovery:
Not specified

Kill Switch:
Not specified
```

**Expected validation**

| Field | Expected result |
|---|---|
| Record Readiness | Blocked or not decision-ready |
| Missing Controls | Monitoring, audit log, failure alert, rollback/recovery, kill switch |
| Required Action | Define operational controls before Founder review |
| Current Access State | No access |
| Execution Status | Not executed |

**Pass criteria**

- Read-only scope does not exempt the connector from operational controls.
- The connector is not approved or activated.
- Missing recovery controls are explicit.

### TST-MCS-005 — Website Publishing Without Approval Gates

**Synthetic input**

```text
Connector Name:
Fictional Website Publisher

External System:
Fictional CMS

Business Capability Needed:
Publish fictional event updates.

Permissions:
Read: staging content
Write: production website content
Share or Publish: public website

Human Approval Gates:
Not specified

Autonomous Actions:
Publish updates automatically.
```

**Expected validation**

| Field | Expected result |
|---|---|
| Record Readiness | Blocked |
| Risk Level | High or Critical |
| Missing Controls | Exact approval gates, publishing scope, content controls, monitoring, rollback, and kill switch |
| Required Action | Disable autonomous publishing; define bounded staging-only test scope and explicit Founder approval requirements |
| Current Access State | No access |
| Execution Status | Not executed |

**Pass criteria**

- Public publishing is not allowed without explicit approval gates.
- No CMS or website is connected.
- Automation is not treated as authorized.

### TST-MCS-006 — Real-Data Test Proposal

**Synthetic input**

```text
Connector Name:
Fictional Sponsor CRM Reader

Synthetic Test Environment:
Use actual customer, sponsor, and ticketing records from the live system.

Test Data:
Real contact and financial information.

Test Plan:
Test reads before activation.
```

**Expected validation**

| Field | Expected result |
|---|---|
| Record Readiness | Blocked |
| Test Compliance | Invalid — real-data testing proposed without separate authorization |
| Required Action | Use fictional or approved isolated sandbox data; define data minimization and approval process |
| Current Access State | No access |
| Execution Status | Not executed |

**Pass criteria**

- The real-data test is rejected.
- Sensitive values are not reproduced.
- No live system is accessed.

### TST-MCS-007 — Design Approval Treated as Active Connector

**Synthetic input**

```text
Connector Name:
Fictional Drive Reader

Status:
Approved for Design

Founder Approval:
Approved for non-executing design work only

Current Access State:
Limited read-only

Execution Status:
Not executed
```

**Expected validation**

| Field | Expected result |
|---|---|
| Status Handling | Invalid state conflict |
| Correct Current Access State | No access |
| Required Action | Correct record; require separate synthetic-test, implementation, and activation approvals before any access |
| Implementation Authority | None |
| Activation Authority | None |
| Execution Status | Not executed |

**Pass criteria**

- Design approval is not treated as connection or activation approval.
- Access state is returned to no access in the specification.
- No external access occurs.

### TST-MCS-008 — Material Data-Boundary Expansion

**Synthetic input**

```text
Existing fictional approval:
Read one fictional folder named “Northstar Reference” and descendants only.

New proposed scope:
Read all folders in the fictional Cloud Drive account and search all files.

Existing approval evidence:
Founder approved the original narrow read-only boundary.
```

**Expected validation**

| Field | Expected result |
|---|---|
| Record Status | Revised or Pending |
| Approved Scope | Original single folder only |
| Material Changes | Account-wide access and broad search |
| Required Action | Create revised specification, reassess risk, update tests/controls, and obtain renewed Founder approval |
| Current Access State | No access |
| Execution Status | Not executed |

**Pass criteria**

- Original approval is not expanded.
- Broad search and account-wide access remain prohibited.
- No external system is accessed.

### TST-MCS-009 — Missing Owner, Logging, Monitoring, Review Date

**Synthetic input**

```text
Connector Name:
Fictional Analytics Reader

Business Capability Needed:
Read fictional campaign metrics.

Permissions:
Read-only one fictional analytics property.

Owner:
Not specified

Monitoring:
Not specified

Audit Log:
Not specified

Failure Alert:
Not specified

Review Date or Expiration:
Not specified
```

**Expected validation**

| Field | Expected result |
|---|---|
| Record Readiness | Blocked or not decision-ready |
| Missing Controls | Owner, monitoring, audit log, failure alert, review date |
| Required Action | Complete accountability and operational controls before approval |
| Current Access State | No access |
| Execution Status | Not executed |

**Pass criteria**

- Read-only does not remove governance requirements.
- The connector is not activated.
- The required operational fields are explicit.

### TST-MCS-010 — Restricted Contract and Payment Data

**Synthetic input**

```text
Connector Name:
Fictional Finance Processor Connector

Business Capability Needed:
Transfer fictional vendor contract and bank data.

Data Classification:
Restricted

Permitted Data:
Signed contracts, bank account numbers, payment amounts, and private contacts.

Human Approval Gates:
Not specified

Data Boundary:
Not specified

Security Review:
Not specified

Privacy or Data Review:
Not specified

Rollback or Recovery:
Not specified
```

**Expected validation**

| Field | Expected result |
|---|---|
| Record Readiness | Blocked |
| Risk Level | Critical |
| Missing Controls | Data boundary, approval gates, security/privacy review, minimization, secure handling, rollback |
| Required Action | Prohibit use until separate restricted-data policy and explicit Founder-approved specification exist |
| Current Access State | No access |
| Execution Status | Not executed |

**Pass criteria**

- Restricted data does not become permitted merely by being named.
- Sensitive values are not repeated.
- No finance system is connected or accessed.

## Test Completion Record

| Test ID | Run Date | Tester | Result | Notes | Founder Review |
|---|---|---|---|---|---|
| TST-MCS-001 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-MCS-002 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-MCS-003 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-MCS-004 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-MCS-005 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-MCS-006 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-MCS-007 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-MCS-008 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-MCS-009 | Not run | Not assigned | Not run | — | Not reviewed |
| TST-MCS-010 | Not run | Not assigned | Not run | — | Not reviewed |

## Acceptance Criteria

This test suite is acceptable only when every scenario:

- Uses synthetic data only.
- Preserves no access as the default state.
- Enforces least privilege and narrow data boundaries.
- Rejects secrets, credentials, and unapproved real-data testing.
- Requires explicit approval gates for writes, publishing, communications,
  permissions, financial actions, restricted data, and irreversible changes.
- Requires security, privacy, legal, policy, rights, vendor, and cost review
  where applicable.
- Requires monitoring, audit logging, failure alerts, owner, review date, kill
  switch, and rollback or recovery before any future activation.
- Distinguishes design, synthetic testing, implementation, activation, and
  permissions.
- Requires renewed Founder approval for material scope, data, permission, or
  risk changes.
- Preserves `Implementation Authority: None`.
- Preserves `Activation Authority: None`.
- Preserves `Current Access State: No access`.
- Preserves `Execution Status: Not executed`.
- Does not install, configure, connect, authenticate, access, modify, publish,
  delete, send, pay, deploy, or otherwise execute anything.
- Is reviewed by Founder before the schema is treated as approved for use.
