# CollectiVAI Chain – Glossary (Draft)

This glossary explains key terms used in the CollectiVAI project,
especially around the CollectiVAI Chain and its governance model.

---

## 1. General Concepts

**CollectiVAI**  
The overall initiative for democratic, human-centred AI in Europe.
Includes the CollectiVAI App, the CollectiVAI Chain and related tools.

**CollectiVAI App**  
The iOS / iPadOS / macOS client application.  
Acts as a user interface for citizens, experts and institutions to
interact with proposals, votes and (later) the CollectiVAI Chain.

**CollectiVAI Chain**  
A planned Cosmos-based App-Chain that provides the governance
and participation layer for democratic decision-making.

**CVA / ucva**  
The planned native token of the CollectiVAI Chain.  
`CVA` is the display unit, `ucva` is the micro-denom used on-chain  
(1 CVA = 1,000,000 ucva).

**On-chain**  
Data and logic that are recorded and executed on the blockchain
(e.g. proposals, votes, parameters).

**Off-chain**  
Processes or data that happen outside of the blockchain
(e.g. AI analysis, drafts, local simulations in the app).

---

## 2. Network & Infrastructure

**App-Chain**  
A blockchain dedicated to a specific application or use case.
The CollectiVAI Chain is an App-Chain focused on governance and participation.

**Devnet**  
A development network. Used for early testing, fast iteration and
internal experiments. Not intended for production use.

**Testnet**  
A public or semi-public network used to test features and governance
under more realistic conditions, before a mainnet is launched.

**Mainnet**  
The main production network, subject to governance decisions.
May be launched only after devnet and testnet phases.

**Validator Node (Validator)**  
A node that participates in consensus, proposes and signs blocks
and is typically backed by staked tokens.

**Full Node**  
A node that keeps a full copy of the blockchain and verifies all blocks,
but may or may not participate in consensus.

**RPC / API Endpoint**  
Network interface (e.g. HTTPS, gRPC, WebSocket) used by clients
such as the CollectiVAI App to communicate with the chain.

---

## 3. Governance & Roles

**Proposal**  
A structured request for the network / community to make a decision.
Examples: change a parameter, start a pilot, adopt a new governance rule.

**Vote**  
An expression of support, rejection or abstention regarding a proposal.
Votes are recorded on-chain in the governance module.

**Quorum**  
The minimum participation (e.g. share of voting power) required for a
proposal to be considered valid.

**Threshold**  
The minimum level of support (e.g. percentage of “yes” votes) required
for a proposal to pass.

**Parameter**  
A configurable setting that influences the behaviour of the chain,
such as voting periods, quorums, or other system limits.

**Role**  
A classification of a participant (e.g. citizen, expert, institution,
technical maintainer). Roles may affect permissions and voting rules.

**Citizen**  
An individual participant in the CollectiVAI ecosystem who can
take part in consultations, discussions and votes.

**Expert**  
A participant with specific domain expertise who can provide analysis,
commentary or specialised input on proposals.

**Institution / Organisation**  
Entities such as public bodies, NGOs, research institutions or civic
organisations participating in or using the CollectiVAI infrastructure.

---

## 4. Modules & Code Structure

**Cosmos SDK**  
A modular framework for building application-specific blockchains.
The CollectiVAI Chain is planned to use Cosmos SDK modules.

**Module**  
A component in the Cosmos SDK that implements specific functionality
(e.g. `bank`, `staking`, `gov`, `params`, or a custom module).

**`bank` module**  
Handles balances and token transfers.

**`staking` module**  
Manages validators, delegations and staking.

**`gov` module**  
Implements on-chain governance (proposals, votes, tallying).

**`params` module**  
Manages on-chain parameters that can be changed via governance.

**`x/collectivai` module**  
Planned custom module for CollectiVAI-specific governance logic:
roles, participation models and additional civic features.

**`app/`**  
Folder for the main application wiring (Cosmos SDK app, module setup,
encoding, configuration).

**`cmd/collectivaid/`**  
Folder containing the main entrypoint for the CollectiVAI Chain binary.

**`networks/devnet/`**  
Folder for devnet configurations (config files, genesis, scripts).

**`scripts/`**  
Folder for helper scripts to build the binary, start/reset devnets,
and perform administrative tasks.

---

## 5. App & AI Concepts

**AI Provider Router**  
Logic in the CollectiVAI App that can route requests to different AI
providers (e.g. OpenAI, Gemini, local models) depending on context
and configuration.

**AI Governance Layer**  
Planned set of features where AI assists governance itself:
explaining proposals, surfacing risks, summarising discussions,
and documenting how AI analyses were used.

**Lab / Simulation Mode**  
A planned experimental mode where alternative voting methods and
“what-if” scenarios can be explored off-chain, separate from real
governance decisions.

---

This glossary is a living document and will be extended as
the CollectiVAI Chain and App evolve.
