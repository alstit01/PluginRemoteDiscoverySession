---
stepsCompleted: ["step-01-validate-prerequisites", "step-02-design-epics", "step-03-create-stories", "step-04-final-validation"]
inputDocuments: 
  - prd.md
  - architecture.md
  - ux-design-specification.md
  - implementation-readiness-report-2026-03-03.md
---

# PluginRemoteDiscoverySession - Epic Breakdown

## Overview

This document provides the complete epic and story breakdown for PluginRemoteDiscoverySession, decomposing the requirements from the PRD, UX Design if it exists, and Architecture requirements into implementable stories.

## Requirements Inventory

### Functional Requirements

FR1: Consultant can trigger automated multi-engine research based on a client conversation transcript
FR2: System can orchestrate research across multiple configured search, crawling, and AI answer engines with defined trigger rules (automatic vs. on-demand)
FR3: Consultant can view structured research results stored in the client workspace directory
FR4: System can analyze a client's web presence for Schema Markup, API readiness, and A2A compatibility
FR5: Consultant can access multi-perspective market positioning analysis for a client's business
FR6: System can identify optimization opportunities (AI methods, automation, new applications, web visibility) specific to the client's industry and market
FR7: Consultant can browse curated solution catalogs filtered by market (DACH, RU, ID)
FR8: System can scan external sources for tool and solution updates on a weekly schedule
FR9: Consultant can review diff-based catalog update proposals before they are committed
FR10: System can maintain version history of all catalog changes via integrated version control
FR11: System can flag deprecated or discontinued tools in solution catalogs automatically
FR12: Consultant can generate jurisdiction-specific NDA templates (DACH, RU, ID)
FR13: Consultant can generate jurisdiction-specific contract templates (DACH, RU, ID)
FR14: System can populate legal documents with client-specific data from workspace
FR15: System can enforce mandatory HITL review gate before any legal document delivery
FR16: Consultant can customize legal document templates with client-specific terms
FR17: Consultant can generate structured questionnaires tailored to client industry and size
FR18: Consultant can process interview transcripts and extract structured insights
FR19: System can evaluate questionnaire responses against predefined assessment criteria
FR20: Consultant can run the complete 5-phase Discovery Session workflow in sequence
FR21: System can track session progress across all five phases with status visibility
FR22: System can connect to client CRM systems in read-only mode via configured CRM connectors
FR23: System can analyze CRM data quality, pipeline health, and automation gaps automatically
FR24: System can detect connector failures and switch to flat-file ingestion mode
FR25: Consultant can upload flat files as alternative to CRM API access
FR26: System can produce identical statistical tables and analysis reports from both API and flat-file data sources
FR27: System can generate a client-specific AI Readiness Scorecard based on Discovery Session inputs
FR28: System can produce a data-centric architecture specification with Quick Wins and long-term roadmap
FR29: System can generate solution-specific recommendations referencing current solution catalog entries
FR30: System can create implementation proposals with phased timelines and cost estimates
FR31: Consultant can review and customize all generated architecture specifications before delivery
FR32: Consultant can generate structured, formatted proposals from research and analysis outputs
FR33: System can populate proposals with V3 Corporate Design branding
FR34: Consultant can customize proposal content before client delivery
FR35: System can generate client communication templates for connector failures and session updates
FR36: System can render delivery packages as templated documents in V3 Corporate Design
FR37: System can generate presentation-format deliverables (16:10 aspect ratio)
FR38: System can generate artifact-format deliverables (client reports, scorecards)
FR39: System can generate document-format deliverables (contracts, NDAs with headers/footers)
FR40: Consultant can customize deliverables with client-specific branding (logo, company name)
FR41: System can generate static document formats (read-only) of legal documents for formal delivery
FR42: System can create private collaborative version-controlled repositories per client automatically
FR43: System can store only anonymized data in client collaborative repositories
FR44: System can enforce PII scanning before any commit to client repositories
FR45: System can maintain workspace isolation between client sessions
FR46: Consultant can access client workspace data across the 5 Discovery phases
FR47: System can enforce read-only access on all CRM/ERP connectors via least-privilege token grants
FR48: System can mask/anonymize PII before data crosses jurisdictional boundaries
FR49: System can apply jurisdiction-specific compliance rules (GDPR, 152-ФЗ, UU PDP) based on client market
FR50: System can include EU AI Act compliance assessment in DACH market Scorecards
FR51: System can flag high-risk AI system recommendations with conformity assessment requirements
FR52: System can label AI-generated content with transparency indicators

### NonFunctional Requirements

NFR1: Research pipeline must complete automated multi-engine research within 2 hours for a standard client engagement
NFR2: Web Presence Analysis must complete within 15 minutes per client website
NFR3: Legal document generation (NDA/Contract) must complete within 30 minutes including template population
NFR4: Architecture Spec generation must complete within 3 hours from Discovery Session data
NFR5: HTML delivery package rendering must complete within 5 minutes per document
NFR6: CRM data analysis must complete within 1 hour for datasets up to 10,000 records
NFR7: Complete 5-phase Discovery Session must be deliverable within 5 business days end-to-end
NFR8: All CRM/ERP connections must use read-only token scopes with no write permissions
NFR9: All data in transit must be encrypted using current industry-standard transport encryption methods
NFR10: All client data at rest must be encrypted
NFR11: PII must be masked/anonymized before crossing jurisdictional boundaries (RU → external, EU → non-EU)
NFR12: Client workspace directories must be isolated — no cross-client data access possible
NFR13: Per-client collaborative repositories must contain only anonymized data verified by automated PII scanning
NFR14: API keys and OAuth tokens must not be stored in source code or client repositories
NFR15: All connector operations must be logged for audit trail purposes
NFR16: Client data must be purgeable within 24 hours of delivery completion (upon request or policy)
NFR17: System must continue functioning when any single MCP server is unavailable (graceful degradation)
NFR18: CRM connector failure must trigger automatic fallback to flat-file ingestion within 30 seconds
NFR19: Flat-file processing must produce analysis output with zero data variance compared to API-sourced data (processing parity)
NFR20: Solution catalog updates must not disrupt active Discovery Sessions
NFR21: Version control operations (repo creation, commits) must include retry logic with 3 attempts before failure notification
NFR22: System must preserve all session data in local workspace even if external services fail
NFR23: MCP server connections must support configurable timeout values (default: 30 seconds per request)
NFR24: CRM connectors must handle rate limiting from external APIs without data loss
NFR25: Research engine fallback chain (Google → Brave → manual) must execute automatically
NFR26: Collaborative platform operations must support both personal and organizational context accounts
NFR27: All external API integrations must be version-pinned in configuration
NFR28: MCP server configuration must be hot-reloadable without restarting the workspace
NFR29: System must support GDPR data subject access requests (export client's data within 72 hours)
NFR30: System must support GDPR right-to-erasure requests (delete client data within 72 hours)
NFR31: RU personal data must remain on Russian infrastructure — only anonymized data may be exported
NFR32: ID market data processing must include consent verification records per UU PDP requirements
NFR33: All AI-generated deliverables must include transparency labeling per EU AI Act requirements
NFR34: Legal document outputs must include jurisdiction-specific disclaimer that content requires professional legal review
NFR35: Solution catalogs must be updateable independently of core system components
NFR36: BMAD workflow steps must be modifiable without affecting other workflow steps
NFR37: New CRM connectors must be addable without modifying existing connector code
NFR38: V3 Corporate Design templates must be updateable without regenerating existing deliverables
NFR39: System must maintain semantic version history for all configuration and catalog changes

### Additional Requirements

- Starter Template / Stack: BMAD Framework with Claude Code, TypeScript/Node.js for MCP servers, HTML/CSS (V3 Corporate Design) for output artifacts, Git-based local storage (no RDBMS).
- Architecture relies on standardized MCP over stdio with Graceful Degradation to flat-file (.csv/.json) on failure.
- Zero-Trust Read-Only Execution Model strictly required for connectors.
- Multi-Jurisdiction legal constraints (DACH EU AI Act/GDPR, Russia 152-ФЗ, Indonesia UU PDP).
- AI generated legal documents require mandatory Human-In-The-Loop review.
- Preference for permissive OSS licenses. GPLv3 and SSPLv1 require legal evaluation.
- PII-Scrubbing is mandated before generating any outputs saved to disk or pushed to GitHub.

### FR Coverage Map

FR1: Epic 1 - Automated multi-engine research trigger
FR2: Epic 1 - Orchestrate research across multiple engines
FR3: Epic 1 - View structured research results
FR4: Epic 1 - Analyze web presence for Schema/API/A2A
FR5: Epic 1 - Multi-perspective market positioning analysis
FR6: Epic 1 - Optimization opportunities identification
FR7: Epic 6 - Browse curated solution catalogs filtered by market
FR8: Epic 6 - Scan external sources for tool/solution updates
FR9: Epic 6 - Review diff-based catalog update proposals
FR10: Epic 6 - Version history of catalog changes
FR11: Epic 6 - Flag deprecated/discontinued tools
FR12: Epic 2 - Generate jurisdiction-specific NDA templates
FR13: Epic 2 - Generate jurisdiction-specific contract templates
FR14: Epic 2 - Populate legal documents with client data
FR15: Epic 2 - Mandatory HITL review gate before delivery
FR16: Epic 2 - Customize legal document templates
FR17: Epic 3 - Generate structured questionnaires
FR18: Epic 3 - Process interview transcripts & extract insights
FR19: Epic 3 - Evaluate questionnaire responses
FR20: Epic 3 - Run complete 5-phase Discovery Session workflow
FR21: Epic 3 - Track session progress across phases
FR22: Epic 3 - CRM systems read-only connections
FR23: Epic 3 - Analyze CRM data quality automatically
FR24: Epic 3 - Detect connector failures (graceful degradation)
FR25: Epic 3 - Upload flat files alternative
FR26: Epic 3 - Statistical processing parity (API vs Flat-file)
FR27: Epic 4 - Generate AI Readiness Scorecard
FR28: Epic 4 - Produce data-centric architecture specification
FR29: Epic 4 - Generate solution-specific recommendations
FR30: Epic 4 - Create implementation proposals
FR31: Epic 4 - Review/customize generated architecture specs
FR32: Epic 2 - Generate structured/formatted proposals
FR33: Epic 2 - Populate proposals with V3 Corporate Design
FR34: Epic 2 - Customize proposal content
FR35: Epic 4 - Client communication templates (failures/updates)
FR36: Epic 4 - Render delivery packages in V3 Corporate Design
FR37: Epic 4 - Presentation-format deliverables (16:10)
FR38: Epic 4 - Artifact-format deliverables (reports/scorecards)
FR39: Epic 2 - Document-format deliverables (contracts/NDAs)
FR40: Epic 4 - Customize deliverables branding
FR41: Epic 2 - Static document formats of legal documents
FR42: Epic 5 - Create private collaborative repos per client
FR43: Epic 5 - Store anonymized data in client repos
FR44: Epic 5 - Enforce PII scanning before commit
FR45: Epic 1 - Maintain workspace isolation
FR46: Epic 1 - Access client workspace data
FR47: Epic 3 - Enforce read-only access (token scopes)
FR48: Epic 5 - Mask/anonymize PII across jurisdictional boundaries
FR49: Epic 2 - Apply jurisdiction-specific compliance rules
FR50: Epic 4 - EU AI Act compliance assessment in DACH
FR51: Epic 4 - Flag high-risk AI system recommendations
FR52: Epic 2 - Label AI-generated content with transparency indicators

## Epic List

### Epic 1: The AI Consultant Workspace & Market Research
Consultants can perform automated, multi-engine market research, web presence audits, and competitive analysis directly from a transcript within an isolated client workspace.
**FRs covered:** FR1, FR2, FR3, FR4, FR5, FR6, FR45, FR46

### Story 1.1: Initialize Isolated Client Workspace

As a consultant,
I want to create an isolated workspace directory for a new client session,
So that all data, transcripts, and research results remain securely separated between clients.

**Acceptance Criteria:**

**Given** I start a new client engagement
**When** I run the workspace initialization command with a client identifier
**Then** a new, isolated directory structure is created for this client
**And** access to other workspaces is blocked from within this execution context.

### Story 1.2: Trigger Transcript-Based Research Orchestration

As a consultant,
I want to upload a conversation transcript to trigger automated multi-engine research,
So that I get structured baseline data orchestrated across search, crawling, and AI answer engines.

**Acceptance Criteria:**

**Given** an initialized client workspace
**When** I provide a valid transcript file and trigger the research process
**Then** the system orchestrates parallel search queries using the configured fallback chain
**And** extracts key entities and topics relevant to the client.

### Story 1.3: Analyze Client Web Presence

As a consultant,
I want the system to analyze the client's public web presence (URLs),
So that I receive technical maturity indicators including Schema Markup, API readiness, and A2A compatibility.

**Acceptance Criteria:**

**Given** the research orchestration has identified the client's primary web properties
**When** the web presence analysis module runs
**Then** the system crawls the domains
**And** outputs a structured JSON report detailing SEO/Schema metadata and detectable API endpoints.

### Story 1.4: Generate Market Positioning & Opportunities Analysis

As a consultant,
I want the system to synthesize the gathered research into a multi-perspective positioning analysis and identify specific optimization opportunities,
So that I can provide tailored strategic advice on AI and automation.

**Acceptance Criteria:**

**Given** completed web presence analysis and transcript research
**When** the analysis engine processes the combined data
**Then** a structured Markdown report is generated detailing market position and industry-specific AI/automation opportunities
**And** outputs are tailored to the specified target market.

### Story 1.5: View Structured Research Results

As a consultant,
I want to view securely structured, consolidated research results stored in the client workspace,
So that I have quick access to all context required for the subsequent Discovery Session phases.

**Acceptance Criteria:**

**Given** all automated research and analysis tasks have completed
**When** I navigate to the client's workspace output directory
**Then** I can read all generated reports in clean, formatted Markdown/JSON files
**And** the data is structured consistently across clients.

### Epic 2: Proposal & Legal Engagement Automation
Consultants can seamlessly generate branded proposals and jurisdiction-specific legal documents (NDAs, contracts) with mandatory human-in-the-loop (HITL) review gates and transparency indicators.
**FRs covered:** FR12, FR13, FR14, FR15, FR16, FR32, FR33, FR34, FR39, FR41, FR49, FR52

### Story 2.1: Generate Structured Proposals with Corporate Design

As a consultant,
I want to generate formatted proposals from research outputs branded with V3 Corporate Design,
So that I can provide professional pitches to the client.

**Acceptance Criteria:**

**Given** research and analysis results are available in the workspace
**When** I trigger the proposal generation
**Then** the system generates a proposal document populated with V3 branding
**And** structures the data appropriately for client presentation.

### Story 2.2: Customize Proposal Content

As a consultant,
I want to review and customize the generated proposal content before client delivery,
So that the proposal perfectly matches client expectations.

**Acceptance Criteria:**

**Given** a generated proposal document
**When** I access the document in the workspace
**Then** I can freely edit and adjust the text and sections
**And** the branding and layout structure remain intact.

### Story 2.3: Generate Jurisdiction-Specific Legal Templates

As a consultant,
I want to generate and customize jurisdiction-specific NDA and contract templates,
So that I comply with local market requirements (DACH, RU, ID).

**Acceptance Criteria:**

**Given** the client's jurisdiction is selected
**When** I request legal templates
**Then** the corresponding NDA and contract templates are retrieved
**And** jurisdiction-specific compliance rules are applied natively.

### Story 2.4: Populate Client Data and Transparency Labels

As a consultant,
I want the system to populate legal templates with client data and apply transparency indicators,
So that the documents are ready for formal engagement and comply with AI output transparency rules.

**Acceptance Criteria:**

**Given** selected legal templates and client data in the workspace
**When** the population process is executed
**Then** all client placeholders are accurately filled
**And** AI-generated text is explicitly labeled with transparency indicators.

### Story 2.5: Enforce HITL Review and Render Static Documents

As a consultant,
I want to pass a mandatory HITL review gate before rendering final static, read-only document formats,
So that no malformed or unverified contract is delivered.

**Acceptance Criteria:**

**Given** populated legal documents are ready
**When** I attempt to finalize them for delivery
**Then** the system blocks generation until a HITL review is explicitly confirmed
**And** upon confirmation, static (read-only) PDF/Document formats are successfully rendered.

### Epic 3: Discovery Session Execution & Automated CRM Audit
Consultants can execute the core discovery execution phase including generating questionnaires, processing transcripts, and auditing CRM data using read-only connectors or flat-file fallbacks.
**FRs covered:** FR17, FR18, FR19, FR20, FR21, FR22, FR23, FR24, FR25, FR26, FR47

### Story 3.1: Generate and Evaluate Questionnaires

As a consultant,
I want to generate structured questionnaires and have the system evaluate responses against predefined criteria,
So that I can systematically assess the client's needs.

**Acceptance Criteria:**

**Given** client size and industry parameters
**When** I trigger questionnaire generation
**Then** a tailored questionnaire is produced
**And** subsequent responses are automatically evaluated against standard assessment criteria.

### Story 3.2: Process Interview Transcripts

As a consultant,
I want to process raw interview transcripts to extract structured insights,
So that manual note-taking and analysis are automated.

**Acceptance Criteria:**

**Given** a transcript from a discovery interview
**When** I run the transcript processing module
**Then** the system extracts structured insights and key pain points
**And** stores them consistently in the workspace.

### Story 3.3: Connect and Extract CRM Data via APIs

As a consultant,
I want to connect to client CRM systems utilizing read-only, least-privilege tokens,
So that I can automatically ingest data for auditing without posing a security risk.

**Acceptance Criteria:**

**Given** valid CRM credentials
**When** I initialize the CRM connector
**Then** the connection is established with strictly read-only scopes
**And** data is extracted without altering the client's live system.

### Story 3.4: Graceful Degradation to Flat-File Ingestion

As a consultant,
I want the system to detect CRM connector failures and seamlessly switch to flat-file uploads,
So that the session is never blocked by API issues while producing identical outputs.

**Acceptance Criteria:**

**Given** an active CRM connection process
**When** the connection fails or API rate limits are exceeded
**Then** the system prompts for a flat-file upload alternative
**And** the downstream statistical processing parity remains perfectly identical to API data.

### Story 3.5: Analyze CRM Data Quality Automatically

As a consultant,
I want the ingested CRM data to be automatically analyzed for pipeline health and automation gaps,
So that I have a factual basis for my recommendations.

**Acceptance Criteria:**

**Given** successfully ingested CRM data (API or flat-file)
**When** the analysis module executes
**Then** statistical tables on data quality and pipeline health are generated
**And** clear automation gaps are mapped into output reports.

### Story 3.6: Execute and Track the Discovery Session Workflow

As a consultant,
I want to run the complete 5-phase session in sequence and track progress,
So that I maintain overview during the engagement.

**Acceptance Criteria:**

**Given** the initiation of a new discovery project
**When** I navigate through the session workflow
**Then** progress across all 5 phases is visually tracked
**And** I can see the completion status of each required module.

### Epic 4: Architecture Specification & Branded Final Delivery
Consultants can synthesize all session data to auto-generate data-centric target architecture specifications, recommendations, and AI readiness scorecards in pristine V3 Corporate Design deliverables.
**FRs covered:** FR27, FR28, FR29, FR30, FR31, FR35, FR36, FR37, FR38, FR40, FR50, FR51

### Story 4.1: Generate AI Readiness Scorecard

As a consultant,
I want the system to generate a client-specific AI Readiness Scorecard based on session inputs,
So that the client instantly understands their baseline and compliance status.

**Acceptance Criteria:**

**Given** evaluated session data
**When** I trigger scorecard generation
**Then** an AI Readiness Scorecard is generated
**And** it critically includes EU AI Act compliance assessments for DACH clients.

### Story 4.2: Produce Data-Centric Architecture Specification

As a consultant,
I want to automatically produce a data-centric architecture specification with flagged high-risk AI recommendations,
So that I have a solid technical blueprint to present to the client.

**Acceptance Criteria:**

**Given** a completed discovery session
**When** I generate the architecture specification
**Then** a structured document detailing Quick Wins and a long-term roadmap is created
**And** any recommendations qualifying as high-risk under AI regulations are explicitly flagged.

### Story 4.3: Create Implementation Proposals and Client Communications

As a consultant,
I want to create phased implementation proposals with cost estimates and communication templates,
So that the client has a transparent roadmap and seamless updates.

**Acceptance Criteria:**

**Given** the architecture specification
**When** I trigger proposal and template generation
**Then** phased timelines and cost estimate documents are generated
**And** standard client communication templates are prepared.

### Story 4.4: Review and Customize Architecture Specs

As a consultant,
I want to freely review and customize the generated specifications and apply client branding,
So that the final output perfectly aligns with the specific context.

**Acceptance Criteria:**

**Given** a generated architecture specification
**When** I edit the document in the workspace
**Then** I can customize content and inject client logos/names
**And** modifications are persisted safely.

### Story 4.5: Render Presentation and Artifact Deliverables

As a consultant,
I want to render the final delivery packages into V3 Corporate Design presentations and artifacts,
So that I have high-quality, professional assets to hand over.

**Acceptance Criteria:**

**Given** customized and finalized content
**When** I execute the rendering process
**Then** presentation-format (16:10) and artifact-format documents are produced
**And** they strictly adhere to the V3 Corporate Design templates.

### Epic 5: Private Client Repositories & Security Governance
Ensure secure delivery and version control for clients through automated creation of private Git repositories filled strictly with anonymized, PII-scrubbed data.
**FRs covered:** FR42, FR43, FR44, FR48

### Story 5.1: Automatically Create Private Version-Controlled Repositories

As a consultant,
I want the system to automatically generate secure, private Git repositories per client,
So that all project deliverables are safely version-controlled and shared.

**Acceptance Criteria:**

**Given** an authorization to publish deliverables
**When** the repository creation script runs
**Then** a private version-controlled repository is instantiated exclusively for this client
**And** basic access controls are applied.

### Story 5.2: Enforce PII Scanning and Anonymization

As a consultant,
I want the system to enforce PII scanning and masking before any commit or cross-jurisdictional transfer,
So that only anonymized data is stored and distributed externally.

**Acceptance Criteria:**

**Given** data ready to be committed to the client repository
**When** the pre-commit hook runs
**Then** a PII scanning process forcefully analyzes the payload
**And** blocks the commit if unmasked PII is found, masking data before cross-jurisdictional movement.

### Epic 6: Solution Catalog Management & Intelligence Updates
The consultant's internal intelligence base stays continuously sharp via weekly, diff-based automated market scans that update solution catalogs and deprecate outdated integrations.
**FRs covered:** FR7, FR8, FR9, FR10, FR11

### Story 6.1: Scan and Update Solution Catalogs Weekly

As a consultant,
I want the system to scan external sources weekly for tool updates and flag deprecated solutions,
So that the internal catalog remains fully up-to-date.

**Acceptance Criteria:**

**Given** external source integrations
**When** the weekly scheduled job triggers
**Then** external APIs/lists are scanned for solution updates
**And** discontinued tools are flagged or deprecated automatically.

### Story 6.2: Review Diff-Based Catalog Proposals

As a consultant,
I want to review automated diff-based catalog update proposals before they are merged,
So that I maintain quality control over recommended solutions.

**Acceptance Criteria:**

**Given** a generated update proposal from the weekly scan
**When** I review the catalog updates
**Then** I am presented with a structured diff of additions and removals
**And** I can approve or reject the proposal before it affects the database.

### Story 6.3: Browse and Version-Control Solution Catalogs

As a consultant,
I want to browse curated catalogs by market and rely on the system to maintain a version history of all changes,
So that I have a reliable and transparent intelligence base.

**Acceptance Criteria:**

**Given** the solution catalog module
**When** I browse tools
**Then** I can filter them accurately by market (DACH, RU, ID)
**And** any changes made to the catalog are stored in an integrated version history log.

