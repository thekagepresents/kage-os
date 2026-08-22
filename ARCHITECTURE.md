# Kage Agency HQ Architecture

## Purpose

This document describes the planned engineering architecture for THE KAGE
PRESENTS Agency HQ.

It is a founder-controlled design specification only.

It does not authorize implementation, installation, execution, connection,
automation, deployment, or external-system access.

## Architectural Principle

Kage Agency HQ is built in layers.

```text
Founder
  ↓
Founder Command
  ↓
Governance and Knowledge
  ↓
Skills
  ↓
Specialist Agents
  ↓
Data Model
  ↓
MCP / Connectors
  ↓
Manual Workflow Validation
  ↓
Automation
  ↓
External Systems
```

Founder retains final approval authority at every layer.

## Core Operating Flow

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

No external or irreversible action may bypass this flow.

## Source-of-Truth Model

### Business Source of Truth

Canonical Kage Google Drive root:

```text
THE KAGE
Folder ID: 1KBwj0yKCznlE4MNNJwzyf43qo-7zdJUE
```

Google Drive holds approved business documents, brand assets, creative materials,
operational registers, finance records, contracts, and project deliverables.

### Project Context and Governance

Claude Project:

```text
THE KAGE PRESENTS — AGENCY HQ
```

Claude Project holds Kage operating instructions, curated Kage Brain knowledge,
project chats, founder directives, and future project-scoped skill activation
records.

### Engineering Source of Truth

This private GitHub repository:

```text
thekagepresents/kage-agency-hq
```

GitHub holds engineering architecture, governance specifications, skill
packages, agent specifications, schemas, workflow definitions, MCP
specifications, technical documentation, and synthetic tests.

## System Layers

### Layer 1 — Founder

Founder defines vision, approves decisions, controls identity, owns systems,
approves external actions, and retains authority over money, contracts, access,
publishing, partners, customers, tickets, streaming, and brand use.

### Layer 2 — Founder Command

Founder Command is the future orchestrator.

It will:

- Understand Founder requests
- Classify facts, decisions, drafts, and risks
- Check approved Kage knowledge
- Select the appropriate skill or specialist workflow
- Synthesize findings
- Present a plan and exact approval request
- Record outcome after Founder approval

Founder Command has orchestration authority only.

Founder retains execution authority.

### Layer 3 — Governance and Knowledge

Governance includes:

- Source-of-truth rules
- Decision and approval controls
- Project data boundaries
- Risk and dependency tracking
- Change control
- Security controls
- Audit records
- Kage Brain documents
- Approved factual source material

### Layer 4 — Skills

Skills are reusable, versioned instruction packages.

Initial Kage skills will be non-executing and instruction-based:

- Kage source-of-truth classification
- Kage governance and approval gates
- Kage research and source verification
- Kage brand and creative governance
- Kage strategy, planning, and dependency management

Skills must not receive automatic external permissions.

### Layer 5 — Specialist Agents

Future specialist roles may include:

- Brand Guardian
- Creative Studio
- Ticketing and Revenue
- Digital Product
- Sponsorship and Partnerships
- Fighter and Talent
- Production and Operations
- Finance and Reporting
- Research and Intelligence
- Streaming and Broadcast
- Marketing, Growth, and Community
- Graphic Designer

No specialist agent is active, autonomous, or connected during foundation build.

### Layer 6 — Data Model

Future structured operational data may include:

- Events
- Concepts
- Venues
- Fighters and talent
- Sponsors and partners
- Ticketing inventory
- Tables and hospitality
- Tasks
- Campaigns
- Assets
- Content
- Contacts
- Decisions
- Approvals
- Vendors
- Contracts
- Budget lines
- Invoices
- Revenue
- KPIs
- Streaming and media assets

No database, Airtable base, Supabase project, CRM, or structured operational
system is selected or active.

### Layer 7 — MCP and Connectors

MCP and connectors are controlled doorways to external systems.

Initial intended connector policy:

```text
Google Drive:
Read-only
Canonical THE KAGE root and descendants only
No account-wide search
No Drive write access without exact Founder approval
```

All other external connectors remain disabled until a business need, source of
truth, permission model, data boundary, security review, owner, cost, approval
gate, test plan, and rollback method are defined.

Potential future systems include:

- GitHub
- Website / CMS
- Hosting / DNS
- Ticketing
- CRM
- Email
- SMS
- Analytics
- Paid media
- Social
- Streaming
- Finance
- Database
- Automation platform

### Layer 8 — Manual Workflow Validation

Before automation, Kage must run manual versions of high-value workflows.

Examples:

- Brand-source audit
- Creative brief
- Event-concept review
- Ticketing-platform evaluation
- Sponsor-package approval
- Fighter intake
- Website content approval
- Streaming-rights checklist
- Budget approval
- Campaign approval
- External-action request

Manual workflow validation must prove:

- Inputs are reliable
- Owners are named
- Approval gates are clear
- Outputs are useful
- Risks are understood
- Logs are maintained
- Recovery process exists

### Layer 9 — Automation

Automation is introduced only after manual workflow validation.

Every automation must have:

- Defined trigger
- Defined approved inputs
- Defined action
- Pre-execution validation
- Founder approval gate where required
- Post-execution verification
- Audit log
- Failure alert
- Rollback or recovery process
- Owner

No automation is active.

### Layer 10 — External Systems

Potential future external systems include:

- Kage website
- Domain hosting and DNS
- Ticketing
- Table / hospitality systems
- Email and SMS
- CRM
- Social and community platforms
- Analytics
- Paid media
- Streaming and broadcast distribution
- Production systems
- Finance and invoicing
- Vendor and partner systems

No external system is connected, configured, active, or authorized through this
repository.

## Current Phase

```text
FOUNDATION BUILD — NO AUTONOMOUS EXECUTION
```

Current work is limited to:

- Identity
- Governance
- Knowledge
- Documentation
- Repository structure
- Skill design
- Agent design
- Synthetic testing
- Manual workflow planning

## Architecture Change Rule

Any change to this architecture requires:

1. Founder approval
2. Updated architecture documentation
3. Security review where applicable
4. Data-boundary definition
5. Permission model
6. Synthetic-data test plan
7. Rollback or recovery plan
8. CHANGELOG.md entry
