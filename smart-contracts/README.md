# CollectiVAI Smart Contracts – Civic Infrastructure, not Casino

> 🇩🇪 Deutsch weiter unten  
> 🇬🇧 English first

---

## 🇬🇧 Why Smart Contracts in CollectiVAI?

CollectiVAI is not a DeFi platform and not a trading app.  
Smart contracts in this project are used as **civic infrastructure**, not as a casino.

The main goals:

- **Transparency** – rules and decisions are encoded in open, verifiable contracts  
- **Traceability** – every proposal, vote and allocation can be audited  
- **Fairness** – the same rules apply to everyone, no hidden backdoors  
- **Public value** – focus on democracy, public goods and civic participation

Smart contracts are one building block of the wider CollectiVAI ecosystem:
they complement the **CollectiVAI App** (frontend) and the **CollectiVAI Chain** (Cosmos App-Chain).

---

## Planned civic use-cases

### 1. Governance Treasury & Public-Goods Funding

A **Treasury smart contract** can hold a budget (tokens or points)  
and distribute it according to transparent rules decided by governance.

Possible scenarios:

- City / region / university funds digital or civic-tech projects  
- Budget is split via on-chain votes or quadratic funding  
- All steps are visible:
  - who proposed which project
  - who supported it
  - how the final allocation was calculated

Key properties:

- No leveraged trading, no speculation features  
- Designed for **grants, pilots and public-interest projects**

---

### 2. Civic Reputation & Participation Points

Instead of speculative tokens, CollectiVAI can issue **non-transferable reputation**:

- Participation points for:
  - voting regularly
  - providing expert feedback
  - moderating discussions
- Badges for:
  - long-term engagement
  - topic expertise (e.g. climate, housing, digital rights)

Technical ideas:

- Soulbound tokens / non-transferable scores  
- Stored in smart contracts, displayed in the CollectiVAI App profile

Use in governance:

- certain processes may require:
  - minimum participation score
  - expert tags to comment on specialised proposals

Again: this is about **trust & accountability**, not about trading.

---

## Design principles

Smart contracts in CollectiVAI follow these principles:

1. **Civic first, not DeFi first**  
   – no yield farming, no leverage, no speculative tokenomics.

2. **Human-readable rules**  
   – for every contract there must be a human-readable description in `docs/`.

3. **Auditability**  
   – contract code and parameters should be reviewable by independent experts.

4. **Regulatory awareness**  
   – design with EU regulation and public-sector use in mind (no hidden securities).

---

## Relation to the CollectiVAI Chain & App

- The **CollectiVAI Chain** provides the base layer for governance and identity.  
- Smart contracts implement specific civic mechanisms:
  - funding rules
  - reputation systems
  - advanced voting schemes

The **CollectiVAI App** will later expose these features via dedicated screens:

- Funding / Grants tab (Treasury)  
- Profile & Reputation tab (Participation points, badges)  

---

## Status

This folder documents the **concept and design** of smart contract components.  
Implementation details (Cosmos modules / CosmWasm contracts) will be added  
once the core chain and governance flows are stable.

---

---

## 🇩🇪 Warum Smart Contracts in CollectiVAI?

CollectiVAI ist keine DeFi-Plattform und keine Trading-App.  
Smart Contracts werden hier als **demokratische Infrastruktur** eingesetzt – nicht als Casino.

Die Hauptziele:

- **Transparenz** – Regeln und Entscheidungen stehen offen im Contract  
- **Nachvollziehbarkeit** – jede Abstimmung und Verteilung ist prüfbar  
- **Fairness** – gleiche Regeln für alle, keine versteckten Hintertüren  
- **Öffentlicher Mehrwert** – Fokus auf Demokratie, Gemeinwohl und Beteiligung

Smart Contracts ergänzen:

- die **CollectiVAI App** (Oberfläche) und  
- die **CollectiVAI Chain** (Cosmos App-Chain).

---

## Geplante Anwendungsfälle

### 1. Governance Treasury & Fördertopf

Ein **Treasury-Smart-Contract** hält ein Budget (Token oder Punkte)  
und verteilt es nach transparenten, gemeinsam beschlossenen Regeln.

Typische Szenarien:

- Stadt / Region / Hochschule fördert digitale oder Civic-Tech-Projekte  
- Budget wird über On-Chain-Abstimmungen oder Quadratic Funding verteilt  
- Alle Schritte sind sichtbar:
  - wer welches Projekt vorgeschlagen hat
  - wer es unterstützt hat
  - wie die finale Verteilung berechnet wurde

Wichtig:

- keine Hebel, kein Trading, keine DeFi-Spielereien  
- gedacht für **Förderungen, Pilotprojekte und Gemeinwohl-Projekte**

---

### 2. Civic Reputation & Beteiligungs-Punkte

Statt spekulativer Token kann CollectiVAI **nicht handelbare Reputation** vergeben:

- Beteiligungspunkte für:
  - regelmäßige Teilnahme an Abstimmungen
  - qualifizierte Kommentare
  - Moderations- oder Expert:innenarbeit
- Badges für:
  - langfristiges Engagement
  - Fachgebiete (z. B. Klima, Wohnen, digitale Rechte)

Technische Idee:

- Soulbound Tokens / nicht übertragbare Scores  
- im Smart Contract gespeichert, in der CollectiVAI App im Profil sichtbar

Nutzung in der Governance:

- bestimmte Prozesse können z. B. verlangen:
  - Mindest-Beteiligungsscore
  - bestimmte Expert:innen-Badges für Fachkommentare

Auch hier: **Vertrauen & Verantwortung**, nicht Spekulation.

---

## Designprinzipien

Smart Contracts in CollectiVAI folgen diesen Prinzipien:

1. **Civic first, nicht DeFi first**  
   – keine Yield-Farming- oder Trading-Features.

2. **Menschenlesbare Regeln**  
   – zu jedem Contract gibt es eine Beschreibung in `docs/`.

3. **Prüfbarkeit**  
   – Code und Parameter sollen von unabhängigen Expert:innen geprüft werden können.

4. **Regulatorische Sensibilität**  
   – Ausrichtung an EU-Rahmen und Public-Sector-Einsatz (kein verstecktes Wertpapier).

---

## Bezug zur CollectiVAI Chain & App

- Die **CollectiVAI Chain** liefert die Basis für Governance und Identitäten.  
- Smart Contracts implementieren konkrete Mechanismen:
  - Förderlogik
  - Reputationssysteme
  - erweiterte Abstimmungsverfahren

Die **CollectiVAI App** wird diese Funktionen später über eigene Bereiche anzeigen:

- Funding / Förder-Tab (Treasury)  
- Profil & Reputation (Beteiligungspunkte, Badges)

---

## Status

Dieser Ordner beschreibt zunächst **Konzept und Ziele** der Smart-Contract-Komponenten.  
Konkrete Implementierungen (Cosmos-Module / CosmWasm-Contracts) folgen,  
sobald Chain und Grund-Governance stabil sind.
