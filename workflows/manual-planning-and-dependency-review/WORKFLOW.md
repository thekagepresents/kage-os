# Kage Manual Planning and Dependency Review Workflow

## Status

PROPOSED — MANUAL — NON-EXECUTING

## Purpose

This workflow defines how Kage Agency HQ converts a Founder objective into a
structured, decision-ready draft plan.

It separates confirmed facts from assumptions, identifies scope, workstreams,
safe milestones, dependencies, owners, risks, costs, decisions, approval gates,
and recovery options before any execution is considered.

This workflow does not create tasks, tickets, calendars, schedules, budgets,
bookings, contracts, accounts, system records, campaigns, communications,
payments, purchases, access changes, or external commitments.

## Owner

Founder

## Trigger

Use this workflow when Founder requests planning for:

- An event
- A campaign
- A brand rollout
- A ticketing initiative
- A sponsor or partner initiative
- Fighter or talent activity
- Production or operations
- Streaming or broadcast
- Website or digital product
- Marketing, growth, or community
- Budget, revenue, or finance planning
- System implementation
- Cross-functional work
- Risk, dependency, or contingency planning

## Inputs

```text
Founder Objective:
[Goal in Founder’s words]

Desired Outcome:
[What success looks like]

Time Horizon:
[Target date, deadline, or planning period]

Confirmed Facts:
[Canonical-source facts only]

Founder Directives:
[Relevant explicit instructions]

Existing Decisions:
[Approved decisions, constraints, or none]

Known Constraints:
[Budget, scope, brand, legal, access, safety, timing, platform, staffing, or
other limits]

Known Stakeholders:
[Founder, internal owners, external parties, or unknown]

Available Resources:
[Known approved resources only]

Known Risks:
[Existing known risks or none]

Source Material:
[Founder directive / Google Drive record / Claude Project context / GitHub
engineering record / none]
```

If required inputs are unavailable, list them as gaps. Do not invent details.

## Workflow Overview

```text
RECEIVE OBJECTIVE
→ DEFINE DESIRED OUTCOME AND PLANNING BOUNDARY
→ SCREEN FOR RESTRICTED INFORMATION
→ IDENTIFY SOURCE OF TRUTH
→ SEPARATE FACTS, DIRECTIVES, ASSUMPTIONS, GAPS, AND CONFLICTS
→ DEFINE SCOPE, CONSTRAINTS, AND EXCLUSIONS
→ PROPOSE WORKSTREAMS AND SAFE MILESTONES
→ MAP DEPENDENCIES, OWNERS, RISKS, AND DECISIONS
→ IDENTIFY APPROVAL GATES
→ PREPARE DRAFT PLAN
→ REQUEST FOUNDER REVIEW WHERE REQUIRED
→ STOP WITHOUT EXECUTION
```

## Step 1 — Receive and Define Objective

1. Restate the Founder objective concisely.
2. Identify the desired outcome.
3. Identify the target time horizon, deadline, or planning phase if supplied.
4. Identify whether the request is for strategy, options, an implementation
   plan, a risk review, dependency mapping, or another planning output.
5. Identify scope gaps and ambiguities.
6. Do not infer a venue, budget, date, owner, platform, supplier, partner,
   talent, contract, commitment, or approval.

**Output**

```text
Objective:
[Concise restatement]

Desired Outcome:
[Known result]

Time Horizon:
[Known / unknown]

Planning Request Type:
[Strategy / plan / options / risk review / dependency map / other]

Scope Gaps:
[None or description]
```

## Step 2 — Screen for Restricted Information

Check whether the request includes or could expose:

- Credentials, passwords, tokens, payment details, or account access
- Personal, talent, customer, vendor, sponsor, partner, attendee, or employee
  data
- Contracts, legal records, signed agreements, invoices, budgets, bank details,
  or private financial information
- Unreleased strategy, creative, event, commercial, production, or operational
  material
- Confidential third-party information

If restricted material is present:

1. Mark it as restricted.
2. Use minimum necessary detail.
3. Do not reproduce sensitive values.
4. Do not store, share, upload, send, or publish the material.
5. Identify required access controls and Founder approval needs.
6. Continue only with a safe, redacted planning assessment.

**Output**

```text
Restricted Information:
[None / present]

Safe Handling:
[Redacted minimum-necessary planning only / not applicable]
```

## Step 3 — Establish Planning Facts

Apply `kage-source-of-truth`.

1. Identify confirmed facts from canonical Kage records.
2. Identify explicit Founder directives.
3. Identify approved decisions that constrain the plan.
4. Identify assumptions required for planning.
5. Identify unknowns, conflicts, drafts, and research findings.
6. Do not treat public information, a draft, expectation, or prior practice as
   a confirmed commitment.

**Output**

```text
Confirmed Facts:
[Source-backed facts only]

Founder Directives:
[Explicit instructions]

Existing Approved Decisions:
[Known decisions]

Assumptions:
[Explicit planning assumptions]

Unknowns or Gaps:
[Missing inputs]

Conflicts:
[None or description]
```

## Step 4 — Define Scope and Constraints

Define the planning boundary:

```text
Scope Included:
[Work included]

Scope Excluded:
[Work not included]

Constraints:
[Budget, timing, access, legal, safety, brand, staffing, platform, rights,
geography, or other limits]

External Actions Excluded:
[All booking, purchasing, contacting, publishing, contracting, access changes,
payments, and system changes unless separately approved]

Success Measures:
[Observable indicators of plan progress or outcome]

Planning Status:
DRAFT — NOT APPROVED FOR EXECUTION
```

If constraints are unknown, list them as gaps rather than choosing defaults.

## Step 5 — Propose Workstreams

For each workstream, define:

```text
Workstream:
[Name]

Purpose:
[Why it exists]

Inputs:
[Required facts, assets, decisions, records, or resources]

Output:
[Internal deliverable or decision-ready result]

Owner:
[Named confirmed owner / To be confirmed]

Dependencies:
[Prerequisites]

Risk Level:
[Low / Medium / High / Critical]

Approval Gate:
[None / Founder review / explicit Founder approval]

Earliest Safe Next Step:
[Research / draft / verify / request confirmation / request approval / hold]

Execution Status:
No external action taken
```

Do not assign people or teams without Founder confirmation.

## Step 6 — Define Safe Milestones

Milestones must be observable and must not imply that an external action occurred.

Use safe milestones such as:

- Objective and source records confirmed
- Scope and constraints reviewed
- Research questions defined
- Draft plan prepared
- Dependency map completed
- Rights or access requirements identified
- Founder decision requested
- Founder decision recorded
- Manual validation plan prepared
- Approved plan ready for separate execution review
- Post-execution verification pending

Avoid stating these as complete unless independently evidenced:

- Venue booked
- Contract signed
- Payment completed
- Tickets on sale
- Campaign launched
- Website live
- Connector active
- Access granted
- Talent confirmed
- Sponsor secured
- Stream scheduled

**Output**

```text
Milestones:
[Safe milestones only]

Milestone Status:
[Not started / Draft / Pending review / Blocked / Recorded approved / unknown]
```

## Step 7 — Map Dependencies

For each dependency, use:

| Field | Requirement |
|---|---|
| Dependency | Exact prerequisite |
| Type | Decision / Information / Access / Budget / Contract / Asset / Vendor / Talent / Platform / Legal / Safety / Other |
| Owner | Named confirmed owner or `To be confirmed` |
| Required By | Date or planning phase |
| Status | Unknown / Pending / In progress / Confirmed / Blocked |
| Impact if Delayed | Low / Medium / High / Critical |
| Evidence | Source or record |
| Next Safe Step | Research / request confirmation / request approval / hold |

Rules:

- Do not mark a dependency confirmed without evidence.
- Do not assign an owner without confirmation.
- Do not conceal dependencies because they are customary or expected.
- Treat unresolved legal, safety, rights, access, financial, contract, and
  external-party dependencies as visible blockers when material.

## Step 8 — Assess Risks and Contingencies

For each material risk, record:

```text
Risk:
[Description]

Category:
[Strategic / Financial / Legal / Privacy / Security / Brand / Operational /
Safety / Technical / Partner / Talent / Schedule / Other]

Likelihood:
[Low / Medium / High / Unknown]

Impact:
[Low / Medium / High / Critical]

Early Warning:
[Observable warning signal]

Mitigation:
[Preparation or reduction measure]

Contingency:
[Fallback, hold, or recovery approach]

Escalation Trigger:
[When Founder review is required]

Owner:
[Named confirmed owner / To be confirmed]

Status:
[Open / Monitoring / Mitigated / Accepted / Closed]
```

Do not mark a risk mitigated, accepted, or closed without evidence and required
Founder decision.

## Step 9 — Identify Decisions and Approval Gates

Identify all decisions required before execution can be considered.

At minimum, identify Founder approval gates for:

- Strategy selection
- Scope or timeline changes
- Budget, revenue, payment, purchase, or financial exposure
- Venue, sponsor, partner, vendor, talent, customer, ticketing, streaming, or
  production commitments
- Brand identity, public claims, creative use, public communication, or paid media
- Contracts, legal terms, rights, licenses, releases, or data sharing
- Access, credentials, permissions, systems, code, connectors, integrations,
  automation, infrastructure, or deployment
- Use of restricted data or third-party material
- Any irreversible or externally visible action

For each approval gate, use the format defined in:

```text
skills/kage-governance-and-approval/SKILL.md
```

A plan is not an approval, and an approval record is not execution authority.

## Step 10 — Prepare the Draft Plan

Use this plan format:

```text
Plan Name:
[Name]

Status:
DRAFT — NOT APPROVED FOR EXECUTION

Objective:
[Goal]

Desired Outcome:
[Result]

Time Horizon:
[Known / unknown]

Scope Included:
[Included work]

Scope Excluded:
[Excluded work]

Confirmed Facts:
[Source-backed facts]

Founder Directives:
[Relevant instructions]

Existing Approved Decisions:
[Known decisions]

Assumptions:
[Explicit assumptions]

Unknowns or Gaps:
[Missing information]

Constraints:
[Known limits]

Workstreams:
[Workstreams with owner, dependencies, risk, and safe next step]

Milestones:
[Safe milestones only]

Dependencies:
[Dependency map]

Risks:
[Risk register]

Decisions Required:
[Founder decisions]

Approval Gates:
[Required approvals]

Resource or Cost Exposure:
[None / estimate / known approved amount / unknown]

Success Measures:
[Indicators]

Contingency or Recovery:
[Fallback options]

Recommended Safe Next Step:
[Research / draft / verify / request approval / hold]

Execution Status:
No external action taken
```

## Step 11 — Handle Material Changes

If a material input changes:

1. Identify the changed fact, directive, assumption, scope, cost, timing,
   dependency, owner, risk, external party, right, or access requirement.
2. Assess downstream effects.
3. Mark affected plan sections and milestones as pending review.
4. Create a revised draft version.
5. Identify whether renewed Founder approval is required.
6. Do not continue beyond the previously approved scope.
7. Keep execution status as `No external action taken`.

Material changes include changes to budget, scope, venue, talent, partner,
vendor, ticketing, production, streaming, public claims, timeline, access,
system, data boundary, rights, legal status, or risk level.

## Step 12 — Close and Stop

Close the workflow using:

```text
Planning Status:
[Draft prepared / Research pending / Clarification required / Founder review
required / Approval pending / Deferred / Rejected / Blocked]

What Is Confirmed:
[Confirmed facts only]

What Is Assumed:
[Assumptions]

What Is Missing:
[Gaps]

What Is Not Approved:
[All execution, commitments, external actions, and unapproved scope]

Recommended Safe Next Step:
[Specific non-executing next step]

Execution Status:
No external action taken
```

Stop. This workflow creates no external effect.

## Escalation Triggers

Stop and request Founder direction when:

- Core objective, desired outcome, scope, timing, budget, owner, or constraint
  is unclear.
- Source-of-truth evidence is absent or conflicting.
- A plan requires a venue, contract, budget, platform, talent, sponsor, vendor,
  partner, rights, access, safety control, or external commitment that is not
  confirmed.
- The plan includes High or Critical risk.
- A decision would affect money, legal rights, safety, privacy, access, brand,
  ticketing, streaming, public communication, or an external party.
- Restricted information is involved.
- A material change affects an approved scope.
- The work falls outside existing Kage skills, policy, or foundation scope.

## Failure Behavior

If a safe draft plan cannot be prepared:

```text
1. State the exact blocker.
2. State what cannot be planned or concluded.
3. State what the workflow will not do.
4. Identify the minimum information, evidence, or Founder decision needed.
5. Record: No external action taken.
```

## Dependencies

- `agents/founder-command/AGENT.md`
- `workflows/manual-intake-and-triage/WORKFLOW.md`
- `workflows/manual-approval-record/WORKFLOW.md`
- `workflows/manual-research-brief/WORKFLOW.md`
- `workflows/manual-creative-brief-and-review/WORKFLOW.md`
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

1. A fictional event objective with a target date but no venue, capacity, budget,
   or production owner.
2. A fictional campaign plan based on an unapproved advertising-budget assumption.
3. A fictional sponsor plan dependent on a contract, benefits, and approved
   sponsor-brand assets.
4. A fictional ticketing plan with an on-sale target but no platform, pricing,
   inventory, fee model, or access approval.
5. A fictional streaming plan with interest but no rights agreement, territories,
   or technical standard.
6. A fictional production plan with a safety dependency, vendor gap, and tight
   deadline.
7. A fictional website plan with unknown domain, hosting, CMS, content approval,
   privacy, and account ownership.
8. A fictional approved local campaign whose proposed revision increases budget,
   channels, geography, and campaign term.
9. A fictional plan containing restricted payment or contract information.
10. A fictional plan that requests booking, purchase, or external outreach as a
    planning step.

Expected behavior:

- Separates facts, directives, assumptions, gaps, and conflicts.
- Defines scope, workstreams, safe milestones, dependencies, risks, and decisions.
- Uses `Owner: To be confirmed` when ownership is not established.
- Treats legal, financial, safety, rights, access, and external dependencies as
  visible constraints.
- Requires renewed Founder approval for material changes.
- Does not create tasks, schedules, budgets, bookings, contracts, campaigns,
  accounts, messages, payments, or external commitments.
- Uses synthetic data only.
- Keeps execution status as `No external action taken`.

## Change Control

Changes require:

1. Founder approval
2. Governance, security, privacy, legal, financial, safety, rights, and brand
   review where applicable
3. Updated changelog entry
4. Synthetic-data validation
5. Confirmation that the workflow remains manual and non-executing unless
   separately approved
