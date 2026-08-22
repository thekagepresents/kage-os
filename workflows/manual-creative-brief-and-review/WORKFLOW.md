# Kage Manual Creative Brief and Review Workflow

## Status

PROPOSED — MANUAL — NON-EXECUTING

## Purpose

This workflow defines how Kage Agency HQ handles a Founder creative request from
initial brief through source review, rights assessment, factual-claim review,
concept or draft preparation, internal review, Founder approval recording, and
defined external-use scope.

It ensures that Kage creative material is not treated as approved, owned,
licensed, factually verified, or authorized for external use until the required
evidence and Founder decision exist.

This workflow does not generate, design, edit, download, upload, publish, print,
schedule, broadcast, distribute, license, purchase, commission, share, or use
creative material externally.

## Owner

Founder

## Trigger

Use this workflow when Founder requests or reviews:

- Brand identity work
- Naming, taglines, messaging, or event identity
- Logos, wordmarks, typography, color, or visual systems
- Creative concepts, briefs, mockups, posters, social content, website creative,
  ticketing creative, campaign creative, motion, video, audio, or streaming
  graphics
- Sponsor, partner, venue, fighter, talent, customer, vendor, or community
  creative
- Photography, illustration, third-party assets, AI-generated material, code
  samples, templates, or licensed creative
- Asset review, version approval, public-use authorization, replacement, or
  retirement
- Creative claims relating to event dates, ticketing, pricing, talent, sponsors,
  streaming, availability, performance, or other Kage facts

## Inputs

```text
Founder Creative Request:
[Request in Founder’s words]

Creative Objective:
[What the creative should achieve]

Intended Audience:
[Known audience / unknown]

Proposed Use:
[Internal / public channel / campaign / ticketing / website / print / sponsor /
partner / streaming / paid media / other]

Time Sensitivity:
[None / date / deadline / urgent]

Known Brand Direction:
[Founder directive, approved brand record, or unknown]

Known Asset Inputs:
[Approved asset references, drafts, third-party material, AI output, or none]

Known Factual Claims:
[Claims proposed for inclusion]

Known Rights or License Information:
[Owned / licensed / permission pending / unknown]

Known Constraints:
[Budget, format, dimensions, channel, geography, duration, partner, talent,
legal, accessibility, platform, or other limits]

Requested Outcome:
[Brief / concept / draft review / approval assessment / unknown]
```

If an input is unavailable, record it as unknown rather than inventing it.

## Workflow Overview

```text
RECEIVE CREATIVE REQUEST
→ SCREEN FOR RESTRICTED MATERIAL
→ DEFINE OBJECTIVE, AUDIENCE, AND USE
→ IDENTIFY BRAND SOURCE OF TRUTH
→ CLASSIFY ASSET STATUS
→ CHECK OWNERSHIP, RIGHTS, LICENSE, ATTRIBUTION, LIKENESS, AND PARTNER TERMS
→ VERIFY FACTUAL CLAIMS
→ PREPARE INTERNAL BRIEF OR DRAFT ASSESSMENT
→ ASSIGN VERSION AND REVIEW STATUS
→ REQUEST FOUNDER APPROVAL FOR DEFINED EXTERNAL SCOPE
→ RECORD APPROVAL STATUS
→ STOP WITHOUT CREATIVE OR EXTERNAL EXECUTION
```

## Step 1 — Receive and Define Request

1. Restate the creative request concisely.
2. Identify objective, audience, intended use, channel, campaign, geography,
   dates, duration, format, and delivery needs where supplied.
3. Identify whether the requested output is a brief, concept, draft review,
   asset-status assessment, approval request, or external action.
4. Identify missing scope details.
5. Do not infer brand direction, approval, ownership, license, format, cost,
   creator, audience, timing, channel, or public-use permission.

**Output**

```text
Creative Request:
[Concise restatement]

Creative Objective:
[Known objective]

Intended Audience:
[Known / unknown]

Proposed Use:
[Known use and scope]

Requested Outcome:
[Brief / concept / draft review / approval assessment / other]

Scope Gaps:
[None or description]
```

## Step 2 — Screen for Restricted Material

Check whether the request includes:

- Unreleased Kage brand, event, commercial, strategy, campaign, talent, sponsor,
  partner, customer, vendor, ticketing, or streaming material
- Personal data, likeness releases, talent agreements, contracts, payment data,
  confidential briefs, or credentials
- Private third-party creative files or licensed material
- Sensitive legal, financial, health, or identity information

If restricted material is present:

1. Mark it as restricted.
2. Use minimum necessary detail.
3. Do not reproduce, store, share, upload, download, or distribute it.
4. Identify access, rights, privacy, and approval requirements.
5. Limit output to a safe internal assessment.

**Output**

```text
Restricted Material:
[None / present]

Safe Handling:
[No sensitive or private values reproduced; authorized handling required /
not applicable]
```

## Step 3 — Identify Brand and Asset Source of Truth

Apply `kage-source-of-truth` and
`kage-brand-and-creative-governance`.

1. Identify any current Founder directive.
2. Identify the canonical Kage brand or creative record, if available.
3. Identify asset name, type, version, creator, source, and status.
4. Classify asset status:
   - Reference
   - Research
   - Concept
   - Draft
   - Review
   - Approved
   - Superseded
   - Deprecated
   - Restricted
   - Unknown
5. Identify conflicts between requested material and current approved identity.
6. Do not treat a prior asset, a public asset, a draft, a social post, a
   third-party file, or AI output as approved by default.

**Output**

```text
Brand Source of Truth:
[Founder directive / canonical record / unknown]

Asset or Material:
[Name, type, version, source]

Current Status:
[Asset status]

Conflicts:
[None or description]

External Use Status:
[Not authorized / authorized within recorded scope / expired / unknown]
```

## Step 4 — Check Rights, License, Attribution, and Representation

For each material asset, source, or person represented:

1. Identify ownership and creator.
2. Identify license, permitted uses, term, territory, modification rights,
   commercial-use rights, paid-media rights, sublicensing, attribution, and
   platform limitations.
3. Identify trademark, logo, sponsor, partner, venue, talent, likeness, music,
   video, photography, code, template, or third-party-content requirements.
4. Treat unknown rights as not authorized.
5. Do not remove watermarks, credits, ownership notices, or license terms.
6. Do not use names, likenesses, logos, protected marks, copyrighted material,
   or third-party assets without appropriate permission and Founder approval.
7. Identify rights-expiration or review date if known.

**Output**

```text
Source and Ownership:
[Known / unknown]

Rights and License:
[Owned / licensed / permission pending / unknown]

Attribution:
[Required / none known / unknown]

Representation or Likeness:
[Permission confirmed / pending / unknown / not applicable]

Rights Gaps:
[None or description]

Permitted Internal Use:
[Yes / No / limited]

External Use Status:
[Not authorized unless explicit scope approval exists]
```

## Step 5 — Verify Factual Claims

For each proposed creative claim:

1. Identify the exact claim.
2. Apply `kage-source-of-truth`.
3. Apply `kage-research-and-source-verification` when the claim relies on
   external research.
4. Classify the claim:
   - Confirmed Fact
   - Founder Directive
   - Approved Plan
   - Draft
   - Research Finding
   - Assumption
   - Conflict
   - Unknown
5. Identify source, date, confidence, conflicts, and required confirmation.
6. Do not include unverified claims in an externally authorized scope.
7. Do not treat a creative layout as evidence that a claim is true.

**Output**

| Proposed Claim | Classification | Evidence | Confidence | External Use Status | Required Next Step |
|---|---|---|---|---|---|
| [Claim] | [Type] | [Source / gap] | [High / Medium / Low] | [Not authorized / pending] | [Verify / revise / approval] |

## Step 6 — Prepare Internal Creative Brief
