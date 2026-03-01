Ziel: Erstellung eines Plugins für Claude Code (Set von Skills, MCP-Servers, Connectoren, Skripten, etc.) oder vergleichbare AI-Agenten-Umgebungen zur Durchführung des "Remote Discovery Session". 
 
Konzept von einer Remote-Variante für Discovery Session: Anhand von Informationen aus dem initialen Gespräch und der Recherche soll ein Angebot für die Durchführung von Discovery Sessions erstellt werden. Das Angebot soll eine klare Auflistung von Arbeitsschritten und Deliverables enthalten damit der Kunde den Mehrwert meiner Dienstleistung erkennt. Es sollen alle für die Discovery Session relevanten Informationen aus der Recherche und dem initialen Gespräch in das Angebot einfließen. Es sollen alle für die Discovery Session notwendige Arbeitsschritte(Interviews, Fragebogen, etc.) in dem Angebot detailliert aufgeführt werden. Es soll ein komplettes Bild über die Discovery Session vermittel werden. Es soll ein Angebot für die Durchführung von Discovery Sessions erstellt werden. Das Angebot kann in unterschiedlichen Sprachen erstellt werden(Deutsch, Englisch, Russisch), wobei primär die Sprache des Kunden verwendet werden soll. Preissrange je nach Komplexität, größe des Unternehmens, Anzahl der Mitarbeiter, soll zwischen 1000 US Dollar und 5000 US Dollar liegen. Als Zusatzleistung soll für jede vorgeschlagene technische Lösung umfassende Spezifikation(PRD, UX-Spec, Daten-Architektur) für die eingeständige (oder durch anderen Autragnehmer) Umsetzung erstellt und angeboten werden.  

Tools/Methoden für Remote Discovery Session: 
- Remote Interviews mit wichtigsten Stakeholdern 
- ausgefühlte Fragebögen, alle möglichen vorhandenen Prozessdokumente, CRM-Auszüge, Kunden-Kommunikationsbeispiele, etc, alles was man in Form von digitaler Information über eine Datenablage austauschen kann
- Analyse der vorhandenen digitalen Informationen aus IT-Systemen wie CRM, ERP via angebundenen MCP-Servern(read only) auf separaten Instanzen oder speziellen Verbindungen.
- Analyse von Webseiten, Social Media, etc. via Crawler oder MCP-Servern.
- Marktanalyse via Crawler oder MCP-Servern.  
- Erstellung von Angeboten für Remote Discovery Session
- Erstellung von Spezifikationen für Architekturen und Lösungen mit BMAD-Methodik
- Erstellung von Angeboten für Umsetzung von vorgeschlagenen Lösungen 
- Erstellung von Verträgen und NDAs
- Projektverfolgung und Management soll über eine einfache Web-Applikation erfolgen, Projektinformationen sollen auf Github in separaten privaten Repositories abgelegt werden. 
- Nach Bedarf soll ein Agenten Memory System (GCC) verwendet werden. Nutze dafür gleiche kundenprojekt-Repo. 
- Erstellung und publishing von statischen HTML (mit CSS und JS) Seiten für Präsentationen, Berichte, Angebote, etc. in Corporate Design. 
- Erstellung von rechtlichen und regulatorischen Richtlinien für jeweilige Märkte, als Leitplanke für Verträge, NDAs und für die Spezifizierung der vorgeschlagenen Lösungen.

Ablauf von gesamten Prozess:

1. Nach dem Initialen Gespräch(oder anderer Form der Informationsgewinnung) und dem daraus erstellten Transkript soll eine Internet Recherche auf Basis von vorhandenen Informationen aus dem Initialgespräch eingeleitet werden. Ziel der Recherche: Multi-perspektivische Betrachtung der Positionierung des Kunden(Untenehmen) auf dem Markt und der Optionen für die Optimierung des Geschäftserfolgs durch einführung von AI-Methoden, Automatisierungen, neuen Applikationen, etc. in Unternehmen oder anderen digitalen Massnahmen(optimierung der Webseite für Sichtbarkeit von KI-Agenten, etc). 
Dabei soll Google interne Search Engine, Brave Search Engine, Firecrawl(optional) und Perplexity Ask (nach User Aufforderung) über MCP-Server/Skills verwendet werden. Im Anschluß sollen aus der Recherche alle sinnvollen Informationen strukturiert zentral in der Workspace abgelegt werden.

2. Nach dem initialen Gespräch und der Recherche soll ein Formales Angebot für die Durchführug von einer Remote Discovery Session erstellt werden. 

3. Nach dem Feedback des Kunden auf das Angebot für die Durchführung von Remote Discovery Session soll ein Vertrag und NDA für den Kunden und AI_Seed.txt erstellt werden. 

4. Nach Vertragsabschluß erfolgt die Durchführung von Remote Discovery Session. Angefangen mit Fragebögen und Interviews, über Analysen, Entwicklung von Lösungsvorschlägen bis zur finaler Berichterstellung. Bei der Analyse und Durchführung von Remote Discovery Session soll der grundlegende Gedanke, die Erschaffung von datenzentrierter Architektur als Basis für die vollständiger Automatisierung der Businessprozesse, permanent berücksichtigt werden. Somit müssen die vorgeschlagene QuickWins als einzelne Bausteine auf dem Weg zu diesem Ziel dienen. Verwende Dafür die BMAD-Methodik. Dabei soll recherchen über aktuellsten Entwicklungen auf den AI-Markt und verwandten Gebieten ständig durchgeführt werden und in die Analyse und Entwicklung von Lösungsvorschlägen einfließen. Die Kundendatenquellen (CRM, Beschreibungen, Fragebögen, etc.) sollen in Absprache mit Kunden automatisiert ausgewertet werden. 

5. Nach der Durchführung von Remote Discovery Session soll ein Bericht, Architektur und Lösungsspezifikationen so wie das Angebot für die Umsetzung von vorgeschlagenen Lösungen als Ergebnis von Remote Discovery Session erstellt werden. 


Zusätzliche Informationen:
Informationen zum User und Unternehmen: AI_Seed.txt
Informationsbasis: Presentation_AI_SME_Russia.md Auf den Slides 21 und 22 ist eine Kompakte Beschreibung von einer Live Discovery Session zur Einführung von KI-Methoden in einem KMU beschrieben.
Corporate Design(vorläufig, finales soll noch entwickelt werden): soll angelehnt sein an design\style.css
Anforderungen an die Kundenwebseite: 20260204_Повышение видимости для ИИ.md
Infos zu SaaS in Russland(müssen regelmässig aktualisiert werden): 20260204_Saas_4_KMU_ru.md
Infos zu SaaS in Deutschland(müssen regelmässig aktualisiert werden): 20260204_SaaS_4_KMU_de.md
Brave-AI search API: https://brave.com/ai/#search-api
Composio MCP (für viele Kundenspezifische MCP-Server): https://docs.composio.dev/docs
Info für Claude Plugin: https://platform.claude.com/docs/en/agent-sdk/plugins#plugin-structure-reference
Claude Plugin für die Entwicklung von Plugins: https://github.com/anthropics/claude-plugins-official/tree/main/plugins/plugin-dev
Beispiel für Claude Plugin: https://github.com/ComposioHQ/awesome-claude-plugins
Agenten memory system: https://github.com/alstit01/GCC.git