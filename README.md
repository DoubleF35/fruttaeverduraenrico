# Frutta e Verdura Enrico — Albenga 🍊

Sito per la bottega **Frutta e Verdura Enrico**, Via Fortino 6, Albenga (SV).

Due esperienze, stessi asset:

- **`docs/index.html`** — il sito principale, **tradizionale e gestibile da Enrico**. Stato APERTO/CHIUSO calcolato dagli orari, banco del giorno con prezzi, offerte "entro chiusura" con countdown, orari, mappa. L'animazione della storia è riusata **dentro una sezione** ("Dalla terra al banco"), non più a schermo intero.
- **`docs/storia-immersiva.html`** — la versione precedente, **scroll-telling a schermo intero** in 3 capitoli (la terra → il viaggio → la bottega). Linkata dal sito principale con "⛶ Schermo intero".

## Il pannello di Enrico 🔑

In basso a destra c'è una chiave: apre un pannello (`localStorage`, nessun backend) dove Enrico può aggiornare da solo, senza toccare il codice:

- **Freschi** — i prodotti appena arrivati, con prezzo, unità e badge "novità"
- **Offerte** — i cesti/sottocosto da prendere entro chiusura
- **Bottega** — stato (auto/aperto/chiuso), contatti, **orari per ogni giorno**, testo e foto del banco

Le foto caricate vengono ridimensionate a 1280px e salvate nel browser. I dati di partenza sono quelli del mockup.

## Struttura

- `docs/` — il sito pubblicabile (si chiama `docs` per GitHub Pages)
  - `frames/s1..s3/` — sequenze WebP per lo scrub (50 frame/scena), usate da entrambe le pagine
  - `frames/prod-*.webp` — medaglioni prodotti (usati dalla versione immersiva)
  - `og-image.jpg` — anteprima social
- `keyframes/` — immagini chiave generate (Higgsfield / Nano Banana 2)
- `video/` — clip sorgente 1080p (Kling 3.0 pro, image-to-video first/last frame)
- `ref/` — foto di riferimento del negozio reale

## Sviluppo locale

```bash
cd docs && python3 -m http.server 8420
# → http://localhost:8420
```

## Deploy

GitHub Pages da branch: **Settings → Pages → Deploy from a branch → `main` / `docs`**.

## Stack

HTML/CSS/JS single-file · GSAP ScrollTrigger (scrub) · WebP frame sequences · stato/orari/offerte data-driven in `localStorage` · JSON-LD GroceryStore · fallback `prefers-reduced-motion`
