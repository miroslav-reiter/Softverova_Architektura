# 🏢 C4 Context: E-shop systém

Cieľom C4 Context diagramu je ukázať systém v jeho okolí.

## Systém

**E-shop systém** umožňuje zákazníkom prezerať produkty, vytvárať objednávky a platiť online.

## Aktéri

| Aktér | Popis |
|---|---|
| Zákazník | prezerá produkty, objednáva, platí |
| Administrátor | spravuje produkty, ceny a objednávky |
| Platobná brána | spracúva online platby |
| E-mailová služba | posiela notifikácie |
| ERP systém | prijíma objednávky na sklad a fakturáciu |

## Textový model

```text
Zákazník → E-shop systém → Platobná brána
Administrátor → E-shop systém
E-shop systém → E-mailová služba
E-shop systém → ERP systém
```

## Otázky na premyslenie

- Ktoré systémy sú externé?
- Ktoré integrácie sú kritické?
- Čo sa stane, keď zlyhá platobná brána?
- Kde vzniká bezpečnostné riziko?
