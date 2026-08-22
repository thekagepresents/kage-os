# Kage Engineering Decision Log Schema

## Status

PROPOSED — DOCUMENTATION ONLY — NON-EXECUTING

## Purpose

This schema defines the required structure for recording material engineering
decisions in the Kage Agency HQ GitHub repository.

It applies to decisions about:

- Repository governance
- Security controls
- Skills
- Agents
- Workflows
- MCP specifications
- Connector specifications
- Schemas
- Synthetic tests
- Technical documentation
- Code proposals
- Automation proposals
- Integration proposals
- Data-model proposals
- Architecture changes
- Deployment or infrastructure proposals

It does not record Kage business decisions, event decisions, commercial terms,
financial decisions, contracts, customer data, talent data, sponsor data,
personal data, credentials, payment details, or operational production records.

## Owner

Founder

## Record Status

| Status | Meaning |
|---|---|
| Draft | Record is being prepared and is not approved |
| Proposed | Decision is ready for Founder review |
| Approved | Founder approved the exact recorded engineering decision |
| Approved With Conditions | Founder approved subject to stated conditions |
| Rejected | Founder declined the proposed decision |
| Revised | Material scope changed; new or updated decision record required |
| Deferred | Founder postponed the decision |
| Blocked | Required evidence, policy, review, dependency, or authorization is absent |
| Superseded | Replaced by a later approved decision |
| Archived | Historical record retained without current authority |

A status of `Approved` or `Approved With Conditions` does not itself authorize
execution. Separate execution approval and a separately authorized mechanism are
required where applicable.

## Required Record Format

Use this format for each engineering decision record:

```text
Decision ID:
[Unique identifier]

Title:
[Short decision title]

Record Status:
[Draft / Proposed / Approved / Approved With Conditions / Rejected / Revised /
Deferred / Blocked / Superseded / Archived]

Decision Date:
[YYYY-MM-DD / Pending]

Decision Owner:
[Founder]

Engineering Area:
[Governance / Security / Skill / Agent / Workflow / MCP / Connector / Schema /
Test / Documentation / Code / Automation / Integration / Data Model /
Architecture / Infrastructure / Other]

Related Repository Paths:
[Relevant repository files or folders]

Purpose:
[Why this decision is needed]

Problem or Opportunity:
[Engineering issue being addressed]

Context:
[Relevant background and constraints]

Source of Truth:
[Founder directive / GitHub repository record / approved Kage context / other
approved source]

Confirmed Facts:
[Source-backed engineering facts only]

Assumptions:
[Explicit unverified assumptions]

Options Considered:
[Option A / Option B / Option C / not applicable]

Recommendation:
[Proposed decision and rationale]

Founder Decision:
[Approved / Approved With Conditions / Rejected / Revised / Deferred / Pending /
Invalid / Blocked]

Approved Scope:
[Exact included scope / Not approved]

Excluded Scope:
[Explicit exclusions]

Conditions:
[Required limits, prerequisites, reviews, or controls]

Risk Level:
[Low / Medium / High / Critical]

Risks:
[Security, privacy, cost, reliability, legal, license, vendor, maintenance,
data, access, operational, or other risk]

Dependencies:
[Required records, skills, approvals, owners, systems, data, tests, or reviews]

Security Review:
[Not required / Pending / Completed / Blocked]

Privacy or Data Review:
[Not required / Pending / Completed / Blocked]

License or Rights Review:
[Not required / Pending / Completed / Blocked]

Synthetic Test Requirement:
[Not required / Required / Pending / Passed / Failed]

Test Evidence:
[Path to synthetic test specification or result record / none]

Rollback or Recovery:
[How a future approved implementation could be reversed, corrected, disabled,
or contained]

Owner:
[Named accountable owner / To be confirmed]

Review Date or Expiration:
[Date / condition / Not specified]

Approval Evidence:
[Founder approval record location / Pending]

Execution Authority:
[None — decision record only]

Execution Status:
[Not executed]

Changelog Entry:
[Path or version reference / Pending]

Supersedes:
[Prior Decision ID / none]

Superseded By:
[Later Decision ID / none]

Notes:
[Additional non-sensitive context]
```

## Field Rules

### Decision ID

Use an identifier in this format:

```text
ENG-YYYY-NNN
```

Example:

```text
ENG-2026-001
```

Do not create a Decision ID until a record is actually being entered into an
approved decision-log location.

### Title

Use a concise, specific title.

Good:

```text
Adopt manual approval-record workflow specification
```

Avoid:

```text
Workflow decision
```

### Engineering Area

Select the most relevant category. If more than one applies, list a primary area
followed by secondary areas.

Example:

```text
Primary: Workflow
Secondary: Governance, Security
```

### Related Repository Paths

List only paths in this private engineering repository.

Examples:

```text
workflows/manual-approval-record/WORKFLOW.md
tests/manual-approval-record/TESTS.md
```

Do not use this field for Google Drive, external systems, credentials, live
customer records, or production data.

### Confirmed Facts and Assumptions

- Put only source-backed engineering facts under `Confirmed Facts`.
- Put all unverified reasoning, estimates, and expectations under `Assumptions`.
- Do not present assumptions as facts.
- Do not include business facts unless strictly necessary to define an
  engineering constraint and approved for minimum-necessary handling.

### Options Considered

For material decisions, identify viable alternatives and why they were not
selected.

For low-impact documentation corrections, state:

```text
Not applicable — documentation correction only
```

### Recommendation and Founder Decision

- A recommendation is not a Founder decision.
- Do not mark a decision approved without explicit Founder evidence.
- If Founder changes scope materially, set status to `Revised` and create an
  updated record.
- If the decision is unclear, use `Pending`, `Invalid`, or `Blocked`.

### Risk and Reviews

A decision involving code, automation, integrations, connectors, MCP, external
systems, data, credentials, access, privacy, security, cost, licensing,
deployment, or third-party dependencies must identify applicable risks and
reviews.

Do not mark a review completed without evidence.

### Synthetic Tests

Synthetic-data validation is required before any skill, agent, workflow,
connector, automation, schema, code, or integration proposal is treated as ready
for approval or future implementation.

Tests must:

- Use fictional data only.
- Avoid secrets, credentials, personal data, financial data, contracts, and
  production records.
- Include expected safe failure behavior.
- State that no external action occurs.
- Be stored under `tests/` or another Founder-approved engineering test location.

### Rollback or Recovery

For a non-executing documentation decision, state:

```text
Revert documentation change through a Founder-approved repository update.
```

For future implementation proposals, define the intended disablement, revocation,
restoration, correction, or recovery approach before approval.

### Execution Authority and Status

Every engineering decision record must state:

```text
Execution Authority:
None — decision record only

Execution Status:
Not executed
```

unless a separate, explicit, current Founder-approved execution mechanism exists
and is documented in an approved future policy.

This schema does not create execution authority.

## Restricted Content Prohibition

Never place the following in an engineering decision record:

- Passwords, API keys, tokens, cookies, recovery codes, secrets, or credentials
- Payment details, bank details, tax data, or private financial information
- Contracts, signatures, legal advice, or private legal materials
- Personal, health, customer, attendee, talent, sponsor, vendor, or partner data
- Raw exports from Google Drive or external systems
- Live production configuration values
- Private account identifiers not required for the engineering decision
- Unapproved third-party code or proprietary material

Use references to approved, access-controlled canonical records only when
necessary and authorized.

## Example Synthetic Record

```text
Decision ID:
ENG-2031-001

Title:
Adopt fictional manual intake workflow specification

Record Status:
Proposed

Decision Date:
2031-04-01

Decision Owner:
Founder

Engineering Area:
Primary: Workflow
Secondary: Governance

Related Repository Paths:
workflows/fictional-manual-intake/WORKFLOW.md
tests/fictional-manual-intake/TESTS.md

Purpose:
Define a safe fictional intake process for internal requests.

Problem or Opportunity:
Fictional requests need consistent classification and approval handling.

Context:
Foundation-build environment with no external execution.

Source of Truth:
Fictional Founder directive recorded in an approved test context.

Confirmed Facts:
The workflow and synthetic test specification exist.

Assumptions:
Founder may later review the workflow for approval.

Options Considered:
Option A: Manual workflow specification
Option B: Automated intake system

Recommendation:
Adopt Option A during foundation build because it has no external execution.

Founder Decision:
Pending

Approved Scope:
Not approved

Excluded Scope:
Automation, external systems, records, notifications, and execution.

Conditions:
Synthetic tests must be reviewed before approval.

Risk Level:
Low

Risks:
Workflow may be incomplete; no external operational risk because it is
non-executing.

Dependencies:
Founder review; synthetic tests.

Security Review:
Not required

Privacy or Data Review:
Not required

License or Rights Review:
Not required

Synthetic Test Requirement:
Required

Test Evidence:
tests/fictional-manual-intake/TESTS.md

Rollback or Recovery:
Revert documentation change through a Founder-approved repository update.

Owner:
To be confirmed

Review Date or Expiration:
Not specified

Approval Evidence:
Pending

Execution Authority:
None — decision record only

Execution Status:
Not executed

Changelog Entry:
Pending

Supersedes:
none

Superseded By:
none

Notes:
Synthetic example only.
```

## Validation Checklist

Before a record is considered ready for Founder review, confirm:

- Decision title and engineering area are clear.
- Repository paths are correct and limited to engineering material.
- Purpose, problem, context, and recommendation are present.
- Confirmed facts are separated from assumptions.
- Risks, dependencies, reviews, and test requirements are identified.
- Approval evidence is present or clearly marked pending.
- Scope and exclusions are explicit.
- No secrets, personal data, business operational records, financial details,
  contracts, or production configuration are included.
- Rollback or recovery is documented.
- Execution authority is `None`.
- Execution status is `Not executed`.

## Dependencies

- `ARCHITECTURE.md`
- `SECURITY.md`
- `CONTRIBUTING.md`
- `CHANGELOG.md`
- `agents/founder-command/AGENT.md`
- `workflows/manual-intake-and-triage/WORKFLOW.md`
- `workflows/manual-approval-record/WORKFLOW.md`
- All approved Kage skill specifications

## Testing

Test this schema using synthetic decision records only.

Minimum synthetic test cases:

1. A fictional proposed workflow decision with complete fields.
2. A fictional automation decision missing a security review and rollback plan.
3. A fictional connector decision containing prohibited credential material.
4. A fictional approved decision whose scope later expands.
5. A fictional decision with contradictory Founder instructions.
6. A fictional documentation-only correction with no options required.
7. A fictional decision marked approved without approval evidence.
8. A fictional decision containing business financial or contract details.

Expected behavior:

- Required fields are present or clearly marked pending.
- Facts and assumptions remain separate.
- Missing reviews, dependencies, or recovery details block readiness.
- Prohibited content is rejected or removed.
- Material scope changes require a revised record and renewed approval.
- Approval cannot be fabricated.
- Execution authority remains none.
- Execution status remains not executed.

## Change Control

Changes require:

1. Founder approval
2. Governance and security review where applicable
3. Updated changelog entry
4. Synthetic-data validation
5. Confirmation that the schema remains documentation-only and non-executing
   unless separately approved
