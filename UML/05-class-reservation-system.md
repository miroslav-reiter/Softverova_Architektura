# UML Class Diagram – Rezervačný systém

## Kontext

Class diagram modeluje doménovú štruktúru systému – triedy, ich atribúty a vzťahy.

Používame ho na návrh backend domény ešte pred implementáciou.

---

## 🧩 Hlavné doménové entity

- User (Používateľ)
- Customer (Zákazník)
- Admin (Administrátor)
- Reservation (Rezervácia)
- Room (Miestnosť / zdroj)
- Payment (Platba)
- Notification (Notifikácia)

---

## 🔗 Vzťahy medzi triedami

- User → má roly (Customer / Admin)
- Customer → vytvára Reservation
- Reservation → patrí k Room
- Reservation → má Payment
- Reservation → generuje Notification

---

## 🧱 Textový UML model

```text
User
- id
- name
- email
- password

Customer extends User

Admin extends User

Reservation
- id
- dateFrom
- dateTo
- status

Room
- id
- name
- capacity

Payment
- id
- amount
- status

Notification
- id
- type
- message
```

---

## 🔄 Vzťahy (cardinality)

- Customer 1 → * Reservation
- Reservation 1 → 1 Room
- Reservation 1 → 0..1 Payment
- Reservation 1 → * Notification

---

## 🧠 Architektonický význam

Class diagram pomáha:

- definovať doménový model
- identifikovať entity systému
- navrhnúť databázovú štruktúru
- oddeliť business logiku od UI

---

## ⚠️ Typické chyby

- príliš veľké „God classes"
- miešanie technickej a doménovej logiky
- chýbajúce väzby medzi entitami
- ignorovanie kardinality vzťahov

---

## 📌 Použitie v praxi

- návrh databázy (ERD mapping)
- návrh JPA / ORM modelu
- domain-driven design (DDD)
- backend architektúra služieb
