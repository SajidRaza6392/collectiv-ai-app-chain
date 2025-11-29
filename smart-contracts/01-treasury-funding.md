# CollectiVAI Treasury & Public-Goods Funding

> 🇬🇧 English first · 🇩🇪 Deutsch weiter unten

---

## 🇬🇧 1. Purpose

The **CollectiVAI Treasury** is a smart-contract based funding mechanism  
for **public-interest and civic-tech projects** – not a DeFi yield farm.

It is designed to:

- transparently manage a budget (tokens or points),
- distribute funding according to clear, on-chain rules,
- support democratic decision-making about **which projects get funded**.

Typical use-cases:

- city or regional „citizen budget“,
- university or foundation grants for civic-tech / AI projects,
- EU or national pilot programmes for democratic digital infrastructure.

The Treasury lives on the **CollectiVAI Chain** (Cosmos App-Chain)  
and can later be exposed in the **CollectiVAI App** as a dedicated „Funding“ section.

---

## 🇬🇧 2. Actors

- **Funders**
  - institutions such as cities, regions, universities, foundations, EU programmes
  - deposit tokens / points into the Treasury

- **Project Owners**
  - submit proposals for funding (projects, pilots, studies, tools)

- **Participants / Citizens**
  - support projects through votes or contribution points
  - do **not** speculate or trade, but signal preferences

- **Governance (CollectiVAI)**
  - defines the rules of the Treasury via on-chain governance:
    - allocation method (simple voting, quadratic funding, etc.)
    - eligibility criteria
    - timelines and phases

---

## 🇬🇧 3. Funding Models (Draft)

### 3.1 Simple Budget Voting

- A fixed budget (e.g. 100,000 units) is available for a round.
- Projects submit a requested amount and description.
- Participants vote which projects should receive funding.
- After the round:
  - the contract distributes the budget according to the chosen rule:
    - top-N projects
    - proportional to votes
    - or threshold-based (only projects above X votes).

### 3.2 Quadratic Funding (QF)

Quadratic Funding is a well-known public-goods mechanism:

- many **small** contributions from many people count more than
  a few large contributions.
- the contract calculates a **matching pool allocation** based on
  how many unique supporters each project has.

In CollectiVAI:

- contributions may be:
  - symbolic civic tokens / points,
  - or just „support signals“ that the contract interprets.
- QF is particularly suited for:
  - grassroots / local projects,
  - open-source and civic-tech tools.

### 3.3 Multi-Round Funding

- funding can be organised in rounds:
  - exploration → pilot → scale-up.
- projects that succeed in one round can qualify for the next one,
  based on impact reports and governance decisions.

---

## 🇬🇧 4. High-Level Flow

```text
1. Treasury round is configured
   - budget, rules, timeline

2. Project submissions open
   - owners submit proposals (title, description, budget, impact)

3. Support / voting phase
   - citizens, experts and institutions express support
   - optional: weighting by participation / reputation score

4. On-chain allocation
   - contract computes result based on chosen mechanism (simple, QF, …)

5. Funding decision
   - allocation is finalised and recorded on-chain
   - off-chain payout or on-chain transfer, depending on integration
