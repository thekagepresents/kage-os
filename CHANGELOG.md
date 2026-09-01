# Changelog

This file records approved changes to the Kage Agency HQ engineering repository.

It does not replace:

- The Kage business Decision Log
- The Kage Confirmed Facts document
- The Kage commercial, creative, ticketing, event, or operating registers
- Founder approvals recorded in the canonical Kage Drive

## 0.2.0 — 2026-08-26

### Changed

- Repository renamed: `thekagepresents/kage-agency-hq` →
  `thekagepresents/kage-os`. Same repository (ID unchanged), full commit
  history, files, issues, and PRs preserved — a rename, not a re-creation.
  GitHub auto-redirects the old URL. See KAGE-DEC-036.
- Visibility confirmed **public** (live-verified via the active
  Composio-mediated GitHub connection), executing the change approved in
  principle at KAGE-DEC-015. See KAGE-DEC-033.
- Phase Gate advanced: FOUNDATION BUILD — NO AUTONOMOUS EXECUTION →
  **EXECUTION PHASE 1 — SCOPED AUTONOMOUS EXECUTION**. See KAGE-DEC-020
  (August 24, 2026) for the exact three-part scope now in force.

### Attempted, Did Not Take

- Enabling secret scanning and secret-scanning push protection via the
  GitHub API: both calls reported success, but a read-back showed both
  settings still disabled. Cause not yet diagnosed (possible token-scope
  limitation). Still requires Founder's own manual toggle under
  Settings → Code security. See KAGE-DEC-033/036.

### Notes

- Repository is now public (was private at 0.1.0).
- No client, financial, talent, sponsor, ticketing, customer, vendor, contract,
  credential, payment, or private operational data has been added.

## 0.1.0 — 2026-08-22

### Added

- Private GitHub organization:
  `thekagepresents`
- Private engineering repository:
  `kage-agency-hq`
- Foundation folders:
  - `governance/`
  - `skills/`
  - `agents/`
  - `mcp/`
  - `schemas/`
  - `workflows/`
  - `references/`
  - `docs/`
  - `tests/`
  - `archive/`
- Root repository documentation:
  - `README.md`
  - `SECURITY.md`
  - `CONTRIBUTING.md`
  - `ARCHITECTURE.md`
  - `CHANGELOG.md`

### Controls Established

- Google Drive remains Kage business source of truth.
- GitHub is Kage engineering source of truth.
- Founder retains final approval authority.
- External execution remains disabled.
- No production code, connectors, MCP servers, agents, automation, secrets,
  external APIs, website systems, ticketing systems, streaming systems, or
  deployment workflows are active.
- Third-party code and tools require review, attribution, synthetic testing,
  and Founder approval before adoption.

### Notes

- Repository was private at this version (see 0.2.0 for the visibility change).
- Foundation-build documentation only at this version (see 0.2.0 for the
  Phase Gate advance).
- No client, financial, talent, sponsor, ticketing, customer, vendor, contract,
  credential, payment, or private operational data has been added.
