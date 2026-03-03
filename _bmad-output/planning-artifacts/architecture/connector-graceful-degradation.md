# Rollback-Strategie & Graceful Degradation (MVP Connector-Ausfälle)

## Konzept
Eine zentrale Schwäche von Multi-Agenten-Systemen und Remote Discovery Sessions ist das Scheitern bei der Systemanbindung (Lesezugriff). Wenn ein MCP-Konnektor (z.B. Composio) nicht lädt, eine API-Limitierung greift, oder sich die Kunden nicht erfolgreich per OAuth einloggen können, darf der **Discovery-Flow nicht sterben**.

Dafür etabliert das Plugin eine mehrstufige **Graceful Degradation Strategie** (elegantes Rückfallen auf weniger automatisierte Optionen).

## Fallback-Ebenen

### Ebene 1: Redundantes Polling & Rate-Limit Backoff (Das Agentennetz)
- **Problem:** API-Limit überschritten / Temporärer 503-Fehler beim Ziel-Tool.
- **Strategie:** Der Agent führt bei API-Errors automatisch Retry-Algorithmen (Exponential Backoff) durch, bevor er abbricht. Der User wird asynchron über eine mögliche Verzögerung informiert.

### Ebene 2: Flat File Fallback (Asynchroner Daten-Drop)
- **Problem:** Der Kunde bekommt die OAuth-App nicht autorisiert / Konnektor ist veraltet.
- **Strategie:** Das Plugin unterbricht den Prozess und triggert den `PMAgent`. Dieser sendet dem Consultant/Kunden eine klare Anleitung, wie er die benötigten Daten als `.csv`, `.xlsx` oder System-Export manuell aus dem CRM zieht (z.B. "Exportiere Kontakte").
- **Ausführung:** Sobald das File in einen definierten Dropbox-Ordner (oder GitHub Repo) gedroppt wird, analysiert der Architect-Agent diese Flat-Files und führt die Discovery Session datengetrieben weiter.

### Ebene 3: Qualitativer Fallback (Das "Menschliche" Review)
- **Problem:** Weder API funktioniert, noch existieren saubere Export-Formate beim Kunden. System-Metadaten können nicht geparst werden.
- **Strategie:** Die Discovery Session stuft sich dynamisch zu einer reinen architektonischen **Top-Down-Session** herunter. Der Agent verlässt sich zu 100% auf die gesammelten qualitativen Interview-Transkripte ("Sub-Aktion 1") und baut ein theoretisches Architektur-Zieldesign, wobei die technische Migrationsebene in das Angebot als "manuelles Audit & API-Evaluation Phase 1" eingereist wird.

## Fazit für das MVP
Der Erfolg der Automatisierung misst sich an ihrer Widerstandsfähigkeit. An jedem neuralgischen API-Callpunkt wird ein "Try/Catch" hinterlegt, welches den Workflow auf den Flat-File-Fallback (`Ebene 2`) umbiegt und dem User via UI/Telegram klare Handlungsanweisungen gibt, um die "Session am Leben zu halten".
