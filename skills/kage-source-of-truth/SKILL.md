# Kage Source of Truth Skill

## Status

PROPOSED — NON-EXECUTING SPECIFICATION

## Purpose

This skill helps Kage Agency HQ classify information, identify the appropriate
source of truth, distinguish confirmed facts from unverified material, and
prevent unsupported assumptions.

It does not access external systems, modify records, send communications,
publish content, make decisions, approve actions, or execute work.

## Owner

Founder

## Scope

Use this skill when a request involves:

- Business facts
- Brand facts
- Event information
- Ticketing information
- Financial information
- Fighter or talent information
- Sponsor, partner, vendor, customer, or attendee information
- Contracts or legal materials
- Creative assets
- Operational plans
- Engineering specifications
- Approval status
- Conflicting information across Kage systems

## Source-of-Truth Hierarchy

Apply the following hierarchy unless Founder explicitly approves an exception.

### 1. Founder Directive

A current, explicit Founder instruction is authoritative for the decision or
task it covers.

A Founder directive does not silently overwrite canonical records. The
resulting approved change must be recorded in the applicable canonical system.

### 2. Kage Business Source of Truth

Canonical Kage Google Drive root:

```text
THE KAGE
Folder ID: 1KBwj0yKCznlE4MNNJwzyf43qo-7zdJUE
```

Google Drive is authoritative for approved Kage business records, including:

- Confirmed facts
- Business decisions
- Brand assets
- Creative materials
- Event records
- Operational documents
- Financial records
- Contracts
- Partner and sponsor materials
- Approved project deliverables

### 3. Kage Project Context

Claude Project:

```text
THE KAGE PRESENTS — AGENCY HQ
```

Claude Project is authoritative for active project instructions, curated Kage
Brain knowledge, project-specific operating context, and Founder-approved
working guidance.

Claude Project does not replace canonical business records held in Google Drive.

### 4. Kage Engineering Source of Truth

Private GitHub repository:

```text
thekagepresents/kage-agency-hq
```

GitHub is authoritative for:

- Engineering architecture
- Governance specifications
- Skill specifications
- Agent specifications
- MCP and connector specifications
- Schemas
- Workflows
- Technical documentation
- Synthetic tests
- Engineering change history

GitHub is not authoritative for live business facts, financial records,
contracts, credentials, customer data, or operational production data.

### 5. External Sources

External sources may inform research but are not authoritative for Kage facts
unless verified, approved, and recorded in the appropriate Kage canonical
system.

Examples include:

- Search engines
- Websites
- Social platforms
- Ticketing platforms
- Vendor portals
- Media coverage
- Public databases
- Third-party reports
- AI-generated content

## Classification Rules

Classify each material claim, datum, or instruction as one of the following.

| Classification | Meaning | Permitted Use |
|---|---|---|
| Confirmed Fact | Verified in a canonical Kage source or explicitly confirmed by Founder | May be used as fact with source reference |
| Founder Directive | Explicit instruction or decision from Founder | May guide work within its stated scope |
| Approved Plan | Founder-approved future action or strategy | May guide preparation; execution still requires applicable approval |
| Draft | Proposed, incomplete, or working material | May be analyzed or improved; not presented as final |
| Research Finding | Information from external or non-canonical sources | Must be labeled and verified before use as Kage fact |
| Assumption | Unverified interpretation used to move planning forward | Must be explicit, minimal, and submitted for confirmation |
| Conflict | Material disagreement between sources | Must be surfaced; do not resolve silently |
| Restricted Information | Sensitive, personal, financial, contractual, credential, or private material | Do not reproduce or distribute beyond approved access |
| Unknown | Information cannot be established from available sources | State that it is unknown; do not infer |

## Required Handling

For every request involving Kage information:

1. Identify the claim, decision, or record needed.
2. Identify the expected source of truth.
3. Determine whether the source is available and current.
4. Classify the information.
5. State conflicts, unknowns, and assumptions clearly.
6. Cite or name the source when presenting confirmed facts.
7. Separate facts from recommendations, drafts, and research.
8. Request Founder confirmation when the information affects money, contracts,
   access, publishing, ticketing, talent, partners, customers, brand use,
   external communication, or irreversible action.
9. Do not execute external actions.

## Conflict Resolution

When sources conflict:

1. Do not choose a version silently.
2. Record the conflicting claims and their sources.
3. Prefer a current explicit Founder directive for immediate guidance.
4. Identify the canonical record that needs updating.
5. Request Founder confirmation when a decision is required.
6. Treat the conflict as unresolved until the appropriate canonical record is
   updated or Founder provides a documented instruction.

## Output Format

When using this skill, produce a concise source-of-truth assessment:

```text
Request:
[What information or decision is needed]

Classification:
[Confirmed Fact / Founder Directive / Draft / Research Finding / Assumption /
Conflict / Restricted Information / Unknown]

Expected Source of Truth:
[Founder / Google Drive / Claude Project / GitHub / External Source]

Available Evidence:
[Source name, document, record, or instruction]

Confidence:
[High / Medium / Low]

Conflicts or Gaps:
[None or description]

Permitted Next Step:
[Research / Draft / Request confirmation / Update canonical record after approval]

Execution Status:
[No external action taken]
```

## Safety Rules

- Never invent Kage facts.
- Never treat a draft as approved.
- Never treat an external source as a canonical Kage record without verification.
- Never expose restricted information unnecessarily.
- Never commit secrets, credentials, personal data, contracts, or financial data.
- Never use this skill to authorize external actions.
- Never infer approval from silence, prior use, public availability, or partial context.
- Never overwrite a canonical record without Founder approval.

## Dependencies

- Founder directives
- Approved Kage Google Drive materials
- Approved Claude Project context
- Approved GitHub engineering documentation

## Testing

Test this skill using synthetic scenarios only.

Minimum synthetic test cases:

1. A confirmed event date in an approved Drive record.
2. A public website date that conflicts with the approved Drive record.
3. A draft sponsor proposal presented as if it were approved.
4. A Founder instruction that requires a canonical record update.
5. An unknown ticketing detail with no available source.
6. A request containing restricted personal or financial information.

Expected behavior:

- Correctly classify each item.
- Identify the appropriate source of truth.
- Surface conflicts and unknowns.
- Avoid unsupported claims.
- Avoid all external execution.

## Change Control

Changes require:

1. Founder approval
2. Security review where applicable
3. Updated version or changelog entry
4. Synthetic-data validation
5. Confirmation that the skill remains non-executing unless separately approved
