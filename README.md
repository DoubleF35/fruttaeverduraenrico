# Frutta e Verdura Enrico — Albenga 🍊

Sito one-page scroll-telling per la bottega **Frutta e Verdura Enrico** di Via Fortino 6, Albenga (SV).

La storia in tre capitoli, controllata dallo scroll (frame-scrub su canvas, stile Apple):

1. **La terra** — l'orto della piana di Albenga cresce in timelapse
2. **Il viaggio** — l'Ape carica scende tra gli ulivi verso il paese
3. **La bottega** — il banco si riempie davanti al negozio

## Struttura

- `docs/` — il sito pubblicabile (single-file `index.html` + asset; si chiama `docs` per GitHub Pages)
  - `frames/s1..s3/` — sequenze WebP per lo scrub (50 frame/scena, 10fps)
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

HTML/CSS/JS single-file · GSAP ScrollTrigger · WebP frame sequences · JSON-LD LocalBusiness
