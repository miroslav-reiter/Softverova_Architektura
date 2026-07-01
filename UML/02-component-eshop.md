# UML Component Diagram – E-shop

## Kontext

Component diagram popisuje vnútornú štruktúru systému a rozdelenie na komponenty.
Nezameriava sa na používateľov, ale na **architektúru aplikácie**.

---

## 🧩 Hlavné komponenty e-shop systému

- Frontend (Web / Mobile UI)
- API Gateway
- Product Service
- Order Service
- User Service
- Payment Service
- Notification Service
- Database Layer

---

## 🔗 Väzby medzi komponentmi

- Frontend komunikuje cez API Gateway
- API Gateway smeruje požiadavky na mikroservisy
- Order Service komunikuje s Payment Service
- Order Service zapisuje do databázy
- Notification Service reaguje na udalosti objednávok

---

## 🧱 Textový model architektúry

```text
Frontend
  ↓
API Gateway
  ↓
--------------------------------
| Product Service              |
| Order Service                |
| User Service                 |
| Payment Service              |
| Notification Service         |
--------------------------------
  ↓
Database Layer
```

---

## ⚙️ Zodpovednosti komponentov

| Komponent | Zodpovednosť |
|----------|-------------|
| Product Service | správa produktov |
| Order Service | správa objednávok |
| User Service | správa používateľov |
| Payment Service | spracovanie platieb |
| Notification Service | emaily a SMS |
| API Gateway | routing, autentifikácia |

---

## 🧠 Architektonický význam

Component diagram pomáha pochopiť:
- rozdelenie systému na služby
- zodpovednosti tímov
- komunikáciu medzi modulmi
- možnosť škálovania systému

---

## ⚠️ Typické chyby

- príliš veľké komponenty (god service)
- zdieľaná databáza bez pravidiel
- silná závislosť medzi službami
- chýbajúce API kontrakty
