# Kage Brand and Creative Governance Skill

## Status

PROPOSED — NON-EXECUTING SPECIFICATION

## Purpose

This skill governs Kage brand identity, creative work, asset status, source
control, review, approval, attribution, and public-use permissions.

It ensures that creative materials are not treated as official, final,
licensed, or approved before the necessary Founder decision and record exist.

It does not generate, publish, upload, edit, distribute, license, purchase,
approve, or otherwise execute creative work.

## Owner

Founder

## Scope

Use this skill for:

- Brand identity
- Brand strategy
- Naming
- Logos
- Wordmarks
- Typography
- Color systems
- Visual direction
- Creative concepts
- Campaign concepts
- Event identities
- Posters
- Social content
- Website creative
- Photography
- Video
- Audio
- Motion graphics
- Streaming graphics
- Merchandise creative
- Sponsor creative
- Fighter and talent creative
- Third-party assets
- AI-generated creative material
- Creative approvals and version control

## Governing Principle

Founder owns and controls Kage identity, public representation, creative
direction, and authorization for brand use.

A creative file, mockup, public reference, prior asset, AI-generated output,
third-party asset, or draft does not constitute approved Kage brand material.

No public, commercial, partner, sponsor, talent, ticketing, streaming, website,
social, paid-media, merchandise, or external use is authorized without explicit
Founder approval.

## Asset Statuses

| Status | Meaning | Permitted Use |
|---|---|---|
| Reference | External or historical material used for inspiration or comparison | Internal review only; rights and attribution must be checked |
| Research | Material gathered to inform a decision | Internal analysis only |
| Concept | Early directional idea | Internal discussion only |
| Draft | Incomplete or proposed creative work | Internal review only |
| Review | Submitted for Founder or designated review | No external use |
| Approved | Explicitly approved by Founder for a defined scope | Use only within recorded scope and conditions |
| Superseded | Replaced by a later approved version | Do not use unless Founder re-approves |
| Deprecated | No longer authorized | Do not use |
| Restricted | Contains private, sensitive, contractual, talent, partner, or unreleased material | Access-controlled internal handling only |
| Unknown | Status, owner, source, rights, or approval cannot be established | Do not use externally |

## Required Asset Record

Before an asset is treated as approved or used externally, record:

```text
Asset Name:
[Name]

Asset Type:
[Logo / Poster / Image / Video / Audio / Copy / Template / Other]

Version:
[Version identifier]

Status:
[Reference / Research / Concept / Draft / Review / Approved / Superseded /
Deprecated / Restricted / Unknown]

Purpose:
[Intended use]

Owner:
[Founder or approved rights holder]

Creator:
[Creator or source, if known]

Source Location:
[Canonical Kage record or external source]

Rights and License:
[Owned / Licensed / Permission pending / Unknown]

Attribution Requirement:
[None / required wording / unknown]

Approved Scope:
[Exact approved channels, audience, geography, dates, campaign, or project]

Restrictions:
[Edits, derivatives, placement, expiration, partner use, paid media, talent use,
or other limits]

Founder Approval Evidence:
[Record location or pending]

Last Reviewed:
[YYYY-MM-DD]

External Use Status:
[Not authorized / Authorized within scope / Expired / Unknown]
```

Do not invent ownership, rights, approval evidence, or asset status.

## Creative Review Workflow

Use this sequence:

```text
REQUEST
→ SOURCE CHECK
→ RIGHTS AND LICENSE CHECK
→ STATUS CLASSIFICATION
→ CONCEPT OR DRAFT
→ INTERNAL REVIEW
→ FOUNDER APPROVAL
→ RECORD APPROVED SCOPE
→ EXTERNAL USE, IF SEPARATELY AUTHORIZED
→ VERSION AND ARCHIVE CONTROL
```

At every stage, distinguish:

- Reference material from Kage-created work
- Concept from draft
- Draft from approved asset
- Approved asset from approval for a specific public use
- Ownership from license
- License from permission for a specific channel, audience, territory, term, or
  paid use

## Founder Approval Requirements

Explicit Founder approval is required before:

- Establishing or changing Kage brand identity
- Approving names, logos, wordmarks, visual systems, messaging, taglines, or
  event identities
- Publishing, posting, printing, broadcasting, distributing, or scheduling
  creative material
- Using a creative asset in ticketing, website, social, paid media, streaming,
  merchandise, sponsor, partner, venue, talent, press, email, SMS, or public
  materials
- Sharing brand assets with an external party
- Licensing, purchasing, commissioning, adapting, or using third-party assets
- Using AI-generated outputs externally
- Representing a sponsor, partner, fighter, talent, venue, vendor, or customer
  in creative material
- Retiring, replacing, or materially changing an approved asset

Approval must specify the asset version and intended scope. If scope changes,
renewed approval is required.

## Third-Party and AI Material

For third-party or AI-generated material:

1. Identify the source or generation method.
2. Identify known ownership, license, and attribution terms.
3. Identify whether commercial use, modification, paid promotion, sublicensing,
   trademark use, talent likeness, and platform use are permitted.
4. Treat unknown rights as not authorized.
5. Do not remove watermarks, credits, or rights notices.
6. Do not use names, likenesses, logos, copyrighted work, or protected marks
   without appropriate permission and approval.
7. Obtain Founder approval before any external use.
8. Record the decision and approved scope.

Public availability, an AI tool output, a search result, or a social post does
not establish permission to use creative material.

## Brand Claim Controls

Before a creative asset includes a claim about Kage, an event, ticketing,
talent, sponsor, partner, venue, streaming, availability, pricing, results,
performance, or product:

1. Verify the claim using `kage-source-of-truth`.
2. Verify research-originated claims using
   `kage-research-and-source-verification`.
3. Classify the asset as draft until approval.
4. Request explicit Founder approval before external use.

## Version Control

- Use a distinct asset name and version identifier.
- Preserve approved versions and their approval evidence.
- Do not overwrite an approved asset without a new version and approval record.
- Mark replaced assets as superseded rather than silently deleting them.
- Preserve required attribution and license information.
- Record expiration or campaign-end dates when applicable.
- Do not reuse an approved asset outside its recorded scope.

## Output Format

For a creative-governance assessment, use:

```text
Creative Request:
[What is requested]

Asset or Material:
[Name, type, and version if known]

Current Status:
[Asset status]

Source and Ownership:
[Canonical Kage source / creator / external source / unknown]

Rights and License:
[Known status and limitations]

Brand or Factual Claims:
[Claims included and verification status]

Proposed Use:
[Internal / external channel / audience / campaign / territory / duration]

Approval Required:
[Yes / No, with reason and approval class]

Required Next Step:
[Research / rights check / draft / internal review / request Founder approval]

External Use Status:
[Not authorized / authorized within scope / unknown]

Execution Status:
[No external action taken]
```

## Safety Rules

- Never treat a draft as an approved Kage asset.
- Never use a brand asset publicly without explicit Founder approval.
- Never claim ownership or permission without evidence.
- Never use third-party or AI-generated material externally when rights are
  unknown.
- Never remove credits, watermarks, ownership notices, or license information.
- Never represent a person, fighter, talent, sponsor, partner, venue, vendor, or
  customer without approval.
- Never publish, upload, distribute, print, broadcast, schedule, license,
  purchase, or modify external creative material by default.
- Never expose unreleased, restricted, personal, contractual, or private
  creative material.
- Never infer approval from previous use, public visibility, or silence.

## Dependencies

- `skills/kage-source-of-truth/SKILL.md`
- `skills/kage-governance-and-approval/SKILL.md`
- `skills/kage-research-and-source-verification/SKILL.md`
- `SECURITY.md`
- `CONTRIBUTING.md`
- Approved Founder directives and canonical Kage brand records

## Testing

Test this skill using synthetic scenarios only.

Minimum synthetic test cases:

1. A fictional logo marked as draft.
2. A fictional approved poster proposed for a new, unapproved campaign.
3. A fictional third-party photograph with no license stated.
4. A fictional AI-generated event image with an unknown commercial-use policy.
5. A fictional sponsor logo supplied for a campaign.
6. A fictional fighter likeness requested for social content.
7. A fictional public claim placed in a poster with incomplete source evidence.
8. A fictional old event identity marked as superseded.

Expected behavior:

- Correctly classify asset status.
- Distinguish internal draft work from external use.
- Identify rights, ownership, attribution, and scope gaps.
- Require explicit Founder approval for external brand use.
- Surface factual-claim verification requirements.
- Avoid generating, publishing, downloading, editing, licensing, or executing.
- Keep execution status as `No external action taken`.

## Change Control

Changes require:

1. Founder approval
2. Security, privacy, rights, and license review where applicable
3. Updated changelog entry
4. Synthetic-data validation
5. Confirmation that the skill remains non-executing unless separately approved
