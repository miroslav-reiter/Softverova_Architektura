# Riešenie 06 - Kvalitatívne vlastnosti architektúry

## Prioritizácia pre e-shop

| Vlastnosť | Priorita | Zdôvodnenie |
|---|---:|---|
| Security | 5 | e-shop pracuje s účtami, objednávkami a platbami |
| Availability | 5 | výpadok znamená stratu objednávok |
| Reliability | 4 | objednávka a platba musia byť spracované správne |
| Performance | 4 | pomalý web znižuje konverzie |
| Scalability | 3 | závisí od veľkosti a sezónnosti e-shopu |
| Maintainability | 4 | systém sa bude často meniť podľa business požiadaviek |

## Kompromisy

- Vyššia bezpečnosť môže zvyšovať komplexitu.
- Vyššia dostupnosť môže zvyšovať náklady na infraštruktúru.
- Mikroservisy môžu zlepšiť škálovanie, ale zhoršiť jednoduchosť vývoja.
- Cache môže zlepšiť výkon, ale komplikuje konzistenciu dát.
