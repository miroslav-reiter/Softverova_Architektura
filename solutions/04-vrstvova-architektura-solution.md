# Riešenie 04 - Vrstvová architektúra

## Návrh vrstiev

| Vrstva | Zodpovednosť | Príklad komponentu | Čo sem nepatrí |
|---|---|---|---|
| Presentation Layer | prijíma požiadavky a vracia odpovede | ProductController | business pravidlá |
| Business Layer | rieši pravidlá a procesy | OrderService | SQL dopyty a HTML UI |
| Data Access Layer | pracuje s databázou | ProductRepository | rozhodovanie o objednávke |
| Database | ukladá dáta | tabuľky products, orders | aplikačná logika |

## Vysvetlenie

Vrstvová architektúra pomáha oddeliť zodpovednosti. Controller nemá vypočítavať cenu objednávky. Repository nemá rozhodovať, či je objednávka platná. Business pravidlá patria do aplikačnej alebo doménovej vrstvy.
