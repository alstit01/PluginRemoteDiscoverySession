---
stepsCompleted: [1]
inputDocuments: [GitHub_Tech-Stack_KMU.md, product-brief-PluginRemoteDiscoverySession-2026-03-01.md]
workflowType: 'research'
lastStep: 1
research_type: 'technical'
research_topic: 'Claude Plugins & Skill-Sets auf GitHub'
research_goals: 'Katalogisierung von frei verfügbaren Claude-kompatiblen Plugins (MCP-Server) und Skill-Sets auf GitHub als priorisierte Bausteine im universellen KMU-Tech-Stack für die Remote Discovery Session'
user_name: 'Alex'
date: '2026-03-02'
web_research_enabled: true
source_verification: true
---

# Research Report: Claude Plugins & Skill-Sets auf GitHub

**Date:** 2026-03-02  
**Author:** Alex  
**Research Type:** Technical  

---

## Technical Research Scope Confirmation

**Research Topic:** Claude Plugins & Skill-Sets auf GitHub  
**Research Goals:** Katalogisierung von frei verfügbaren Claude-kompatiblen Plugins (MCP-Server) und Skill-Sets auf GitHub als priorisierte Bausteine im universellen KMU-Tech-Stack, direkt einsetzbar in der Discovery Session zur Plugin-Auswahl für spezifische Kunden-Use-Cases.

**Technical Research Scope:**

- Katalog verfügbarer MCP-Server – Offizielle, community-gepflegte und use-case-spezifische Claude Plugins
- Claude Skill-Sets (awesome-claude-skills) – Review der verfügbaren Skills und ihre Einsatzszenarien
- Kategorisierung nach KMU-Use-Cases – CRM, ERP, Finanzen, HR, Kommunikation, Voice, OCR
- Lizenz & Produktionsreife – Einordnung nach MIT/Apache, „production-ready" vs. experimental
- Integrations-Patterns – Wie werden diese Plugins in Claude Code / BMAD / den universellen Tech-Stack eingebunden?

**Research Methodology:**

- Current web data with rigorous source verification
- Multi-source validation for critical technical claims
- Confidence level framework for uncertain information
- Comprehensive technical coverage with architecture-specific insights

**Scope Confirmed:** 2026-03-02

---

## 1. Executive Summary

Die Recherche hat eine umfangreiche und stark wachsende Landschaft an Model Context Protocol (MCP) Servern und Claude Skill-Sets auf GitHub identifiziert. Diese Tools erweitern die Fähigkeiten von LLMs (wie Claude) enorm, indem sie sichere und standardisierte Wege bieten, um auf externe Systeme (CRM, ERP, Datenbanken, APIs) zuzugreifen. Für den KMU-Tech-Stack sind besonders Plattformen wie **Composio** (die >500 Tools zentral mit verwalteter Authentifizierung anbieten) sowie erstklassige, offiziell gepflegte Open-Source-Integrationen (Anthropic, AWS Labs) von strategischer Bedeutung.

## 2. Katalog verfügbarer MCP-Server (Fokus KMU)

Basierend auf den Repositories `ever-works/awesome-mcp-servers` und offiziellen Verzeichnissen lassen sich die wichtigsten MCP-Server für KMUs wie folgt katalogisieren:

### 2.1 CRM, Sales & Marketing
- **HubSpot MCP Server**: Ermöglicht natürliches Sprachmanagement von Kontakten und Unternehmen inkl. Erstellung und Abruf von CRM-Datensätzen (Open Source & via Composio).
- **Salesforce & Pipeline CRM**: Integrierbar über Multi-Tool-Plattformen wie Composio mit verwaltetem Auth-Handling.
- **Notion MCP Server**: Suchen, Lesen, Aktualisieren und Erstellen von Notion-Seiten über Claude.

### 2.2 ERP & Finanzen
- **Erpnext MCP**: Direkte Integration in das Open-Source-ERP über Composio.
- **Stripe Agent Toolkit**: MCP-kompatibles Toolkit zur Interaktion mit der Stripe-API für Zahlungsprozesse und Finanzdaten.

### 2.3 Kommunikation & Collaboration
- **Slack (Anthropic Official)**: Channel-Management, Messaging und Automatisierung über LLMs.
- **Google Workspace (Gmail, Calendar, Drive)**: Umfangreiche Server zum Lesen/Schreiben von E-Mails, Terminplanung und Dateiverwaltung.
- **Discord**: Lesen und Schreiben von Nachrichten für Community-Management.

### 2.4 IT, Infrastruktur & DevOps
- **GitHub & GitLab (Anthropic Official)**: Code-Lesen, PR-Review, Issue-Management.
- **Cloud & Kubernetes**: AWS MCP Servers (offiziell von AWS Labs), Google Cloud Plattform (GCP), Azure MCP.
- **Sentry**: Fehler- und Performance-Monitoring aus Claude heraus analysieren.

### 2.5 Datenbanken & Datenanalyse
- **PostgreSQL / MySQL / MSSQL / SQLite**: Schema-Inspektion und SQL-Query-Ausführung im Read-Only- oder Lese/Schreib-Modus.
- **BigQuery / Snowflake / MotherDuck**: Für erweiterte Datenanalytik und BI.
- **Elasticsearch MCP**: Indizierung und Suchabfragen.

### 2.6 Web-Suche & Content Extraction (Voice/OCR)
- **FireCrawl MCP**: Fortgeschrittenes Web Scraping mit JavaScript-Rendering und PDF-Unterstützung (inkl. OCR-Fähigkeiten).
- **Puppeteer MCP**: Browser-Automatisierung für dynamischen Web-Content.
- **Markdownify MCP**: Konvertierung von PPTX, HTML, PDF, YouTube-Transkripten etc. in LLM-lesbares Markdown.
- **ElevenLabs MCP**: Text-to-Speech-Generierung für Voice-Ausgaben.

## 3. Claude Skill-Sets (`awesome-claude-skills`)

Neben dedizierten MCP-Servern gibt es kuratierte "Skills" und Prompts, die das Verhalten von Claude für bestimmte Aufgaben optimieren. Zu den relevanten Skill-Kategorien gehören:
- **Document Skills**: Spezialisierte Ansätze für Document Parsing, Zusammenfassung und Inhaltskorrektur.
- **Data & Analysis**: Skills zur Erstellung von Python-Skripten, die lokal über Code-Executors (z.B. E2B MCP oder Conda Code Executor) ausgeführt werden, um Daten aufzubereiten.
- **Development Tools**: Spezifische Prompt-Vorlagen für Refactoring, Bug-Hunting oder Architektur-Grobplanung.

## 4. KMU Use Cases & Plugin Mapping

In der Discovery Session können diese Tools gezielt für Kunden-Demos oder Architekturentwürfe genutzt werden:

| KMU-Bereich | Typischer Use Case | Empfohlenes Plugin / MCP Server |
| :--- | :--- | :--- |
| **Vertrieb / CRM** | Automatisierte Lead-Recherche und Eintragung ins CRM | HubSpot MCP, FireCrawl MCP für Web-Recherche |
| **Backoffice / HR** | Terminvereinbarung, Urlaubsverwaltung, Onboarding | Google Calendar MCP, Notion MCP, Slack MCP |
| **Finanzen** | Analyse von Zahlungsströmen, Abo-Verwaltung | Stripe Agent Toolkit MCP, PostgreSQL MCP |
| **Produktion / IT** | Analyse von Systemprotokollen, Bug-Tracking | Sentry MCP, GitHub MCP, AWS / Cloud MCP |
| **Marketing** | Content-Generierung und Deployment | Markdownify, Cloudinary MCP, Netlify MCP |

## 5. Lizenzmodelle & Produktionsreife

Die Analyse der GitHub-Landschaft zeigt eine starke Zweiteilung, die für die finale Tech-Stack-Auswahl essenziell ist:

1. **Enterprise-Backed / Offiziell (Produktionsreif)**:
   - *Tools*: Anthropic Reference Servers (GitHub, Slack, Postgres), AWS Labs MCPs, Supabase MCPs.
   - *Lizenz*: Häufig **MIT License** oder **Apache 2.0**. Sie sind frei verwendbar, auch in kommerziellen Kundenprojekten.
   - *Wertung*: Hervorragend für den KMU-Tech-Stack geeignet.

2. **Managed Integration Platforms (Produktionsreif)**:
   - *Tools*: **Composio** (bietet SDK und MCP-Integration für hunderte Tools wie ERPNext, Salesforce, etc.).
   - *Lizenz / Kosten*: Bietet Open-Source-SDKs (MIT), jedoch sind die Managed-Auth und Routing-Dienste des Anbieters oft kostenpflichtig (Freemium-Modell).
   - *Wertung*: Besonders nützlich, wenn komplizierte OAuth-Flows (z.B. Google, Microsoft, HubSpot) für KMUs out-of-the-box gelöst werden sollen, ohne eigene Auth-Infrastruktur aufbauen zu müssen.

3. **Community & Experimental (Proof of Concept)**:
   - *Tools*: Viele private Repositories, die MCP auf individuelle Tools mappen.
   - *Lizenz*: Oft MIT, teilweise ungeregelt.
   - *Wertung*: Gut für den "Remote Discovery Session" Mock-up, aber für echte Kundenprozesse muss Code-Audit und Security-Review (Least-Privilege-Prinzip) erfolgen.

## 6. Integrations-Patterns für den BMAD / KMU Tech-Stack

Um diese Plugins systematisch im Rahmen der "Remote Discovery Session" einzusetzen und später in Betriebsstrukturen zu überführen, empfehlen sich folgende Patterns:

### Pattern A: Self-Hosted Native MCP Server
- **Wie**: Das Plugin (z.B. Postgres MCP oder GitLab MCP) wird lokal oder in einem Firmennetzwerk-Docker-Container betrieben und über das Transportprotokoll `stdio` an den Claude Desktop Client (oder BMAD-Agenten) gebunden.
- **Konfiguration**: Einfügen in die Konfigurationsdatei (z.B. `mcp.json` oder `claude_desktop_config.json`).
- **Vorteil**: Volle Datenkontrolle, keine API-Kosten an Middleware.

### Pattern B: Managed Tool-Router via Composio
- **Wie**: Nutzung einer Middleware (wie Composio). Der AI-Agent verbindet sich mit dem *einen* Composio-MCP-Server, welcher wiederum Hunderte von Tools (ERPNext, HubSpot, X, Slack) routet.
- **Vorteil**: Löst das Problem von OAuth 2.0 Token-Refreshes. Der User (KMU-Mitarbeiter) authorisiert sich einmalig ("Connect specific credentials"). Der Agent greift sicher zu.
- **Nachteil**: Vendor Lock-in und potenzielle API-Limitationen/Kosten bei Skalierung.

### Fazit & nächste Schritte
Die verfügbaren MCP-Server (insbesondere durch Multi-Konnektoren wie Composio und etablierte Open-Source Integratoren) decken bereits heute fast alle gängigen KMU-Use-Cases (HR, CRM, ERP, IT, Marketing) ab. Dies bestärkt die Entscheidung, die *Architektur-Spezifikation* in Phase 5 der Discovery Session aktiv um MCP-Plugin-Integrationen herum zu bauen. 

Offene Restpunkte (z. B. Anthropic Platform Commercial Terms für den tatsächlichen Agentenbetrieb beim Kunden) sollten in einem separaten Legal/Compliance Workflow geprüft werden, aber technologisch ist der Baukasten auf GitHub mehr als bereit für die Produktion.
