# UML Sequence Diagram – Login + 2FA

## Kontext

Sekvenčný diagram popisuje proces prihlásenia používateľa so zapnutým dvojfaktorovým overením (2FA).

Zameriava sa na tok autentifikácie, overenie hesla a následnú verifikáciu druhého faktora.

---

## 👤 Aktér

- Používateľ

---

## 🧩 Účastníci (lifelines)

- Frontend (Web / Mobile)
- Authentication Service
- User Database
- 2FA Service (TOTP / SMS / Email)
- Session Service

---

## 🔐 Sekvenčný flow

```text
Používateľ -> Frontend: zadá username + password
Frontend -> Auth Service: login request
Auth Service -> User DB: overenie kredencií
User DB --> Auth Service: user OK

Auth Service -> 2FA Service: generuj/over 2FA challenge
2FA Service --> Auth Service: challenge odoslaný

Auth Service --> Frontend: vyžiadanie 2FA kódu
Frontend --> Používateľ: zadanie 2FA kódu

Používateľ -> Frontend: zadá 2FA kód
Frontend -> Auth Service: verify 2FA
Auth Service -> 2FA Service: validácia kódu
2FA Service --> Auth Service: OK / FAIL

Auth Service -> Session Service: vytvorenie session
Session Service --> Auth Service: session token

Auth Service --> Frontend: login success + token
Frontend --> Používateľ: prihlásenie úspešné
```

---

## 🧠 Architektonický význam

Tento diagram ukazuje:

- oddelenie autentifikácie a 2FA logiky
- bezpečnostné kroky pri login procese
- závislosť na externých 2FA mechanizmoch
- tvorbu session po úspešnom overení

---

## ⚠️ Typické problémy

- slabá ochrana proti brute-force útokom
- chýbajúce rate limiting
- 2FA viazané priamo na auth service (tight coupling)
- neexistujúce fallback mechanizmy pre 2FA
- chýbajúce session invalidation

---

## 📌 Použitie v praxi

- bankové systémy
- enterprise login systémy
- cloud identity provider (SSO)
- IAM systémy (Keycloak, Auth0, Azure AD)
