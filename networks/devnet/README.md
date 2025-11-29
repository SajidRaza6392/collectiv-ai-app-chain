# CollectiVAI Chain – Devnet

This folder will contain configuration files and scripts
for running a local or remote **devnet** of the CollectiVAI Chain.

The devnet is the first step before a public testnet or mainnet.
It is used to experiment with governance flows, roles and app integration.

---

## Planned contents

- `config/`  
  Sample configuration files:
  - `app.toml`
  - `config.toml`
  - `genesis.json` (initial chain state)

- `scripts/`  
  Helper scripts to:
  - start a single-node devnet
  - start a multi-node (cloud/VPS) devnet
  - reset the chain state for testing

- Documentation  
  - how to run a node (locally or on a VPS)
  - how to connect a client (e.g. the CollectiVAI App)
  - how to submit a simple proposal and vote on it

---

## Planned devnet topology (cloud)

The first long-running devnet is planned to run on **cloud / VPS servers in the EU**:

- 2–3 validator + RPC nodes  
  - 2–4 vCPUs  
  - 4–8 GB RAM  
  - 80–200 GB SSD  
- Region: EU-based data centres (e.g. Germany / Netherlands)

Basic chain identity (draft):

- **Chain-ID:** `collectivai-devnet-1`  
- **Token display:** `CVA`  
- **Token denom:** `ucva` (1 CVA = 1,000,000 ucva)

These values are drafts for the devnet and can be adjusted later.

---

## Usage goals

The devnet will be used to:

- test the CollectiVAI governance flow:
  - create proposals
  - vote on proposals
  - observe the final decisions
- experiment with different roles and parameters
- connect the **CollectiVAI App** as a client:
  - read proposals and votes from the devnet
  - submit transactions (proposals, votes) to the devnet

---

## Status

This devnet description is a **planning draft**.  
Concrete configuration files and scripts will be added
once the Cosmos SDK integration for the CollectiVAI Chain starts.
