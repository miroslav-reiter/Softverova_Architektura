# Riešenie 02 - Monolit vs mikroservisy

## Rozhodnutie

Pre menší e-shop s 3 vývojármi a 500 objednávkami mesačne je vhodnejší monolit.

## Dôvod

Monolit znižuje komplexitu vývoja a prevádzky. Tím sa nemusí starať o API Gateway, service discovery, distribuovaný monitoring a komunikáciu medzi službami.

## Riziká

- systém môže časom narásť,
- môže vzniknúť silné prepojenie modulov,
- databáza sa môže stať úzkym miestom,
- refaktoring bude náročnejší.

## Kedy uvažovať o rozdelení

- keď pribudne viac tímov,
- keď niektoré moduly potrebujú samostatné škálovanie,
- keď deployment celej aplikácie začína brzdiť vývoj,
- keď domény systému budú jasne oddelené.

## Kandidáti na oddelenie

- platby,
- notifikácie,
- objednávky,
- produktový katalóg.
