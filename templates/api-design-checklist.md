# API Design Checklist

Použi tento checklist pri návrhu REST API.

## Základ

- Sú endpointy pomenované podľa resource modelu?
- Používajú sa správne HTTP metódy?
- Je API konzistentné?
- Je definovaný formát odpovedí?

## HTTP metódy

| Metóda | Použitie |
|---|---|
| GET | čítanie dát |
| POST | vytvorenie záznamu |
| PUT | úplná aktualizácia |
| PATCH | čiastočná aktualizácia |
| DELETE | odstránenie záznamu |

## Odpovede

- 200 OK pre úspešné čítanie
- 201 Created pre vytvorenie
- 400 Bad Request pre chybný vstup
- 401 Unauthorized pre neprihláseného používateľa
- 403 Forbidden pre nedostatočné oprávnenie
- 404 Not Found pre neexistujúci zdroj
- 500 Internal Server Error pre chybu servera

## Bezpečnosť

- Je použitá autentifikácia?
- Je riešená autorizácia?
- Nie sú v odpovediach citlivé dáta?
- Je riešené rate limiting?

## Dokumentácia

- Existuje OpenAPI špecifikácia?
- Sú uvedené príklady requestov a response?
- Sú popísané chybové stavy?
