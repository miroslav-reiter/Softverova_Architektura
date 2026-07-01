# 🧱 Príklad: E-shop ako monolit

Tento príklad ukazuje jednoduchý e-shop navrhnutý ako monolitická aplikácia.

## Kontext

Malý tím vytvára e-shop s produktmi, košíkom, objednávkami a platbami. Systém má zatiaľ nízku návštevnosť a vývoj má byť rýchly.

## Komponenty

```text
Web UI
↓
Backend aplikácia
↓
Jedna databáza
```

## Moduly v monolite

- používateľský modul,
- produktový katalóg,
- košík,
- objednávky,
- platby,
- administrácia.

## Výhody

- jednoduchší vývoj na začiatku,
- jednoduché lokálne spustenie,
- jednoduchší deployment,
- menej sieťovej komunikácie,
- jednoduchšie testovanie celého toku.

## Nevýhody

- pri raste vzniká silné prepojenie modulov,
- zmena v jednej časti môže ovplyvniť celý systém,
- škáluje sa celá aplikácia naraz,
- databáza sa môže stať úzkym miestom,
- pri veľkom tíme vznikajú konflikty v jednom kóde.

## Kedy je monolit vhodný

- začiatok projektu,
- malý tím,
- nejasný business model,
- nízka alebo stredná záťaž,
- interný systém,
- MVP produkt.

## Architektonické rozhodnutie

Pre prvú verziu systému je monolit rozumná voľba, pretože znižuje prevádzkovú zložitosť. Mikroservisy by boli v tejto fáze zbytočný overengineering.
