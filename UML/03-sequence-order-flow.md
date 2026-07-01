# UML Sequence Diagram – Vytvorenie objednávky

## Kontext

Sekvenčný diagram zachytáva časový priebeh interakcie medzi komponentmi systému pri vytváraní objednávky v e-shope.

## 👤 Aktér

- Zákazník

## 🧩 Účastníci (lifelines)

- Frontend (Web/Mobile)
- API Gateway
- Order Service
- Product Service
- Payment Service
- Database
- Notification Service

## 🔄 Sekvenčný flow

```text
Zákazník -> Frontend: klikne "Kúpiť"
Frontend -> API Gateway: POST /orders
API Gateway -> Order Service: createOrder()
Order Service -> Product Service: overenie dostupnosti
Product Service --> Order Service: OK
Order Service -> Database: uloženie objednávky
Order Service -> Payment Service: autorizácia platby
Payment Service --> Order Service: výsledok platby
Order Service -> Notification Service: odoslanie emailu
Order Service --> API Gateway: potvrdenie
API Gateway --> Frontend: 201 Created
Frontend --> Zákazník: potvrdenie objednávky
```

## 🧠 Architektonický význam

Tento diagram ukazuje:
- závislosti medzi službami
- poradie operácií
- synchronné a asynchrónne volania
- kritické miesta systému (payment, DB)

## ⚠️ Typické problémy v praxi

- Payment service ako single point of failure
- chýbajúca idempotencia createOrder
- silná synchronná väzba medzi službami
- nedostatočné timeouty a retry mechanizmy

## 📌 Použitie v architektúre

Sekvenčné diagramy sa používajú na:
- návrh API tokov
- analýzu výkonu systému
- identifikáciu bottleneckov
- komunikáciu medzi tímami
