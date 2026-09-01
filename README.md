# Kage Agency HQ

Founder-controlled engineering architecture, skills, agent specifications,
governance, schemas, workflows, and technical documentation for
THE KAGE PRESENTS.

> **Repository name note:** This repository was renamed from
> `kage-agency-hq` to `kage-os` on August 26, 2026 (KAGE-DEC-036). Same
> repository, same history — GitHub auto-redirects the old name. Internal
> documents may still refer to it as "Kage Agency HQ"; that is the system's
> name, not the repository's current URL.

## Purpose

This repository is the engineering source of truth for the future Kage Agency HQ
system.

It will eventually contain:

- Governance policies and approval controls
- Kage skill specifications
- Founder Command and specialist-agent definitions
- Data schemas and validation models
- Manual workflow specifications
- Future MCP and connector policies
- Technical architecture and implementation documentation
- Synthetic test cases and safety-validation records
- Third-party source, license, and provenance notes

## Source-of-Truth Model

Business, brand, creative, operational, commercial, and asset source material
remains in the canonical Kage Google Drive root:

```text
THE KAGE
Folder ID: 1KBwj0yKCznlE4MNNJwzyf43qo-7zdJUE
```

This GitHub repository is the engineering source of truth only.

## Operating Rule

```text
REQUEST
→ UNDERSTAND
→ RESEARCH
→ PLAN
→ FOUNDER APPROVAL
→ EXECUTE
→ VERIFY
→ LOG
```

Founder retains final approval authority for all Kage decisions, integrations,
automation, external actions, financial commitments, publishing, outreach, and
irreversible changes.

## Current Status

```text
EXECUTION PHASE 1 — SCOPED AUTONOMOUS EXECUTION (KAGE-DEC-020, AUGUST 24, 2026)
```

Supersedes the prior FOUNDATION BUILD — NO AUTONOMOUS EXECUTION phase.
Autonomous authority in this phase is limited to exactly:

1. Reading, searching, classifying, reconciling, indexing, organizing,
   creating, renaming, editing, moving, archiving, and versioning Kage-native
   drafts, documentation, templates, registers, source maps, specifications,
   and configuration.
2. Git branches, commits, pull requests, issues, labels, documentation,
   tests, scripts, and non-production configuration in this repository only,
   plus local commands, package managers, formatters, linters, builds, and
   test suites. Self-merge to this repository's default/protected branch is
   explicitly excluded — merges require Founder's explicit confirmation each
   time.
3. Drive write limited to the canonical THE KAGE root and its descendants —
   no account-wide or Drive-wide search or write.

No production code, live agents, MCP servers, automation, databases, website
integrations, ticketing integrations, streaming integrations, external APIs,
deployment workflows, or external execution is active. Every item on this
Project's "Always Blocked Without Specific Founder Approval" list remains in
force without exception.

## Security Rule

Do not commit or paste into this repository:

- Passwords
- Raw Google Drive exports
- Contracts
- Fighter, talent, sponsor, customer, or vendor private data
- Unapproved third-party code
- Production configuration files containing secrets

Do not add a connector, MCP server, automation, deployment, browser tool,
scraper, crawler, agent runtime, database connection, ticketing integration,
website integration, streaming integration, email system, social system, payment
system, or external API without explicit Founder approval.

## Repository Structure

```text
governance/  → policies, approval gates, safety controls, audit standards
skills/      → versioned Kage instruction packages
agents/      → Founder Command and specialist-agent definitions
mcp/         → future MCP specifications and connector policies
schemas/     → data models, validation rules, classifications
workflows/   → manual and future automation workflow specifications
references/  → source metadata, licenses, attribution, adaptation notes
docs/        → technical architecture, runbooks, implementation plans
tests/       → synthetic tests and expected safe outputs
archive/     → superseded technical material; never active source
```

## Contribution Rule

All substantive changes require Founder approval and must include:

1. Required business capability
2. Source of truth
3. Permitted and prohibited data
4. Minimum required permissions
5. Approval gate
6. Synthetic-data test plan
7. Rollback or recovery method
8. Source attribution and license notes where relevant
9. Changelog entry

## Repository Status

**Public**, confirmed live August 26, 2026 (KAGE-DEC-033, executing the
visibility change approved in principle at KAGE-DEC-015). Owner
`thekagepresents` is a personal GitHub User account, not an organization.
A native Claude/claude.ai GitHub connector for this repository is
Founder-approved (KAGE-DEC-013) but not yet technically connected in any
session; a separate Composio-mediated GitHub connection is active and is
what performed the rename and this update (see KAGE-DEC-033/034/036).

Known open item: secret scanning and secret-scanning push protection are
currently disabled on this repository. An API attempt to enable them did
not take effect; enabling them requires Founder's own manual toggle under
Settings → Code security.
