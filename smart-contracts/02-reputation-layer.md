---

## 2) `smart-contracts/02-reputation-layer.md`

```markdown
# CollectiVAI Reputation & Participation Layer

> 🇬🇧 English first · 🇩🇪 Deutsch weiter unten

---

## 🇬🇧 1. Purpose

The **Reputation & Participation Layer** is a smart-contract component  
that rewards **constructive democratic engagement**, without creating  
a speculative, tradeable token.

Goals:

- recognise long-term participation and contribution,
- support more nuanced governance (beyond 1-person-1-vote),
- remain compatible with public-sector and EU requirements.

Reputation is treated as **Civic Points / Badges**,  
not as a financial asset.

---

## 🇬🇧 2. Core Ideas

- **Non-transferable**: reputation cannot be traded or sold.
- **Transparent**: rules for earning points are defined on-chain.
- **Privacy-aware**: no forced linkage to real identities on-chain.
- **Configurable**: institutions and processes can define what counts.

Reputation is optional: governance processes can choose  
whether and how to use it.

---

## 🇬🇧 3. What counts towards reputation?

Examples (to be refined through governance):

- participation in votes (e.g. „took part in ≥ X votes“),
- constructive comments or expert reviews,
- moderation and conflict-resolution work,
- initiating well-documented proposals.

Possible categories:

- **Participation Score** – frequency and consistency of engagement,
- **Expertise Badges** – topic-based tags (climate, housing, digital rights, …),
- **Trust Badges** – roles such as moderator, community steward, auditor.

---

## 🇬🇧 4. How it interacts with governance

The reputation layer can be used by governance processes, for example:

- setting **eligibility criteria**:
  - „Only accounts with Participation Score ≥ N can moderate this process.“
  - „Expert panel requires at least one Climate Badge holder.“
- **weighting** certain advisory signals (not necessarily final votes):
  - expert reviews receive more weight in background analysis,
  - citizens with long-term participation may have higher influence in some consultations.

Important:

- final decision rules must remain **transparent and understandable**,
- reputation should support, not replace, democratic legitimacy.

---

## 🇬🇧 5. App Integration

In the **CollectiVAI App**, reputation could appear as:

- **Profile view**
  - Civic Score (Participation Score),
  - list of badges (e.g. „Early Participant“, „Climate Expert“, „Moderator“),
  - short explanation of what each badge means.

- **Process view**
  - indication of how many high-reputation participants contributed,
  - ability to filter comments or analyses by badge.

The app will always explain, in human-readable language,  
how reputation is used in a given process.

---

## 🇬🇧 6. Technical Notes (Draft)

Implementation options:

- smart contract (e.g. CosmWasm) that:
  - stores scores and badges per on-chain address,
  - exposes queries for apps and other modules.
- tighter integration with the `x/collectivai` module for:
  - mapping roles (citizen, expert, institution) to reputation logic,
  - ensuring consistent governance behaviour.

Key requirements:

- upgradability via formal governance (no hidden admin keys),
- possibility to reset / anonymise data if legal or ethical concerns arise,
- careful integration with any off-chain identity or KYC/verification system.

---

---

## 🇩🇪 1. Zweck

Die **Reputations- und Beteiligungsschicht** ist eine Smart-Contract-Komponente,  
die **konstruktive demokratische Beteiligung** sichtbar macht –  
ohne einen spekulativen, handelbaren Token zu schaffen.

Ziele:

- langfristiges Engagement und Beiträge anerkennen,
- differenziertere Governance unterstützen (über „eine Person, eine Stimme“ hinaus),
- mit Anforderungen von öffentlicher Hand und EU vereinbar bleiben.

Reputation wird als **Civic Points / Badges** verstanden,  
nicht als Finanzanlage.

---

## 🇩🇪 2. Grundideen

- **Nicht übertragbar**: Reputation kann nicht gehandelt oder verkauft werden.
- **Transparent**: Regeln zum Erwerb von Punkten stehen im Smart Contract.
- **Datenschutzbewusst**: keine erzwungene Verknüpfung mit Klarnamen auf der Chain.
- **Konfigurierbar**: Institutionen und Prozesse können definieren, was zählt.

Reputation ist optional – einzelne Prozesse können entscheiden,  
ob und wie sie sie nutzen.

---

## 🇩🇪 3. Was fließt in die Reputation ein?

Beispiele (später durch Governance zu verfeinern):

- Teilnahme an Abstimmungen (z. B. „mind. X Abstimmungen mitgemacht“),
- konstruktive Kommentare oder Expert:innen-Gutachten,
- Moderations- und Konfliktlösungsarbeit,
- gut dokumentierte, nachvollziehbare Vorschläge.

Mögliche Kategorien:

- **Participation Score** – Häufigkeit und Konstanz der Beteiligung,
- **Expertise-Badges** – Themen-Tags (Klima, Wohnen, digitale Rechte, …),
- **Trust-Badges** – Rollen wie Moderator:in, Community-Steward, Auditor:in.

---

## 🇩🇪 4. Nutzung in der Governance

Die Reputationsschicht kann in Governance-Prozessen genutzt werden, z. B.:

- als **Zugangskriterium**:
  - „Nur Accounts mit Participation Score ≥ N dürfen diesen Prozess moderieren.“
  - „Im Fachgremium muss mind. eine Person mit Klima-Badge sitzen.“
- zur **Gewichtung** bestimmter Signale (nicht unbedingt der endgültigen Stimmen):
  - Expert:innen-Gutachten zählen stärker in Hintergrundanalysen,
  - Bürger:innen mit langjähriger Beteiligung haben in bestimmten Konsultationen mehr Einfluss.

Wichtig:

- Entscheidungsregeln müssen **verständlich und transparent** bleiben,
- Reputation soll demokratische Legitimation **unterstützen**, nicht ersetzen.

---

## 🇩🇪 5. Integration in die App

In der **CollectiVAI App** könnte Reputation z. B. so erscheinen:

- **Profilansicht**
  - Civic Score (Participation Score),
  - Liste von Badges (z. B. „Early Participant“, „Climate Expert“, „Moderator“),
  - kurze Erklärung, was jeder Badge bedeutet.

- **Prozessansicht**
  - Hinweis, wie viele Teilnehmende mit hoher Reputation mitgewirkt haben,
  - Filtermöglichkeit für Kommentare oder Analysen nach Badges.

Die App erklärt stets in verständlicher Sprache,  
wie Reputation im jeweiligen Prozess verwendet wird.

---

## 🇩🇪 6. Technische Hinweise (Entwurf)

Mögliche Umsetzung:

- Smart Contract (z. B. CosmWasm), der:
  - Scores und Badges pro On-Chain-Adresse speichert,
  - Abfragen für Apps und andere Module bereitstellt.
- engere Integration mit dem `x/collectivai`-Modul, um:
  - Rollen (Bürger:in, Expert:in, Institution) mit Reputationslogik zu verbinden,
  - ein konsistentes Governance-Verhalten sicherzustellen.

Wichtige Anforderungen:

- Änderbarkeit nur über formale Governance (keine versteckten Admin-Keys),
- Möglichkeit, Daten bei rechtlichen / ethischen Problemen zurückzusetzen oder zu anonymisieren,
- sorgfältige Abstimmung mit möglichen Off-Chain-Identitäts- oder Verifikationssystemen.
