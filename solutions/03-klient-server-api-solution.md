# Riešenie 03 - Klient-server model a API

## Endpointy pre produktový katalóg

| Operácia | Metóda | URL | Popis |
|---|---|---|---|
| Zoznam produktov | GET | `/products` | vráti zoznam produktov |
| Detail produktu | GET | `/products/{id}` | vráti detail produktu |
| Vytvorenie produktu | POST | `/products` | vytvorí nový produkt |
| Aktualizácia produktu | PUT | `/products/{id}` | aktualizuje produkt |
| Odstránenie produktu | DELETE | `/products/{id}` | odstráni produkt |

## Príklad odpovede

```json
{
  "id": 1,
  "name": "Notebook",
  "price": 900
}
```

## Poznámka

API kontrakt musí byť stabilný, zrozumiteľný a dokumentovaný. Frontend tím a backend tím sa podľa neho vedia dohodnúť bez neformálnych výkladov.
