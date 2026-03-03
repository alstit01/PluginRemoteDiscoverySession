---
stepsCompleted: [1, 2, 3, 4, 5, 6, 7, 8]
inputDocuments:
  - _bmad-output/planning-artifacts/prd.md
  - _bmad-output/planning-artifacts/prd-validation-report.md
  - _bmad-output/planning-artifacts/product-brief-PluginRemoteDiscoverySession-2026-03-01.md
  - _bmad-output/planning-artifacts/ux-design-specification.md
  - _bmad-output/planning-artifacts/research/Data_Centric_Architecture_SME.md
  - _bmad-output/planning-artifacts/research/20260301_Technical_Research_RDS_Plugin.md
  - _bmad-output/planning-artifacts/research/Connector_Research.md
  - _bmad-output/planning-artifacts/research/domain-research-indonesia.md
  - _bmad-output/planning-artifacts/research/domain-research.md
  - _bmad-output/planning-artifacts/research/github-connector-implementation-research-2026-03-02.md
  - _bmad-output/planning-artifacts/research/technical-Claude-Plugins-Skillsets-GitHub-research-2026-03-02.md
  - _bmad-output/planning-artifacts/research/report-ai-leadgen-vs-ads.md
  - _bmad-output/planning-artifacts/research/report-legal-ai-plugins.md
  - Anweisungen.md
workflowType: 'architecture'
project_name: 'PluginRemoteDiscoverySession'
user_name: 'Alex'
date: '2026-03-03T03:08:57+01:00'
status: 'complete'
lastStep: 8
completedAt: '2026-03-03'
---

# Architecture Decision Document

_This document builds collaboratively through step-by-step discovery. Sections are appended as we work through each architectural decision together._

## Project Context Analysis

### Requirements Overview

**Functional Requirements:**
- **Pipeline-Integration:** Orchestrierung von externen Search-/Research-Engines (Brave, Firecrawl, Perplexity), gefolgt von der automatisierten Erstellung von Angeboten, NDAs und Verträgen mit HITL-Gate.
- **CRM-Analyse & Fallback:** Read-Only-Datenextraktion aus diversen globalen CRM-Systemen (HubSpot, Salesforce, Bitrix24, amoCRM, Odoo) inklusive der Fähigkeit, bei Fehlern nahtlos auf manuelle CSV-Uploads umzuschwenken (Graceful Degradation).
- **Architektur-Gen & Delivery:** Auswertung von Kundeninterviews und Daten, um datenzentrische Architektur-Spezifikationen als Client-Deliverables (HTML) in erstklassigem V3 Corporate Design (Neural Network Aesthetic, Glassmorphismus) zu generieren.

**Non-Functional Requirements:**
- **Security & Privacy (Critical):** Zero-Trust-Architektur, PII-Anonymisierung zwingend erforderlich vor Repo-Comits, mandantenisolierte Workspaces.
- **Compliance:** Multi-Jurisdiction-Fähigkeit (DSGVO/EU AI Act, 152-ФЗ, UU PDP).
- **Maintainability & Radikaler Reuse:** Wöchentlich unabhängig aktualisierbare Solution Catalogs; MCP-Server und Skills müssen der BMAD-Methodik folgen und extrem modular ausgelegt sein.
- **Performance:** Strikte Timeboxing-Regeln (2h Research, 3h Architekturgenerierung).

**Scale & Complexity:**
- Primary domain: AI Agent Orchestration / Developer Tool
- Complexity level: High (Kombination aus NLP, Compliance, Daten-Sicherheit und verteilten Systemen)
- Estimated architectural components: ~12-15 Kernmodule (Connectors, Evaluators, Document Generators, Orchestrator, Workspace Manager, etc.)

### Technical Constraints & Dependencies

- **Platform Lock-in vs. Agnostic:** Primäre Umgebung ist Claude Code, was die Sprache und Laufzeit bestimmt.
- **API Limits:** Abhängigkeit von Drittanbietern (Search und CRM), wodurch Resilienz (Retry/Fallback) architektonisch verankert werden muss.
- **Datenhaltung:** Github dient als asynchroner Speicher (anonymisiert) und ersetzt klassische Persistenzschichten wie relationale Datenbanken für den Kernprozess.

### Cross-Cutting Concerns Identified

- **Graceful Degradation:** Fehlerbehandlung muss auf höchster architektonischer Ebene konzipiert werden (API-Error -> Manual Mode).
- **Data Governance & PII:** Ein zentrales "Masking & Anonymization"-Gateway ist erforderlich, bevor Daten verarbeitet oder gespeichert werden.
- **Radical Reusability:** Die Modularisierung von Skills (z.B. Research-Skill separat von Legal-Doc-Skill) bedarf stark standardisierter Schnittstellen.
- **UX Consistency:** HTML-Rendering-Pipeline muss in allen Output-Prozessen streng einheitliche Designs anwenden können.

## Starter Technology Stack

### Primary Technology Domain
**AI Agent Orchestration & MCP Server Ecosystem**

### Selected Technologies
- **Agent Framework**: BMAD (AI Agent Methodologies) with Claude Code runner setup.
- **Core Languages**: 
  - **TypeScript/Node.js** for custom Model Context Protocol (MCP) servers (CRM integrations, document generation).
  - **Markdown/YAML** for BMAD agent instructions, workflows, and configuration.
  - **HTML/CSS** for artifact delivery using the Neural Network Aesthetic (V3 Corporate Design).
- **Data Persistence**: Git-based local storage (`_bmad-output`), Markdown files, generated Client HTML deliverables.
- **External Integrations**: MCP ecosystem tools, Composio connectors, Bitrix24/Odoo local client implementations via REST API.

## Core Architectural Decisions

### Data Architecture
**Decision:** Git-Driven, Flat-File Local Storage
**Context:** Centralized RDBMS systems present a liability under Zero-Trust policies. The solution requires processing highly sensitive, multi-jurisdictional client data. 
**Resolution:**
- Use isolated, client-specific local workspace directories.
- Storing configurations, intermediate analysis, and output generation exclusively in `.md`, `.json`, `.csv`, and `.html` files.
- Commit to GitHub restricted exclusively to anonymized/sanitized structures without any PII. 

### API & External Communication
**Decision:** Standardized MCP (Model Context Protocol) via stdio
**Context:** The architecture must interact with diverse 3rd party APIs (Firecrawl, Brave, Perplexity, CRMs) maintaining strict security policies and retry mechanisms.
**Resolution:**
- Utilize MCP strictly over `stdio` mapping to local Node.js server scripts.
- Implemented **Graceful Degradation**: If an MCP/API fails, the AI agent is instructed to gracefully degrade into requesting flat-file `.csv`/`.json` uploads from the consultant via the standard command line interface.

### Security
**Decision:** Zero-Trust Read-Only Execution Model 
**Context:** Security is a primary project constraint with the requirement to protect against API token leaks or inadvertent data modifications in client CRMs.
**Resolution:**
- CRM Connectors strictly implement `READ_ONLY` scopes.
- PII-Scrubbing is mandated before generating any outputs saved to disk.
- Environment variables (`.env`) must handle sensitive API keys exclusively and are explicitly `.gitignore`d.

### Frontend / Output Architecture
**Decision:** Static HTML compiled with V3 Corporate Design CSS
**Context:** Outputs must establish a high premium feel representing the consulting firm's aesthetics dynamically.
**Resolution:**
- The system generates client deliverables as independent HTML files.
- A central `assets` folder contains the unified, reusable CSS reflecting the visual specifications (Glassmorphism, dark themes, neural visual elements). The HTML artifacts link to this static central CSS.

## Implementation Patterns & Consistency Rules

### Naming Conventions
- **BMAD Workflows:** `kebab-case.md` for workflow files (e.g., `remote-discovery.md`).
- **Skills/Agents:** Prefix conventions mapped inside `.agents/skills/`.
- **MCP Servers:** `kebab-case` for repository and execution folders (e.g., `mcp-crm-connector`).
- **Artifacts:** Verb-noun formatting or precise semantic labels (e.g., `architecture-report.html`).

### Structure Patterns
- The project follows a strict micro-file architecture under the BMAD philosophy. Separation of concerns dictates workflow instructions remain detached from execution scripts (MCP servers).

### Communication Patterns
- System instructions communicate via standardized markdown prompt engineering.
- AI logic communicates to MCP tools via strongly typed JSON schema exposed by the MCP `ListTools` protocol.
- Error states explicitly prompt the user for human-in-the-loop (HITL) resolution directly via standard output.

### Process & Workflow Patterns
- **HITL Verification:** Critical steps, specifically Contract/NDA generation and Final Client Delivery dispatch, require explicit Human-in-the-Loop triggers before proceeding.
- **Progressive Enhancement:** Begin extraction via advanced tooling (APIs); if unavailable, fallback progressively to simple methods (parsing local CSVs).

## Project Structure & Boundaries

### Complete Project Directory Structure

```text
PluginRemoteDiscoverySession/
├── .agents/                        # Agent configurations and contextual brains
│   ├── skills/                     # BMAD skills defining agent capabilities
│   └── workflows/                  # Defined orchestrator flows
├── _bmad/                          # Core config for BMAD Framework
│   ├── bmm/                        # BMAD base implementation defaults
│   │   ├── config.yaml
│   │   └── workflows/
│   └── core/
├── _bmad-output/                   # Git-ignored by default or sanitized repository
│   ├── planning-artifacts/         # PRD, Architecture, Research (Current output)
│   ├── discovery-artifacts/        # Extracted client info and interim parsed text
│   └── client-deliverables/        # Final generated HTML representations
├── mcp-servers/                    # Custom local MCP integrations
│   ├── crm-read-only/              # Node.js server integrating Composio/1C/Odoo
│   │   ├── package.json
│   │   └── src/
│   ├── market-research/            # MCP proxy for Firecrawl/Perplexity/Brave
│   └── legal-doc-gen/              # Local server or mapping to legal templates
├── templates/                      # Raw design layouts
│   ├── html-deliverables/          # V3 Corporate Design baseline structures
│   ├── assets/                     # Shared CSS/JS (Glassmorphism, Net aesthetic)
│   └── contracts/                  # Baseline markdown NDA and SaaS contracts
├── tests/                          # Automated suite for mapping & degradation logic
├── .env.example                    # Template for required integrations
├── .gitignore                      # Strict exclusion of .env, PII paths, node_modules
├── package.json                    # Project metadata & root scripts
└── README.md                       # Consultant handoff & installation overview
```

### Architectural Boundaries

**API Boundaries:**
- The AI Agent logic execution is firmly bounded within the `Claude Code` orchestration layer. External calls are strictly routed down through isolated `mcp-servers`.

**Data Boundaries:**
- Non-anonymized data cannot leave the memory context of the execution without specifically being written to `.gitignore`d isolation paths within `_bmad-output/discovery-artifacts`. Only sanitized presentations are published.

### Requirements to Structure Mapping

**Epic Mapping:**
- **Automated Research Pipeline** -> `mcp-servers/market-research`
- **Graceful CRM Connectors** -> `mcp-servers/crm-read-only`
- **Aesthetic Deliverable Gen** -> `templates/html-deliverables` & `_bmad-output/client-deliverables/`

## Architecture Validation Results

### Coherence Validation ✅
**Decision Compatibility:** Technology stack directly maps to constraints. The usage of Claude + MCP combined with Node.js servers ensures stability without introducing unnecessary enterprise backend architecture. Zero-Trust mapping is naturally reinforced through the isolated tools and local nature of the framework.

**Pattern Consistency:** Adherence to BMAD methodology guarantees modular creation of skills and tasks, satisfying "Radical Reusability" demands.

### Requirements Coverage Validation ✅
**Epic/Feature Coverage:** All defined epics (CRM integration, fallback strategies, artifact generation, legal generation) are mapped structurally to explicit MCP server implementations or local template workflows. The workflow incorporates explicit HITL components for the legal generation.

**Non-Functional Requirements Coverage:** Read-only structures cover basic info-sec mandates. The graceful degradation constraint is satisfied universally across tool interaction protocols.

### Implementation Readiness Validation ✅
**Project Assessment:** READY FOR IMPLEMENTATION

**Confidence Level:** High
The project constraints have been heavily vetted through market research and architecture mapping. The structure separates concern clearly between the AI Agent logic (BMAD workflows) and integration execution (MCP servers).

### Implementation Handoff

**AI Agent Guidelines:**
- Follow all architectural decisions exactly as documented.
- Use implementation patterns consistently across all components.
- Respect project structure and boundaries.

**First Implementation Priority:**
Proceed to setup the foundational directory structures (especially the `.agents` and `mcp-servers` folders) and prepare the base HTML template rendering pipeline to ensure output aesthetics match the expectations defined in the UX specification.

---
*Workflow completed successfully.*
