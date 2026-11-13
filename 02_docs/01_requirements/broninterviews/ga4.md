## GA4

| Vraag | Antwoord |
|---|---|
| Eigenaar | Online marketing team |
| Systeem | GA4-property 123456789, webstream `www.marktvizier.example` |
| Integratie | Native BigQuery-export, dagelijks (dataset `analytics_123456789`) |
| Volume | ± 60.000 sessies en ± 300.000 events per maand |
| Historie | Vanaf januari 2025 |
| Tijden | `event_timestamp` in microseconden UTC; `event_date` in Nederlandse tijd |
| Bedragen | `purchase`-waarde inclusief btw, exclusief verzendkosten |

**Wat de eigenaar zelf noemt:**

- Niet iedereen geeft toestemming voor cookies, dus **GA4 ziet niet alle bezoeken en aankopen**.
- Google Ads gebruikt **auto-tagging (`gclid`)**; een deel van de campagnes heeft daarnaast **UTM-parameters**.
- **Meta- en e-mailcampagnes worden getagd met UTM-parameters**, "maar niet iedereen doet dat even netjes".
- In maart 2026 is een nieuw thema op de webshop gezet; de tracking is toen opnieuw ingericht.
- Een **dagtabel kan tot ± 3 dagen na de dag nog worden bijgewerkt**.

---
