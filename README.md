<p align="center">
  <img src="collectivai_logo_1_unified.png" alt="CollectiVAI Logo" width="220" />
</p>

<h1 align="center">CollectiVAI Chain</h1>
<h3 align="center">Democratic AI for Europe – Cosmos App-Chain</h3>

<p align="center">
  <a href="#deutsch">🇩🇪 Deutsch</a> &nbsp;|&nbsp; <a href="#english">🇬🇧 English</a>
</p>

---

## 🇩🇪 Deutsch {#deutsch}

### Überblick

**CollectiVAI Chain** ist eine eigene **App-Chain** auf Basis des Cosmos-Ökosystems.  
Ziel ist eine transparente, überprüfbare Governance-Infrastruktur für demokratische Entscheidungen  
mit Fokus auf Europa und digitale Bürgerbeteiligung.

Die Chain dient als neutrale, nachvollziehbare Grundlage für:

- **Abstimmungen und Entscheidungen** (Governance)
- **Rollen & Identitäten** (z. B. Bürger:innen, Expert:innen, Institutionen)
- **Parameter-Management** (z. B. Quoren, Abstimmungsfristen, Gebühren)

Die CollectiVAI iOS/macOS-App (und weitere Clients) fungiert als **Frontend**,  
während die CollectiVAI Chain die **Infrastruktur- und Governance-Logik** bereitstellt.

---

### Ziele

- **Transparente Governance**  
  Alle relevanten Entscheidungen, Abstimmungen und Parameteränderungen sind on-chain nachvollziehbar.

- **Rollenbasierte Beteiligung**  
  Unterschiedliche Rollen (Bürger:innen, Expert:innen, Institutionen) können unterschiedliche Rechte und Verantwortlichkeiten erhalten.

- **Offene Infrastruktur**  
  Die Chain ist als offene Plattform gedacht, auf der mehrere Clients, Tools und Initiativen aufbauen können.

- **Europäischer Fokus**  
  Ausrichtung auf demokratische Prozesse, Bürgerbeteiligung und Projekte mit EU-Kontext.

---

### Kernkonzepte

- **App-Chain auf Cosmos-Basis**  
  Die CollectiVAI Chain wird als eigenständige App-Chain mit dem Cosmos-Ökosystem entwickelt  
  (Cosmos SDK / kompatible Komponenten, Details folgen).

- **On-Chain-Governance**  
  Vorschläge (Proposals), Abstimmungen (Votes) und Parameteränderungen erfolgen transparent und überprüfbar auf der Chain.

- **Trennung von Infrastruktur und Clients**  
  - **Chain:** Validatoren, Governance-Logik, Token-Ökonomie  
  - **Clients:** CollectiVAI App, Web-Oberflächen, weitere Frontends

---

### Projektstatus

> **Status:** Frühe Projektphase (Pre-Alpha)  
> Diese Repository-Version definiert zunächst:
>
> - die Grundstruktur der App-Chain,
> - die Modul-Aufteilung,
> - und die Dokumentationsbasis.
>
> Die konkrete Implementierung (Cosmos SDK, Module, Netzwerk-Konfiguration) folgt Schritt für Schritt.

---

### Repository-Struktur (Entwurf)

```text
collectivai-chain/
├─ cmd/
│  └─ collectivaid/        # Einstiegspunkt für das Chain-Binary
├─ app/                    # App-Definition (Cosmos-App-Wiring)
├─ x/
│  └─ collectivai/         # Eigene Module für Governance / Civic-Logik
├─ docs/                   # Dokumentation (Overview, Architektur, Roadmap)
├─ networks/               # Devnet / Testnet-Konfigurationen (Genesis, Peers)
├─ scripts/                # Hilfsskripte (Build, Run, Wartung)
├─ go.mod                  # Go-Moduldefinition
├─ README.md               # Dieses Dokument
└─ collectivai_logo_1_unified.png  # Projektlogo
