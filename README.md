<p align="center">
  <img src="logo.png" alt="CollectiVAI Logo" width="400" />
</p>

<h1 align="center">CollectiVAI App-Chain</h1>
<h3 align="center">Cosmos-based governance chain for democratic AI in Europe</h3>

<p align="center">
  <a href="https://collectivai.org">
    <img src="https://img.shields.io/badge/Website-collectivai.org-003399?style=flat" alt="Website" />
  </a>
  <a href="https://github.com/collectiv-ai/collectiv-ai-app">
    <img src="https://img.shields.io/badge/Client-CollectiVAI%20App-ffcc00?style=flat" alt="CollectiVAI App" />
  </a>
  <img src="https://img.shields.io/badge/Chain-Devnet%20%7C%20Pre--alpha-555555?style=flat" alt="Devnet" />
  <img src="https://img.shields.io/badge/Stack-Go%20%7C%20Cosmos--SDK-2c3e50?style=flat" alt="Go · Cosmos-SDK" />
  <img src="https://img.shields.io/badge/Made%20in-Europe-003399?style=flat" alt="Made in Europe" />
</p>

---

## Overview

The **CollectiVAI App-Chain** is a **Cosmos-based governance chain** for the CollectiVAI ecosystem.

Its purpose is to provide **neutral, auditable infrastructure** for:

- on-chain **proposals** (policies, projects, civic programmes),
- **votes** (citizens, experts, institutions – depending on governance rules),
- and **treasury allocations** tied to democratic, human-centred AI projects.

Core idea:

> The CollectiVAI Chain is where **long-term, public decisions live**,  
> while the CollectiVAI App and Router focus on **UX, AI assistance and routing**.

This repository contains the **chain implementation in Go**, based on the Cosmos SDK.

---

## Design goals

The chain is designed around a few simple principles:

1. **Democratic by design**  
   - Governance is not an afterthought – it is the main purpose of the chain.  
   - Proposals, votes and roles are encoded in modules and state.

2. **Human-centred**  
   - Proposals and metadata are meant to be **human-readable** first.  
   - The CollectiVAI App acts as a friendly client, not a trading UI.

3. **Auditability & transparency**  
   - All important decisions (proposals, parameter changes, treasury flows)  
     should be **traceable over time**.

4. **Modular & extensible**  
   - Built on Cosmos-SDK patterns (modules, messages, keepers).  
   - Additional modules (e.g. reputation, programme registries) can be added later.

5. **Europe-focused, globally useful**  
   - Governance logic is shaped by European democratic context,  
     but the codebase is general enough to be forked and adapted elsewhere.

---

## Repository structure (high level)

This repo follows a typical Cosmos App-Chain layout:

```text
collectiv-ai-app-chain/
├─ app/               # Cosmos app wiring (modules, keepers, encoding)
├─ cmd/
│  └─ collectivaid/   # Main binary entrypoint (CLI node)
├─ docs/              # Chain-specific documentation & specs
├─ networks/
│  └─ devnet/         # Example devnet configuration (pre-alpha)
├─ scripts/           # Helper scripts for devnet / local nodes
├─ smart-contracts/   # Placeholder for future contract-style components
├─ x/
│  └─ collectivai/    # Custom CollectiVAI module (proposals, votes, roles, etc.)
├─ go.mod
└─ README.md          # (this file)
```

> The `x/collectivai` module is where the **governance logic for CollectiVAI**  
> lives and evolves over time.

---

## Core concepts

### Proposals

A **proposal** on the CollectiVAI Chain represents a structured civic item such as:

- a university or city project,
- an AI safety programme,
- a climate-related initiative,
- or a governance parameter change.

Key properties (conceptual):

- human-readable **title & description**,
- **category / domain** (e.g. education, climate, democracy),
- **sponsor(s)** (citizens, institutions, programmes),
- requested **budget / funding source** (if applicable),
- links to **off-chain artefacts** (docs, reports, pilots, etc.).

### Voting

Votes allow different roles to express support or rejection:

- citizens,
- experts / councils,
- institutions / programmes.

The exact voting rules and weightings are **governance-configurable** and may evolve across phases (devnet → testnet → mainnet-like).

### Treasury

A treasury module (or integration) is planned to manage:

- on-chain **funding pools** (programme-based),
- **allocations to proposals** that passed governance,
- basic accountability (who allocated what to which project and when).

---

## Getting started (local dev)

> **Status:** The chain is in **pre-alpha / devnet** shape.  
> Commands and scripts may change as the modules evolve.

### 1. Prerequisites

- Go (1.22+ recommended)
- Git
- A Unix-like shell (macOS / Linux / WSL)

### 2. Clone and build

```bash
git clone https://github.com/collectiv-ai/collectiv-ai-app-chain.git
cd collectiv-ai-app-chain

# Fetch Go modules
go mod tidy

# Build the node binary (collectivaid)
go build -o ./build/collectivaid ./cmd/collectivaid
```

After this, you should have a `build/collectivaid` binary.

### 3. Initialize a local node (example)

> The exact flags and chain-IDs may change; treat the following as a **starting point**  
> and adapt to the current `app/` and `x/collectivai` configuration.

```bash
# Initialise node config & genesis
./build/collectivaid init local-dev --chain-id collectivai-devnet

# (Optional) create a local key for testing
./build/collectivaid keys add validator --keyring-backend test
```

You can then inspect the generated config in the usual Cosmos directories  
(e.g. `~/.collectivaid/config/` and `~/.collectivaid/data/`).

### 4. Start the node

```bash
./build/collectivaid start
```

This will start a **single local node**. For a richer devnet (multiple validators, funded accounts),  
use the helper files under `networks/devnet/` and `scripts/` once they are fully wired up.

---

## Relation to other CollectiVAI components

The chain is one part of a larger ecosystem:

- **CollectiVAI App (SwiftUI client)**  
  <https://github.com/collectiv-ai/collectiv-ai-app>  
  - acts as the **civic client** for citizens, experts and institutions,  
  - helps draft proposals, analyse policies and navigate governance,  
  - will later connect directly to this chain via RPC/REST/gRPC.

- **CollectiVAI Router (AI backend)**  
  <https://github.com/collectiv-ai/collectiv-ai-router>  
  - handles **multi-provider AI chat routing**,  
  - never stores API keys in the apps,  
  - can be used by both the App and other civic frontends.

- **Website & public docs**  
  <https://github.com/collectiv-ai/collectiv-ai.github.io>  
  - high-level documentation, roadmap and governance drafts.

The App-Chain is the **on-chain anchor** for all of this:  
it turns drafts and AI-assisted discussions into **actual proposals and votes**.

---

## Status & roadmap (chain)

**Current focus (pre-alpha):**

- ✅ Basic Cosmos app wiring and module layout  
- ✅ Initial `x/collectivai` module structure  
- ✅ Devnet scaffolding (directories, scripts, docs placeholders)  
- ⏳ Detailed proposal / voting / roles spec  
- ⏳ Fully scripted devnet with multiple validators & funded accounts  
- ⏳ Integration tests and simulation  
- ⏳ Public devnet for app & router integration

**Planned phases:**

1. **Devnet (internal / early adopters)**  
   - Iterate on proposal types, roles, voting rules.  
   - Connect early CollectiVAI App prototypes.

2. **Public testnet (partners / pilots)**  
   - Selected cities, universities, NGOs participate in real pilots.  
   - Governance parameters tuned with real feedback.

3. **Production-grade chain (subject to governance)**  
   - Hardening, audits, and institutional governance.  
   - Clear rules for upgrades, forks and long-term stewardship.

---

## Contributing

At this stage, the chain is a **research & prototyping platform**.

If you are:

- familiar with Cosmos-SDK / Go,
- interested in democratic governance, civic tech or AI safety,
- or want to explore pilots (city, university, NGO, EU programme),

you can:

- open issues in this repository,
- propose improvements to module design,
- or discuss pilots via the contact details on the website.

Please do **not** submit any code that embeds secrets, API keys or proprietary logic.

---

## Security notes

- This chain is **not a financial product** and not intended for speculation.  
- Devnets/testnets **must not** be used to store assets with real-world value.  
- Governance parameters and modules are still evolving; consider every network  
  non-final until clearly marked otherwise.

If you believe you found a security issue in the chain code, please use the  
**Security Policy** in this repository or reach out privately (see GitHub “Security” tab).

---

## License & branding

The code in this repository may later be published under a permissive open-source licence.  
Until then, treat it as:

> **“Public, non-confidential reference code – All rights reserved.”**

The **CollectiVAI** name, logo and visual identity are protected.  
Any use in products, services or campaigns requires prior written permission.

© 2025 David Compasso / CollectiVAI.
