# Riešenie 01 - Čo je softvérová architektúra

Príklad systému: e-shop.

## Hlavné komponenty

- Frontend web aplikácia
- Backend API
- Databáza
- Platobná brána
- E-mailová služba
- Administrácia

## Komunikácia

Frontend komunikuje s backend API cez HTTP. Backend API komunikuje s databázou, platobnou bránou a e-mailovou službou.

## Dáta

Produkty, zákazníci a objednávky sú uložené v databáze. Platobné údaje sa nesmú ukladať priamo bez dodržania bezpečnostných pravidiel.

## Architektonické rozhodnutia

- monolit alebo mikroservisy,
- výber databázy,
- API štýl,
- spôsob autentifikácie,
- nasadenie systému,
- zálohovanie a dostupnosť.

## Implementačné rozhodnutia

- názvy tried,
- konkrétne metódy,
- interný formát premenných,
- detailný kód vo funkciách.
