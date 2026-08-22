# Security Policy

## Core Rule

No secrets, credentials, API keys, tokens, passwords, cookies, recovery codes,
payment data, private personal data, client-sensitive data, raw Drive exports,
contracts, financial records, or private commercial records may be committed to
this repository.

## Security Reporting

Report suspected exposure, unauthorized access, unsafe automation, connector
risk, credential risk, or policy violation directly to the Founder.

Do not open a public issue for a security concern.

## Access Control

- Repository remains private.
- Founder is the only collaborator during foundation build.
- No outside collaborator, contractor, vendor, developer, or agent receives
  access without explicit Founder approval.
- No shared credentials.
- No personal access token, SSH key, deploy key, OAuth app, GitHub App, or
  machine user is permitted without a documented business need and Founder
  approval.

## Connector and Execution Rule

No connector, MCP server, agent runtime, automation, browser tool, deployment,
database, external API, website integration, ticketing integration, streaming
integration, email, SMS, social, advertising, payment, or financial system may
be configured, authenticated, or activated without explicit Founder approval.

All future external-system actions must follow:

REQUEST
→ UNDERSTAND
→ RESEARCH
→ PLAN
→ FOUNDER APPROVAL
→ EXECUTE
→ VERIFY
→ LOG

## Third-Party Code and Tool Rule

Third-party code, packages, skills, plugins, frameworks, repositories,
templates, models, and automation tools require:

1. License review
2. Security review
3. Privacy and data-use review
4. Source attribution
5. Synthetic-data-only test plan
6. Founder approval before adoption
7. Changelog entry after approval

No code may be cloned, installed, executed, or connected merely because it is
publicly available.

## Data Classification

Do not add these data classes to GitHub:

- Credentials and secrets
- Payment and financial details
- Private personal data
- Customer, attendee, ticket-holder, fighter, talent, sponsor, vendor, or
  partner data
- Contracts and legal documents
- Private Drive documents or raw exports
- Private pricing, budgets, invoices, or financial models
- Unreleased event details
- Unapproved marketing or partnership information

## Incident Response

If a secret, private record, unsafe configuration, or unauthorized file is
committed:

1. Stop all further repository work.
2. Do not assume deleting a visible file removes the exposure.
3. Notify Founder immediately.
4. Revoke or rotate affected credentials outside GitHub.
5. Document the incident in a restricted governance record.
6. Remove the material using an approved remediation plan.
7. Review access, logs, integrations, and prevention controls.
8. Resume only after Founder approval.

## Current Status

FOUNDATION BUILD — EXTERNAL EXECUTION DISABLED
