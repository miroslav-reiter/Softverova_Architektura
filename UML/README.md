# UML príklady pre softvérovú architektúru

Tento priečinok obsahuje praktické UML príklady pre kurz **Softvérová Architektúra I. Začiatočník**.

Cieľom nie je kresliť UML len formálne, ale používať ho ako nástroj na pochopenie systému, komunikáciu s tímom a dokumentovanie architektonických rozhodnutí.

## Čo tu nájdete

| Súbor | Diagram | Praktický scenár |
|---|---|---|
| `01-use-case-eshop.md` | Use Case Diagram | používateľské scenáre e-shopu |
| `02-component-eshop.md` | Component Diagram | komponenty e-shop architektúry |
| `03-sequence-order-flow.md` | Sequence Diagram | vytvorenie objednávky |
| `04-deployment-cloud.md` | Deployment Diagram | nasadenie web aplikácie v cloude |
| `05-class-reservation-system.md` | Class Diagram | rezervačný systém |
| `06-activity-payment-flow.md` | Activity Diagram | platobný proces |
| `07-state-order-lifecycle.md` | State Machine Diagram | životný cyklus objednávky |
| `08-component-helpdesk.md` | Component Diagram | helpdesk / ticketing systém |
| `09-sequence-login-2fa.md` | Sequence Diagram | prihlásenie s 2FA |
| `10-architecture-review-uml-checklist.md` | Checklist | kontrola UML diagramov v architektúre |

## Odporúčaný postup tréningu

1. Začni use case diagramom, aby bolo jasné, kto systém používa.
2. Pokračuj component diagramom, aby boli jasné hlavné časti systému.
3. Dopĺňaj sequence diagramy pre najdôležitejšie procesy.
4. Použi deployment diagram na vysvetlenie nasadenia systému.
5. Class diagram používaj až vtedy, keď potrebuješ vysvetliť štruktúru domény.
6. Activity a state diagram použi pri procesoch a stavoch.

## Praktické pravidlo

- Use Case Diagram = čo používatelia robia so systémom
- Component Diagram = z čoho sa systém skladá
- Sequence Diagram = ako komponenty komunikujú v čase
- Deployment Diagram = kde systém beží
- Class Diagram = aké doménové objekty systém obsahuje
- Activity Diagram = ako prebieha proces
- State Machine Diagram = aké stavy môže mať objekt

## Poznámka pre kurz

Tieto príklady sú vhodné na praktické precvičenie v nástrojoch ako Enterprise Architect, Visual Paradigm, StarUML, PlantUML, Mermaid alebo draw.io.
