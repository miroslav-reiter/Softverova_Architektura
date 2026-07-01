# Architecture Review Checklist

Použi tento checklist pri hodnotení návrhu architektúry.

## Kontext

- Je jasné, kto systém používa?
- Sú identifikované externé systémy?
- Sú popísané hlavné business procesy?

## Komponenty

- Sú komponenty jasne pomenované?
- Má každý komponent jednu hlavnú zodpovednosť?
- Nie sú komponenty zbytočne silno prepojené?

## Dáta

- Je jasné, kde sú uložené dáta?
- Je určený vlastník dát?
- Sú riešené zálohy a obnova?

## API

- Sú API kontrakty dokumentované?
- Sú endpointy konzistentné?
- Sú chybové odpovede definované?

## Bezpečnosť

- Je riešená autentifikácia?
- Je riešená autorizácia?
- Sú citlivé dáta chránené?
- Je dostupný audit log?

## Prevádzka

- Je riešený monitoring?
- Je riešené logovanie?
- Je jasný deployment model?
- Je známe správanie pri výpadku?

## Kvalitatívne vlastnosti

- Výkon
- Škálovateľnosť
- Dostupnosť
- Spoľahlivosť
- Udržiavateľnosť
