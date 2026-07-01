# UML Deployment Diagram – Cloud nasadenie e-shopu

## Kontext

Deployment diagram popisuje, kde a ako je systém fyzicky nasadený (infra štruktúra).

Nezameriava sa na kód, ale na:
- servery
- cloud služby
- kontajnery
- databázy
- sieťové väzby

---

## ☁️ Architektúra nasadenia (príklad)

E-shop systém beží v cloud prostredí.

### Komponenty infraštruktúry

- Load Balancer
- Web Server (Frontend)
- Application Server (Backend API)
- Container platform (Docker/Kubernetes)
- Database Server
- Cache (Redis)
- External Services (Payment, Email)

---

## 🔗 Textový deployment model

```text
Internet
   ↓
Load Balancer
   ↓
---------------------------
| Web Frontend Cluster    |
---------------------------
   ↓
---------------------------
| Backend API Cluster     |
| (Docker / Kubernetes)   |
---------------------------
   ↓
---------------------------
| Database (PostgreSQL)   |
| Cache (Redis)           |
---------------------------
   ↓
External Services
(Payment Gateway, Email API)
```

---

## ☁️ Cloud mapping (AWS/Azure všeobecne)

| Logická časť | Cloud služba |
|---|---|
| Load Balancer | AWS ALB / Azure Load Balancer |
| Containers | ECS / EKS / AKS |
| Database | RDS / Azure SQL |
| Cache | ElastiCache / Azure Cache |
| Storage | S3 / Blob Storage |

---

## 🧠 Architektonický význam

Deployment diagram vysvetľuje:

- kde systém beží
- ako je škálovaný
- aké sú single points of failure
- ako prebieha komunikácia medzi vrstvami

---

## ⚠️ Typické chyby

- chýbajúci load balancer
- databáza bez redundancy
- všetko beží na jednom serveri
- žiadny failover mechanizmus
- ignorovanie škálovania backendu

---

## 📌 Použitie v praxi

Používa sa pri:

- návrhu cloud architektúry
- DevOps plánovaní
- CI/CD pipeline dizajne
- škálovaní systému
- security review infraštruktúry
