# 🧩 Príklad: E-shop ako mikroservisy

Tento príklad ukazuje e-shop rozdelený na samostatné služby.

## Kontext

E-shop rastie, má viac tímov, viac objednávok a samostatné oblasti vývoja. Produktový katalóg, objednávky, platby a notifikácie sa menia nezávisle.

## Komponenty

```text
Frontend
↓
API Gateway
↓
user-service
product-service
order-service
payment-service
notification-service
```

## Služby

| Služba | Zodpovednosť |
|---|---|
| user-service | registrácia, prihlásenie, profil |
| product-service | produkty, kategórie, ceny |
| order-service | objednávky, stav objednávky |
| payment-service | platby, transakcie, platobná brána |
| notification-service | e-mail, SMS, potvrdenia |

## Dôležitý princíp

> Každá služba má jasnú zodpovednosť a ideálne vlastné dátové úložisko.

## Výhody

- nezávislé nasadzovanie služieb,
- škálovanie iba kritických častí,
- rozdelenie práce medzi tímy,
- menšie kódové bázy,
- možnosť rôznych technológií.

## Nevýhody

- vyššia infraštruktúrna komplexita,
- sieťová latencia,
- zložitejší monitoring,
- zložitejšie testovanie end-to-end,
- distribuované transakcie,
- potreba API kontraktov.

## Kedy sú mikroservisy vhodné

- veľký systém,
- viac tímov,
- vysoká záťaž,
- nezávislý vývoj domén,
- potreba škálovať rôzne časti systému rozdielne.

## Kedy nie sú vhodné

- malý tím,
- MVP produkt,
- nejasné domény,
- nízka záťaž,
- slabá DevOps zrelosť.
