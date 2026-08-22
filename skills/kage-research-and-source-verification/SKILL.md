# Kage Research and Source Verification Skill

## Status

PROPOSED — NON-EXECUTING SPECIFICATION

## Purpose

This skill defines how Kage Agency HQ should research external information,
evaluate sources, distinguish evidence from opinion, disclose uncertainty, and
verify material claims before they are used as Kage facts.

It does not browse automatically, access external accounts, scrape websites,
contact sources, publish findings, update canonical records, or execute work.

## Owner

Founder

## Scope

Use this skill when work involves:

- Market, audience, venue, competitor, sponsor, partner, vendor, fighter,
  talent, ticketing, streaming, media, platform, or technology research
- Public claims, statistics, dates, prices, availability, rules, policies, or
  regulations
- External references, articles, websites, reports, social posts, or databases
- Research briefs and recommendations
- Source attribution
- Conflicting public information
- Fact-checking a proposed public, commercial, or operational claim

## Research Principles

- Define the decision or question before gathering information.
- Prefer primary, official, direct, and current sources.
- Separate observed facts from interpretation and recommendation.
- Do not represent public information as a confirmed Kage fact without
  verification and appropriate recording.
- Treat a source's publication as evidence of what that source says, not proof
  that every claim within it is true.
- State limits, gaps, conflicts, dates, and confidence.
- Use only the minimum information necessary for the purpose.
- Respect privacy, access restrictions, terms, licenses, and applicable law.
- Never use research to bypass Founder approval or source-of-truth controls.

## Source Tiers

| Tier | Source Type | Typical Examples | Default Confidence |
|---|---|---|---|
| 1 | Primary or official source | Official organization website, signed document, official filing, direct written confirmation, official platform policy | High, subject to currency and scope |
| 2 | Credible independent source | Established trade publication, reputable research organization, recognized industry body | Medium to high |
| 3 | Secondary reporting | News coverage, analyst commentary, interviews, summaries | Medium |
| 4 | Community or promotional source | Social posts, forums, fan pages, vendor marketing, unverified directories | Low to medium |
| 5 | Unverifiable or anonymous source | Unsourced claims, anonymous posts, screenshots without provenance, AI-generated material without source support | Low |

Source tier does not alone determine truth. Currency, relevance, independence,
corroboration, access, incentives, and directness must also be assessed.

## Verification Standard

Before using a research finding as a material Kage fact:

1. Define the exact claim.
2. Identify the source and publication or update date.
3. Determine the source tier.
4. Check whether the source is primary, current, and directly supports the claim.
5. Seek corroboration where material risk, cost, legal exposure, public impact,
   or uncertainty is significant.
6. Record contradictions or missing evidence.
7. Classify the result using `kage-source-of-truth`.
8. Obtain Founder approval before adding or changing a canonical Kage record.
9. Preserve attribution, license, and usage restrictions.

Material claims include claims affecting money, contracts, legal compliance,
public communications, ticketing, talent, partnerships, venues, safety,
reputation, brand use, production, streaming, or operational commitments.

## Research Output Format

Use the following format for a research assessment:

```text
Research Question:
[Decision or question being investigated]

Claim:
[Exact claim, separated from interpretation]

Finding:
[Concise evidence-based answer]

Source:
[Publisher, title, URL or record identifier]

Publication or Update Date:
[Date, if available]

Source Tier:
[1 / 2 / 3 / 4 / 5]

Evidence Type:
[Primary / Official / Independent reporting / Commentary / Promotional /
Community / Unknown]

Corroboration:
[None / Source names / Not required with reason]

Limitations:
[Currency, scope, access, conflicts, missing evidence, incentives, or unknowns]

Classification:
[Research Finding / Confirmed Fact / Assumption / Conflict / Unknown]

Confidence:
[High / Medium / Low]

Permitted Use:
[Internal research / Draft recommendation / Request verification /
Request Founder approval]

Execution Status:
[No external action taken]
```

## Attribution Rules

- Name the source for each material research finding.
- Preserve required attribution and license notices.
- Quote only what is necessary and permitted.
- Do not present copied third-party material as Kage-created work.
- Do not use an image, logo, video, document, template, code sample, dataset,
  or creative asset without reviewing rights and usage restrictions.
- Do not cite a source that was not actually reviewed.
- Do not use fabricated, incomplete, or unverifiable citations.
- Clearly distinguish direct quotation, paraphrase, synthesis, and opinion.

## Handling Conflicts

When credible sources conflict:

1. State the conflicting claims.
2. Identify each source, tier, and date.
3. Prefer a current primary or official source when it directly addresses the
   claim.
4. Do not conceal unresolved conflict.
5. Lower confidence where conflict remains.
6. Request direct confirmation or Founder guidance when the claim is material.
7. Do not update canonical Kage records until verification and approval are
   complete.

## Prohibited Research Conduct

- Do not access systems without authorization.
- Do not scrape, bypass paywalls, evade controls, or circumvent terms.
- Do not impersonate Kage, Founder, staff, talent, partners, customers, or
  vendors.
- Do not contact external parties without explicit Founder approval.
- Do not collect unnecessary personal, financial, health, legal, credential, or
  sensitive information.
- Do not treat AI output as evidence without source verification.
- Do not create fake citations, sources, quotes, documents, reviews, or data.
- Do not publish, send, or act on research without the required approval.
- Do not copy third-party material without license and attribution review.

## Safety Rules

- Research is not approval.
- A recommendation is not a decision.
- A public source is not automatically a Kage canonical source.
- Absence of evidence is not evidence of approval, availability, legality, or
  suitability.
- Time-sensitive claims must include source dates.
- High-impact claims require stronger verification.
- Unknowns must remain explicit.
- No external action is authorized by this skill.

## Dependencies

- `skills/kage-source-of-truth/SKILL.md`
- `skills/kage-governance-and-approval/SKILL.md`
- `SECURITY.md`
- `CONTRIBUTING.md`
- Approved Founder directives and canonical Kage records

## Testing

Test this skill using synthetic scenarios only.

Minimum synthetic test cases:

1. A fictional venue's official availability page.
2. Two conflicting fictional ticketing-price sources.
3. A fictional sponsor statistic from a vendor marketing page.
4. An undated fictional social-media claim.
5. A fictional industry report with a stated publication date.
6. A request to use a fictional third-party event image.
7. An AI-generated claim with no cited source.
8. A material fictional public claim requiring direct confirmation.

Expected behavior:

- Assign the appropriate source tier.
- Identify source date, evidence type, limits, and confidence.
- Separate research findings from confirmed Kage facts.
- Surface conflicts and avoid unsupported conclusions.
- Preserve attribution and license considerations.
- Require appropriate verification and Founder approval.
- Avoid external access, contact, publishing, and execution.

## Change Control

Changes require:

1. Founder approval
2. Security, privacy, and license review where applicable
3. Updated changelog entry
4. Synthetic-data validation
5. Confirmation that the skill remains non-executing unless separately approved
