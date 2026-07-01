# UML Component Diagram – Helpdesk / Ticketing systém

## Kontext

Tento komponentový diagram modeluje helpdesk systém pre správu incidentov, tiketov a používateľskej podpory.

Zameriavame sa na **architektúru servisov a ich zodpovednosti**, nie na UI.

---

## 🧩 Hlavné komponenty systému

- Helpdesk Frontend (UI)
- API Gateway
- Ticket Service
- User Service
- Notification Service
- SLA / Escalation Service
- Knowledge Base Service
- Database Layer

---

## 🔗 Väzby medzi komponentmi

- Frontend komunikuje cez API Gateway
- Ticket Service je centrálna doménová služba
- Ticket Service komunikuje s User Service (identita)
- Ticket Service spúšťa Notification Service
- SLA Service monitoruje časové limity tiketov
- Knowledge Base Service poskytuje články riešení

---

## 🧱 Textový architektonický model

```text
User UI
  ↓
API Gateway
  ↓
----------------------------------
| Ticket Service                 |
| User Service                   |
| SLA / Escalation Service      |
| Knowledge Base Service        |
| Notification Service          |
----------------------------------
  ↓
Database Layer
```

---

## ⚙️ Zodpovednosti komponentov

| Komponent | Zodpovednosť |
|----------|-------------|
| Ticket Service | správa tiketov, stavov a workflow |
| User Service | používatelia a oprávnenia |
| SLA Service | kontrola časových limitov |
| Notification Service | email, SMS, alerty |
| Knowledge Base | články riešení |
| API Gateway | routing, autentifikácia |

---

## 🧠 Architektonický význam

Component diagram pomáha:

- pochopiť tok incidentov
- oddeliť zodpovednosti služieb
- navrhnúť škálovanie podpory
- identifikovať kritické závislosti

---

## ⚠️ Typické problémy

- SLA logika zmiešaná s Ticket Service
- chýbajúca centralizovaná notifikácia
- slabá integrácia Knowledge Base
- monolitický helpdesk bez škálovania

---

## 📌 Použitie v praxi

- ITSM systémy (ServiceNow, Jira Service Management)
- interné support systémy
- customer support platformy
- incident management systémy
