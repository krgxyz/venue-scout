# Venue Scout

Find and rank venues for Paradigm events. Searches Eater, Infatuation, Resy, OpenTable, Reddit, Yelp, Instagram, and local press to surface the best matches — including new and under-the-radar spots — scored against Paradigm's criteria.

## How to invoke

```
@Centaur open venue scout
@Centaur venue scout
@Centaur find me a venue
```

## Behavior

When this skill is invoked, respond with the web app URL so the user can go through the full intake flow:

> 🗺️ **Venue Scout is ready.**
> Open the full intake flow here: **https://venue-scout.centaur.paradigm.xyz**
>
> Or give me a quick brief and I'll return a shortlist right here in Slack:
> `city · event type · guest count · vibe · budget`

If the user provides a brief directly in Slack (no app), use the websearch tool to research venues and return a ranked shortlist using the criteria below.

## Paradigm's venue database

**SF:** Saison, Quince, Benu, Californios, Birdsong, Sons & Daughters, Lazy Bear, Niku, Nisei, Gary Danko, Rich Table, Nightbird, The Progress, Frances, Octavia, Nopa, Rintaro, Cotogna, Flour + Water, Che Fico, Foreign Cinema, Sorrel, Spruce, Liho Liho Yacht Club, Ernest, Wayfare Tavern, Angler, Miller & Lux, Kokkari Estiatorio, Mister Jiu's, Penny Roma, Good Good Culture Club, Roaming Goat, True Laurel, ABV, Pacific Cocktail Haven, Trick Dog, Wildhawk, The Battery SF, Shack15, Fort Mason Gallery 308, Hazie's, Charmaine's Rooftop, Local Edition, Novela

**NYC:** Atomix, Crown Shy, Gramercy Tavern, Via Carota, Don Angie, Carbone, Manhatta, Rezdora, Cote, Jua, Blue Hill, Torrisi, Peasant, Balthazar, Dirty French, Gage & Tollner, LaserWolf, Death & Co, Maison Premiere, Aska, Charlie Bird, Altro Paradiso, Shuka, Union Square Cafe, Dame, Sushi Nakazawa, Tatiana by Kwame Onwuachi, Semma, Bar Calico, Oxomoco, Chinese Tuxedo, Dhamaka, Fish Cheeks, Caffe Dante, Bar Goto, Dante West Village, Buvette, Sant Ambroeus, Public Records, Dead Letter No9, Cervo's, Nudibranch, Gjelina NYC, The Pool, Crane Club, Oiji Mi, Atoboy, Wayla, Swan Room, Broken Shaker

**Las Vegas:** Carbone, Esther's Kitchen, Cut by Wolfgang Puck, Estiatorio Milos, Spago, Gjelina Vegas, Motherwolf, KYU, The Bazaar by Jose Andres, Nobu, Scarpetta, Momofuku

**Resorts/Offsites:** Sun Valley Resort, Big Sky Resort, Snowbird, Jackson Lake Lodge, Fairmont Banff Springs, Fairmont Chateau Lake Louise, Cavallo Point, Carneros Resort, Post Ranch Inn, Ventana Big Sur, Auberge du Soleil, Calistoga Ranch, Bardessono, Solage Calistoga, Wildflower Farms, Gurney's Montauk, Shou Sugi Ban House, AutoCamp, Viceroy Snowmass

## Event type → venue logic

| Event type | Venue tier |
|---|---|
| Dinner / fellow dinner (≤60) | Michelin-tier restaurant, private dining room |
| Happy hour / cocktail party (≤150) | Bar, wine bar, or rooftop — full buyout or semi-private |
| Offsite / retreat (multi-day) | Wine country or mountain resort |
| Flagship / tentpole (150–500+) | Full resort buyout — Sun Valley / Big Sky tier |
| Workshop / team lunch (≤40) | Intimate, quiet, natural light |
| Conference / summit (50–200) | Private event space or club setting |

## Scoring dimensions

Score each venue 1–10 across:
- **Food quality** — Michelin tier, kitchen reputation
- **Private dining** — PDR quality, buyout flexibility
- **Neighborhood** — authentic, walkable, not touristy
- **Design & light** — interior design, natural light, visual cohesion
- **Logistics** — capacity fit, A/V, F&B minimum reasonableness

## Research sources (use websearch for all of these)

Search at least 5 of: Eater, The Infatuation, Resy blog, OpenTable Digest, Beli app, Yelp, Reddit (r/[city]food), Instagram, SF Chronicle, Grub Street, NY Times Food, Time Out. Surface at least 1–2 new or under-the-radar venues per search.

## Output format (Slack shortlist)

Return 5 venues ranked best-to-worst:

```
*1. Venue Name* · Neighborhood, City
Score: 9.2/10  |  Food: 9  Design: 9  Neighborhood: 8  PDR: 8  Logistics: 7
_Why it fits:_ 2–3 sentence verdict specific to the brief.
⚠️ _Watch out:_ one honest concern.
```
