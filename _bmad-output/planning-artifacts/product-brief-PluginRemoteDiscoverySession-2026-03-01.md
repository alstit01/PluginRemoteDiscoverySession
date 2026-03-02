---
stepsCompleted: [1, 2, 3, 4, 5, 6]
inputDocuments:
  - 20260301_Technical_Research_RDS_Plugin.md
  - _bmad-output/domain-research.md
date: 2026-03-01
author: Alex
---

# Product Brief: PluginRemoteDiscoverySession

<!-- Content will be appended sequentially through collaborative workflow steps -->

## Executive Summary

Das Projekt "PluginRemoteDiscoverySession" zielt auf die Entwicklung eines fortschrittlichen Claude-Plugins (bzw. eines äquivalenten Agenten-Ökosystems) ab, welches den strategischen Consulting-Prozess der "Remote Discovery Session" für kleine und mittlere Unternehmen (KMUs) in der DACH-Region, Russland und Indonesien automatisiert, standardisiert und skaliert. Das Plugin orchestriert spezialisierte Agenten, um Marktrecherchen durchzuführen (Brave Search), Kunden-IT-Systeme (via Composio MCP) auszulesen und vollautomatisiert bewertete Lösungsarchitekturen, Angebote, Verträge (NDAs) sowie Spezifikationen (PRDs, UX-Specs) zu generieren. Dadurch lässt sich der klassische Beratungsansatz für KI-Einführungen im Wert von 1.000 bis 5.000 USD signifikant beschleunigen und in ein wiederholbares, vertrauensbildendes "Produkt" für KMUs verwandeln, das innerhalb kürzester Zeit zu Proof-of-Concepts führt.

---

## Core Vision

### Problem Statement

KMUs stehen unter extremem Kostendruck und leiden massiv unter Fachkräftemangel. Obwohl künstliche Intelligenz und SaaS-Automatisierung die Lösung bieten, scheitern Unternehmen oft an der Initialhürde: unstrukturierte Daten-Silos, komplexe regulatorische Vorgaben (Compliance, EU AI Act, 152-ФЗ) und das fehlende interne Wissen ("AI Literacy"). Consulting-Dienstleistungen zur Ermittlung des Digitalisierungsbedarfs und der IT-Readiness sind klassischerweise manuell, teuer, langwierig und bieten KMUs selten sofort fassbaren Nutzen. 

### Problem Impact

Wenn dieses Problem ungelöst bleibt, verpassen KMUs entscheidende Automatisierungs-Potenziale, was in einem harten Marktumfeld ihre Wettbewerbsfähigkeit massiv gefährdet ("Opportunitätskosten"). Gleichzeitig können klassische IT-Berater ihre Dienstleistungen nicht schnell genug skalieren, da tiefgreifende IT-Analysen, das Schreiben von Angeboten und das Konzipieren von Architekturen enorme manuelle Aufwände erfordern.

### Why Existing Solutions Fall Short

Traditionelle IT-Systemhäuser versuchen oft, monolithische Systeme tief im Legacy-Code zu integrieren, was zu jahrelangen Projektlaufzeiten führt ("Lift-and-Shift"). Einmal implementierte Standard-Lösungen sind durch den rapiden Fortschritt im KI-Markt nach wenigen Wochen technologisch veraltet ("Technical Debt at Birth"). Gleichzeitig fehlen reinen neuen "AI-Agenturen" häufig das tiefe Verständnis für unternehmenskritische Systemarchitektur, Datensicherheit und Compliance. Es mangelt an einem schlanken, automatisierten Werkzeug, das die Analyse der IST-Situation (CRM, ERP, Web-Präsenz) und das Architekturoperating effizient und remote durchführt, um innerhalb weniger Tage entscheidungsreife Konzepte für sofortige "Quick-Wins" zu liefern. 

### Proposed Solution

Die Lösung ist die Automatisierung der Beratungsdienstleistung selbst durch das "PluginRemoteDiscoverySession". Ein intelligenter "Positioning Router", gesteuert durch Agenten (Researcher, Solution Architect, PM), der den Zyklus nahtlos in Claude abwickelt:
1. **Profiler & Qualitatives Audit:** Das Plugin agiert als KI-Interviewer, analysiert unstrukturierte Prozessbeschreibungen und identifiziert asynchrone Flaschenhälse (Low-Hanging Fruits), um sofortiges Vertrauen und messbaren ROI aufzuzeigen.
2. **Just-in-Time Lösungs-Design:** Automatisierte Echtzeit-Recherche (z.B. Brave Search API) nach den neuesten KI-Methoden und SaaS-Startups der letzten 1-2 Monate, um dem Kunden immer die "State-of-the-Art"-Lösung anzubieten.
3. **Audit & Architektur:** Erst nach ROI-Nachweis erfolgt der lesende Systemzugriff (via Composio MCP) auf dezidierte, vom Kunden angelegte *Parallelinstanzen/Sandboxes*. Dies ermöglicht den Entwurf von KI-Systemen, die neben Legacy-Prozessen laufen und ein Höchstmaß an Sicherheit und Compliance (DACH) oder Skalierungsgeschwindigkeit (Russland/Indonesien) garantieren.

### Key Differentiators

- **Echtzeit-Arbitrage & Disposable Architecture:** Das Plugin kreiert keine veralteten Monolithen, sondern nutzt Echtzeit-Recherche für tagesaktuelle KI-Implementierungen. Die parallele Architektur erlaubt einen einfachen Austausch der Modelle bei zukünftigen Discovery Sessions.
- **Marktabhängige Modularität:** Ein dynamisches Profiling (Location/Risk-Assessment) passt das Narrativ an (Fokus auf Sicherheit/Compliance für DACH vs. Profit/Wachstumsbeschleunigung für RU/ID).
- **Prozess-Detektiv vor System-Integration:** Das Plugin nutzt tiefes Requirements Engineering, um manuell Flaschenhälse zu finden, bevor auch nur ein API-Key übergeben wird. Dies senkt technische und psychologische Hürden drastisch.
- **Technisch-methodische Exzellenz:** Das Framework nutzt Prinzipien des Model-Based Systems Engineering (MBSE) und Know-how aus der Entwicklung von Safety-Critical Systems für unvergleichliche Struktur und inhärente Sicherheit.

---

## Target Users

### Primary Users

**Der AI Solution Architect / Consultant (User: Alex)**
- **Rolle & Kontext:** Der primäre Nutzer ist der externe Berater, der das Plugin als operativ taktische "Workbench" (Exoskelett) nutzt, um seine Delivery-Kapazität und Dienstleistungsqualität extrem zu skalieren. Alles spielt sich in seiner Arbeitsumgebung (dem Private GitHub Repository des Kunden und seinen lokalen IDEs/Web-Frontends) ab.
- **Problem:** Die Akquise, die manuelle Auswertung von Kundenprozessen und die darauf folgende, aufwändige Dokumentenerstellung (Verträge, Angebote, PRDs, Architektur-Konzepte) limitieren drastisch die Zeit, die für die eigentliche Lösungsfindung zur Verfügung steht.
- **Erfolgsvision:** Ein Agenten-Ökosystem, das im Hintergrund als orchestriertes "Backoffice" arbeitet. Es liefert zu jedem Prozessschritt das perfekte Artefakt (vom NDA bis zum HTML-Report), automatisiert Systemaudits via MCP und hält mithilfe eines Agent Memory Systems (GCC) dauerhaft den Kontext.

### Secondary Users

**Die KMU-Klienten (DACH, Russland, Indonesien)**
- **C-Level Entscheider (Geschäftsführer/COO):** Fokus auf strategischen ROI. Sie sind die *Empfänger* der erstellten Stakeholder-Berichte. Ihr Erlebnis ist geprägt von der unerwarteten Aktualität der Lösung und dem beeindruckenden Format der Delivery (interaktive HTML-Dashboards im Corporate Design).
- **IT-Administratoren des Kunden:** Zuständig für Berechtigungen. Profitieren von der Klarheit der Anforderungen, da sie lediglich dedizierte Parallelinstanzen/Sandboxes für den Lese-Zugriff der MCP-Server einrichten müssen, was ihre Sicherheitsbedenken sofort beschwichtigt.
- **ICP (Ergänzung):** B2B-Unternehmen mit ca. **5–100 Mitarbeitenden**.

### User Journey (The 5-Phase Consulting Machine)

Die Journey des primären Nutzers wird durch präzise Prozessphasen mit klar definierten Trigger-Aktionen, eingesetzten Tools und generierten Artefakten strukturiert:

1. **Phase 1: Multi-Perspektivische Markt- & Kundenrecherche**
   - *Aktion:* Auswertung von Leads/Initialgesprächen. Das Plugin führt eine tiefgehende Recherche über Marktpositionierung, Konkurrenz ("Webseiten, Social Media") und aktuelle KI-Methoden durch.
   - *Tools:* Brave Search, Firecrawl (optional), Perplexity Ask (via MCP).
   - *Artefakte:* Strukturierte Ablage der recherchierten Informationen im dedizierten Project-Workspace.

2. **Phase 2: Formales Scoping & Akquise**
   - *Aktion:* Transformation der initialen Erkenntnisse in ein maßgeschneidertes Leistungsversprechen für die eigentliche Dienstleistung.
   - *Artefakte:* Automatisierte Erstellung eines formalen und visuell ansprechenden **Angebots für die Durchführung der Remote Discovery Session**.

3. **Phase 3: Formaler Abschluss & Setup**
   - *Aktion:* Nach Angebotsrücklauf des Kunden orchestriert das Plugin die rechtlichen Leitplanken und initiiert das System-Setup.
   - *Artefakte:* Maßgeschneiderte **Verträge** und **NDAs** (unter Berücksichtigung regionaler regulatorischer Richtlinien als Leitplanke) sowie die Initialisierung der `AI_Seed.txt`. Einrichtung des Private GitHub Repo und GCC-Memorys für das Projektmanagement.

4. **Phase 4: Remote Discovery Session (Der Kernprozess)**
   - *Aktion:* Durchführung der Session basierend auf BMAD-Methodik.
   - *Sub-Aktion 1 (Qualitativ):* Remote Interviews mit Stakeholdern. Auswertung von unstrukturierten Daten (Fragebögen, Prozessdokumente, CRM-Exporte, Transkripte) zur Identifikation von "Low-Hanging Fruits".
   - *Sub-Aktion 2 (Quantitativ/System):* Lesende Analyse von digitalen IT-Systemen (CRM, ERP, Projektmanagement). Hierbei orchestriert das Plugin je nach Zielmarkt die passenden Konnektoren (z.B. DACH: Salesforce/HubSpot via dedizierten nativen MCP-Servern; RU/ID: 1C/Bitrix24/Lark via Composio oder generischen REST-Proxies) auf speziellen Kunden-Parallelinstanzen.
   - *Leitmotiv:* Jeder identifizierte Quick Win wird als Baustein in die große Vision einer komplett datenzentrischen Architektur zur Prozess-Automatisierung eingeordnet. Begleitet von ständiger Echtzeit-Forschung zum aktuellsten Stand der KI-Technologie (max. 1-2 Monate alt).

5. **Phase 5: Delivery & Follow-Up (Architektur & Folgetikett)**
   - *Aktion:* Synthese aller Discovery-Erkenntnisse in finale, geschäftsführende Dokumente zur Umsetzung. Die Entwicklung von PRDs und Architekturen bildet hiermit den strategischen Abschluss der Discovery Session.
   - *Artefakte:* **Architektur- und Lösungsspezifikationen** (inkl. Web-Applikationsplänen). **Implementierungs-Angebot** für die vorgeschlagenen Lösungen.
   - *Delivery-Format:* Statische, lokal gerenderte HTML-Seiten (mit CSS/JS) für Präsentationen und Berichte im Corporate Design des Kunden.
   - *Architektur-Präzisierung:* Als Basis für die Architektur-Spec dient ein universeller Tech-Stack (dokumentiert in `GitHub_Tech-Stack_KMU.md`), dessen Kernkomponenten als ausgewählt gelten. Dieser Stack ist jedoch nicht in Stein gemeißelt und bedarf weiterer Optimierung (z.B. fehlen dort noch auf GitHub vorhandene Claude Plugins und Claude Skill-Sets; zudem ist das Thema Lizensierung noch nicht final geklärt). Für die Erstellung der Architektur-Spec bedeutet dies: Der Fokus liegt weniger auf der generellen Auswahl des Tech-Stacks, sondern vielmehr auf der gezielten Suche und Erstellung von Plugins für den spezifischen Kunden-Use-Case sowie dem richtigen Zusammenspiel der einzelnen Applikationen.

---

## Success Metrics

### User Success (Consultant Experience)
- **High-Quality Artefakt-Generierung (Corporate Identity):** Die automatisch erstellten Dokumente und Berichte (insbesondere die HTML-Präsentationen) werden nicht nur inhaltlich exzellent, sondern stets in das zu entwickelnde Corporate Design des Consultants (`design\style.css`) eingebettet. Sie sind repräsentativ und hochgradig standardisiert.
- **Event-gesteuerte Autonomie:** Der Workflow läuft zwischen den einzelnen Eingriffen (Reviews/Freigaben) des Consultants vollkommen autark. 
- **Adaptives Kontext-Management:** Sobald dem System ein neues Informationspartikel (wie Interviewtranskripte, ausgefüllte Fragebögen, Kunden-Datensätze) übergeben wird, aktualisiert das Plugin sofort die gesamte interne Wissensbasis (GCC), analysiert die Auswirkungen auf bereits erstellte Dokumente und weist den Nutzer proaktiv auf Aktualisierungsbedarf (Impact-Analyse) hin.

### Business Objectives
- **Skalierbare Profitabilität:** Reduzierung des manuellen Aufwands für Analyse, Dokumentation und Architekturplanung auf ein Minimum, sodass der Consultant ein deutlich höheres Projektvolumen parallel bedienen kann. Die Delivery baut auf hochsicheren Konzepten auf (EDD, TDD, automatisierte Agenten), was Fehlerraten drastisch senkt.
- **Realistische & Moderne Delivery:** Die vorgeschlagenen Agenten-Ökosysteme und Automatisierungen müssen immer den technologischen State-of-the-Art verkörpern UND für das Entwicklerteam bei optimalem Zeiteinsatz marginal und sicher realisierbar sein.
- **Wettbewerbsvorteil durch Tempo & Vollständigkeit:** Lösungsarchitekturen betrachten nicht nur klassische Systeme (CRM, ERP), sondern auditieren explizit auch die Kundenwebseite in Hinblick auf ihre "KI-Sichtbarkeit" (z.B. für LLM-Agenten, Perplexity etc., basierend auf `20260204_Повышение видимости для ИИ.md`). Das positioniert das Consulting unantastbar.

### Key Performance Indicators (KPIs)
- **Margen-Ziel (ROI):** Die erstellten Angebote müssen basierend auf dem hochautomatisierten Prozess (EDD/TDD für Delivery) und dem tatsächlichen Realisierungsaufwand konstant eine **Bruttomarge von 200 %** bezogen auf den investierten Stundenaufwand sichern (Beispiel: 10h × $80 = $800 Kostenbasis → Angebot $2.400).
- **Corporate Consistency:** 100 % der freigegebenen Lösungspräsentationen entsprechen dem zentral festgelegten Corporate Webdesign (`style.css`), was den wahrgenommenen Service-Wert im KMU-Sektor drastisch steigert.

## MVP Scope

### Core Features
- **Discovery & Architektur-Spezifikation (Das Kernprodukt):** Vollständige Unterstützung der 5-Phasen-Consulting-Journey. Der Hauptfokus liegt auf der Automatisierung der Dokumentengenerierung für Akquise, rechtliches Setup (NDA, Verträge) und Lösungsarchitektur-Spezifikationen (inkl. PRDs). Da ein universeller Tech-Stack als Basis vorausgesetzt wird, fokussiert sich das Plugin bei der Architekturerstellung primär auf die Recherche und Erstellung kontextspezifischer Plugins (Claude Plugins, Skills) sowie die Orchestrierung des Zusammenspiels der Applikationen für den individuellen Kunden-Use-Case.
- **AI-Sichtbarkeits-Audit (Website):** In Phase 1 ist die vollautomatische, strukturelle Überprüfung der Kundenwebsite auf "AI-Readiness" (Lesbarkeit für RAGs & Web-Crawler wie Perplexity) integraler Bestandteil des MVP.
- **Multi-Markt Connector-Set (Read-Only, v1):** Russland: Bitrix24, kommo/amoCRM, 1C. Indonesien: Odoo, Mekari Qontak. Deutschland: über Composio-Verbindungen (konfigurationsgetrieben; Zielsysteme v1: HubSpot, Salesforce, Microsoft 365, Google Workspace).
- **Zielmarkt-spezifische MCP-Integrationen (Lesend):** Das Plugin etabliert automatisiert und zur Laufzeit der Session die passenden Verbindungen. Für dominante KMU-Systeme im DACH-Markt kommen dedizierte, native Open-Source MCP-Server zum Einsatz (z.B. **Salesforce MCP** via `tsmztech/mcp-server-salesforce` oder **HubSpot MCP** via `shinzo-labs/hubspot-mcp`), um eine maximale Informationstiefe (wie SOQL Queries oder native Object Metadata) zu gewährleisten. Für breitere Tool-Landschaften (Asana, Trello oder Odoo) fungiert **Composio MCP** als universelle Bridge. Die Fähigkeit zur **selbstständigen Skill-Sondierung und -Integration** via `awesome-claude-skills` (GitHub) – oder über generische REST API MCP Server (z.B. für SAP B1 oder Tools wie Bitrix24/1C) – ist als dynamische Fallback-Strategie fester Bestandteil des MVP.
- **Corporate Delivery Engine:** Generierung von Repräsentationsmaterialien (z. B. Architektur-Dashboards) in Form von gebrandeten statischen HTML/CSS-Seiten basierend auf dem definierten `design\style.css`.
- **Projekt-Memory via GCC:** Kontext- und Wissenserhalt für das jeweilige Kundenprojekt im Private Repository.

### Out of Scope for MVP
- **Vollautomatischer Implementierungsagent:** Das MVP übernimmt NICHT die tatsächliche Code-Umsetzung oder das Deployment der vorgeschlagenen Lösungen in die Kundenumgebung. EDD und TDD sind zwar methodische Leitlinien der Lösungsarchitektur, aber das Plugin *schreibt* im MVP keine LLM-Anwendungen für den Kunden.
- **Aktives Systemdaten-Management (Schreibender Zugriff):** Der Zugriff über die MCP-Server auf Kunden-Parallelinstanzen (CRM/ERP) ist im MVP strikt "read-only". Datenveränderungen in Kundenumgebungen sind in dieser Version ausgeschlossen.

### MVP Success Criteria
- **Fehlerfreie Artefakt-Generierung:** Das Plugin generiert aus einem unstrukturierten Interviewtranskript selbstständig rechtssichere NDAs, ein Angebot und einen initialen Architektur-Entwurf (im korrekten Corporate Design), ohne dass es zu Systemabbrüchen kommt.
- **Agile MCP-Anbindung:** Die dynamische Einbindung von unvorhergesehenen Kunden-Tools (z.B. ein seltenes Nischen-ERP) zur Laufzeit über Composio oder via GitHub-Fallback (`awesome-claude-skills`) funktioniert reibungslos für den "Read-Only"-Zugang.
- **Erste erfolgreiche Kunden-Session:** Eine komplette "Remote Discovery Session" mit einem echten Pilot-Kunden wird unter Einsatz des Plugins durchgeführt und schließt mit einem beauftragten Folge-Angebot ab.
