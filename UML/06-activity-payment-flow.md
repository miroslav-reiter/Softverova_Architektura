# UML Activity Diagram – Platobný proces

## Kontext

Activity diagram popisuje workflow procesu platby v e-shope.
Nezameriava sa na komponenty, ale na **tok činností a rozhodnutí**.

---

## 💳 Proces platby

### Hlavné kroky

- Zákazník vytvorí objednávku
- Systém overí objednávku
- Systém spustí platbu
- Platobná brána spracuje transakciu
- Výsledok sa vráti do systému
- Systém potvrdí alebo zamietne objednávku
- Zákazník dostane notifikáciu

---

## 🔄 Activity flow (textový model)

```text
Start
  ↓
Vytvorenie objednávky
  ↓
Validácia objednávky
  ↓
[OK?] ── nie → Zrušiť objednávku
  ↓ áno
Spustenie platby
  ↓
Platobná brána
  ↓
[Úspech?]
   ├── áno → Potvrdenie objednávky
   └── nie → Zlyhanie platby
  ↓
Odoslanie notifikácie
  ↓
End
```

---

## 🧠 Architektonický význam

Tento diagram ukazuje:

- rozhodovacie body v systéme
- business logiku procesu
- závislosť na externých systémoch
- error handling scenáre

---

## ⚠️ Typické problémy

- chýbajúce retry pri platbe
- nejasné stavy objednávky
- nedostatočná validácia vstupu
- nedoriešené rollback scenáre

---

## 📌 Použitie v praxi

Activity diagram sa používa na:

- modelovanie business procesov
- návrh workflow systémov
- optimalizáciu procesov
- komunikáciu s biznis stakeholdermi
