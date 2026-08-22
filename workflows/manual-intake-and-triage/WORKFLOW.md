# Kage Manual Intake and Triage Workflow

## Status

PROPOSED — MANUAL — NON-EXECUTING

## Purpose

This workflow defines how Kage Agency HQ handles a Founder request from initial
intake through classification, analysis, drafting, approval preparation, and
safe handoff.

It ensures that every request is routed through source-of-truth, governance,
research, creative, and planning controls as relevant.

This workflow does not create an intake form, ticket, task, record, account,
automation, integration, notification, or external action.

## Owner

Founder

## Trigger

A Founder request is provided in an approved Kage working context.

Examples:

- A question
- A fact check
- A research request
- A strategy request
- A creative request
- A planning request
- A request to communicate externally
- A request to publish, buy, book, sign, pay, connect, deploy, or change access
- A request involving contracts, restricted data, talent, sponsors, ticketing,
  streaming, finance, or public claims

## Inputs

```text
Founder Request:
[Request in Founder’s words]

Relevant Founder Directives:
[Known explicit directions]

Available Source Material:
[Canonical records, approved project context, or none]

Time Sensitivity:
[None / date / deadline / urgent]

Known Constraints:
[Budget, scope, access, legal, brand, safety, platform, or other limits]

Requested Outcome:
[Question answer / draft / plan / research / action proposal / unknown]
```

If inputs are incomplete, record the gap rather than inferring missing details.

## Workflow Overview

```text
RECEIVE REQUEST
→ SCREEN FOR RESTRICTED INFORMATION
→ CLASSIFY REQUEST TYPE
→ IDENTIFY SOURCE OF TRUTH
→ IDENTIFY FACTS, DIRECTIVES, ASSUMPTIONS, GAPS, AND CONFLICTS
→ SELECT APPLICABLE SKILLS
→ ASSESS RISK AND APPROVAL CLASS
→ PREPARE SAFE OUTPUT
→ REQUEST FOUNDER DECISION WHEN REQUIRED
→ RECORD STATUS
→ STOP WITHOUT EXTERNAL EXECUTION
```

## Step 1 — Receive and Restate

1. Capture the request in concise form.
2. Identify the intended outcome.
3. Identify whether the request asks for analysis, drafting, research, planning,
   or an external action.
4. Restate ambiguous requests using the minimum necessary clarification.
5. Do not assume authority, deadline, scope, recipient, budget, or approval.

**Output**

```text
Request:
[Concise restatement]

Requested Outcome:
[Type]

Ambiguities:
[None or description]
```

## Step 2 — Restricted-Information Screen

Check whether the request includes or could expose:

- Credentials, passwords, tokens, API keys, recovery codes, or payment details
- Personal, health, legal, contractual, talent, customer, vendor, partner, or
  attendee data
- Private financial records, bank details, invoices, contracts, or tax material
- Unreleased creative, strategy, event, or commercial information
- Confidential third-party material

If restricted material is present:

1. Classify it as `Restricted Information`.
2. Use minimum necessary detail.
3. Do not repeat sensitive values.
4. Do not store, send, upload, publish, or distribute it.
5. Identify the access and approval requirement.
6. Continue only with a safe, redacted internal assessment.

**Output**

```text
Restricted Information:
[None / present]

Handling:
[No sensitive values reproduced; authorized handling required / not applicable]
```

## Step 3 — Classify the Request

Classify the request into one or more categories:

| Category | Typical Output |
|---|---|
| Question or fact check | Source-of-truth assessment |
| Research | Research brief and verification plan |
| Draft | Clearly labeled internal draft |
| Creative | Asset and brand-governance assessment |
| Strategy or planning | Draft plan, dependencies, risks, and decision gates |
| External action | Exact approval request |
| Financial, legal, access, or contract matter | High-risk approval assessment |
| System, code, automation, connector, or deployment matter | Foundation-scope and security assessment |
| Restricted-information matter | Redacted handling assessment |
| Ambiguous request | Clarification request or bounded options |

**Output**

```text
Request Type:
[One or more categories]

Primary Intended Output:
[Assessment / draft / plan / approval request / clarification]
```

## Step 4 — Identify Source of Truth

Apply `kage-source-of-truth`.

1. Identify the claims, records, or decisions needed.
2. Identify the expected authoritative source:
   - Founder directive
   - Canonical Kage Google Drive record
   - Approved Claude Project context
   - GitHub engineering record
   - External research source
3. Classify available information:
   - Confirmed Fact
   - Founder Directive
   - Approved Plan
   - Draft
   - Research Finding
   - Assumption
   - Conflict
   - Restricted Information
   - Unknown
4. Identify gaps and conflicts.
5. Do not silently resolve conflicts or treat public sources as canonical Kage
   facts.

**Output**

```text
Confirmed Facts:
[Source-backed facts]

Founder Directives:
[Explicit instructions]

Assumptions:
[Explicit assumptions]

Unknowns or Gaps:
[Missing information]

Conflicts:
[None or description]
```

## Step 5 — Select Applicable Skills

Select only the skills relevant to the request:

| Condition | Required Skill |
|---|---|
| Any Kage claim, record, directive, conflict, or unknown | `kage-source-of-truth` |
| Any approval, external, financial, legal, access, public, sensitive, or irreversible action | `kage-governance-and-approval` |
| External research, public information, attribution, or verification | `kage-research-and-source-verification` |
| Brand, creative, asset, rights, public-use, sponsor, talent, likeness, or factual claim in creative | `kage-brand-and-creative-governance` |
| Objective, plan, timeline, workstream, dependency, risk, milestone, or cross-functional coordination | `kage-strategy-planning-dependency-management` |

If no existing skill covers a material requirement, state the gap and proceed only
with a conservative, non-executing assessment.

**Output**

```text
Skills Applied:
[List]

Uncovered Control Gaps:
[None or description]
```

## Step 6 — Assess Risk and Approval Class

Apply `kage-governance-and-approval`.

Assign a risk level:

```text
Low / Medium / High / Critical
```

Assign an approval class:

| Class | Handling |
|---|---|
| A — Informational | Internal analysis or reversible draft may proceed |
| B — Review Required | Present material recommendation or plan for Founder review |
| C — Explicit Approval Required | Obtain explicit Founder approval before external, financial, public, access, contractual, sensitive, or irreversible action |
| D — Prohibited Pending Separate Authorization | Do not proceed beyond assessment; identify required authorization |

Treat the following as Class C at minimum:

- External communication, outreach, or representation
- Publishing, posting, paid media, printing, broadcasting, or public claims
- Money, budgets, payments, purchases, refunds, invoices, or financial promises
- Contracts, agreements, legal materials, or commitments
- Access, credentials, permissions, systems, connectors, or integrations
- Ticketing, venue, sponsor, partner, vendor, talent, customer, streaming, or
  production commitments
- Use or sharing of restricted data
- Deployment, automation, code, infrastructure, or production changes

**Output**

```text
Risk Level:
[Level and concise reason]

Approval Class:
[A / B / C / D]

Approval Status:
[Not required / Pending / Evidence supplied / Not valid / Not executed]
```

## Step 7 — Prepare Safe Output

Prepare the correct non-executing output.

### For questions or fact checks

Provide a source-of-truth assessment with confidence, gaps, and conflicts.

### For research

Provide:

- Research question
- Exact claim
- Source tiers needed
- Verification plan
- Attribution and rights considerations
- Confidence and limitations
- Permitted internal use

### For drafts

Provide a clearly labeled draft with:

```text
Status: DRAFT — NOT APPROVED FOR EXTERNAL USE
```

### For creative requests

Provide:

- Asset status and version
- Source, ownership, rights, license, and attribution status
- Brand and factual-claim checks
- Defined proposed-use scope
- Approval requirement
- External-use status

### For plans

Provide:

- Objective and desired outcome
- Confirmed facts and assumptions
- Scope and constraints
- Workstreams and safe milestones
- Dependencies and risks
- Owners or `To be confirmed`
- Decision and approval gates
- Safe next step

### For external-action requests

Do not execute. Prepare the exact approval request defined in:

```text
skills/kage-governance-and-approval/SKILL.md
```

### For Class D requests

State:

```text
Status: PROHIBITED PENDING SEPARATE AUTHORIZATION
```

Then identify the policy, approval, security review, data boundary, owner, test
plan, and recovery plan required before reassessment.

## Step 8 — Request Founder Decision

For Class B or C work, present:

```text
Decision or Action:
[Concise description]

Why It Is Needed:
[Purpose]

Approval Class:
[B / C]

Scope:
[Included and excluded work]

Proposed Action:
[Exact action]

External Systems or Parties:
[None or named]

Data Involved:
[None / public / internal / restricted]

Cost or Financial Exposure:
[None / estimate / exact amount]

Risk:
[Level and explanation]

Dependencies:
[Prerequisites]

Rollback or Recovery:
[Recovery approach]

Requested Founder Decision:
[Approve / Reject / Revise / Defer]

Execution Status:
[Not executed]
```

Do not treat a response as approval unless it is explicit, current, specific,
recorded, and uncontradicted.

## Step 9 — Record Outcome and Stop

Record the current workflow result:

```text
Workflow Status:
[Draft prepared / Research pending / Clarification required / Approval pending /
Approved scope recorded / Deferred / Rejected / Blocked]

Founder Decision:
[None / Approved / Rejected / Revised / Deferred]

Next Safe Step:
[Action that remains non-executing unless separately authorized]

Execution Status:
[No external action taken]
```

Stop. This workflow creates no external effect.

## Escalation Triggers

Stop and request Founder direction when:

- Facts conflict or source-of-truth evidence is absent.
- Scope, budget, owner, rights, access, timing, or commitment is unclear.
- The request involves High or Critical risk.
- An external, financial, legal, access, public, contractual, or irreversible
  action is requested.
- Restricted information is involved.
- A request exceeds the current foundation scope.
- A needed skill, policy, or control does not exist.
- A material change affects a previously approved scope.

## Failure Behavior

If safe output cannot be prepared:

```text
1. State the specific blocker.
2. State the minimum information or decision needed.
3. Do not infer missing details.
4. Do not execute or imply execution.
5. Record: No external action taken.
```

## Dependencies

- `agents/founder-command/AGENT.md`
- `skills/kage-source-of-truth/SKILL.md`
- `skills/kage-governance-and-approval/SKILL.md`
- `skills/kage-research-and-source-verification/SKILL.md`
- `skills/kage-brand-and-creative-governance/SKILL.md`
- `skills/kage-strategy-planning-dependency-management/SKILL.md`
- `SECURITY.md`
- `CONTRIBUTING.md`
- `ARCHITECTURE.md`

## Testing

Test this workflow using synthetic scenarios only.

Minimum synthetic test cases:

1. A fictional fact-check request with conflicting canonical and public sources.
2. A fictional research request about a venue with no booking authority.
3. A fictional internal creative brief request.
4. A fictional social post request using a draft asset.
5. A fictional sponsor outreach request with a financial amount.
6. A fictional ticketing-access request for a contractor.
7. A fictional event plan request with missing venue, budget, and owner.
8. A fictional urgent public statement with no confirmed facts.
9. A fictional connector, automation, or deployment request.
10. A request containing fictional restricted payment or contract information.

Expected behavior:

- Correctly routes the request through applicable skills.
- Identifies source-of-truth category, gaps, conflicts, risk, and approval class.
- Produces a safe assessment, draft, plan, or exact approval request.
- Treats all external
