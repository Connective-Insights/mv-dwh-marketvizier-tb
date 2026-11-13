## E-mailplatform

| Vraag | Antwoord |
|---|---|
| Eigenaar | CRM-marketeer |
| Integratie | Eigen **Cloud Run job** haalt elke nacht de** events** van gisteren op **via de API**; elk event komt als **JSON-payloa**d binnen |
| Events | `Received Email`, `Opened Email`, `Clicked Email`, `Subscribed to List`, `Unsubscribed` |
| Campagnes | Wekelijkse nieuwsbrief (donderdag 10:00) en een welkomstflow bij inschrijving |
| Volume | ± 75.000 events per maand, groeiend met het aantal abonnees |
| Tijden | `timestamp` in lokale tijd met offset (bijvoorbeeld `+01:00`) |

**Wat de eigenaar zelf noemt:**

- Afmeldingen gaan alleen in het e-mailplatform; "volgens mij wordt dat niet teruggezet in de webshop".
- Klikken in een **nieuwsbrief** krijgen **UTM-parameters met de campagnenaam** erin.
- Mensen typen hun e-mailadres zelf in, dus "er zit van alles tussen".
