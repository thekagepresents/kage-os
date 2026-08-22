# Contributing to Kage Agency HQ

## Purpose

This repository is the engineering source of truth for the Kage Agency HQ
system. All material added here must support a documented Kage business
capability and remain aligned with Founder-controlled governance.

## Founder Approval Rule

All substantive changes require Founder approval before they are committed,
merged, installed, connected, activated, executed, or used in a Kage project.

A substantive change includes:

- New or revised skills
- New or revised agent definitions
- MCP or connector specifications
- Schema changes
- Workflow changes
- Automation proposals
- Third-party references or dependencies
- Code, scripts, packages, or configuration
- Security-policy changes
- Data-model changes
- External-system integrations
- Production or deployment changes

## Required Proposal Before Addition

Before adding any substantive material, document:

1. Capability needed
2. Business problem addressed
3. Intended users and workstreams
4. Source of truth
5. Permitted data
6. Prohibited data
7. Minimum permissions required
8. External systems involved
9. Risk assessment
10. Approval gate
11. Test plan using synthetic data only
12. Rollback, failure, or recovery plan
13. Owner
14. Version and changelog entry
15. Source attribution and license notes, if applicable

## Contribution Standards

Every approved addition must:

- Use clear filenames and folders.
- State its purpose and owner.
- State its status:
  DRAFT / PROPOSED / APPROVED / DEPRECATED / ARCHIVED.
- Avoid business secrets and private data.
- Avoid unsupported facts, claims, or implementation assumptions.
- Identify dependencies.
- Include an approval gate where an external or irreversible action is possible.
- Include safe failure behavior.
- Be reviewed against SECURITY.md.
- Update CHANGELOG.md.

## Data and Secret Prohibition

Never commit:

- Passwords
- API keys
- Tokens
- Cookies
- Recovery codes
- Payment details
- Private personal data
- Fighter, talent, sponsor, attendee, partner, vendor, or customer data
- Contracts
- Invoices
- Private financial records
- Raw Google Drive exports
- Unapproved third-party code
- Production secrets or configuration files

## Third-Party Material

Do not copy, clone, install, execute, or adapt third-party material without:

1. Confirming the source.
2. Recording the license.
3. Reviewing commercial-use compatibility.
4. Reviewing security and privacy implications.
5. Preserving attribution requirements.
6. Creating a synthetic-data test plan.
7. Receiving Founder approval.

Public availability does not equal approval for Kage use.

## Branch and Change Policy

During foundation build:

- Commit directly to `main` only for Founder-approved foundational documents.
- Do not create branches, pull requests, GitHub Actions, releases, tags, or
  automated deployment workflows.
- Do not add collaborators.
- Do not connect external services.

A branch-and-review workflow may be established later after Founder approval.

## Current Status

FOUNDATION BUILD — CONTRIBUTIONS LIMITED TO FOUNDER-APPROVED GOVERNANCE,
DOCUMENTATION, AND NON-EXECUTING SPECIFICATIONS.
