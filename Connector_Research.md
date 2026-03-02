# Technical Research: Open-Source \"Read-Only\" Connectors

**Ziel**: Identifikation existierender OSS-Implementierungen (MCP-Server, SDKs/Clients, Bridges) für CRM/ERP Systeme zur Integration in ein einheitliches Connector-Interface (strikt \"read-only\" für v1).

**Projekt**: PluginRemoteDiscoverySession (Remote Discovery Session Automatisierung)
**Märkte**: DACH, Russland, Indonesien (ICP: B2B 5–100 Mitarbeiter)

---

## 1. Composio (HubSpot, Salesforce, Microsoft 365, Google Workspace)
Composio bietet bereits fertige Enterprise-Integrationen für Tier-1 Märkte (DACH). Die Suche konzentrierte sich auf offizielle SDKs und MCP-Einbindungen.

### Kandidaten

| Repo + Owner | URL | Kat. | Lang. | Lizenz | Letzter Commit | Auth | Abgedeckte Use-Cases | Qualität | Risiken / Red Flags |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| **ComposioHQ/composio** | [Link](https://github.com/ComposioHQ/composio) | A, B | Py/TS/Go | Apache-2.0 | Aktuell (2025/2026) | OAuth2, API Key | HubSpot, SFDC, M365, Google (Kontakte, E-Mail, Repo) | Exzellent (offiziell, 500+ Apps, Typings, Tests) | Umfangreiches Framework, nicht \"nur\" read-only (Mutations möglich/müssen gefiltert werden). |
| **MCP-Mirror/ComposioHQ_composio-mcp-server** | [Link](https://github.com/MCP-Mirror/ComposioHQ_composio-mcp-server) | A | TS | Apache-2.0 | Aktuell | OAuth2 | Standard-Apps via Composio MCP Interface | Hoch | Nur Mirror des offiziellen MCP-Teils. |
| **cfdude/composio-google-workspace** | [Link](https://github.com/cfdude/composio-google-workspace) | A | TS | MIT | 2024/2025 | OAuth2 | Read-Only Docs, Mail, Calendar, Drive | Spezialisiert, production-ready | Sehr spezifisch auf GWorkspace. |

### Empfehlung
- **Best Candidate**: `ComposioHQ/composio` (Offizielles SDK)
  - **Begründung**: Composio an sich ist exakt für diesen Use-Case ausgelegt. Die offiziellen SDKs (TypeScript / Python) und der offizielle MCP-Server bringen bereits ein Standard-Interface für HubSpot, Salesforce und Workspace mit. Read-only Scopes lassen sich über die OAuth-Apps bei Composio einschränken.
- **Runner-up**: Eigener, minimaler MCP-Server/Client, der nur die Composio REST-API bzw. die read-only Endpunkte konsumiert, um die Größe des Abhängigkeitsbaums gering zu halten.

---

## 2. Bitrix24 (Tier-1 Russland)

Bitrix24 hat ein weitreichendes REST API, welches via Inbound Webhooks / OAuth angesprochen wird.

### Kandidaten

| Repo + Owner | URL | Kat. | Lang. | Lizenz | Letzter Commit | Auth | Abgedeckte Use-Cases | Qualität | Risiken / Red Flags |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| **2BAD/bitrix** | [Link](https://github.com/2BAD/bitrix) | B | TypeScript | MIT | 2024/2025 | Webhook, Token | CRM (Leads, Deals, Kontakte), User, Tasks | Sehr gut (Type-safe, modern, gepflegt) | - |
| **gunnit/bitrix24-mcp-server** | [Link](https://github.com/gunnit/bitrix24-mcp-server) | A | TS/Node | MIT | 2025 | Webhook | Umfassend (CRM-Daten, Listen) | Gut | Möglicherweise unstable oder auf spezifische API-Versionen fixiert. |
| **mesilov/bitrix24-php-sdk** | [Link](https://github.com/mesilov/bitrix24-php-sdk) | B | PHP | MIT | Aktuell | OAuth, Webhook | Alle Standard-Entities | Exzellent (Inoffizieller Standard für PHP) | Falsche Sprache für einen Node/Go/Python stack. |
| **gebvlad/bitrix24-python-sdk** | [Link](https://github.com/gebvlad/bitrix24-python-sdk) | B | Python | MIT | Aktuell | Webhook | Leichtgewichtiger Wrapper | Befriedigend | Wenig Tests / explizite Typisierung. |
| **VadimTikh/mcp_bitrix24_tasks** | [Link](https://github.com/VadimTikh/mcp_bitrix24_tasks) | A | Python | MIT | 2025 | Webhook | Nur Tasks & Comments | POC-Level | Zu stark eingeschränkt für Full-CRM Indexing. |

### Empfehlung
- **Best Candidate**: `2BAD/bitrix` (TypeScript SDK)
  - **Begründung**: Bietet als API Client das beste Developer-Erlebnis mit voll typisierten Interfaces für TypeScript. Erlaubt den sauberen Eigenbau eines read-only MCP-Servers oder Integration-Services.
- **Runner-up**: `gunnit/bitrix24-mcp-server` als fertiger MCP-Server, dessen Tools man read-only mappen/limitieren kann.

---

## 3. kommo / amoCRM (Tier-1 Russland)

Benötigt zwingend OAuth2 / Long-lived Tokens (API v4).

### Kandidaten

| Repo + Owner | URL | Kat. | Lang. | Lizenz | Letzter Commit | Auth | Abgedeckte Use-Cases | Qualität | Risiken / Red Flags |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| **ampulex-23/KommoMCP** | [Link](https://github.com/ampulex-23/KommoMCP) | A | TS | MIT | 2024/2025 | OAuth2 | Leads, Contacts, Analytics (Read-Fokus) | Gut | Niche Repo, Wartung unklar. |
| **DocAtWork2026/amocrm-mcp** | [Link](https://github.com/DocAtWork2026/amocrm-mcp) | A | TypeScript | MIT | 2024/2025 | OAuth2 | Leads, Contacts, Companies, Tasks | Gut (Features explizit dokumentiert) | Geringe Verbreitung. |
| **Blackgard/amocrm-api** | [Link](https://github.com/Blackgard/amocrm-api) | B | Python | MIT | 2024 | OAuth2 | AmoCRM v4 Endpoints | Solide Python-Lib | Könnte Updates benötigen (v4 ändert sich gelegentlich). |
| **whatcrm/go-amocrm** | [Link](https://github.com/whatcrm/go-amocrm) | B | Go | MIT | 2023/2024 | Bearer | Entities, Webhooks, Users | Robust | Go statt JS/TS (falls Stack-Mismatch), etwas älter. |
| **shevernitskiy/amo** | [Link](https://github.com/shevernitskiy/amo) | B | JS/Node | MIT | 2023 | OAuth2 | Basic API v4 Wrapper | Befriedigend | Eher verwaist / selten Updates. |

### Empfehlung
- **Best Candidate**: `ampulex-23/KommoMCP` oder `DocAtWork2026/amocrm-mcp` (als Basiscode)
  - **Begründung**: Beide implementieren bereits MCP-Server Logic in TypeScript, was viel Boilerplate für Auth & Paging (amoCRM v4 ist strikt mit Rate-Limits und Paging) abnimmt.
- **Runner-up**: \"No good OSS found\" (für 100% stabile Enterprise SDKs).
  - **Alternative**: amoCRM v4 ist eine sehr simple JSON-REST-API. Es ist am sichersten, einen eigenen minimalen Axios/Fetch Wrapper zu nutzen, der strikt `GET /api/v4/leads` u.ä. aufruft und das Token-Refresh (sehr kritisch bei amoCRM) über eine zentrale Middleware handelt.

---

## 4. Odoo (Indonesien Tier-1)

Odoo wird vorrangig über seine integrierte XML-RPC Schnittstelle (oder JSON-RPC) angesprochen. 

### Kandidaten

| Repo + Owner | URL | Kat. | Lang. | Lizenz | Letzter Commit | Auth | Abgedeckte Use-Cases | Qualität | Risiken / Red Flags |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| **ivnvxd/mcp-server-odoo** | [Link](https://github.com/ivnvxd/mcp-server-odoo) | A | TS/Node | MIT | 2025 | XML-RPC (User/Pass/DB) | Records Lesen & Suchen, Meta-Daten | Sehr Gut (Explizit für Claude/MCP) | - |
| **iraycd/odoo-xmlrpc-ts** | [Link](https://github.com/iraycd/odoo-xmlrpc-ts) | B | TS | MIT | Aktuell | XML-RPC | Alle Odoo Models | Sehr Gut (Type-safe) | Lediglich ein SDK, kein Out-of-the-Box Server. |
| **alazzi-az/laraodoo-xmlrpc** | [Link](https://github.com/alazzi-az/laraodoo-xmlrpc) | B | PHP | MIT | 2024 | XML-RPC | Alle Odoo Models | Sehr stark im Laravel Ökosystem | Falsche Sprache. |
| **mah007/odooMCP** | [Link](https://github.com/mah007/odooMCP) | A | TS | MIT | 2025 | XML-RPC | Production-ready Bridge | Gut | Eventuell überladen (Middleware logic). |
| **hachecito/odoo-mcp-improved** | [Link](https://github.com/hachecito/odoo-mcp-improved) | A | TS | MIT | 2024/2025 | XML-RPC | Odoo Query Data | Gut | Fork/Weiterentwicklung, evtl. inkonsistente Maintainance. |

### Empfehlung
- **Best Candidate**: `ivnvxd/mcp-server-odoo`
  - **Begründung**: Einer der populärsten MCP-Server für Odoo. Er bietet bereits Tools für `searchRecord`, `readRecord`, was exakt dem Read-Only Use-Case entspricht. Basiert auf XML-RPC.
- **Runner-up**: `iraycd/odoo-xmlrpc-ts` als pure Library, falls der MCP-Server in-house gebaut wird. XML-RPC in NodeJS ist nervig zu implementieren, weshalb eine gute, typsichere Lib extrem vorteilhaft ist.

---

## 5. 1C (Russland Tier-2)

1C:Enterprise publiziert APIs hauptsächlich über OData (meist v3/v4) oder eigene REST/SOAP-Schnittstellen.

### Kandidaten

| Repo + Owner | URL | Kat. | Lang. | Lizenz | Letzter Commit | Auth | Abgedeckte Use-Cases | Qualität | Risiken / Red Flags |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| **belov38/1c-odata** | [Link](https://github.com/belov38/1c-odata) | B | TS/JS | MIT | 2021/2023 | Basic Auth | General OData queries against 1C endpoints | Befriedigend, simple implementation | Etwas veraltet. 1C OData kann Tücken (kyrillische Keys etc.) haben. |
| **vvasystem/o-data** | [Link](https://github.com/vvasystem/o-data) | B | PHP | MIT | 2021 | Basic Auth | 1C REST API via OData / Metadata | Solide für PHP (häufig in RU genutzt) | Nützt im TS-Stack wenig, alt. |
| **SysUtils/1c-gateway** | [Link](https://github.com/SysUtils/1c-gateway) | C | Go/TS | MIT | 2022 | Basic Auth | Odata Middleware & Type Generation | Interessanter CodeGen Ansatz | Kompliziertes Deployment. |

### Empfehlung
- **Best Candidate**: \"No good OSS found\" (für MCP oder High-Quality TS SDK).
- **Alternative / Begründung**: Alle relevanten 1C OData-Libs sind entweder auf PHP fokussiert oder verwaist. Da 1C in jeder Installation völlig unterschiedliche Models exportiert (oft mit russischen Property-Namen), empfiehlt sich ein dynamischer Ansatz: Ein generischer **OData Client SDK** (wie `odata-client` oder `axios`) kombiniert mit eigenen Utility-Funktionen, der den `/odata/standard.odata/` Endpunkt read-only ausliest. 

---

## 6. Mekari Qontak (Indonesien Tier-2)

Qontak (von Mekari) bietet Omnichannel/WhatsApp-CRM APIs.

### Kandidaten

| Repo + Owner | URL | Kat. | Lang. | Lizenz | Letzter Commit | Auth | Abgedeckte Use-Cases | Qualität | Risiken / Red Flags |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| **mekari-engineering/qontak-api-js** | [Link](https://github.com/mekari-engineering/qontak-api-js) | B | NodeJS | MIT | 2022+ | Bearer Token | WhatsApp / Messaging, Contacts | Offiziell / Semi-Offiziell | Stark Messenger-zentriert, weniger ein reinrassiges CRM-SDK. |
| **mimamch/qontak** | [Link](https://github.com/mimamch/qontak) | B | TS | MIT | 2023 | Token | Basic Wrapper | Durchschnittlich | Eher ein Privatprojekt, keine Garantie für Vollständigkeit. |
| **maskentir/qontalk** | [Link](https://github.com/maskentir/qontalk) | B | Go | MIT | 2023 | Token | Qontak + FSM Kombi | Spezialisiert | Zu spezifisch an FSM (Finite State Machines) gekoppelt. |

### Empfehlung
- **Best Candidate**: `mekari-engineering/qontak-api-js`
  - **Begründung**: Direkt vom Provider/Ecosystem. Bietet zuverlässig die Modelle für Kontakte und Channel-Kommunikation.
- **Runner-up**: \"No good OSS found\" (für MCP-Standards).
  - **Alternative**: Einen simplen OpenAPI/REST-Fetch Client bauen. Die API-Dokumentation von Mekari Qontak ist modern; oftmals ist die auto-generierte Variante via OpenAPI-Generator (falls eine Swagger.json existiert) robuster als verwaiste Community-Packages.

---

### Zusammenfassende Architektur-Notiz
Für **Tier-1** Use Cases ist der Stack hervorragend via OSS abgedeckt. Die Existenz von dezidierten TS-basierten **MCP-Servern (Odoo, amoCRM, Bitrix24)** ist sehr wertvoll. Diese können geforkt (oder als Submodule eingebunden) und durch eine Firewall / Middleware strikt auf **READ-ONLY** (HTTP GET / Read-Records Requests) limitiert werden, was die Anforderung aus v1 effektiv löst und dem Agenten sofort strukturierten Zugriff ("Discovery") gewährt.
