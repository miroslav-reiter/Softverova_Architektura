# Vrstvová architektúra backend aplikácie

Tento príklad ukazuje typickú vrstvenú architektúru backend systému.

## Vrstvy

```text
Presentation Layer
Business Layer
Data Access Layer
Database
```

## Presentation Layer

Táto vrstva prijíma požiadavky a vracia odpovede. Typicky obsahuje REST controllery, web endpointy a základnú validáciu vstupu.

## Business Layer

Táto vrstva obsahuje aplikačnú logiku a pravidlá systému. V e-shope sem patrí výpočet ceny objednávky, kontrola dostupnosti produktu alebo spracovanie objednávky.

## Data Access Layer

Táto vrstva pracuje s databázou. Obsahuje repository triedy, mapovanie dát a databázové operácie.

## Typická chyba

Business logika sa často dostane do controllerov alebo priamo do databázovej vrstvy. To znižuje testovateľnosť a zvyšuje prepojenie vrstiev.

## Odporúčanie

Každá vrstva má mať jasnú zodpovednosť. Controller nemá riešiť business pravidlá a databázová vrstva nemá rozhodovať o používateľských scenároch.
