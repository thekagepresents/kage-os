# Kage Manual Approval Record Workflow

## Status

PROPOSED — MANUAL — NON-EXECUTING

## Purpose

This workflow defines how Kage Agency HQ records and validates Founder decisions
for proposed actions, plans, assets, changes, and commitments.

It ensures that approval is explicit, current, specific, scoped, attributable,
and traceable before it is treated as valid.

This workflow records approval status only. It does not send, publish, pay,
sign, grant access, create records, modify systems, execute work, or authorize
an execution mechanism.

## Owner

Founder

## Governing Principle

Founder retains final decision authority.

A recommendation, draft, prior approval, silence, informal discussion, public
information, assumed intent, or partial instruction is not approval.

An approval is valid only for the exact action and scope that Founder explicitly
approved.

## Trigger

Use this workflow when:

- A Class B or Class C proposal is ready for Founder review
- Founder gives an approval, rejection, revision, or deferral instruction
- A previously approved scope may have changed
- A decision must be recorded before later execution can be considered
- An approval is unclear, incomplete, stale, contradictory, or missing
- A plan, asset, budget, external communication, contract, access change,
  system change, or other material item needs a decision record

## Inputs

```text
Decision or Action:
[Concise description]

Approval Class:
[B or C]

Proposed Scope:
[Exact included and excluded work]

Source of Truth:
[Founder directive / Google Drive / Claude Project / GitHub / other approved source]

Proposed Action:
[Exact action]

External Systems or Parties:
[None or named]

Data Involved:
[None / public / internal / restricted]

Cost or Financial Exposure:
[None / estimate / exact amount and currency]

Risk:
[Low / Medium / High / Critical]

Dependencies:
[Required facts, rights, records, approvals, access, contracts, or other prerequisites]

Rollback or Recovery:
[How an action could later be reversed, corrected, or contained]

Approval Evidence:
[Founder instruction, record location, or pending]
```

If a required input is absent, record the gap and do not infer it.

## Workflow Overview

```text
RECEIVE PROPOSAL OR FOUNDER DECISION
→ CHECK APPROVAL CLASS
→ CHECK SOURCE OF TRUTH
→ CHECK SCOPE AND EXACT ACTION
→ CHECK RISK, DATA, COST, DEPENDENCIES, AND RECOVERY
→ VALIDATE FOUNDER DECISION
→ RECORD APPROVAL STATUS
→ IDENTIFY CONDITIONS AND EXPIRY
→ HAND OFF AS RECORD ONLY
→ STOP WITHOUT EXECUTION
```

## Step 1 — Receive Proposal or Decision

1. Identify the exact action or decision under review.
2. Identify whether it is Class B or Class C.
3. Capture the proposed scope, including what is excluded.
4. Capture all material details: recipient, channel, content, asset, system,
   record, permission, amount, timing, audience, geography, term, or other
   relevant details.
5. Identify whether Founder has supplied a decision or whether approval remains
   pending.

**Output**

```text
Decision or Action:
[Description]

Approval Class:
[B / C]

Proposal Status:
[Ready for review / Pending clarification / Pending Founder decision]
```

## Step 2 — Validate Source of Truth

Apply `kage-source-of-truth`.

1. Identify the relevant canonical record and Founder directive.
2. Confirm that facts, asset status, rights, budget, access, commitments, and
   dependencies are supported by an appropriate source.
3. Identify conflicts, gaps, drafts, assumptions, restricted information, or
   outdated material.
4. Do not validate approval using an unsupported or non-canonical source.

**Output**

```text
Source Evidence:
[Available evidence]

Classification:
[Confirmed Fact / Founder Directive / Draft / Research Finding / Assumption /
Conflict / Restricted Information / Unknown]

Gaps or Conflicts:
[None or description]
```

## Step 3 — Validate Proposal Completeness

A proposal is decision-ready only when it identifies, where applicable:

- Exact action
- Business purpose
- Approval class
- Scope included and excluded
- Recipient, party, or external system
- Exact content, asset, record, permission, or configuration
- Data classification and minimum necessary disclosure
- Cost, amount, currency, or financial exposure
- Timing, duration, expiration, or deadline
- Dependencies and prerequisites
- Risk level and material risks
- Rights, license, contract, or legal status
- Owner or `To be confirmed`
- Rollback, recovery, correction, removal, revocation, or hold method
- Evidence location
- Execution status

If any material element is unknown, label the proposal:

```text
NOT DECISION-READY — CLARIFICATION REQUIRED
```

Do not use a general approval to fill in missing material details later.

## Step 4 — Validate Founder Decision

A Founder decision is valid only when it is:

1. Explicit.
2. Given by Founder.
3. Specific enough to identify the action and scope.
4. Current to the proposal.
5. Recorded in an approved Kage context or canonical record.
6. Not contradicted by a later Founder instruction.
7. Not dependent on missing prerequisites unless those conditions are stated.
8. Consistent with current security, rights, data, and governance controls.

Classify the decision as one of:

| Decision Status | Meaning |
|---|---|
| Approved | Founder explicitly approved the exact scoped proposal |
| Approved With Conditions | Founder approved subject to recorded conditions |
| Rejected | Founder explicitly declined the proposal |
| Revised | Founder changed material scope; a revised proposal is required |
| Deferred | Founder postponed decision |
| Pending | No valid Founder decision exists |
| Invalid | Evidence is ambiguous, stale, incomplete, contradictory, or out of scope |
| Blocked | Required facts, rights, dependencies, policy, or authorization are absent |

Never convert `Pending`, `Invalid`, `Blocked`, `Deferred`, or `Revised` into an
approval.

## Step 5 — Record Decision

Record the decision using:

```text
Decision ID:
[Unique identifier or pending]

Date:
[YYYY-MM-DD]

Decision or Action:
[Exact description]

Approval Class:
[B / C]

Founder Decision:
[Approved / Approved With Conditions / Rejected / Revised / Deferred / Pending /
Invalid / Blocked]

Approved Scope:
[Exact scope; state Not approved if pending or rejected]

Excluded Scope:
[Items explicitly not approved]

Conditions:
[Prerequisites, limits, dates, rights, data handling, budget caps, required review,
or other conditions]

Evidence:
[Approved record location or Pending]

Risk:
[Level and concise explanation]

Dependencies:
[Required prerequisites and status]

Owner:
[Named owner or To be confirmed]

Expiration or Review Date:
[Date / event / condition / Not specified]

Execution Authority:
[None — this workflow records approval only]

Execution Status:
[Not executed]

Follow-Up:
[Required next safe action]
```

Do not fabricate a Decision ID, evidence location, Founder decision, owner, or
execution status.

## Step 6 — Handle Material Changes

A new or renewed approval is required if any of the following changes:

- Recipient, party, system, account, platform, channel, or audience
- Content, copy, attachment, asset, version, public claim, or configuration
- Amount, budget, price, payment method, currency, financial exposure, or term
- Scope, geography, timing, duration, deadline, or campaign period
- Data category, privacy exposure, access level, permission, or credential scope
- Contract, rights, license, legal status, or commitment
- Risk level, dependency, rollback method, or owner
- Any other detail that materially changes the approved action

When a change occurs:

1. Mark previous approval as limited to its original scope.
2. Create a revised proposal.
3. Set status to `Pending` or `Revised`.
4. Request Founder decision again.
5. Keep execution status as `Not executed`.

## Step 7 — Handle Ambiguous, Stale, or Conflicting Approval

If approval evidence is ambiguous, old, partial, conflicting, or not clearly
connected to the exact proposal:

1. Set decision status to `Invalid` or `Pending`.
2. State the specific problem.
3. Preserve the original evidence without expanding its meaning.
4. Present the minimum clarification needed.
5. Do not authorize any external or irreversible action.

Examples:

- “Looks good” without identifying a version, channel, or recipient
- Prior approval for a local campaign reused for national paid media
- Prior approval before a budget, price, asset, or recipient changed
- Approval from someone other than Founder
- An approval contradicted by a later Founder instruction
- A decision without a required rights, access, contract, or security prerequisite

## Step 8 — Close and Hand Off

Close the workflow with:

```text
Approval Record Status:
[Approved / Approved With Conditions / Rejected / Revised / Deferred / Pending /
Invalid / Blocked]

What Is Authorized:
[Decision record only; no execution authority created here]

What Is Not Authorized:
[Any unapproved or excluded scope]

Required Conditions:
[Conditions or none]

Next Safe Step:
[Draft revision / obtain evidence / request clarification / separate execution
authorization review / hold]

Execution Status:
[Not executed]
```

Stop. This workflow has no external effect.

## Restricted Information Handling

If the proposal or evidence includes personal, financial, contractual,
credential, payment, health, legal, or unreleased information:

- Use minimum necessary detail.
- Do not reproduce sensitive values.
- Mark data as restricted.
- Verify that any proposed disclosure is specifically scoped and approved.
- Require secure, authorized handling before any separate execution path is
  considered.
- Do not store or transmit restricted data through this workflow.

## Failure Behavior

If the approval cannot be validated:

```text
1. Mark status as Pending, Invalid, or Blocked.
2. State the missing, ambiguous, stale, conflicting, or out-of-scope element.
3. State the minimum required clarification or evidence.
4. Preserve the prohibition on execution.
5. Record: Execution Status: Not executed.
```

## Dependencies

- `agents/founder-command/AGENT.md`
- `workflows/manual-intake-and-triage/WORKFLOW.md`
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

1. A complete fictional public-post approval request with explicit Founder
   approval.
2. A fictional sponsor outreach approval where the amount changes after approval.
3. A fictional ticketing-access approval lacking duration and removal plan.
4. A fictional approved poster reused for a new paid campaign scope.
5. A fictional payment request with only a vague “approved” comment.
6. A fictional urgent venue change with incomplete facts.
7. A fictional connector approval missing data-boundary and rollback details.
8. A fictional contract disclosure request with restricted information.
9. A fictional Founder decision that defers a proposal.
10. A fictional approval contradicted by a later Founder instruction.

Expected behavior:

- Validates approval class, source, scope, evidence, risk, dependencies, and
  conditions.
- Records only explicit, current, specific Founder decisions.
- Treats material changes as requiring renewed approval.
- Keeps unclear, stale, partial, or conflicting approvals invalid or pending.
- Creates no execution authority and performs no external action.
- Uses synthetic data only.

## Change Control

Changes require:

1. Founder approval
2. Governance and security review
3. Updated changelog entry
4. Synthetic-data validation
5. Confirmation that the workflow remains manual and non-executing unless
   separately approved
