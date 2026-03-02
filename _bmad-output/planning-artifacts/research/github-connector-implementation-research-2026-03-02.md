---
date: 2026-03-02
author: Alex
project: PluginRemoteDiscoverySession
purpose: "GitHub-Recherche nach existierenden Connector-/MCP-Implementierungen für Zielsysteme"
status: draft
---

# GitHub Connector Implementation Research (2026-03-02)

## Ziel

Existierende Open-Source-Implementierungen (Libraries, SDKs, Integrations-Server, ggf. MCP-Server) für die folgenden Systeme identifizieren und bewerten:

- Russland: Bitrix24, kommo/amoCRM, 1C
- Indonesien: Odoo, Mekari Qontak
- Deutschland (DACH): primär via Composio-Verbindungen (konfigurationsgetrieben; Zielsysteme v1: HubSpot, Salesforce, Microsoft 365, Google Workspace; SAP initial bewusst ausgeschlossen)

## Scope-Kontrolle (Leitplanken)

- v1 ist **read-only** (keine write-APIs, keine Mutations)
- Connectoren müssen in einen **einheitlichen Contract** passen (Capabilities-Matrix, optionale Features nicht voraussetzen)
- Jeder Connector-Call ist **auditierbar** (Event-Log), und je nach Risk-Level **Human-in-the-loop** freigabepflichtig

## Suchstrategie (GitHub)

### GitHub UI (manuell)

Nutze pro System mindestens diese Suchachsen:
- `mcp` / `model context protocol` / `mcp server`
- `api client` / `sdk` / `connector` / `integration`
- Sprache: `typescript`, `node`, `python`, `go` (nach geplanter Implementierung)

Beispiel-Queries (copy/paste):
- Bitrix24: `bitrix24 mcp`, `bitrix24 api client typescript`, `bitrix24 rest api sdk`
- kommo/amoCRM: `amocrm api client`, `kommo api client`, `amocrm oauth`, `kommo sdk`
- 1C: `1c api client`, `1c enterprise rest`, `1c odata`, `1C:Enterprise OData`
- Odoo: `odoo mcp`, `odoo api client`, `odoo xmlrpc client`, `odoo jsonrpc client`
- Mekari Qontak: `qontak api`, `mekari qontak api client`, `qontak whatsapp api`
- Composio: `composio mcp`, `composio connector`, `composio sdk`

### GitHub CLI (falls verfügbar)

Repo-Suche:
- `gh search repos "bitrix24 api client" --limit 20`
Code-Suche:
- `gh search code "Bitrix24" --language TypeScript --limit 20`

## Bewertungsrubrik (pro Kandidat)

- **Aktivität:** letzter Commit, Issues/PRs offen/geschlossen, Release-Frequenz
- **Lizenz:** kompatibel mit kommerziellem Einsatz
- **Auth:** OAuth/Token, dokumentiert, testbar
- **API-Coverage:** Minimalset für RDS (Read-Only) abgedeckt?
- **Qualität:** Tests, Typisierung, Error-Handling, Rate-Limits/Backoff
- **Erweiterbarkeit:** klare Abstraktionen, gute Docs

## Candidate Capture (auszufüllen)

> Hinweis: Diese Tabelle ist das Ziel-Format. Konkrete Repo-Namen/Links werden nach der GitHub-Recherche ergänzt.

### Bitrix24

| Typ | Kandidat | Sprache | Lizenz | Aktivität | Notizen |
|---|---|---|---|---|---|
| MCP Server | TBD | TBD | TBD | TBD | Suche nach “bitrix24 mcp server” |
| SDK/Client | TBD | TBD | TBD | TBD | REST/ OAuth? |
| Sonstiges | TBD | TBD | TBD | TBD |  |

### kommo / amoCRM

| Typ | Kandidat | Sprache | Lizenz | Aktivität | Notizen |
|---|---|---|---|---|---|
| MCP Server | TBD | TBD | TBD | TBD | Suche nach “amocrm mcp” / “kommo mcp” |
| SDK/Client | TBD | TBD | TBD | TBD | OAuth flows, rate-limits |
| Sonstiges | TBD | TBD | TBD | TBD |  |

### 1C

| Typ | Kandidat | Sprache | Lizenz | Aktivität | Notizen |
|---|---|---|---|---|---|
| MCP Server | TBD | TBD | TBD | TBD | Unwahrscheinlich; eher REST/OData bridge |
| SDK/Client | TBD | TBD | TBD | TBD | Fokus: OData/HTTP read-only |
| Sonstiges | TBD | TBD | TBD | TBD |  |

### Odoo

| Typ | Kandidat | Sprache | Lizenz | Aktivität | Notizen |
|---|---|---|---|---|---|
| MCP Server | TBD | TBD | TBD | TBD | Suche nach “odoo mcp server” |
| SDK/Client | TBD | TBD | TBD | TBD | XML-RPC / JSON-RPC |
| Sonstiges | TBD | TBD | TBD | TBD |  |

### Mekari Qontak

| Typ | Kandidat | Sprache | Lizenz | Aktivität | Notizen |
|---|---|---|---|---|---|
| MCP Server | TBD | TBD | TBD | TBD | Suche nach “qontak mcp” |
| SDK/Client | TBD | TBD | TBD | TBD | WhatsApp/CRM API? |
| Sonstiges | TBD | TBD | TBD | TBD |  |

### Composio (DACH)

| Typ | Kandidat | Sprache | Lizenz | Aktivität | Notizen |
|---|---|---|---|---|---|
| SDK/Client | TBD | TBD | TBD | TBD | DACH-Connectoren via Konfiguration |
| MCP/Bridge | TBD | TBD | TBD | TBD | Prüfen, ob MCP-first möglich ist |

## Entscheidungsvorlage (v1 “Tier-1 must work”)

Wenn die Implementierungsrisiken hoch sind, priorisieren:
1) **Odoo** (breit, gut dokumentierbar)
2) **Bitrix24** (regional wichtig)
3) **amoCRM/kommo** (regional wichtig)
4) **1C** (hoher Wert, aber potenziell hoher Integrationsaufwand)
5) **Qontak** (ID-spezifisch; abhängig von API-Reife)

Diese Reihenfolge ist ein Vorschlag und wird nach ICP-Realität und GitHub-Fundlage finalisiert.
