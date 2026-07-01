# UML State Machine Diagram – Životný cyklus objednávky

## Kontext

State machine diagram popisuje **stavy objektu v čase** a prechody medzi nimi.
V tomto prípade modelujeme životný cyklus objednávky v e-shope.

---

## 📦 Hlavný objekt

- Order (Objednávka)

---

## 🔄 Stavy objednávky

- Created (Vytvorená)
- Pending Payment (Čaká na platbu)
- Paid (Zaplatená)
- Processing (Spracováva sa)
- Shipped (Odoslaná)
- Delivered (Doručená)
- Cancelled (Zrušená)
- Refunded (Vrátená platba)

---

## 🔁 Prechody medzi stavmi

```text
[Start]
  ↓
Created
  ↓
Pending Payment
  ↓
[Payment success?]
   ├── áno → Paid
   └── nie → Cancelled
  ↓
Processing
  ↓
Shipped
  ↓
Delivered
  ↓
[End]

Alternatívne vetvy:
- Paid → Cancelled (ak storno pred odoslaním)
- Paid → Refunded (po reklamácii)
```

---

## 🧠 Architektonický význam

State machine diagram pomáha:

- definovať business pravidlá stavov
- eliminovať neplatné stavy
- riadiť lifecycle objektov
- implementovať robustnú logiku v backend systémoch

---

## ⚠️ Typické chyby

- neexistujúci stavový model (ad-hoc logika)
- preskakovanie stavov bez pravidiel
- chýbajúce rollback/refund stavy
- nejednoznačné prechody

---

## 📌 Použitie v praxi

- e-commerce systémy
- ticketing systémy
- banking a payment processing
- workflow engines
- order management systémy
