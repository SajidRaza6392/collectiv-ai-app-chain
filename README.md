<p align="center">
  <img src="logo.png" alt="CollectiVAI Logo" width="400" />
</p>

<h1 align="center">CollectiVAI Chain</h1>
<h3 align="center">Democratic AI for Europe – Cosmos App-Chain</h3>

<p align="center">
  <a href="#deutsch">🇩🇪 Deutsch</a> &nbsp;|&nbsp; <a href="#english">🇬🇧 English</a>
</p>

---

## 🇩🇪 Deutsch <a id="deutsch"></a>

### Übersicht

**CollectiVAI Chain** ist eine eigene **App-Chain** auf Basis des Cosmos-Ökosystems.  
Ziel ist eine transparente, überprüfbare Governance-Infrastruktur für demokratische Entscheidungen  
mit Fokus auf Europa und digitale Bürgerbeteiligung.

Die Chain dient als neutrale, nachvollziehbare Grundlage für:

- **Abstimmungen und Entscheidungen** (Governance)
- **Rollen & Identitäten** (z.&nbsp;B. Bürger:innen, Expert:innen, Institutionen)
- **Parameter-Management** (z.&nbsp;B. Quoren, Abstimmungsfristen, Gebühren)

Die CollectiVAI iOS/macOS App (und weitere Clients) fungiert als **Frontend**,  
während die CollectiVAI Chain die **Infrastruktur- und Governance-Logik** bereitstellt.

---

### Kernideen

- **On-Chain-Governance**  
  Vorschläge, Abstimmungen und Parameter-Änderungen werden transparent on-chain abgebildet.

- **Rollen & Identitäten**  
  Unterschiedliche Rollen (Bürger:innen, Expert:innen, Institutionen) können eigene Rechte und Verantwortlichkeiten erhalten.

- **Trennung von Infrastruktur und Clients**  
  - **Infrastruktur:** Chain, Validatoren, Governance-Logik  
  - **Clients:** CollectiVAI App, Web-Frontends, weitere Tools

---

### Projektstatus

> **Status:** Frühe Projektstruktur (**Pre-Alpha**)  
> Dieses Repository definiert aktuell:
>
> - die grundlegende Struktur der App-Chain,
> - die geplante Modul-Aufteilung,
> - und die Basis für Dokumentation und Netzwerkkonfigurationen.
>
> Die eigentliche Cosmos-App-Logik wird Schritt für Schritt ergänzt.

---

### Repository-Struktur (Entwurf)

```text
collectivai-chain/
├─ cmd/
│  └─ collectivaid/        - main entrypoint for the CollectiVAI chain binary
├─ app/                    - chain application wiring (Cosmos app, modules, config)
├─ x/
│  └─ collectivai/         - custom module(s) for Civic / Governance logic
├─ docs/                   - documentation (overview, architecture, roadmap)
├─ networks/               - devnet / testnet configurations
├─ scripts/                - helper scripts (build, run, deploy)
├─ go.mod                  - Go module definition
└─ README.md               - this document

<p align="center">
  <img src="logo.png" alt="CollectiVAI Logo" width="400" />
</p>

<h1 align="center">CollectiVAI Chain</h1>
<h3 align="center">Democratic AI for Europe – Cosmos App-Chain</h3>

---

## Overview

**CollectiVAI Chain** is a dedicated **Cosmos-based App-Chain**  
designed as a transparent governance and voting infrastructure  
for democratic decision-making with a strong European focus.

The chain acts as a neutral, auditable foundation for:

- **Votes and decisions** (governance)
- **Roles & identities** (e.g. citizens, experts, institutions)
- **Parameter management** (e.g. quorums, voting periods, fees)

The CollectiVAI iOS/macOS app (and other clients) serves as the **frontend**,  
while the CollectiVAI Chain provides the **infrastructure and governance logic**.

---

## Core Concepts

- **On-chain governance**  
  Proposals, votes and parameter changes are processed in a transparent, verifiable way on-chain.

- **Roles & identities**  
  Different roles (citizens, experts, institutions) can be granted different rights and responsibilities.

- **Separation of infrastructure and clients**  
  - **Infrastructure:** chain, validators, governance logic, token economy  
  - **Clients:** CollectiVAI app, web frontends, additional tools

- **European focus**  
  Designed with democratic processes, civic participation and EU-related projects in mind.

---

## Project Status

> **Status:** Early project structure (**pre-alpha**)  
> This repository currently focuses on:
>
> - defining the base App-Chain layout,
> - designing the module structure,
> - and providing a starting point for documentation and network setup.
>
> The actual Cosmos app logic will be added step by step.

---

## Repository Structure (Draft)

```text
collectivai-chain/
├─ cmd/
│  └─ collectivaid/        - main entrypoint for the CollectiVAI chain binary
├─ app/                    - chain application wiring (Cosmos app, modules, config)
├─ x/
│  └─ collectivai/         - custom module(s) for civic / governance logic
├─ docs/                   - documentation (overview, architecture, roadmap)
├─ networks/               - devnet / testnet configurations
├─ scripts/                - helper scripts (build, run, deploy)
├─ go.mod                  - Go module definition
└─ README.md               - this document
