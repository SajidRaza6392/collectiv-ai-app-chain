<p align="center">
  <img src="logo.png" alt="CollectiVAI Logo" width="400" />
</p>

<h1 align="center">CollectiVAI Chain</h1>
<h3 align="center">Democratic AI for Europe – Cosmos App-Chain</h3>

<p align="center">
  <a href="#deutsch">🇩🇪 Deutsch</a> &nbsp;|&nbsp; <a href="#english">🇬🇧 English</a>
</p>

---

## 🇩🇪 Übersicht <a id="deutsch"></a>

**CollectiVAI Chain** ist eine eigene **App-Chain** auf Basis des Cosmos-Ökosystems.  
Ziel ist eine transparente, überprüfbare Governance-Infrastruktur für demokratische Entscheidungen  
mit Fokus auf Europa und digitale Bürgerbeteiligung.

**Kernideen:**

- On-Chain-Governance (Vorschläge, Abstimmungen, Parameter-Änderungen)
- Rollen & Identitäten (z.&nbsp;B. Bürger:innen, Expert:innen, Institutionen)
- Trennung von:
  - **Infrastruktur** (Chain, Validatoren, Governance-Logik)
  - **Clients & Apps** (z.&nbsp;B. die CollectiVAI iOS/macOS App)

Dieses Repository enthält:

- den Chain-Code (`app/`, `x/`)
- das Binary (`cmd/collectivaid`)
- Netzwerkkonfigurationen (`networks/`)
- Dokumentation (`docs/`)

> ⚠️ **Aktueller Status:** Frühe Projektstruktur (**Pre-Alpha**) –  
> die eigentliche Cosmos-App-Logik wird Schritt für Schritt ergänzt.

---

## 🇩🇪 CollectiVAI App & Cosmos-Anbindung – Kurzüberblick

Die **CollectiVAI Chain** und die **CollectiVAI App** gehören zusammen, erfüllen aber unterschiedliche Rollen:

- **CollectiVAI App (iOS/macOS, Xcode-Projekt)**  
  - ist die **Benutzeroberfläche** für Bürger:innen, Expert:innen und Institutionen  
  - zeigt Vorschläge, Abstimmungen und Ergebnisse an  
  - ermöglicht das Erstellen von Proposals und das Abgeben von Votes  
  - kommuniziert über eine API / RPC-Endpunkte mit der CollectiVAI Chain

- **CollectiVAI Chain (Cosmos App-Chain)**  
  - ist die **neutrale Governance-Infrastruktur**  
  - speichert Proposals, Votes, Parameter und Rollen **on-chain**  
  - sorgt für Nachvollziehbarkeit, Transparenz und Reproduzierbarkeit  
  - läuft auf Validator-Nodes (z. B. VPS, Server, später ggf. Community-Nodes)

- **GitHub (dieses Repository)**  
  - ist der **offene Quellcode- und Dokumentationsort** für die Chain  
  - enthält:
    - den Chain-Code (`app/`, `x/collectivai/`)
    - das Binary (`cmd/collectivaid`)
    - Netzwerk-Setups (`networks/`)
    - technische und konzeptionelle Docs (`docs/`)
  - macht Entwicklung, Reviews und externe Beiträge nachvollziehbar

Die CollectiVAI App liegt in einem **eigenen Repository**, während  
die CollectiVAI Chain in diesem Repo entwickelt wird.  
Beide sind logisch verbunden, aber technisch getrennt.

---

## 🇬🇧 Overview <a id="english"></a>

**CollectiVAI Chain** is a dedicated **Cosmos-based App-Chain**  
designed as a transparent governance and voting infrastructure  
for democratic decision-making with a strong European focus.

**Core concepts:**

- On-chain governance (proposals, votes, parameter changes)
- Roles & identities (e.g. citizens, experts, institutions)
- Separation between:
  - **Infrastructure** (chain, validators, governance logic)
  - **Clients & apps** (e.g. the CollectiVAI iOS/macOS app)

This repository contains:

- the chain code (`app/`, `x/`)
- the binary (`cmd/collectivaid`)
- network configuration (`networks/`)
- documentation (`docs/`)

> ⚠️ **Current status:** Early project structure (**pre-alpha**) –  
> the actual Cosmos app logic will be added step by step.

---

## 🇬🇧 CollectiVAI App & Cosmos Integration – Summary

The **CollectiVAI Chain** and the **CollectiVAI App** belong together,  
but they serve different purposes:

- **CollectiVAI App (iOS/macOS, Xcode project)**  
  - acts as the **user interface** for citizens, experts and institutions  
  - displays proposals, votes and results  
  - allows users to create proposals and cast votes  
  - communicates with the CollectiVAI Chain via an API / RPC endpoints

- **CollectiVAI Chain (Cosmos App-Chain)**  
  - acts as the **neutral governance infrastructure**  
  - stores proposals, votes, parameters and roles **on-chain**  
  - ensures traceability, transparency and reproducibility  
  - runs on validator nodes (e.g. VPS, servers, later possibly community nodes)

- **GitHub (this repository)**  
  - is the **open source and documentation hub** for the chain  
  - contains:
    - chain code (`app/`, `x/collectivai/`)
    - the binary (`cmd/collectivaid`)
    - network setups (`networks/`)
    - technical & conceptual documentation (`docs/`)
  - enables transparent development, reviews and external contributions

The CollectiVAI App lives in a **separate repository**,  
while the CollectiVAI Chain is developed in this one.  
They are logically connected, but technically separated.

---

## 🗂 Repository structure (draft)

- `app/` – Cosmos app wiring (modules, configuration, encoding)  
- `x/collectivai/` – custom module(s) for CollectiVAI civic / governance logic  
- `cmd/collectivaid/` – main entrypoint for the CollectiVAI Chain binary  
- `networks/` – devnet / testnet configurations (e.g. `networks/devnet/`)  
- `scripts/` – helper scripts (build, run, reset devnets; planned)  
- `docs/` – documentation (overview, architecture, roadmap, governance, glossary)  
- `logo.png` – CollectiVAI project logo for this repository

---

## 📚 Documentation

- High-level overview: [`docs/01-overview.md`](docs/01-overview.md)  
- Architecture draft: [`docs/02-architecture.md`](docs/02-architecture.md)  
- Roadmap (phases): [`docs/03-roadmap.md`](docs/03-roadmap.md)  
- Governance model: [`docs/04-governance-model.md`](docs/04-governance-model.md)  
- Glossary: [`docs/99-glossary.md`](docs/99-glossary.md)

---

## 🔗 Related repositories

- Client app (iOS / iPadOS / macOS):  
  [`collectiv-ai-app`](https://github.com/collectiv-ai/collectiv-ai-app)

- Main website & public docs:  
  [`collectiv-ai.github.io`](https://github.com/collectiv-ai/collectiv-ai.github.io)
