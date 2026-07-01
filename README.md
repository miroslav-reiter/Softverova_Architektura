# 🧩 Softvérová Architektúra

Tréingový repozitár k online kurzu **Softvérová Architektúra I. Začiatočník**.

Repozitár slúži na praktické precvičovanie základných architektonických pojmov, modelov, diagramov, rozhodnutí a návrhov systémov. Je určený pre začiatočníkov, junior analytikov, vývojárov, testerov, DevOps, IT konzultantov a všetkých, ktorí sa chcú naučiť rozmýšľať nad softvérom ako nad systémom, nie iba ako nad kódom.

## 📌 Čo je softvérová architektúra

Softvérová architektúra je disciplína zameraná na návrh štruktúry softvérového systému na úrovni komponentov, vzťahov a pravidiel interakcie.

Architektúra nerieši primárne detail implementácie, ale zásadné rozhodnutia o systéme ako celku:

- ako budú komponenty komunikovať,
- kde budú uložené dáta,
- ako sa bude systém škálovať,
- ako bude systém nasadený,
- čo sa stane pri výpadku,
- aké kompromisy robíme medzi výkonom, bezpečnosťou, dostupnosťou a udržiavateľnosťou.

> Architektúra je mapa systému, nie jeho kód.

## 📚 Definícia podľa ISO/IEC/IEEE 42010

Norma ISO/IEC/IEEE 42010 definuje architektúru ako základné koncepty alebo vlastnosti entity v jej prostredí a riadiace princípy pre jej realizáciu a vývoj.

V kurze to preložíme do jednoduchšieho jazyka:

> Architektúra určuje, z čoho sa systém skladá, ako časti spolu súvisia a podľa akých princípov sa bude systém ďalej vyvíjať.

## 🎯 Na čo sa softvérová architektúra používa

| Otázka | Praktický význam |
|---|---|
| Ako systém rozdeliť? | Komponenty, moduly, služby |
| Ako budú časti komunikovať? | API, messaging, eventy, databázy |
| Kde budú dáta? | SQL, NoSQL, cache, storage |
| Ako systém nasadíme? | server, cloud, kontajnery, Kubernetes |
| Ako bude systém škálovať? | horizontálne / vertikálne škálovanie |
| Ako zabezpečíme systém? | autentifikácia, autorizácia, audit, šifrovanie |
| Ako znížime technický dlh? | rozdelenie zodpovedností, dokumentácia, testovanie |

## 🧠 Mentálny model systému

| Vrstva | Význam | Príklad v e-shope |
|---|---|---|
| Používateľská vrstva | čo vidí používateľ | web, mobilná appka, formulár objednávky |
| Aplikačná vrstva | logika a pravidlá | výpočet ceny, objednávka, platba |
| Dátová vrstva | trvalé dáta | produkty, zákazníci, objednávky |

```text
Používateľ klikne Kúpiť
→ frontend pošle request
→ backend spracuje objednávku
→ databáza uloží order
→ systém pošle potvrdenie
```

## 🧱 Základné komponenty softvérovej architektúry

| Komponent | Úloha | Príklady technológií |
|---|---|---|
| Frontend | používateľské rozhranie | React, Angular, Vue, JavaFX, Swing, WPF, WinForms, Qt, wxPython |
| Backend | business logika | Java Spring Boot, .NET, Node.js, Python FastAPI, PHP Laravel |
| Databáza | ukladanie dát | PostgreSQL, MySQL, SQL Server, MongoDB, Redis |
| API | kontrakt medzi systémami | REST, GraphQL, gRPC |
| Integrácie | externé systémy | platobná brána, e-mail, SMS, ERP, CRM |
| Infra | nasadenie a prevádzka | Docker, Kubernetes, Linux, cloud, CI/CD |

## 🧩 Monolit vs mikroservisy

| Kritérium | Monolit | Mikroservisy |
|---|---|---|
| Štruktúra | jedna aplikácia | viac samostatných služieb |
| Deployment | jeden deployment | samostatný deployment služieb |
| Databáza | často jedna spoločná DB | často database per service |
| Vývoj na začiatku | jednoduchší | zložitejší |
| Škálovanie | škáluje sa celý systém | škálujú sa konkrétne služby |
| Prevádzka | jednoduchšia | náročnejšia |
| Riziko | spaghetti code | distribuovaná komplexita |

> Monolit nie je automaticky zlý návrh. Mikroservisy nie sú automaticky lepšia architektúra.

## 🌐 Klient-server model

```text
Klient → požiadavka → server → spracovanie → odpoveď → klient
```

Príklad:

```http
GET /api/products
```

Server vráti:

```json
[
  { "id": 1, "name": "Notebook", "price": 900 },
  { "id": 2, "name": "Monitor", "price": 180 }
]
```

## 🔌 API komunikácia

| HTTP metóda | Význam | Príklad |
|---|---|---|
| GET | čítanie dát | `GET /products` |
| POST | vytvorenie záznamu | `POST /orders` |
| PUT | aktualizácia záznamu | `PUT /products/1` |
| DELETE | odstránenie záznamu | `DELETE /products/1` |

## 🏛️ Vrstvová architektúra

```text
Presentation Layer
↓
Business Layer
↓
Data Access Layer
↓
Database
```

Výhoda:

- každá vrstva má jasnú zodpovednosť,
- ľahšie sa testuje,
- systém je zrozumiteľnejší.

Problém:

- pri veľkých systémoch môže byť štruktúra rigidná,
- zmeny sa môžu šíriť cez celý stack.

## 🧭 UML modelovanie

| Diagram | Na čo slúži |
|---|---|
| Class Diagram | triedy a vzťahy |
| Component Diagram | komponenty systému |
| Sequence Diagram | tok správ v čase |
| Deployment Diagram | nasadenie systému |

## 🏢 C4 model

| Úroveň | Otázka | Príklad |
|---|---|---|
| Context | kto používa systém a s čím komunikuje? | zákazník, e-shop, platobná brána |
| Container | z akých aplikácií sa systém skladá? | frontend, API, DB |
| Component | čo je vo vnútri aplikácie? | controller, service, repository |
| Code | ako je to implementované? | triedy, funkcie, metódy |

## ⚖️ Kvalitatívne vlastnosti architektúry

| Vlastnosť | Význam |
|---|---|
| Performance | výkon a rýchlosť odozvy |
| Scalability | schopnosť rásť pri vyššej záťaži |
| Availability | dostupnosť služby |
| Security | ochrana systému a dát |
| Reliability | spoľahlivosť správania |
| Maintainability | udržiavateľnosť systému a kódu |

## ⚠️ Najčastejšie chyby začiatočníkov

| Chyba | Prečo je problém |
|---|---|
| Overengineering | zbytočne zložitý návrh |
| Mikroservisy bez dôvodu | vysoká prevádzková komplexita |
| Tight coupling | zmena jedného modulu rozbíja ostatné |
| Chýbajúce API kontrakty | tímy nevedia, čo presne majú implementovať |
| Miešanie vrstiev | business logika v UI alebo databáze |
| Ignorovanie škálovania | systém funguje iba pre malú záťaž |
| Slabá dokumentácia | tím nerozumie rozhodnutiam |

## 🗂️ Štruktúra repozitára

```text
Softverova_Architektura/
├── README.md
├── examples/
├── exercises/
├── solutions/
├── diagrams/
├── templates/
└── docs/
```

## 🚀 Rýchly štart

1. Prejdi si `examples/eshop-monolith.md`.
2. Porovnaj ho s `examples/eshop-microservices.md`.
3. Vypracuj cvičenia v priečinku `exercises/`.
4. Skontroluj riešenia v `solutions/`.
5. Vytvor vlastný ADR z `templates/adr-template.md`.
6. Skús nakresliť vlastný C4 model podľa Mermaid diagramov v `diagrams/`.

## 🎬 Praktické príklady vo videu

1. Návrh architektúry jednoduchého e-shopu.
2. Porovnanie monolitu a mikroservisov.
3. Návrh REST API kontraktu pre produkty a objednávky.
4. C4 Context diagram pre e-shop.
5. C4 Container diagram pre frontend, API a databázu.
6. Sekvenčný diagram vytvorenia objednávky.
7. Vrstvová architektúra backend aplikácie.
8. Vyplnenie ADR: rozhodnutie monolit vs mikroservisy.
9. Vyhodnotenie kvalitatívnych vlastností.
10. Kontrola najčastejších architektonických chýb.

## 📚 Užitočné zdroje

- ISO/IEC/IEEE 42010 - Architecture description
- C4 model - https://c4model.com/
- Martin Fowler - Software Architecture Guide
- Microsoft Azure Architecture Center
- AWS Architecture Center
- arc42 Architecture Template
- REST API Guidelines

## ✅ Cieľ kurzu

Po prejdení repozitára by mal študent vedieť:

- vysvetliť, čo je softvérová architektúra,
- rozlíšiť monolit a mikroservisy,
- vysvetliť klient-server model,
- navrhnúť jednoduché API,
- použiť základný C4 model,
- rozumieť vrstvenej architektúre,
- pomenovať kvalitatívne vlastnosti systému,
- vyplniť jednoduchý ADR dokument,
- identifikovať základné architektonické chyby.
