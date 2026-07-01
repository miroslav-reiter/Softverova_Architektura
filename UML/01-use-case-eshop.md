# UML Use Case Diagram – E-shop

## Kontext

Tento príklad popisuje používateľské scenáre pre e-shop systém.

Use Case diagram zachytáva **čo používatelia robia so systémom**, nie ako je to implementované.

---

## 👤 Aktéri

- Zákazník
- Administrátor
- Platobná brána
- E-mailový systém

---

## 🧩 Use cases

### Zákazník
- Registrovať sa
- Prihlásiť sa
- Prezerať produkty
- Vyhľadávať produkty
- Pridať produkt do košíka
- Vytvoriť objednávku
- Zaplatiť objednávku
- Zobraziť históriu objednávok

### Administrátor
- Spravovať produkty
- Spravovať ceny
- Spravovať objednávky
- Spravovať používateľov

### Externé systémy
- Spracovať platbu (payment gateway)
- Odoslať email (notification service)

---

## 🔗 Vzťahy

- Zákazník vytvára objednávku
- Objednávka vyžaduje platbu
- Platba je spracovaná externou platobnou bránou
- Systém posiela notifikáciu o objednávke

---

## 🧠 Architektonický význam

Use Case diagram definuje:
- hranice systému
- interakcie používateľov
- externé integrácie

Nie je to technický diagram, ale **business pohľad na systém**.

---

## 📌 Príklad použitia v praxi

Tento model sa používa pri:
- návrhu API
- definovaní požiadaviek
- komunikácii s biznisom
- tvorbe backlogu v Agile

---

## 🧪 Poznámka pre tréning

Tento diagram je základ pre všetky ďalšie UML diagramy:
- Component diagram
- Sequence diagram
- Deployment diagram
