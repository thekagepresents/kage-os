# Kage Manual Research Brief Workflow

## Status

PROPOSED — MANUAL — NON-EXECUTING

## Purpose

This workflow defines how Kage Agency HQ turns a Founder research request into a
structured internal research brief.

It ensures that research questions are tied to a decision, sources are
evaluated, claims are separated from evidence, uncertainty is disclosed,
attribution and rights are considered, and research findings are not treated as
confirmed Kage facts without verification and Founder approval.

This workflow does not browse automatically, access external accounts, scrape,
contact sources, request quotes, negotiate, publish findings, update canonical
records, create tasks, or execute work.

## Owner

Founder

## Trigger

Use this workflow when Founder requests research involving:

- Venues
- Events
- Audiences
- Markets
- Competitors
- Sponsors
- Partners
- Vendors
- Fighters or talent
- Ticketing
- Tables or hospitality
- Streaming or broadcast
- Media
- Technology
- Platforms
- Website or digital products
- Marketing
- Community
- Finance or pricing
- Policies, regulations, rules, or requirements
- Public claims, statistics, dates, availability, pricing, or terms
- Third-party assets, content, code, templates, data, or services

## Inputs

```text
Founder Research Request:
[Question in Founder’s words]

Decision Context:
[Decision the research should inform]

Desired Output:
[Brief / comparison / options / verification plan / unknown]

Time Sensitivity:
[None / date / deadline / urgent]

Known Facts:
[Canonical-source facts only]

Known Constraints:
[Budget, scope, geography, brand, legal, privacy, rights, platform, access, or
other limits]

Known Sources:
[None or identified records, websites, documents, reports, contacts, or other
sources]

Requested Claim or Question:
[Exact claim to verify or question to answer]
```

If inputs are incomplete, record the gap rather than inventing the research
scope, decision, or criteria.

## Workflow Overview

```text
RECEIVE RESEARCH REQUEST
→ DEFINE DECISION QUESTION
→ SCREEN FOR RESTRICTED INFORMATION
→ IDENTIFY SOURCE-OF-TRUTH CONTEXT
→ DEFINE CLAIMS AND RESEARCH BOUNDARIES
→ SELECT SOURCE TYPES AND EVALUATION CRITERIA
→ PREPARE RESEARCH BRIEF
→ IDENTIFY VERIFICATION, RIGHTS, RISK, AND APPROVAL NEEDS
→ PRESENT FINDINGS AS RESEARCH ONLY
→ REQUEST FOUNDER DECISION WHERE REQUIRED
→ STOP WITHOUT EXTERNAL ACTION
```

## Step 1 — Define the Research Question

1. Restate the Founder request concisely.
2. Identify the decision the research will inform.
3. Identify the exact question, claim, comparison, or option set.
4. Identify the time period, geography, audience, budget range, or other scope
   only when supplied or explicitly marked as unknown.
5. Identify what a useful answer would enable.
6. Do not infer that research authorizes a decision, outreach, booking, purchase,
   contract, public claim, or external action.

**Output**

```text
Research Question:
[Exact question]

Decision Context:
[Decision to be informed]

Desired Output:
[Brief / comparison / verification plan / other]

Scope:
[Known scope and explicit unknowns]

Decision Not Yet Made:
[What remains for Founder]
```

## Step 2 — Screen for Restricted Information

Check for:

- Credentials, passwords, tokens, API keys, payment details, or account access
- Personal, health, legal, contractual, talent, customer, vendor, sponsor,
  partner, or attendee information
- Private financial records, rates, invoices, budgets, bank data, or tax material
- Unreleased creative, strategy, commercial, event, or operational material
- Confidential third-party information or documents

If restricted information is present:

1. Mark it as restricted.
2. Use minimum necessary detail.
3. Do not reproduce sensitive values.
4. Do not upload, send, publish, share, or store the material.
5. State any access, privacy, legal, or Founder-approval requirement.
6. Limit the brief to safe, redacted planning guidance.

**Output**

```text
Restricted Information:
[None / present]

Safe Handling:
[No sensitive values reproduced; authorized handling required / not applicable]
```

## Step 3 — Establish Source-of-Truth Context

Apply `kage-source-of-truth`.

1. Identify Kage facts already established by canonical records or Founder
   directives.
2. Separate those Kage facts from external research questions.
3. Identify whether a proposed public claim needs confirmation.
4. Identify conflicts, assumptions, drafts, and unknowns.
5. Do not treat external sources as canonical Kage records.

**Output**

```text
Confirmed Kage Facts:
[Source-backed facts]

Founder Directives:
[Relevant instructions]

Research Questions:
[External matters to investigate]

Assumptions:
[Planning assumptions]

Unknowns or Conflicts:
[None or description]
```

## Step 4 — Define Research Boundaries

Define what research may and may not cover.

```text
In Scope:
[Specific questions, sources, markets, dates, categories, or comparisons]

Out of Scope:
[Actions, sensitive data, contact, negotiation, booking, purchase, contract,
publishing, external representation, or unrelated questions]

Permitted Evidence:
[Public official sources, approved documents, licensed reports, or other approved
source types]

Prohibited Evidence or Conduct:
[Unauthorized access, scraping, paywall circumvention, personal data collection,
unverified AI claims, hidden data, impersonation, or contact without approval]

Data Boundary:
[Minimum necessary categories]

Rights and Attribution Boundary:
[What must be checked before quoting, copying, using, or distributing material]
```

Do not expand the scope without Founder review when the change is material.

## Step 5 — Select Source Strategy

Apply `kage-research-and-source-verification`.

For each material claim or question:

1. Define the exact claim.
2. Identify the preferred source tier:
   - Tier 1: Primary or official
   - Tier 2: Credible independent
   - Tier 3: Secondary reporting
   - Tier 4: Community or promotional
   - Tier 5: Unverifiable or anonymous
3. Identify required publication or update date.
4. Identify corroboration needs.
5. Identify rights, license, attribution, privacy, and access considerations.
6. Identify any need for direct confirmation before material use.
7. Do not claim a source has been reviewed unless evidence is actually supplied.

**Output**

| Research Item | Preferred Source Tier | Date Needed | Corroboration Needed | Rights / Attribution Check | Risk |
|---|---|---|---|---|---|
| [Item] | [1–5] | [Date requirement] | [Yes / No / Why] | [Requirement] | [Low / Medium / High] |

## Step 6 — Prepare the Research Brief

Use this format:

```text
Research Brief Title:
[Title]

Status:
DRAFT — RESEARCH ONLY — NOT A CONFIRMED KAGE RECORD

Research Question:
[Exact question]

Decision Context:
[Decision the research informs]

Scope:
[In scope and out of scope]

Confirmed Kage Facts:
[Canonical-source facts only]

External Research Items:
[List of claims or questions]

Source Strategy:
[Source tiers, dates, corroboration, and access boundaries]

Evaluation Criteria:
[How alternatives or claims will be assessed]

Potential Sources:
[Named source types or known sources; do not imply access or review]

Evidence Required:
[What would support a conclusion]

Known Limitations:
[Missing data, source incentives, dated material, lack of access, scope limits]

Rights, License, and Attribution:
[Requirements and unknowns]

Risks:
[Research, privacy, legal, brand, financial, operational, or reputational risk]

Approval Requirements:
[What requires Founder approval before research expansion, contact, use, or action]

Recommended Safe Next Step:
[Review brief / provide source material / approve bounded research / request direct confirmation]

Execution Status:
No external action taken
```

## Step 7 — Evaluate Supplied Research Material

When Founder supplies a source, document, excerpt, claim, or finding:

1. Identify the source, title, date, and source tier if available.
2. State what the source directly supports.
3. State what it does not establish.
4. Identify conflicts, incentives, missing methodology, currency concerns, and
   rights limitations.
5. Classify the material:
   - Research Finding
   - Confirmed Fact
   - Assumption
   - Conflict
   - Unknown
   - Restricted Information
6. Assign confidence:
   - High
   - Medium
   - Low
7. Do not convert a research finding into a Kage fact unless verification and
   Founder-approved canonical recording occur.

**Output**

```text
Claim:
[Exact claim]

Source:
[Publisher, title, URL or record reference]

Date:
[Known / Unknown]

Source Tier:
[1 / 2 / 3 / 4 / 5]

What It Supports:
[Direct support only]

What It Does Not Establish:
[Limits]

Classification:
[Research Finding / Confirmed Fact / Assumption / Conflict / Unknown / Restricted]

Confidence:
[High / Medium / Low]

Permitted Use:
[Internal research / draft recommendation / request verification / request Founder approval]

Execution Status:
No external action taken
```

## Step 8 — Prepare Recommendations and Decision Options

Research may inform a recommendation but not make a decision.

When producing options:

1. Separate evidence from interpretation.
2. State the decision criteria.
3. Identify trade-offs, dependencies, risks, costs, and unknowns.
4. Avoid false precision.
5. State what evidence would change the recommendation.
6. Identify any public, financial, legal, rights, access, brand, contract, or
   external-communication approval gate.
7. Use `kage-governance-and-approval` for Class B or Class C actions.

**Output**

```text
Evidence Summary:
[Evidence-based findings]

Interpretation:
[Reasoned analysis, labeled]

Options:
[Option A / Option B / Option C]

Trade-Offs:
[Benefits, limitations, risks, dependencies]

Recommendation:
[Recommended option or no recommendation due to insufficient evidence]

Founder Decision Required:
[Specific decision / none]

Approval Class:
[A / B / C / D]

Execution Status:
No external action taken
```

## Step 9 — Handle Contact, Quotes, Access, or Public Use Requests

Research does not authorize:

- Contacting venues, vendors, sponsors, partners, talent, media, platforms, or
  customers
- Requesting quotes, proposals, availability, contracts, or access
- Booking holds, meetings, demos, or services
- Logging into external accounts
- Scraping, downloading, or copying restricted material
- Publishing or repeating public claims
- Using third-party assets, code, content, data, logos, names, or likenesses
- Updating canonical Kage records

If any of these are requested:

1. Stop research-only handling.
2. Classify the action under `kage-governance-and-approval`.
3. Prepare
