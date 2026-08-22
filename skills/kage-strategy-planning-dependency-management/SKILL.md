# Kage Strategy, Planning, and Dependency Management Skill

## Status

PROPOSED — NON-EXECUTING SPECIFICATION

## Purpose

This skill defines how Kage Agency HQ should convert a Founder objective into a
structured, decision-ready plan.

It separates confirmed facts from assumptions, identifies outcomes, scope,
workstreams, milestones, owners, dependencies, risks, decisions, approval
gates, costs, success measures, and recovery options.

It does not create live tasks, assign people, change schedules, commit budgets,
contact external parties, procure services, publish plans, or execute work.

## Owner

Founder

## Scope

Use this skill for:

- Strategic planning
- Event planning
- Campaign planning
- Brand rollout planning
- Ticketing planning
- Sponsorship planning
- Fighter and talent planning
- Production planning
- Streaming planning
- Website and digital-product planning
- Marketing and growth planning
- Budget and revenue planning
- Operational planning
- System implementation planning
- Cross-functional dependency management
- Risk and contingency planning
- Founder decision preparation

## Planning Principles

- Start with the Founder objective and desired outcome.
- Use confirmed facts only as facts; label all assumptions.
- Define what is included and excluded before proposing work.
- Prefer the smallest viable plan that can be reviewed and approved.
- Identify decision gates before downstream commitments.
- Make dependencies explicit, including their owner and required date.
- Treat cost, legal, privacy, reputation, safety, access, brand, and operational
  exposure as risks requiring visibility.
- Separate recommendation from decision and plan from execution.
- Do not conceal uncertainty with false precision.
- Do not represent a plan as approved until Founder approval is recorded.
- Do not execute external work without the required approvals.

## Planning Inputs

Before producing a plan, identify:

```text
Objective:
[Founder goal]

Desired Outcome:
[What success looks like]

Time Horizon:
[Target date, deadline, or planning period]

Confirmed Facts:
[Canonical-source facts only]

Founder Directives:
[Relevant explicit instructions]

Assumptions:
[Unverified items required for planning]

Constraints:
[Budget, timing, access, legal, brand, staffing, venue, platform, or policy limits]

Stakeholders:
[Founder, internal owners, external parties, or unknown]

Existing Decisions:
[Approved decisions and unresolved decisions]

Available Resources:
[Known approved resources only]

Source of Truth:
[Founder / Google Drive / Claude Project / GitHub / other approved source]
```

If required inputs are absent, list them as gaps rather than inventing them.

## Plan Structure

Use this structure for every material plan:

```text
Plan Name:
[Name]

Status:
[Draft / Proposed / Approved / Deferred / Archived]

Objective:
[Goal]

Desired Outcome:
[Measurable or observable result]

Scope Included:
[Included work]

Scope Excluded:
[Excluded work]

Confirmed Facts:
[Source-backed facts]

Assumptions:
[Explicit assumptions]

Constraints:
[Known limits]

Workstreams:
[Major areas of work]

Milestones:
[Decision-ready checkpoints, not implied commitments]

Dependencies:
[Prerequisites, owners, due dates, and impact of delay]

Risks:
[Risk, likelihood, impact, mitigation, escalation trigger]

Decisions Required:
[Decision, decision owner, required-by date, options]

Approval Gates:
[What requires Founder approval before proceeding]

Resource or Cost Exposure:
[None / estimate / known approved amount / unknown]

Success Measures:
[How progress or outcome will be assessed]

Contingency or Recovery:
[Fallback options, hold points, or recovery actions]

Next Safe Step:
[Research / draft / confirm facts / request approval / manual validation]

Execution Status:
[No external action taken]
```

## Workstream Rules

A workstream must include:

- Purpose
- Owner or owner gap
- Inputs
- Output
- Dependencies
- Decision or approval gate
- Risk level
- Earliest safe next step

Do not assign a person or team without Founder confirmation. If ownership is
unknown, state `Owner: To be confirmed`.

## Dependency Rules

For each dependency, identify:

| Field | Requirement |
|---|---|
| Dependency | Exact prerequisite |
| Type | Decision / Information / Access / Budget / Contract / Asset / Vendor / Talent / Platform / Legal / Other |
| Owner | Named owner or `To be confirmed` |
| Required By | Date or planning phase |
| Status | Unknown / Pending / In progress / Confirmed / Blocked |
| Impact if Delayed | Low / Medium / High |
| Evidence | Source or record |
| Next Safe Step | Research / request confirmation / request approval / hold |

Never treat a dependency as resolved because it is expected, customary, publicly
mentioned, or previously available.

## Milestone Rules

Milestones must be observable and should not imply completed external action.

Use milestones such as:

- Source and scope confirmed
- Founder decision requested
- Founder decision recorded
- Draft prepared
- Rights verified
- Manual workflow validated
- Approved plan ready for execution
- Post-execution verification pending

Avoid milestones such as:

- Contract signed
- Campaign launched
- Tickets on sale
- Venue booked
- Payment completed
- Integration live

unless a separate approved record confirms completion.

## Risk Management

Assess each risk using:

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
[Observable signal]

Mitigation:
[Preparation or reduction measure]

Contingency:
[Fallback or hold action]

Escalation Trigger:
[When Founder review is required]

Owner:
[Named owner or To be confirmed]

Status:
[Open / Monitoring / Mitigated / Accepted / Closed]
```

Do not label a risk mitigated without evidence.

## Decision and Approval Gates

Every plan must identify decisions requiring Founder approval, including:

- Strategy selection
- Budget or financial exposure
- Contractual or legal commitments
- Brand identity or public claims
- Partner, sponsor, venue, talent, vendor, or customer commitments
- Ticketing, streaming, website, marketing, or publishing actions
- Access, integration, automation, infrastructure, or system changes
- Use of restricted data or third-party assets
- Changes to scope, timing, cost, or risk

For each gate, use the approval format defined in:

```text
skills/kage-governance-and-approval/SKILL.md
```

A plan may be drafted without approval. Execution may not begin merely because a
plan exists.

## Handling Changes

When a material plan input changes:

1. Identify the changed fact, assumption, scope, cost, dependency, timing, risk,
   owner, or external party.
2. Assess downstream effects.
3. Mark affected milestones and decisions as pending review.
4. Update the plan as a new draft version.
5. Request renewed Founder approval if the approved scope materially changes.
6. Do not continue external execution beyond the previously approved scope.

## Output Format

Use this concise planning assessment when full plan detail is not needed:

```text
Objective:
[Goal]

Current Status:
[Draft / Proposed / Approved / Deferred / Blocked]

Confirmed Facts:
[Source-backed facts]

Assumptions:
[Explicit assumptions]

Recommended Plan:
[High-level workstreams and milestones]

Key Dependencies:
[Most important prerequisites]

Key Risks:
[Most important risks]

Founder Decisions Required:
[Decisions and approval gates]

Next Safe Step:
[Research / draft / confirm / request approval]

Execution Status:
[No external action taken]
```

## Safety Rules

- Never invent facts, budgets, dates, owners, commitments, approvals, or
  dependencies.
- Never treat a plan as an approval.
- Never treat a milestone as evidence that an external action occurred.
- Never assign people, commit spending, or contact parties without approval.
- Never hide a dependency, unresolved decision, or material risk.
- Never use false precision for estimates or timelines.
- Never execute external work under this skill.
- Never include secrets, personal data, financial details, contracts, or
  restricted operational information in planning artifacts without authorized,
  minimum-necessary handling.

## Dependencies

- `skills/kage-source-of-truth/SKILL.md`
- `skills/kage-governance-and-approval/SKILL.md`
- `skills/kage-research-and-source-verification/SKILL.md`
- `skills/kage-brand-and-creative-governance/SKILL.md`
- `SECURITY.md`
- `CONTRIBUTING.md`
- `ARCHITECTURE.md`
- Approved Founder directives and canonical Kage records

## Testing

Test this skill using synthetic scenarios only.

Minimum synthetic test cases:

1. A fictional event objective with missing venue confirmation.
2. A fictional campaign plan with an unapproved budget assumption.
3. A fictional sponsor plan dependent on a contract and approved brand assets.
4. A fictional ticketing plan with a target on-sale date but no platform access.
5. A fictional streaming plan with unresolved distribution rights.
6. A fictional production plan with a safety dependency and tight deadline.
7. A fictional website plan with unknown domain and hosting ownership.
8. A material change to an already fictional Founder-approved plan.

Expected behavior:

- Separates facts, assumptions, gaps, and recommendations.
- Identifies workstreams, dependencies, risks, milestones, and decision gates.
- Does not assign owners or imply commitments without confirmation.
- Requires renewed approval for material scope changes.
- Uses safe, non-executing milestones.
- Avoids external actions and real Kage data.
- Keeps execution status as `No external action taken`.

## Change Control

Changes require:

1. Founder approval
2. Security, privacy, legal, rights, and financial review where applicable
3. Updated changelog entry
4. Synthetic-data validation
5. Confirmation that the skill remains non-executing unless separately approved
