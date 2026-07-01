# Riešenie 05 - C4 model

## Context

E-shop používajú zákazníci a administrátori. Systém komunikuje s platobnou bránou, e-mailovou službou a ERP systémom.

## Container

| Container | Popis |
|---|---|
| Frontend | webová aplikácia pre zákazníkov |
| Backend API | aplikačná logika a API |
| Databáza | produkty, objednávky, zákazníci |
| Admin UI | správa produktov a objednávok |

## Component

Backend API môže obsahovať tieto komponenty:

- ProductController
- ProductService
- ProductRepository
- OrderController
- OrderService
- PaymentClient
- NotificationClient

## Code

V order module môžu byť napríklad tieto triedy:

- Order
- OrderItem
- OrderService
- OrderRepository
- CreateOrderRequest
- OrderStatus

## Záver

C4 model umožňuje vysvetliť systém rôznym publikám. Manažér potrebuje Context, vývojár potrebuje Component a Code úroveň.
