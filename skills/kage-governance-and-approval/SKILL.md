# Kage Governance and Approval Skill

## Status

PROPOSED — NON-EXECUTING SPECIFICATION

## Purpose

This skill ensures that Kage Agency HQ work remains Founder-controlled. It
identifies decisions and actions that require approval, prepares clear approval
requests, records the decision outcome, and prevents execution before the
required approval is present.

It does not access external systems, modify records, send communications,
publish content, make financial commitments, sign agreements, change access,
or execute work.

## Owner

Founder

## Governing Principle

Founder retains final authority over Kage identity, strategy, money, contracts,
access, publishing, partners, customers, talent, ticketing, streaming,
production, systems, and all external or irreversible actions.

No silence, prior practice, draft, public information, partial instruction, or
agent recommendation constitutes approval.

## Approval Classes

| Class | Meaning | Required Handling |
|---|---|---|
| A — Informational | Internal analysis or a reversible draft with no external impact | May proceed as a draft; label clearly |
| B — Review Required | Material recommendation, internal plan, or change to an approved working artifact | Present for Founder review before treating as approved |
| C — Explicit Approval Required | External, financial, contractual, access-related, public, sensitive, or irreversible action | Obtain explicit Founder approval before execution |
| D — Prohibited Pending Separate Authorization | Activity outside current Kage foundation scope or requiring a separately approved policy | Do not proceed; identify authorization required |

## Actions Requiring Explicit Approval

Treat the following as Class C unless Founder establishes a stricter rule:

- Sending email, SMS, direct messages, outreach, invitations, or proposals
- Publishing or scheduling website, social, streaming, email, SMS, or paid-media
  content
- Creating, editing, or deleting live ticketing, event, venue, table,
  hospitality, streaming, CRM, finance, website, hosting, DNS, or advertising
  records
- Making purchases, payments, refunds, credits, transfers, commitments, or
  budget changes
- Signing, accepting, negotiating, or sending contracts, terms, releases,
  invoices, quotes, or legal documents
- Granting, changing, or removing access, permissions, credentials, roles, or
  connected services
- Sharing restricted data with any person, team, vendor, partner, platform, or
  system
- Using Kage brand assets publicly or approving public brand use
- Confirming or changing fighter, talent, sponsor, partner, vendor, customer,
  venue, event, ticketing, table, hospitality, or streaming commitments
- Deploying code, configuration, infrastructure, automation, MCP servers,
  connectors, integrations, databases, or production systems
- Creating a GitHub branch, pull request, release, tag, collaborator invitation,
  GitHub Action, secret, webhook, or external integration
- Deleting, archiving, overwriting, or materially changing a canonical record
- Representing Kage in any external communication or negotiation

## Actions Permitted as Drafts

The following may be prepared as Class A or B work, depending on impact, but
must remain clearly labeled as drafts:

- Research briefs
- Internal analyses
- Recommendations
- Concepts
- Strategy options
- Creative briefs
- Copy drafts
- Mockups
- Checklists
- Workflow designs
- Skill specifications
- Agent specifications
- Schema proposals
- Risk registers
- Budget models using synthetic or approved non-sensitive inputs
- Implementation plans
- Test plans using synthetic data only

Draft preparation does not authorize sending, publishing, uploading, deploying,
signing, purchasing, connecting, or otherwise executing the draft.

## Approval Request Format

Before a Class B or Class C item is treated as approved or executed, present:

```text
Decision or Action:
[Concise description]

Why It Is Needed:
[Business or operational purpose]

Approval Class:
[A / B / C / D]

Scope:
[Exactly what is included and excluded]

Source of Truth:
[Founder directive / Google Drive / Claude Project / GitHub / other approved source]

Proposed Action:
[Exact action to be approved]

External Systems or Parties:
[None or named systems/parties]

Data Involved:
[None / public / internal / restricted; minimum necessary detail]

Cost or Financial Exposure:
[None / estimate / exact amount and currency]

Risk:
[Low / Medium / High, with concise explanation]

Dependencies:
[Prerequisites and approvals]

Rollback or Recovery:
[How the action can be reversed, corrected, or contained]

Requested Founder Decision:
[Approve / Reject / Revise / Defer]

Execution Status:
[Not executed]
```

For a Class C action, include the exact intended recipient, system, content,
record, permission, amount, asset, or configuration whenever applicable.

## Valid Approval Standard

An approval is valid only when it is:

- Explicit
- Given by Founder
- Specific enough to identify the action and scope
- Current to the proposed action
- Recorded in an approved Kage context or canonical record
- Not contradicted by a later Founder instruction

If material scope, recipient, cost, timing, content, data, system, or risk
changes, request approval again.

## Approval Record

After Founder decides, record:

```text
Decision ID:
[Unique identifier]

Date:
[YYYY-MM-DD]

Founder Decision:
[Approved / Rejected / Revised / Deferred]

Approved Scope:
[Exact approved scope]

Conditions:
[Requirements, limits, or prerequisites]

Evidence:
[Where the approval is recorded]

Owner:
[Named accountable owner]

Execution Status:
[Not executed / Executed / Verified / Reversed]

Follow-Up:
[Required next action]
```

Do not create a fictional approval record. If no approved record exists, state
that approval is pending.

## Handling Unclear Instructions

If Founder instruction is ambiguous:

1. Identify the ambiguity.
2. State the most conservative interpretation.
3. Offer bounded options where useful.
4. Request clarification before any Class B or C action.
5. Do not infer approval from intent alone.

## Emergency or Time-Sensitive Matters

Urgency does not remove approval requirements.

For time-sensitive matters:

1. Prepare the shortest complete approval request possible.
2. Identify deadline, impact of delay, and reversible alternatives.
3. Preserve the prohibition on unauthorized external action.
4. If no approval is available, prepare a draft or hold position only.

## Safety Rules

- Never execute a Class C action without explicit Founder approval.
- Never treat a recommendation as a decision.
- Never infer approval from silence or prior similar work.
- Never expand an approved scope without renewed approval.
- Never conceal financial, legal, reputational, privacy, or security risk.
- Never publish, send, sign, pay, connect, deploy, or grant access by default.
- Never use approval language that suggests an action has occurred when it has
  not.
- Never store secrets, credentials, private financial data, or personal data in
  this skill or associated synthetic tests.

## Dependencies

- `skills/kage-source-of-truth/SKILL.md`
- `SECURITY.md`
- `CONTRIBUTING.md`
- `ARCHITECTURE.md`
- Approved Founder directives and canonical Kage records

## Testing

Test this skill using synthetic scenarios only.

Minimum synthetic test cases:

1. Drafting a public event announcement.
2. Sending a sponsor proposal with a fictional financial amount.
3. Changing access to a fictional ticketing account.
4. Preparing an internal creative brief.
5. A Founder approval whose recipient or scope later changes.
6. An urgent fictional event issue without available Founder approval.
7. Creating a fictional GitHub release or connector.
8. A request to handle restricted fictional contract or payment data.

Expected behavior:

- Correctly assign the approval class.
- Produce a complete approval request for Class B and C items.
- Keep execution status as not executed until valid approval exists.
- Require renewed approval if material scope changes.
- Avoid external action, secrets, and real business data.

## Change Control

Changes require:

1. Founder approval
2. Security review where applicable
3. Updated changelog entry
4. Synthetic-data validation
5. Confirmation that the skill remains non-executing unless separately approved
