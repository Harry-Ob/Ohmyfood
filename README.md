# Ohmyfood — Mobile-first restaurant booking site

**[🔗 Live demo](https://harry-ob.github.io/Ohmyfood/)** · HTML5 · Sass · CSS animations · No JavaScript

> from OpenClassrooms 

Ohmyfood is a (fictional) start-up that lets people pick their menu in advance in gourmet restaurants.
I built the home page and the four restaurant menu pages from a Figma mock-up, **mobile-first**,
with every animation done in pure CSS — no JavaScript allowed.

## What I built

- **5 responsive pages**: home + 4 restaurant menus (`delice`, `francaise`, `note`, `palette`), adapted for mobile, tablet and desktop.
- **Loading screen**: a spinning ring that fades out after ~2 s (`@keyframes spin` + `fadeOut`), shown before the home page appears.
- **"Like" heart**: hovering the outline heart fills it with a pink → violet gradient (`background-clip: text` + scale transition).
- **Staggered menu**: starters, mains and desserts slide in one after the other (`fadeSlideIn` with increasing `animation-delay`).
- **Dish hover**: hovering a dish slides in its price and a check mark.

## How the Sass is organised

```
code/Sass/
├── abstracts/   variables, mixins (breakpoints, card, flex helpers), keyframes
├── base/        typography
├── components/  buttons, cards
├── layout/      header, footer
├── pages/       restaurants list, menu pages
└── main.scss    single entry point → compiled to code/css/index.css
```

Reusable mixins (`card()`, `form-item-center()`, `desktop`, `tablet`, `heart-animation`) keep the pages
consistent and avoid repeating the same flexbox/media-query code.

## Run it locally

```bash
npm install
npm run sass:watch   # recompiles code/Sass → code/css/index.css on save
```

Then open `code/index.html` in a browser.

## What I learned

- Thinking **mobile-first** and adding breakpoints upward
- Structuring a Sass codebase so it stays readable as it grows
- Building convincing interactions with CSS only (keyframes, transitions, delays)
- Versioning with Git and deploying on GitHub Pages

<details>
<summary>🇫🇷 Version française</summary>

### Ohmyfood — Site de réservation de menus, mobile-first

**[🔗 Démo en ligne](https://harry-ob.github.io/Ohmyfood/)**

Projet 4 du parcours *Développeur Web* d'OpenClassrooms. Intégration d'une maquette Figma pour une start-up
(fictive) qui permet de réserver son menu à l'avance dans des restaurants gastronomiques.

- 5 pages responsives (accueil + 4 menus), conçues **mobile-first**
- Écran de chargement animé, cœur « j'aime » avec dégradé, apparition en cascade des plats, effet au survol des plats
- **Toutes les animations en CSS pur** — aucun JavaScript
- Sass organisé en `abstracts / base / components / layout / pages`, avec des mixins réutilisables
- Déployé sur GitHub Pages

</details>
