# CollectiVAI Chain – Architecture (Draft)

## 1. Chain Identity

This section defines the basic identity of the CollectiVAI Chain.

- **Chain name:** CollectiVAI Chain  
- **Devnet chain-id:** `collectivai-devnet-1`  
- **Native token (display):** `CVA`  
- **Native token (denom):** `ucva`  
  - (1 CVA = 1,000,000 ucva – typical Cosmos-style micro-denom)

These values are **drafts** for the first devnet and can be adjusted later if needed.

---

## 2. Module Overview (Planned)

The CollectiVAI Chain is planned to be built on top of Cosmos SDK modules
plus at least one custom module:

- **Core Cosmos SDK modules (planned):**
  - `bank` – token transfers and balances
  - `staking` – validator and delegator staking
  - `gov` – on-chain governance (proposals and votes)
  - `params` – on-chain parameter management

- **Custom modules (planned):**
  - `x/collectivai` – civic / governance specific logic for the CollectiVAI project  
    (roles, participation models, additional governance features)

The exact module set and versions will be defined once the Cosmos SDK integration starts.

---

## 3. High-Level Data Flows

### 3.1 Governance Flow (simplified)

1. A user creates a **proposal** via the CollectiVAI App.
2. The app sends a transaction to the chain:
   - `MsgSubmitProposal` (or a custom message defined in `x/collectivai`).
3. The proposal is stored on-chain and becomes visible to all participants.
4. Users vote on the proposal:
   - `MsgVote` (or equivalent custom messages).
5. After the voting period ends, the chain evaluates the result
   and, if accepted, applies the corresponding changes (e.g. parameters).

### 3.2 Roles & Identities (concept)

The CollectiVAI Chain is intended to support different participant types:

- citizens
- experts
- institutions

How these roles are represented on-chain (accounts, metadata, custom module state)
will be specified in more detail as part of the `x/collectivai` module design.

---

## 4. Clients & Access

The chain is designed to be accessed by multiple clients:

- **CollectiVAI App (iOS / macOS):**
  - primary end-user client
  - communicates via RPC / API endpoints (HTTPS, gRPC, WebSocket)

- **Developer / admin tools:**
  - command line tools for managing nodes and governance operations
  - scripts stored under `scripts/` in this repository

- **Potential web frontends:**
  - dashboards for monitoring proposals, votes and network status

In later phases, additional clients (e.g. city dashboards, research tools)
can be added without changing the core chain.

---

## 5. Network Layout (Devnet)

For the initial development phase a **devnet** is planned:

- single- or few-node setup
- configuration files under `networks/devnet/`
- used to:
  - test basic transactions and governance flows
  - connect the CollectiVAI App to a running chain
  - experiment with roles and participation models

The first long-running devnet is planned to run on **cloud / VPS servers in the EU**, e.g.:

- 2–3 validator + RPC nodes  
- region: EU-based data centres (e.g. Germany / Netherlands)

Later phases may introduce:

- **public testnets** (multi-validator)
- and eventually a **mainnet** depending on project progress and governance decisions.

---

## 6. Status

This architecture document is a **draft** and will be updated as:

- the Cosmos SDK integration is added,
- the module set is refined,
- and concrete governance / role models are implemented.

Current implementation status (high level):

- Repository structure: ✅ defined  
- Chain identity (devnet, token): ✅ draft  
- Cosmos SDK wiring: ⏳ planned  
- Devnet configuration & scripts: ⏳ planned  

For a high-level conceptual overview, see also:

- `docs/01-overview.md`
