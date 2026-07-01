# UML Architecture Review Checklist

## Kontext

Tento checklist slúži na kontrolu kvality UML diagramov a architektonických modelov v softvérovom návrhu.

Používa sa pri:
- review architektúry
- návrhu systému
- kontrolných auditoch
- code review na úrovni dizajnu

---

## 🧩 Use Case kontrola

- Sú jasne definovaní aktéri?
- Sú use cases popísané z pohľadu používateľa?
- Nie sú tam implementačné detaily?
- Je jasne definovaná hranica systému?

---

## 🧱 Component diagram kontrola

- Sú komponenty správne oddelené?
- Má každý komponent jednu zodpovednosť?
- Nie je prítomný "God component"?
- Sú jasné závislosti medzi komponentmi?

---

## 🔄 Sequence diagram kontrola

- Je jasné poradie volaní?
- Sú zachytené externé služby?
- Existujú timeouty alebo error scenáre?
- Nie sú tam zbytočné synchronné väzby?

---

## ☁️ Deployment diagram kontrola

- Je jasné kde systém beží?
- Sú definované servery / cloud služby?
- Je riešená redundancia?
- Existuje škálovanie komponentov?

---

## 🧠 Class diagram kontrola

- Sú entity správne modelované?
- Nie sú tam anemické modely?
- Sú správne kardinality vzťahov?
- Nie sú zmiešané doménové a technické objekty?

---

## 🔁 Activity diagram kontrola

- Je proces logicky konzistentný?
- Sú zachytené všetky rozhodnutia?
- Existujú error vetvy?

---

## 📦 State diagram kontrola

- Sú definované všetky stavy objektu?
- Sú povolené len validné prechody?
- Existujú fallback alebo error stavy?

---

## ⚠️ Architektonické problémy

- tight coupling medzi komponentmi
- chýbajúce API kontrakty
- nejasné zodpovednosti
- prekomplikovaný návrh (overengineering)
- ignorovanie škálovania a failure scenárov

---

## 📌 Výstup review

Po použití checklistu musí byť jasné:

- čo systém robí
- ako je rozdelený
- kde sú riziká
- čo treba refaktorovať
