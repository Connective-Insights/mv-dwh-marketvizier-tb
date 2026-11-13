## Google Ads

| Vraag | Antwoord |
|---|---|
| Eigenaar | Online marketing team |
| Integratie | BigQuery Data Transfer Service, klant-ID 123-456-7890, **refresh window 7 dagen** |
| Tabellen | `ads_Campaign_1234567890` (dagelijkse momentopname van de campagnes), `ads_CampaignBasicStats_1234567890` (dag × campagne × apparaat), `ads_ClickStats_1234567890` (één rij per klik, met `gclid`) |
| Campagnes | Merk, Generiek, Shopping bestsellers, Performance Max, Shopping tuin (seizoen), Black Friday |
| Bedragen | Kosten in micro-eenheden (`metrics_cost_micros` / 1.000.000 = euro) |

**Wat de eigenaar zelf noemt:**

- "Google Ads rapporteert altijd meer conversies dan de webshop. Dat komt door de attributie van Google."
- De Black Friday- en tuincampagnes staan buiten hun seizoen op pauze.
- In februari 2026 is de Performance Max-campagne hernoemd.

