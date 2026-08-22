# Kage MCP Connector Specification Schema

## Status

PROPOSED — DOCUMENTATION ONLY — NON-EXECUTING

## Purpose

This schema defines the minimum information required before Kage Agency HQ may
consider a future MCP server, connector, integration, API client, webhook,
automation link, or other controlled doorway to an external system.

It is a planning and governance record only.

It does not create, install, configure, connect, authenticate, authorize, test
against, access, read from, write to, search, upload to, download from, or
modify any external system.

## Owner

Founder

## Governing Principle

External systems are controlled boundaries.

No connector, MCP server, integration, API client, webhook, automation link, or
external-system permission may be proposed as active unless its business need,
source of truth, data boundary, minimum permissions, security controls, owner,
cost, approval gate, test plan, monitoring, failure behavior, rollback method,
and Founder approval are explicitly defined.

A specification is not approval.

An approval is not implementation.

Implementation is not activation.

Activation is not permission for unrestricted access.

## Scope

Use this schema for proposed connections involving:

- Google Drive
- GitHub
- Website or CMS
- Hosting or DNS
- Ticketing
- Table or hospitality systems
- CRM
- Email
- SMS
- Social platforms
- Community platforms
- Analytics
- Paid media
- Streaming or broadcast platforms
- Finance or invoicing systems
- Databases
- Automation platforms
- Vendor portals
- Partner systems
- Internal tools
- APIs
- Webhooks
- MCP servers
- AI tools with external data access
- Any future external system

## Connector Status

| Status | Meaning |
|---|---|
| Idea | Need or system has been identified; no specification is complete |
| Draft | Specification is being prepared |
| Proposed | Specification is ready for Founder review |
| Approved for Design | Founder approved further non-executing design work only |
| Approved for Synthetic Test | Founder approved synthetic or sandbox testing only |
| Approved for Limited Implementation | Founder approved a defined implementation scope; activation remains separate |
| Approved for Limited Activation | Founder approved a defined, monitored, reversible live scope |
| Deferred | Proposal is postponed |
| Rejected | Proposal is not approved |
| Blocked | Required policy, review, evidence, ownership, access, test, or recovery control is absent |
| Deprecated | Connector should not be used for new work |
| Disabled | Connector is not active |
| Retired | Connector is permanently removed from approved use |

Unless a separate, current Founder approval explicitly says otherwise, connector
status is:

```text
Disabled
```

## Required Specification Format

Use this format for every connector proposal:

```text
Connector ID:
[Unique identifier / Pending]

Connector Name:
[Short descriptive name]

Connector Type:
[MCP Server / API Client / OAuth Integration / Service Account / Webhook /
Automation Link / Database Connection / File Connector / Other]

Status:
[Idea / Draft / Proposed / Approved for Design / Approved for Synthetic Test /
Approved for Limited Implementation / Approved for Limited Activation / Deferred /
Rejected / Blocked / Deprecated / Disabled / Retired]

External System:
[System name]

System Owner:
[Organization or account owner / To be confirmed]

Business Capability Needed:
[Specific business problem or outcome]

Purpose:
[Why Kage needs this connection]

In Scope:
[Exact permitted capabilities]

Out of Scope:
[Explicitly prohibited capabilities]

Source of Truth:
[Founder directive / canonical Kage record / GitHub engineering record / other
approved source]

Data Classification:
[None / Public / Internal / Restricted / Mixed]

Permitted Data:
[Minimum necessary data categories]

Prohibited Data:
[Secrets, credentials, payment data, personal data, contracts, or other prohibited categories]

Data Boundary:
[Exact folders, records, objects, accounts, projects, channels, tables, or
resources; never account-wide unless separately approved]

Data Residency or Location:
[Known / Unknown / Not applicable]

Read Permissions:
[None / exact read scope]

Write Permissions:
[None / exact write scope]

Delete Permissions:
[None / exact delete scope]

Search Permissions:
[None / exact search scope]

Share or Publish Permissions:
[None / exact share or publish scope]

Permission Model:
[Least privilege, role, token type, approval requirement, duration, renewal]

Authentication Method:
[OAuth / Service account / API key / Other / Not selected]

Credential Handling:
[No credentials stored in repository; approved secure method required]

Human Approval Gates:
[Actions requiring explicit Founder approval before execution]

Autonomous Actions:
[None unless separately approved]

External Parties Affected:
[None or named categories]

Financial Exposure:
[None / estimated / exact known cost]

Pricing and Billing Owner:
[To be confirmed / named approved owner]

Security Risks:
[Threats, misuse cases, access risks, supply-chain risks]

Privacy Risks:
[Data exposure, retention, sharing, identity, or sensitive-data risks]

Legal, Contract, or Policy Risks:
[Terms, licenses, regulatory, contract, platform-policy risks]

Brand or Reputational Risks:
[Public output, misrepresentation, partner, talent, or customer risk]

Operational Risks:
[Failure modes, dependency, outage, incorrect writes, duplicate actions]

Risk Level:
[Low / Medium / High / Critical]

Risk Mitigations:
[Controls, validations, restrictions, review]

Preconditions:
[Policies, records, approvals, accounts, rights, owners, sandbox, or other requirements]

Dependencies:
[Skills, workflows, schemas, systems, vendors, contracts, data, approvals]

Synthetic Test Environment:
[None / fictional simulator / sandbox / test account; must be approved]

Synthetic Test Plan:
[Test cases, expected behavior, failure cases, no-real-data rule]

Test Data:
[Synthetic only / approved sandbox data only / prohibited categories]

Test Success Criteria:
[Observable pass criteria]

Test Failure Behavior:
[Safe stop, no write, log, alert, revoke, or rollback behavior]

Security Review:
[Not required / Pending / Completed / Blocked]

Privacy or Data Review:
[Not required / Pending / Completed / Blocked]

Legal, Contract, or Policy Review:
[Not required / Pending / Completed / Blocked]

Vendor or Third-Party Review:
[Not required / Pending / Completed / Blocked]

License Review:
[Not required / Pending / Completed / Blocked]

Monitoring:
[None / proposed signals, logs, review cadence]

Audit Log:
[Required fields, storage location, retention policy / Pending]

Failure Alert:
[None / proposed recipient and condition]

Rate Limits and Quotas:
[Known / Unknown / Not applicable]

Cost Limits:
[None / proposed cap / approved cap]

Rollback or Recovery:
[Disable, revoke, rotate, restore, correct, contain, notify]

Kill Switch:
[How access is immediately disabled]

Owner:
[Named accountable owner / To be confirmed]

Support and Escalation:
[Owner, vendor contact policy, incident escalation path]

Review Date or Expiration:
[Date / condition / Not specified]

Founder Approval:
[Pending / Approved scope and evidence / Rejected / Deferred]

Approval Evidence:
[Approved record location / Pending]

Implementation Authority:
[None / separate approved scope]

Activation Authority:
[None / separate approved scope]

Current Access State:
[No access / Sandbox only / Limited read-only / Limited write / Other]

Execution Status:
[Not executed]

Changelog Entry:
[Path or version reference / Pending]

Notes:
[Non-sensitive additional context]
```

## Minimum Permission Rules

Every connector proposal must follow least privilege.

Default permission posture:

```text
Read: None
Write: None
Delete: None
Search: None
Share or Publish: None
Autonomous Actions: None
Current Access State: No access
Execution Status: Not executed
```

Permissions may be proposed only when each permission is:

1. Necessary for a defined business capability.
2. Limited to a defined data boundary.
3. Approved by Founder.
4. Tested safely using synthetic or approved sandbox data.
5. Logged and reviewable.
6. Reversible through a documented kill switch or recovery method.

Account-wide access, broad search, unrestricted write access, delete access,
public publishing, permission changes, financial actions, credential access, or
autonomous external actions are prohibited unless separately justified,
reviewed, tested, and explicitly approved by Founder.

## Data-Boundary Rules

A connector specification must identify the narrowest permitted boundary.

Examples:

```text
Google Drive:
One approved folder and its descendants only

GitHub:
One approved private repository only

Ticketing:
One approved event record only

CRM:
One approved pipeline or object group only

Website CMS:
One approved staging site only

Analytics:
One approved property with read-only metrics only
```

Do not state:

```text
All Drive files
Entire account
All repositories
All contacts
All events
All website content
Any available data
```

unless an exceptional approval explicitly defines the need, risk, controls,
duration, and rollback.

## Authentication and Credential Rules

- Never place credentials, tokens, API keys, passwords, cookies, recovery codes,
  private keys, client secrets, connection strings, or secret configuration in
  this repository.
- Never place credential values in a connector specification, test, issue,
  changelog, commit message, screenshot, or documentation example.
- Use an approved secure credential-management method only after separate
  Founder approval.
- Prefer revocable, scoped, time-limited authentication.
- Identify token ownership, rotation, revocation, expiry, and incident response
  before implementation.
- Do not use personal accounts, shared credentials, or unmanaged service
  accounts by default.
- Authentication method remains `Not selected` until the design is approved.

## Approval-Gate Rules

A connector must require explicit Founder approval before any action that:

- Writes, edits, deletes, moves, uploads, downloads, shares, or publishes data
- Sends communications or represents Kage externally
- Creates or changes tickets, events, inventory, prices, customers, contacts,
  campaigns, finances, contracts, access, or public content
- Uses restricted information
- Creates financial, legal, brand, privacy, security, customer, talent, partner,
  vendor, or reputational exposure
- Changes permissions, account settings, system configuration, DNS, hosting,
  code, automation, deployment, or external connections

The connector itself must not treat a prior general approval as permission for a
new material action.

## Testing Rules

Before any live implementation or activation is considered:

1. A complete specification must exist.
2. Founder must approve the test scope.
3. Tests must use synthetic data or an approved isolated sandbox.
4. Tests must avoid real Kage business data, personal data, payment data,
   contracts, credentials, or production systems unless separately approved.
5. Expected success and failure behavior must be documented.
6. Write, delete, publish, payment, communication, permission, and irreversible
   paths must remain disabled unless each is separately approved for a test.
7. Test results must be recorded.
8. Security, privacy, legal, rights, and vendor reviews must be completed where
   applicable.
9. Rollback, kill switch, logging, monitoring, and ownership must be validated.

A successful synthetic test is not approval for production access.

## Implementation and Activation Rules

Implementation requires a separate explicit Founder decision after the
specification and required reviews are complete.

Activation requires another separate explicit Founder decision after
implementation and approved testing are complete.

Before activation, verify:

- Exact data boundary
- Minimum permissions
- Authentication and credential controls
- Approval gates
- Monitoring and audit logging
- Failure alerts
- Kill switch
- Rollback or recovery
- Owner and support path
- Cost limits
- Review date
- No unapproved data categories
- No hidden autonomous actions

Default implementation and activation state:

```text
Implementation Authority: None
Activation Authority: None
Current Access State: No access
Execution Status: Not executed
```

## Prohibited Content and Practices

Never:

- Store or display secrets or credential values.
- Use real personal, financial, contract, customer, talent, sponsor, vendor,
  partner, attendee, or operational data in a connector specification or
  synthetic test.
- Connect to an external system based on a draft or general request.
- Request account-wide access by default.
- Enable write, delete, publish, payment, communication, permission, or
  autonomous actions without exact approval.
- Bypass platform terms, access controls, rate limits, paywalls, or legal
  restrictions.
- Use unreviewed third-party code, MCP servers, packages, connectors, or vendor
  tools.
- Treat implementation as activation or activation as unrestricted permission.
- Claim a connector is connected, tested, secure, compliant, or active without
  recorded evidence.
- Leave a connector active without an owner, monitoring, audit log, kill switch,
  review date, and recovery plan.

## Example Synthetic Specification

```text
Connector ID:
CONN-2031-001

Connector Name:
Fictional Drive Read-Only Reference Connector

Connector Type:
MCP Server

Status:
Proposed

External System:
Fictional Cloud Drive

System Owner:
To be confirmed

Business Capability Needed:
Review approved fictional reference documents during internal planning.

Purpose:
Allow limited read-only retrieval from one fictional project folder.

In Scope:
Read a single approved fictional project folder and descendants.

Out of Scope:
Account-wide search, writes, uploads, downloads, sharing, deletion, permissions,
external communication, and autonomous actions.

Source of Truth:
Fictional Founder directive in approved test context.

Data Classification:
Internal

Permitted Data:
Fictional non-sensitive reference documents only.

Prohibited Data:
Credentials, payment data, contracts, personal data, and all real Kage data.

Data Boundary:
Fictional folder `Northstar Reference` and descendants only.

Read Permissions:
Proposed: Read files in defined boundary only.

Write Permissions:
None

Delete Permissions:
None

Search Permissions:
None outside defined boundary.

Share or Publish Permissions:
None

Permission Model:
Least privilege; read-only; Founder approval required before each future access
phase.

Authentication Method:
Not selected

Credential Handling:
No credentials stored in repository; approved secure method required.

Human Approval Gates:
Any change to boundary, search scope, data class, or permission.

Autonomous Actions:
None

External Parties Affected:
None

Financial Exposure:
None known

Pricing and Billing Owner:
To be confirmed

Security Risks:
Overbroad file access.

Privacy Risks:
Unexpected restricted material in folder.

Legal, Contract, or Policy Risks:
Cloud-drive terms require review.

Brand or Reputational Risks:
Incorrect use of unreleased reference material.

Operational Risks:
Stale or incomplete document retrieval.

Risk Level:
Medium

Risk Mitigations:
Defined folder boundary; read-only; no search; no write; synthetic test first;
Founder approval gate.

Preconditions:
Folder classification, Founder approval, security review, sandbox plan.

Dependencies:
Source-of-truth skill, governance skill, synthetic tests.

Synthetic Test Environment:
Fictional simulator only.

Synthetic Test Plan:
Verify boundary enforcement, read-only behavior, restricted-data stop, and kill
switch behavior using fictional files.

Test Data:
Synthetic only.

Test Success Criteria:
Only fictional approved-boundary files are readable; all writes and broad search
are blocked.

Test Failure Behavior:
Stop; log proposed failure; retain no data; no external action.

Security Review:
Pending

Privacy or Data Review:
Pending

Legal, Contract, or Policy Review:
Pending

Vendor or Third-Party Review:
Pending

License Review:
Not required

Monitoring:
Proposed access-attempt log only.

Audit Log:
Pending.

Failure Alert:
Pending.

Rate Limits and Quotas:
Unknown.

Cost Limits:
None.

Rollback or Recovery:
Disable connector proposal and revoke future access before any activation.

Kill Switch:
No live access exists; mark proposal disabled.

Owner:
To be confirmed

Support and Escalation:
Founder review required.

Review Date or Expiration:
Not specified

Founder Approval:
Pending

Approval Evidence:
Pending

Implementation Authority:
None

Activation Authority:
None

Current Access State:
No access

Execution Status:
Not executed

Changelog Entry:
Pending

Notes:
Synthetic example only.
```

## Validation Checklist

Before a connector specification is ready for Founder review, confirm:

- Business capability and purpose are specific.
- In-scope and out-of-scope capabilities are explicit.
- Source of truth and owner are identified.
- Data classification, permitted data, prohibited data, and narrow data boundary
  are defined.
- Read, write, delete, search, share, publish, and autonomous permissions are
  individually stated.
- Authentication and credential handling do not expose secrets.
- Human approval gates are documented.
- Risks and mitigations cover security, privacy, legal, rights, brand,
  operations, cost, and vendors where applicable.
- Preconditions, dependencies, test environment, test plan, success criteria,
  and failure behavior are complete.
- Required reviews are marked accurately.
- Monitoring, audit log, alerting, kill switch, rollback, owner, support path,
  cost limits, and review date are identified.
- Implementation authority and activation authority are `None`.
- Current access state is `No access`.
- Execution status is `Not executed`.

## Dependencies

- `ARCHITECTURE.md`
- `SECURITY.md`
- `CONTRIBUTING.md`
- `CHANGELOG.md`
- `schemas/engineering-decision-log/SCHEMA.md`
- `agents/founder-command/AGENT.md`
- `workflows/manual-intake-and-triage/WORKFLOW.md`
- `workflows/manual-approval-record/WORKFLOW.md`
- All approved Kage skill specifications

## Testing

Test this schema using synthetic connector specifications only.

Minimum synthetic test cases:

1. A fictional read-only file connector with a narrow folder boundary.
2. A fictional CRM connector requesting account-wide write access.
3. A fictional connector specification containing a credential or API key.
4. A fictional ticketing connector with no rollback or kill switch.
5. A fictional website connector with public publishing proposed without approval
   gates.
6. A fictional connector with real-data testing proposed instead of sandbox data.
7. A fictional connector approved for design but incorrectly treated as active.
8. A fictional connector with a material data-boundary expansion after approval.
9. A fictional connector without an owner, audit log, monitoring, or review date.
10. A fictional connector request involving restricted contract or payment data.

Expected behavior:

- Enforces narrow scope and least privilege.
- Rejects secret material and real-data testing without separate authorization.
- Requires data boundaries, approvals, reviews, tests, monitoring, kill switch,
  rollback, owner, and cost controls.
- Distinguishes proposal, design, testing, implementation, activation, and
  permission.
- Requires renewed approval for material scope or permission changes.
- Preserves no access and no execution by default.

## Change Control

Changes require:

1. Founder approval
2. Security, privacy, legal, policy, rights, and vendor review where applicable
3. Updated changelog entry
4. Synthetic-data validation
5. Confirmation that the schema remains documentation-only and non-executing
   unless separately approved
