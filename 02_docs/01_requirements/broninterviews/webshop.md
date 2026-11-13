
## 1. Webshopdatabase

| Vraag | Antwoord |
|---|---|
| Eigenaar | IT / het webbureau dat de shop onderhoudt |
| Bedrijfsproces | Bestellen, betalen, verzenden, retourneren; klantaccounts |
| Systeem en opslag | Cloud SQL for PostgreSQL (`mv-orders-db`), database van de webshopsoftware |
| Integratie | Datastream (CDC) naar BigQuery, merge-modus; producten in append-only-modus (elke versie een rij) |
| Tabellen | `orders`, `orderregels`, `klanten`, `producten` |
| Sleutels | `order_id`, (`order_id`, `regel_nr`), `klant_id`, `product_id` (en `sku` als artikelnummer) |
| Volume | ± 1.800 orders per maand, ± 1,5 regel per order; ± 30.000 klantrijen |
| Historie | Vanaf januari 2025 (oudere orders zijn bij de migratie naar deze shop niet meegenomen) |
| Bedragen | In euro's **inclusief** btw; btw-tarief per regel (21%, kruidenplanten 9%) |
| Tijden | TIMESTAMP in UTC |
| Toegang | Via Datastream; geen directe querytoegang voor het datateam |

**Wat de eigenaar zelf noemt:**

- Bij een gastbestelling maakt de shop elke keer een nieuwe klantrij aan, ook als dezelfde persoon al eerder bestelde.
- Er is een testaccount waarmee het webbureau bestellingen test; die orders hebben `is_testorder = true`.
- Orders veranderen na het plaatsen van status: betaald, verzonden, geannuleerd, geretourneerd.
- In september 2025 is de shopsoftware bijgewerkt; "er is toen wat aan de statussen veranderd".
- Verzendkosten: € 4,95 onder de € 75, daarboven gratis.
