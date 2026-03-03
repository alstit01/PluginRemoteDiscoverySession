---
stepsCompleted: [step-01-init, step-02-discovery, step-02b-vision, step-02c-executive-summary, step-03-success, step-04-journeys, step-05-domain, step-06-innovation, step-07-project-type, step-08-scoping, step-09-functional, step-10-nonfunctional, step-11-polish, step-12-complete]
inputDocuments:
  - product-brief-PluginRemoteDiscoverySession-2026-03-01.md
  - research/20260301_Technical_Research_RDS_Plugin.md
  - research/Connector_Research.md
  - research/Data_Centric_Architecture_SME.md
  - research/domain-research-indonesia.md
  - research/domain-research.md
  - research/github-connector-implementation-research-2026-03-02.md
  - research/report-ai-leadgen-vs-ads.md
  - research/report-legal-ai-plugins.md
  - research/technical-Claude-Plugins-Skillsets-GitHub-research-2026-03-02.md
  - architecture/connector-graceful-degradation.md
  - GitHub_Tech-Stack_KMU.md
  - 20260204_Saas_4_KMU_ru.md
  - 20260204_SaaS_4_KMU_de.md
documentCounts:
  briefs: 1
  research: 9
  architecture: 1
  additional: 3
  projectContext: 0
  projectDocs: 0
classification:
  projectType: developer_tool
  domain: AI Consulting (with Legal Support)
  complexity: medium
  projectContext: greenfield
workflowType: 'prd'
validationDate: '2026-03-02'
---

# Product Requirements Document - PluginRemoteDiscoverySession

**Author:** Alex
**Date:** 2026-03-02

## Executive Summary

PluginRemoteDiscoverySession is an agentic developer tool that automates the strategic consulting process of the "Remote Discovery Session" for SMEs. It serves as an AI exoskeleton for an AI Solution Architect: from a 60-minute client conversation, CRM data analysis, and automated market research, a complete Discovery Delivery is produced end-to-end — including architecture specification, proposal, and NDA.

The plugin orchestrates specialized agents and MCP servers within Claude Code (or comparable agent runners). The workflow comprises five phases: (1) Multi-perspective market research (Brave Search, Firecrawl, Perplexity), (2) Formal scoping & proposal generation, (3) Legal-Tech setup (NDAs, contracts via Legal MCPs with HITL approval), (4) Remote Discovery Session (qualitative interviews + quantitative system audit via read-only MCP connectors), and (5) Delivery (architecture specification, PRDs, HTML reports in corporate design).

The core is not software development, but intelligent orchestration of existing tools — BMAD methodology, MCP server ecosystem, pre-built skills, and a universal tech stack — to produce high-quality consulting artifacts. Outputs are specifications and architecture documents, not software products.

**Solution Space & Currency:** Architecture and tool recommendations for clients are based on curated, market-specific solution catalogs (`20260204_Saas_4_KMU_ru.md` for RU, `20260204_SaaS_4_KMU_de.md` for DACH). These catalogs cover categories including RAG/Knowledge Management, OCR/Document Automation, Voice Bots, AI Assistants, Accounting, Scheduling, Lead Qualification, and Forecasting — and are **updated weekly** to keep pace with rapid market evolution. This ensures every Discovery Session delivers up-to-date recommendations rather than stale references.

**Web Presence Analysis:** As part of the Discovery Session, the client's web presence is analyzed — Schema Markup (JSON-LD), API readiness, Agent-to-Agent compatibility — to assess readiness for AI-powered interactions and machine-readable content.

Target markets are DACH (EU AI Act, GDPR), Russia (152-ФЗ), and Indonesia (UU PDP), each with market-specific CRM connectors (Salesforce/HubSpot via Composio for DACH; Bitrix24/amoCRM/1C for RU; Odoo/Mekari Qontak for ID). All system access is strictly read-only.

**Time Window:** AI-driven automation currently presents opportunities that will significantly shrink by end of 2026 as autonomous long-running agents mature (SaaS-pocalypse). Those who deliver now occupy the niche.

### What Makes This Special

- **Zero-Friction Execution:** No lengthy AI discussions — orchestrated workflows deliver results directly. The consultant triggers, the agent ecosystem executes.
- **Consulting as Product:** The *process of consulting delivery* is automated and scalable, not the end result. Each Discovery Session produces individual, client-specific architecture — but the path to delivery is standardized and reproducible.
- **Real-Time Arbitrage & Disposable Architecture:** Real-time research delivers up-to-the-day AI methods and SaaS startups. Weekly-updated solution catalogs per market (DACH/RU) ensure recommendations never go stale.
- **Web Presence as Discovery Dimension:** Automated analysis of the client's website for AI-readiness (Schema Markup, API exposure, A2A compatibility) feeds directly into architectural recommendations.
- **Data-Centric Security by Design:** Decoupled, multi-layered architecture (Core Data, Governance, Security, Semantic API) with Zero-Trust protection — no risky API integrations into legacy systems.
- **200% Gross Margin:** The highly automated process (EDD/TDD) enables proposal prices of $2,400 on a ~10h / $800 cost basis.

## Project Classification

| Dimension | Value |
|---|---|
| **Project Type** | Developer Tool (AI Consulting Exoskeleton) |
| **Domain** | AI Consulting with Legal Support |
| **Complexity** | Medium — Orchestration of existing components (BMAD, MCP, Skills) |
| **Project Context** | Greenfield |

## Success Criteria

### User Success

The primary user is the AI Solution Architect running Remote Discovery Sessions. Success means:

- **Zero-Friction Workflow:** Triggering a workflow produces results without iterative AI coaching. The consultant issues a command, the agent ecosystem delivers — no prompt engineering during delivery.
- **Session Turnaround ≤ 5 Business Days:** From initial client contact to delivered architecture specification, proposal, and NDA — full cycle completion within one business week.
- **Pre-Session Research < 2 Hours:** Automated market research, competitor analysis, and client web presence assessment complete within 2 hours of triggering.
- **Legal Document Generation < 30 Minutes:** NDA and contract drafts generated with HITL review gate, ready for client signature.
- **Architecture Spec Generation < 3 Hours:** From Discovery Session transcript + CRM data + research → complete architecture specification.
- **Corporate Consistency ≥ 90%:** All deliverables (HTML reports, proposals, NDAs) conform to V3 Corporate Design templates.
- **"Aha" Moment:** The consultant realizes within the first session that the tool eliminates the manual bottleneck between research and delivery.

### Business Success

- **Gross Margin ≥ 200%:** Revenue per session $2,400 on cost basis of ~$800 (~10h at $80/h blended rate), yielding $1,600 profit per session.
- **3-Month Target:** Complete 4+ paid Discovery Sessions using the plugin, validating the productized workflow end-to-end.
- **12-Month Target:** 24+ sessions delivered, establishing the Remote Discovery Session as a repeatable, scalable product offering across DACH and RU markets.
- **Client Validation ≥ 80%:** AI Readiness Scorecard accuracy confirmed through client post-session feedback.
- **Solution Catalog Currency:** Market-specific SaaS/tool catalogs (`_ru.md`, `_de.md`) successfully updated weekly with zero stale recommendations in delivered reports.
- **Market Expansion:** Indonesia (ID) market pilot initiated within 12 months using UU PDP-compliant connector stack.

### Technical Success

- **Read-Only Enforcement:** 100% of CRM/ERP connector access verified as read-only — zero write operations to client systems.
- **Multi-Jurisdiction Compliance:** Parallel compliance validation for GDPR/EU AI Act (DACH), 152-ФЗ (RU), and UU PDP (ID) without manual jurisdiction switching.
- **Graceful Degradation:** When connectors fail, the workflow falls back to flat-file ingestion (CSV/Excel uploads) without session interruption.
- **Data-Centric Security:** Zero data leakage across tenant boundaries; PII masking applied before any data leaves the client's governance perimeter.
- **BMAD Workflow Integration:** All Discovery Session phases executable via existing BMAD workflows and skills without custom code.

### Measurable Outcomes

| Metric | Target | Measurement Method |
|---|---|---|
| Session Turnaround | ≤ 5 business days | Timestamp: first contact → final delivery |
| Pre-Session Research Time | < 2h | Agent execution logs |
| Legal Doc Generation | < 30min | Agent execution logs |
| Architecture Spec Generation | < 3h | Agent execution logs |
| Corporate Design Compliance | ≥ 90% | Template validation checklist |
| Gross Margin per Session | ≥ 200% ($1,600 profit) | Revenue - direct costs |
| Client Scorecard Validation | ≥ 80% accuracy | Post-session client survey |
| Catalog Freshness | Weekly updates | Git commit frequency on catalog files |
| Connector Read-Only Compliance | 100% | Automated integration tests |

## Product Scope

### MVP - Minimum Viable Product

The MVP enables a single consultant to run complete Remote Discovery Sessions across all three target markets. For detailed MVP strategy, automation decisions, and phased roadmap, see *Project Scoping & Phased Development*.

1.  **Research Agent Pipeline:** Google Search + Brave Search + Firecrawl (optional) + Perplexity Ask (on user command) for automated multi-perspective client/market research
2.  **Web Presence Analyzer:** Schema Markup, API readiness, and A2A compatibility assessment of client websites
3.  **Legal Document Generator:** NDA and contract templates with HITL approval gate (jurisdiction-specific: DACH, RU, ID)
4.  **Discovery Session Workflow:** Structured questionnaires + interview guide + transcript processing + evaluation
5.  **Architecture Spec Generator:** Client-specific data-centric architecture from Discovery Session inputs
6.  **CRM Data Audit Module:** Automated read-only analysis of client CRM data quality, pipeline health, and automation gaps
7.  **Delivery Pipeline:** HTML report generation in V3 Corporate Design (presentation, artifact, and document templates)
8.  **DACH Market Support:** Salesforce/HubSpot connectors via Composio (read-only), EU AI Act compliance references, `SaaS_4_KMU_de.md` catalog
9.  **RU Market Support:** Bitrix24/amoCRM/1C connectors (read-only), 152-ФЗ compliance layer, `Saas_4_KMU_ru.md` catalog
10. **ID Market Support:** Odoo/Mekari Qontak connectors (read-only), UU PDP compliance, localized solution catalog
11. **Per-Client GitHub Repository:** Automated creation of private GitHub repos per client for anonymized data storage and collaboration
12. **Solution Catalog Management:** Weekly update workflow for all market-specific catalogs

### Growth Features (Post-MVP)

1.  **Parallel Architecture Generator:** Automated "shadow process" architecture proposals that run alongside client's existing workflows
2.  **Multi-Session Client Intelligence:** Cross-session learning for returning clients (architecture evolution tracking)

### Vision (Future)

1.  **Multi-Consultant Platform:** Role-based access for consulting teams, shared client intelligence, branded white-label deliverables
2.  **Self-Service Discovery Lite:** Client-facing intake workflow where SMEs self-complete initial assessment before consultant session
3.  **Continuous Monitoring:** Post-delivery monitoring of implemented architecture recommendations with automated health checks

## User Journeys

### Journey 1: Alex — The Complete Discovery Session (Success Path)

**Phase 1 — Initial Conversation & Research**

**Opening Scene:** Alex receives a referral — a 45-employee wholesale company in Stuttgart struggling with manual processes. The first touchpoint is a 30-minute introductory call. While the conversation happens, the transcript is captured. Afterwards, Alex triggers the research pipeline, feeding it the transcript content.

**Rising Action:** The research agents fan out across multiple engines — Google Search (internal), Brave Search, and optionally Firecrawl for deep web scraping — each examining the client's market position from a different perspective: competitive landscape, industry AI adoption benchmarks, SEO/web presence for AI agent visibility (Schema Markup, A2A readiness), and optimization opportunities through AI methods, automation, new applications, and digital measures. Perplexity Ask is triggered on Alex's explicit command for synthesized follow-up questions. Within 2 hours, all findings are structured and stored centrally in the workspace — organized by perspective (market positioning, AI opportunities, web presence, competitive scan).

**Phase 2 — Formal Proposal**

Based on the initial conversation and the research findings, Alex triggers the proposal generator. The agent produces a formal proposal for conducting a Remote Discovery Session — scoped, priced ($2,400 fixed), with clear deliverables outlined. Alex reviews, adjusts the scope if needed, and sends it to the client.

**Phase 3 — Contract & NDA**

**Climax of Trust:** After the client confirms the proposal, Alex triggers the legal document generator. Two documents are produced: a client-specific **contract** and an **NDA**. Both go through a HITL review gate before being sent for signature.

**Phase 4 — Remote Discovery Session Execution**

**The Core Work:** After contract signing, the actual Remote Discovery Session begins. This is not a single event but a structured process:

1.  **Questionnaires & Interviews:** Structured questionnaires are generated and sent to the client. Follow-up interviews are conducted, transcribed, and processed.
2.  **Analysis & Solution Development:** Client data sources (CRM exports, business descriptions, questionnaire responses) are analyzed — automated where possible, always in agreement with the client. Research on the latest AI market developments and related fields is conducted as needed and informs the analysis and solution proposals.
3.  **Data-Centric Architecture as North Star:** Every analysis and every Quick Win proposal serves as a building block toward the overarching goal: a **data-centric architecture** as the foundation for full business process automation. Quick Wins are not isolated fixes — they are stepping stones toward this larger vision.
4.  **BMAD Methodology:** The entire Discovery Session execution follows the BMAD methodology — structured workflows, skills, and agent orchestration ensure reproducible quality.

**Phase 5 — Delivery**

**Resolution:** At the end of the Discovery Session, Alex triggers the delivery pipeline. The output package includes:
- **Discovery Report:** Comprehensive findings in branded HTML (V3 Corporate Design)
- **AI Readiness Scorecard:** The client scores 28/100 — "Early Stage," honest and actionable
- **Architecture Specification:** Data-centric target architecture showing how each proposed solution contributes to full process automation
- **Solution Specifications:** Individual specs for each recommended Quick Win, with tool recommendations from the weekly-updated solution catalogs, pricing estimates, and integration effort
- **Implementation Proposal:** A phased commercial offer for implementing the recommended solutions

The client receives a coherent package that answers: "Where do we stand, where should we go, and what's the first step?" Total consultant time: ~10 hours. Profit: $1,600.

---

### Journey 2: Alex — Connector Failure & Graceful Degradation (Edge Case)

**Opening Scene:** Alex is preparing for a Discovery Session with a Russian logistics company that uses Bitrix24 and 1C. The client has granted read-only API access to their Bitrix24 instance. Alex triggers the CRM connector.

**Rising Action:** The Bitrix24 connector fails — the client's self-hosted instance is running an outdated API version. The graceful degradation system kicks in automatically: Alex receives a notification explaining the failure, and a flat-file upload wizard appears requesting CSV exports of deals, contacts, and activity logs. Alex emails the client with precise export instructions (auto-generated in Russian from the standardized template).

**Climax:** The client sends three CSV files. Alex drops them into the designated folder. The data ingestion pipeline processes them identically to how it would have processed the API data — same analysis, same output quality. The only difference: 4 hours delay due to the manual export step.

**Resolution:** The Discovery Session proceeds as planned. The final delivery is indistinguishable from an API-connected session. The client never knows there was a technical issue.

---

### Journey 3: Alex — Weekly Catalog Maintenance (Operations)

**Opening Scene:** Every Sunday evening, Alex receives an automated notification: "Solution catalog update due."

**Rising Action:** Alex triggers the catalog update workflow. The research agents scan predefined sources and propose additions and removals. The agent presents a diff: 2 new tools to add, 1 tool to update (pricing change), 1 tool to flag as deprecated.

**Climax:** Alex reviews the proposed changes — each with source links and evaluation scoring. One tool lacks DSGVO documentation — marked as "under review."

**Resolution:** Catalogs committed. Next week's sessions reference updated data. Total time: 25 minutes.

---

### Journey 4: KMU Client — Receiving the Discovery Delivery (Client Perspective)

**Opening Scene:** Markus, owner of a 45-employee wholesale company in Stuttgart, agreed to the session after receiving a professional, clearly scoped proposal.

**Rising Action:** He signed the NDA and contract. During the Discovery Session, he filled out structured questionnaires and participated in focused interviews. He shared CRM exports (with his agreement), feeling that the process was thorough yet efficient.

**Climax:** He receives the branded delivery package — AI Readiness Scorecard, architecture specification showing a path from Quick Wins to full data-centric automation, and individual solution specs with concrete tool recommendations, pricing, and timelines.

**Resolution:** "This is the first time someone showed us *specifically* what AI could do for *our* business — and how each step builds toward something bigger." He signs up for Phase 1 implementation.

---

### Journey Requirements Summary

| Journey | Key Capabilities Revealed |
|---|---|
| **Alex — Success Path** | Transcript processing → multi-engine research orchestration (Google, Brave, Firecrawl, Perplexity) → structured workspace storage → proposal generation → contract/NDA generation → questionnaire creation → interview processing → CRM/data analysis (with client consent) → data-centric architecture spec → solution specs → implementation proposal → HTML delivery pipeline |
| **Alex — Graceful Degradation** | Connector failure detection, automatic fallback to flat-file ingestion, client communication templates, processing parity between API and manual inputs |
| **Alex — Catalog Maintenance** | Automated source scanning, diff-based update proposals, evaluation scoring, Git-based versioning, review workflow |
| **Client — Delivery Experience** | Professional proposal → NDA/contract → structured questionnaires → focused interviews → AI Readiness Scorecard → architecture with Quick Win-to-automation path → solution specs → implementation proposal |

The user journeys above define the end-to-end experience. The following sections specify the regulatory, technical, and domain constraints that shape how these journeys are implemented.

## Domain-Specific Requirements

### Compliance & Regulatory

**Multi-Jurisdiction Framework:**

| Jurisdiction | Primary Regulation | Key Requirements | Impact on Plugin |
|---|---|---|---|
| **DACH** | GDPR + EU AI Act | Data minimization, purpose limitation, AI literacy (mandatory Feb 2025), high-risk AI conformity (Aug 2026) | All client data processing must have legal basis; AI-generated deliverables require transparency labeling; EU AI Act compliance checklist for recommended solutions |
| **Russia** | 152-ФЗ (Personal Data) | Personal data of Russian citizens must be stored/processed on Russian servers; anonymized data may be exported | RU client PII must not leave Russian infrastructure; anonymized analytical data may be processed externally; per-client private GitHub repos contain only anonymized data |
| **Indonesia** | UU PDP (Law 27/2022) | Consent-based processing, data breach notification (3×24h), data controller registration | ID market connectors must implement consent verification; data processing agreements required |

**Legal-Tech Constraints:**
- AI-generated legal documents (NDAs, contracts) require mandatory Human-in-the-Loop review before client delivery
- Plugin must not provide legal advice — outputs are templates requiring professional legal review
- Contract templates must be jurisdiction-specific (German/Austrian law for DACH, Russian civil law for RU, Indonesian law for ID)
- Digital signature requirements vary by jurisdiction (eIDAS for EU, qualified electronic signature for RU)

**EU AI Act Specific:**
- AI Readiness Scorecard must include EU AI Act compliance assessment for recommended solutions
- Any AI system recommendations classified as "high-risk" must be flagged with conformity assessment requirements
- AI literacy training references must be included in DACH market deliverables

### Technical Constraints

**Data Security:**
- Zero-Trust architecture: no implicit trust between system components
- PII masking/anonymization before any data crosses governance boundaries
- Per-client private GitHub repository for anonymized data storage — no client data in shared repos
- Tenant isolation: client data must never be accessible cross-session
- All CRM/ERP access strictly read-only — enforced at connector level, not just convention
- Encryption in transit (TLS 1.3) and at rest for all client data

**Data Handling:**
- Session data retention policy: client data purged after delivery unless explicitly retained (with consent)
- Transcript data classified as sensitive — processed in-memory where possible
- CRM export data (CSV/Excel) must be stored in client-specific workspace directories with access controls
- Anonymized data exports permitted across jurisdictions; PII remains jurisdiction-locked

**Component Licensing:**
- Preference for permissive OSS licenses (MIT, Apache 2.0, BSD) for productized components
- GPLv3 components (Neo4j) and SSPLv1 components (FalkorDB) require legal evaluation before inclusion in commercial workflow
- Claude Code is proprietary — usage within Anthropic's commercial terms, not redistributable

### Integration Requirements

**CRM/ERP Connectors (all MVP):**

| Market | Systems | Access Pattern | Fallback |
|---|---|---|---|
| **DACH** | Salesforce, HubSpot (via Composio) | REST API, read-only OAuth scopes | CSV/Excel upload |
| **RU** | Bitrix24, amoCRM, 1C | REST API, self-hosted instances common | CSV/Excel upload with Russian-language instructions |
| **ID** | Odoo, Mekari Qontak | REST API | CSV/Excel upload |

**Research Engines:**

| Engine | Access Method | Role | Trigger |
|---|---|---|---|
| Google Search | Internal search engine | Primary market/web research | Automatic |
| Brave Search | MCP Server | Privacy-focused secondary research | Automatic |
| Firecrawl | MCP Server | Deep web scraping, content extraction | Optional |
| Perplexity Ask | MCP Server | Synthesized analysis queries | On user command |

**Client Data Infrastructure:**
- Per-client private GitHub repository (automated creation)
- Repository contains only anonymized data: analysis results, architecture specs, solution catalogs
- No PII, no raw CRM exports, no unmasked transcripts in repositories
- Git-based versioning enables audit trail and collaboration

**Delivery Pipeline:**
- HTML templates (V3 Corporate Design) for presentations, artifacts, and documents
- PDF generation capability for contract/NDA delivery
- Branded output with client-specific customization (logo, company name placeholders)

### Risk Mitigations

| Risk | Severity | Mitigation |
|---|---|---|
| **Client data breach via CRM connector** | Critical | Read-only enforcement at OAuth scope level; connector audit logging; no credential storage |
| **AI-generated contract with legal errors** | High | Mandatory HITL gate; disclaimer in all legal documents; template review by licensed attorney per jurisdiction |
| **Stale solution catalog recommendations** | Medium | Weekly update workflow; catalog entries include "last verified" timestamp; deprecated tools flagged automatically |
| **Connector failure during active session** | Medium | Graceful degradation to flat-file ingestion; client communication templates; processing parity guarantee |
| **Cross-jurisdiction data leakage** | High | Per-client private repos with anonymized data only; PII masking before export; jurisdiction tags on all data objects |
| **EU AI Act non-compliance in recommended solutions** | Medium | AI Act compliance checklist in Scorecard; high-risk system flagging; transparency labeling on AI-generated content |
| **GitHub repo containing PII** | High | Automated PII scanning before commit; anonymization pipeline mandatory; review gate on all repo pushes |

## Innovation & Novel Patterns

### Detected Innovation Areas

**1. Consulting-Process-as-Code (Primary Innovation)**
The core innovation is treating the consulting delivery process — not the client's software — as an automatable, orchestratable system. Traditional consulting relies on individual expertise and manual artifact creation. PluginRemoteDiscoverySession encodes the entire Discovery Session methodology into reproducible agent workflows:
- Research → Proposal → Contract → Discovery → Delivery becomes a pipeline, not a craft
- Each phase has defined inputs, outputs, and quality gates
- The consultant shifts from executing to orchestrating and reviewing

**2. BMAD-as-Consulting-Framework (Paradigm Transfer)**
BMAD methodology was designed for software development (PRDs, architecture, epics). This project repurposes it as a consulting methodology — using the same structured approach to produce client-facing deliverables instead of code specifications. The methodological framework (workflows, skills, agents) is applied to a fundamentally different domain: business consulting and architecture advisory.

**3. Data-Centric Architecture as Unifying Philosophy**
Every Quick Win recommendation is explicitly designed as a building block toward full business process automation via a data-centric architecture. This distinguishes the approach from typical consulting that delivers isolated point solutions. The client receives not just "do X," but "do X as step 1 of N toward fully automated operations."

**4. Disposable Architecture with Weekly Refresh**
The recommendation engine treats its own knowledge base as disposable — weekly-updated solution catalogs acknowledge that today's best tool may be obsolete next month. This anti-pattern of deliberately building impermanent recommendations is itself innovative in a field that typically produces "5-year roadmaps."

**5. Anonymized Client Repos as Collaboration Medium**
Using private GitHub repositories with exclusively anonymized data as the client collaboration and delivery medium bridges the gap between consultant tooling (Git-native) and client accessibility (web-based repo viewing), while maintaining cross-jurisdictional compliance.

### Market Context & Competitive Landscape

The closest existing approaches are:
- **Management consulting firms** (McKinsey, BCG) — manual process, premium pricing ($50K+), not accessible for SMEs
- **AI readiness assessment tools** (generic online scorecards) — superficial, no architecture output, no market-specific recommendations
- **Fractional CTO services** — ad-hoc, not productized, no standardized methodology
- **Consulting-tech platforms** (Miro, Notion, etc.) — tools for consultants, but don't automate the consulting process itself

**White space:** No productized service exists that combines automated multi-perspective market research, structured Discovery Sessions, data-centric architecture specification, and jurisdiction-specific legal document generation into a single orchestrated workflow at the $2,400 price point.

### Validation Approach

| Innovation Aspect | Validation Method | Success Criteria |
|---|---|---|
| Consulting-Process-as-Code | First 4 paid sessions (3-month target) | Turnaround ≤ 5 days, quality comparable to manual delivery |
| BMAD-as-Consulting-Framework | Post-session client feedback | ≥ 80% Scorecard accuracy validation |
| Data-Centric Architecture Philosophy | Client follow-up at 6 months | ≥ 1 client proceeds with Phase 1 implementation |
| Disposable Architecture | Catalog diff analysis | Weekly updates contain ≥ 2 changes; zero stale recommendations in delivered reports |
| Anonymized Client Repos | Client usability feedback | Clients successfully access and reference their repos |

### Risk Mitigation

| Innovation Risk | Mitigation |
|---|---|
| **Consulting-as-Code produces generic outputs** | HITL review gates at every phase; consultant retains creative control over architecture recommendations |
| **BMAD methodology doesn't translate to consulting** | Pilot with 2 sessions using BMAD; fallback to manual process with BMAD for documentation only |
| **Data-centric philosophy overwhelms SME clients** | Layer delivery: Quick Win actions first, architecture vision as appendix; let client choose depth of engagement |
| **Weekly catalog updates create recommendation instability** | Version control with "stable" and "edge" tracks; client reports reference specific catalog version |

*Note: Market timing risk (SaaS-pocalypse window) is addressed in Project Scoping & Phased Development → Risk Mitigation Strategy.*

## Developer Tool Specific Requirements

### Project-Type Overview

PluginRemoteDiscoverySession is a developer tool in the form of an agentic plugin system. Unlike traditional developer tools (npm packages, CLI tools, SDKs), it operates as an orchestration layer within Claude Code (or compatible agent runners). The "installation" is a workspace configuration; the "API" is a set of BMAD workflows, MCP server connections, and skill definitions; the "documentation" is embedded in the methodology itself.

### Language & Runtime Matrix

| Component | Language/Runtime | Purpose |
|---|---|---|
| **Agent Orchestration** | Claude Code (Anthropic) | Primary agent runner — executes workflows, skills, MCP calls |
| **BMAD Workflows** | Markdown + YAML frontmatter | Methodology definition — steps, templates, data CSVs |
| **MCP Servers** | TypeScript/Node.js (primary), Python (secondary) | External tool integration — Brave Search, Firecrawl, Perplexity, Notion, CRM connectors |
| **Skills** | Markdown (SKILL.md) + optional scripts | Specialized capabilities — research, analysis, document generation |
| **Templates** | HTML + CSS (V3 Corporate Design) | Delivery artifacts — reports, proposals, presentations |
| **Solution Catalogs** | Markdown (.md) | Curated market-specific tool recommendations |
| **Configuration** | JSON (MCP config), YAML (workflow config) | System setup and parameterization |

### Installation & Setup Methods

The plugin is workspace-based, not package-based:

1.  **Repository Clone:** `git clone` the PluginRemoteDiscoverySession repository into the consultant's workspace
2.  **MCP Server Configuration:** Configure `claude_desktop_config.json` or equivalent with required MCP server connections (Brave Search, Firecrawl, Perplexity, Notion, CRM connectors)
3.  **API Key Provisioning:** Set environment variables for external services (Brave API, Firecrawl API, Anthropic API, CRM OAuth tokens)
4.  **BMAD Initialization:** Verify BMAD methodology files are properly structured in `_bmad/` directory
5.  **Template Verification:** Confirm V3 Corporate Design templates are present and rendering correctly
6.  **Solution Catalog Sync:** Ensure market-specific catalogs (`_de.md`, `_ru.md`) are current

**No package manager required.** The system is Git-native — versioned, branched, and updated via standard Git operations.

### API Surface & Integration Points

The plugin does not expose a traditional API. Instead, it orchestrates through:

**MCP Server Integrations (Required for MVP):**

| MCP Server | Function | Required |
|---|---|---|
| Brave Search | Web research, market analysis | Yes |
| Firecrawl | Deep web scraping, content extraction | Optional |
| Perplexity Ask | Synthesized analysis queries | Yes (on-demand) |
| Notion | Knowledge management, client workspace | Yes |
| GitHub | Per-client private repo management | Yes |
| CRM Connectors (Composio) | Salesforce/HubSpot read-only access | Market-dependent |
| CRM Connectors (Native) | Bitrix24/amoCRM/1C/Odoo/Qontak | Market-dependent |

**BMAD Workflow Entry Points:**

| Workflow | Trigger | Phase |
|---|---|---|
| Research Pipeline | `research-client {transcript}` | Phase 1 |
| Proposal Generator | `generate-proposal {research-output}` | Phase 2 |
| Legal Document Generator | `generate-legal {client-data}` | Phase 3 |
| Discovery Session Runner | `run-discovery {client-id}` | Phase 4 |
| Delivery Pipeline | `generate-delivery {session-data}` | Phase 5 |
| Catalog Update | `update-catalogs` | Operations |

### Code Examples & Workflow Patterns

- `docs/examples/trigger_research.js`: Demonstrates triggering research pipeline with fallback logic
- `docs/examples/generate_architecture.py`: Shows how to connect Discovery Session output to architecture generator
- `docs/workflows/custom_connectors.md`: Explains how to add new CRM connectors to the `ConnectorFactory`

**Migration & Upgrade Guide:**
- `docs/migration/v1_to_v2.md`: Guide for upgrading from legacy standalone Discovery tools to integrated BMAD workflow
- `docs/migration/custom_templates.md`: Instructions for preserving custom V3 Corporate Design modifications during framework updates
- Workflows must be designed to be backwards compatible with older JSON session states for returning clients.

**Typical Workflow Trigger Pattern:**
```
# Phase 1: Trigger research after initial call
/research-client --transcript ./transcripts/client-xyz.md --market DACH

# Phase 2: Generate proposal from research
/generate-proposal --client client-xyz --research ./research/client-xyz/

# Phase 3: Generate legal documents after proposal acceptance
/generate-legal --client client-xyz --jurisdiction DE --type nda,contract

# Phase 4: Run Discovery Session workflow
/run-discovery --client client-xyz --questionnaire standard-v1

# Phase 5: Generate delivery package
/generate-delivery --client client-xyz --format html --template v3-corporate
```

### Implementation Considerations

**Workspace Architecture:**
- Each Discovery Session operates within a client-specific workspace subdirectory
- Workspace isolation prevents cross-client data leakage
- Git-based versioning enables rollback and audit trail

**MCP Server Reliability:**
- External MCP servers may be unavailable or rate-limited
- Graceful degradation for each research engine (fallback order: Google → Brave → manual)
- CRM connector failures trigger flat-file ingestion mode

**Update Strategy:**
- Plugin updates via `git pull` from main repository
- Solution catalog updates via weekly scheduled workflow
- MCP server versions pinned in configuration to prevent breaking changes
- BMAD methodology updates versioned independently

**Documentation Strategy:**
- Methodology documentation is embedded in SKILL.md files and workflow step files
- No external documentation site required for MVP
- README.md provides installation and configuration guide
- Each workflow step is self-documenting via its step file

## Project Scoping & Phased Development

### MVP Strategy & Philosophy

**MVP Approach:** Problem-Solving MVP — prove that the automated consulting pipeline produces deliverables of equal or superior quality to manual consulting work, at 3x speed and 200% margin.

**Resource Requirements:** Single consultant (Alex) + Claude Code agent ecosystem. No additional team members required for MVP. Key resource investments are in workflow creation, MCP server configuration, and template development — all one-time setup costs amortized across sessions.

**MVP Philosophy:** "Build the first highway, not all highways." The MVP covers the complete 5-phase Discovery Session cycle for all three markets, but with the minimum viable automation at each step. Manual intervention is acceptable where automation is not yet reliable — the key is that the *end-to-end flow* works.

### MVP Feature Set (Phase 1)

**Core User Journeys Supported:**
- Journey 1 (Success Path): Full 5-phase cycle — research → proposal → legal → discovery → delivery
- Journey 2 (Graceful Degradation): Connector failure → flat-file fallback → session continues
- Journey 3 (Catalog Maintenance): Weekly update cycle for solution catalogs
- Journey 4 (Client Delivery): Professional receipt of Discovery delivery package

**Must-Have Capabilities:**

| # | Capability | Journey Coverage | MVP vs. Manual |
|---|---|---|---|
| 1 | Research Agent Pipeline (Google, Brave, Firecrawl, Perplexity) | J1 Phase 1 | Automated |
| 2 | Web Presence Analyzer (Schema, API, A2A) | J1 Phase 1 | Automated |
| 3 | Legal Document Generator (NDA, Contract + HITL) | J1 Phase 3 | Semi-automated |
| 4 | Discovery Session Workflow (Questionnaires, Interviews, Transcripts) | J1 Phase 4 | Semi-automated |
| 5 | Architecture Spec Generator | J1 Phase 5 | Semi-automated |
| 6 | CRM Data Audit Module (read-only) | J1 Phase 4 | Automated |
| 7 | Delivery Pipeline (HTML, V3 Corporate Design) | J1 Phase 5 | Automated |
| 8 | DACH CRM Connectors (Composio: Salesforce/HubSpot) | J1, J2 | Automated + fallback |
| 9 | RU CRM Connectors (Bitrix24/amoCRM/1C) | J1, J2 | Automated + fallback |
| 10 | ID CRM Connectors (Odoo/Mekari Qontak) | J1, J2 | Automated + fallback |
| 11 | Per-Client Private GitHub Repo | J1, J4 | Automated |
| 12 | Solution Catalog Management (weekly updates) | J3 | Semi-automated |

**"Can It Be Manual Initially?" — Decision Log:**

| Capability | Manual OK for MVP? | Decision |
|---|---|---|
| Research pipeline | No — speed is the differentiator | Must automate |
| Proposal generation | Partial — template + manual customization acceptable | Semi-automate |
| NDA/Contract generation | Partial — template + HITL review mandatory anyway | Semi-automate |
| CRM data analysis | No — manual analysis defeats the purpose | Must automate |
| Architecture spec generation | Partial — AI draft + consultant review | Semi-automate |
| Delivery pipeline | No — corporate design compliance requires templates | Must automate |
| Catalog updates | Partial — AI scan + manual review acceptable | Semi-automate |

### Post-MVP Features

**Phase 2 (Growth):**

| Feature | Dependency | Value Add |
|---|---|---|
| Parallel Architecture Generator | MVP architecture spec output | Automated "shadow process" proposals alongside client's existing workflows |
| Multi-Session Client Intelligence | Per-client GitHub repos (MVP) | Cross-session learning for returning clients; architecture evolution tracking |

**Phase 3 (Expansion):**

| Feature | Dependency | Value Add |
|---|---|---|
| Multi-Consultant Platform | Multi-Session Intelligence | Team collaboration, role-based access, white-label deliverables |
| Self-Service Discovery Lite | Full delivery pipeline (MVP) | Client-facing intake reducing consultant pre-session effort |
| Continuous Monitoring | Architecture specs + implementation | Post-delivery health checks on implemented recommendations |

### Risk Mitigation Strategy

**Technical Risks:**

| Risk | Probability | Impact | Mitigation |
|---|---|---|---|
| MCP server instability/rate limits | Medium | High | Graceful degradation chain; fallback to manual research; rate limit monitoring |
| CRM connector incompatibility (self-hosted instances) | High (RU market) | Medium | CSV/Excel fallback as first-class citizen, not afterthought |
| Template rendering inconsistencies | Low | Medium | Template validation checklist; browser testing matrix (Chrome, Firefox) |
| Claude Code API changes | Low | High | Pin API versions; maintain compatibility layer; monitor Anthropic changelog |

**Market Risks:**

| Risk | Probability | Impact | Mitigation |
|---|---|---|---|
| SME clients not ready to pay $2,400 for Discovery Session | Medium | Critical | Validate with first 4 sessions; prepare lighter $1,200 "Quick Scan" alternative |
| SaaS-pocalypse closes window faster than expected | Medium | High | Aggressive 3-month MVP; launch with minimum viable automation |
| Regulatory changes (EU AI Act enforcement) | Low | Medium | Built-in compliance checklist; adapt Scorecard as regulations finalize |

**Resource Risks:**

| Risk | Probability | Impact | Mitigation |
|---|---|---|---|
| Solo consultant bottleneck | High | Medium | Prioritize workflow automation over manual quality; accept 80% automation |
| API cost overrun (Brave, Firecrawl, Claude) | Medium | Medium | Monitor per-session API costs; set hard budget limits per research pipeline run |
| Burnout from simultaneous 3-market support | Medium | High | Stagger market launch: DACH first (month 1), RU (month 2), ID (month 3) |

## Functional Requirements

### Research & Market Intelligence

- **FR1:** Consultant can trigger automated multi-engine research based on a client conversation transcript
- **FR2:** System can orchestrate research across multiple configured search, crawling, and AI answer engines with defined trigger rules (automatic vs. on-demand)
- **FR3:** Consultant can view structured research results stored in the client workspace directory
- **FR4:** System can analyze a client's web presence for Schema Markup, API readiness, and A2A compatibility
- **FR5:** Consultant can access multi-perspective market positioning analysis for a client's business
- **FR6:** System can identify optimization opportunities (AI methods, automation, new applications, web visibility) specific to the client's industry and market

### Solution Catalog Management

- **FR7:** Consultant can browse curated solution catalogs filtered by market (DACH, RU, ID)
- **FR8:** System can scan external sources for tool and solution updates on a weekly schedule
- **FR9:** Consultant can review diff-based catalog update proposals before they are committed
- **FR10:** System can maintain version history of all catalog changes via integrated version control
- **FR11:** System can flag deprecated or discontinued tools in solution catalogs automatically

### Legal Document Generation

- **FR12:** Consultant can generate jurisdiction-specific NDA templates (DACH, RU, ID)
- **FR13:** Consultant can generate jurisdiction-specific contract templates (DACH, RU, ID)
- **FR14:** System can populate legal documents with client-specific data from workspace
- **FR15:** System can enforce mandatory HITL review gate before any legal document delivery
- **FR16:** Consultant can customize legal document templates with client-specific terms

### Discovery Session Workflow

- **FR17:** Consultant can generate structured questionnaires tailored to client industry and size
- **FR18:** Consultant can process interview transcripts and extract structured insights
- **FR19:** System can evaluate questionnaire responses against predefined assessment criteria
- **FR20:** Consultant can run the complete 5-phase Discovery Session workflow in sequence
- **FR21:** System can track session progress across all five phases with status visibility

### CRM & Data Analysis

- **FR22:** System can connect to client CRM systems in read-only mode via configured CRM connectors
- **FR23:** System can analyze CRM data quality, pipeline health, and automation gaps automatically
- **FR24:** System can detect connector failures and switch to flat-file ingestion mode
- **FR25:** Consultant can upload flat files as alternative to CRM API access
- **FR26:** System can produce identical statistical tables and analysis reports from both API and flat-file data sources

### Architecture & Recommendations

- **FR27:** System can generate a client-specific AI Readiness Scorecard based on Discovery Session inputs
- **FR28:** System can produce a data-centric architecture specification with Quick Wins and long-term roadmap
- **FR29:** System can generate solution-specific recommendations referencing current solution catalog entries
- **FR30:** System can create implementation proposals with phased timelines and cost estimates
- **FR31:** Consultant can review and customize all generated architecture specifications before delivery

### Proposal & Client Communication

- **FR32:** Consultant can generate structured, formatted proposals from research and analysis outputs
- **FR33:** System can populate proposals with V3 Corporate Design branding
- **FR34:** Consultant can customize proposal content before client delivery
- **FR35:** System can generate client communication templates for connector failures and session updates

### Delivery Pipeline

- **FR36:** System can render delivery packages as templated documents in V3 Corporate Design
- **FR37:** System can generate presentation-format deliverables (16:10 aspect ratio)
- **FR38:** System can generate artifact-format deliverables (client reports, scorecards)
- **FR39:** System can generate document-format deliverables (contracts, NDAs with headers/footers)
- **FR40:** Consultant can customize deliverables with client-specific branding (logo, company name)
- **FR41:** System can generate static document formats (read-only) of legal documents for formal delivery

### Client Data Management

- **FR42:** System can create private collaborative version-controlled repositories per client automatically
- **FR43:** System can store only anonymized data in client collaborative repositories
- **FR44:** System can enforce PII scanning before any commit to client repositories
- **FR45:** System can maintain workspace isolation between client sessions
- **FR46:** Consultant can access client workspace data across the 5 Discovery phases

### Compliance & Security

- **FR47:** System can enforce read-only access on all CRM/ERP connectors via least-privilege token grants
- **FR48:** System can mask/anonymize PII before data crosses jurisdictional boundaries
- **FR49:** System can apply jurisdiction-specific compliance rules (GDPR, 152-ФЗ, UU PDP) based on client market
- **FR50:** System can include EU AI Act compliance assessment in DACH market Scorecards
- **FR51:** System can flag high-risk AI system recommendations with conformity assessment requirements
- **FR52:** System can label AI-generated content with transparency indicators

## Non-Functional Requirements

### Performance

- **NFR1:** Research pipeline must complete automated multi-engine research within 2 hours for a standard client engagement
- **NFR2:** Web Presence Analysis must complete within 15 minutes per client website
- **NFR3:** Legal document generation (NDA/Contract) must complete within 30 minutes including template population
- **NFR4:** Architecture Spec generation must complete within 3 hours from Discovery Session data
- **NFR5:** HTML delivery package rendering must complete within 5 minutes per document
- **NFR6:** CRM data analysis must complete within 1 hour for datasets up to 10,000 records
- **NFR7:** Complete 5-phase Discovery Session must be deliverable within 5 business days end-to-end

### Security

- **NFR8:** All CRM/ERP connections must use read-only token scopes with no write permissions
- **NFR9:** All data in transit must be encrypted using current industry-standard transport encryption methods
- **NFR10:** All client data at rest must be encrypted
- **NFR11:** PII must be masked/anonymized before crossing jurisdictional boundaries (RU → external, EU → non-EU)
- **NFR12:** Client workspace directories must be isolated — no cross-client data access possible
- **NFR13:** Per-client collaborative repositories must contain only anonymized data verified by automated PII scanning
- **NFR14:** API keys and OAuth tokens must not be stored in source code or client repositories
- **NFR15:** All connector operations must be logged for audit trail purposes
- **NFR16:** Client data must be purgeable within 24 hours of delivery completion (upon request or policy)

### Reliability

- **NFR17:** System must continue functioning when any single MCP server is unavailable (graceful degradation)
- **NFR18:** CRM connector failure must trigger automatic fallback to flat-file ingestion within 30 seconds
- **NFR19:** Flat-file processing must produce analysis output with zero data variance compared to API-sourced data (processing parity)
- **NFR20:** Solution catalog updates must not disrupt active Discovery Sessions
- **NFR21:** Version control operations (repo creation, commits) must include retry logic with 3 attempts before failure notification
- **NFR22:** System must preserve all session data in local workspace even if external services fail

### Integration

- **NFR23:** MCP server connections must support configurable timeout values (default: 30 seconds per request)
- **NFR24:** CRM connectors must handle rate limiting from external APIs without data loss
- **NFR25:** Research engine fallback chain (Google → Brave → manual) must execute automatically
- **NFR26:** Collaborative platform operations must support both personal and organizational context accounts
- **NFR27:** All external API integrations must be version-pinned in configuration
- **NFR28:** MCP server configuration must be hot-reloadable without restarting the workspace

### Compliance

- **NFR29:** System must support GDPR data subject access requests (export client's data within 72 hours)
- **NFR30:** System must support GDPR right-to-erasure requests (delete client data within 72 hours)
- **NFR31:** RU personal data must remain on Russian infrastructure — only anonymized data may be exported
- **NFR32:** ID market data processing must include consent verification records per UU PDP requirements
- **NFR33:** All AI-generated deliverables must include transparency labeling per EU AI Act requirements
- **NFR34:** Legal document outputs must include jurisdiction-specific disclaimer that content requires professional legal review

### Maintainability

- **NFR35:** Solution catalogs must be updateable independently of core system components
- **NFR36:** BMAD workflow steps must be modifiable without affecting other workflow steps
- **NFR37:** New CRM connectors must be addable without modifying existing connector code
- **NFR38:** V3 Corporate Design templates must be updateable without regenerating existing deliverables
- **NFR39:** System must maintain semantic version history for all configuration and catalog changes
