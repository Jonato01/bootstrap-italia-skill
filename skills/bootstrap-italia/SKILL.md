---
name: bootstrap-italia
description: "Bootstrap Italia v2.x — Italian PA design system based on Bootstrap 5.2.3. Components, patterns, and utilities for Italian Public Administration websites. Use when: building Italian government/PA websites, using Bootstrap Italia components, implementing design system del Paese, working with Titillium Web fonts, Italian PA accessibility. Keywords: bootstrap-italia, PA, pubblica amministrazione, design-italia, agid, designers-italia, bootstrap 5, governo italiano."
version: 1.0.0
---

# Bootstrap Italia Expert

**Production-ready implementations using Bootstrap Italia v2.x — the official Italian PA design system built on Bootstrap 5.2.3.**

Documentation: https://italia.github.io/bootstrap-italia/
GitHub: https://github.com/italia/bootstrap-italia

## Installation

```bash
npm i bootstrap-italia@latest --save
```

### CSS
```html
<link rel="stylesheet" href="<path>/dist/css/bootstrap-italia.min.css" />
```

### JavaScript (module import — recommended)
```javascript
import { Carousel, Alert } from 'bootstrap-italia'
```

### JavaScript (bundle)
```html
<script src="<path>/dist/js/bootstrap-italia.bundle.min.js"></script>
```

### Fonts (Titillium Web, Lora, Roboto Mono)
```javascript
import { loadFonts } from 'bootstrap-italia'
loadFonts('/bootstrap-italia/dist/fonts')
```

## Required HTML Setup

```html
<!doctype html>
<html lang="it">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">
  <link rel="stylesheet" href="dist/css/bootstrap-italia.min.css" />
</head>
<body>
  <!-- content -->
  <script src="dist/js/bootstrap-italia.bundle.min.js"></script>
</body>
</html>
```

## Component Categories

### Navigation (Menu di navigazione)
- **Header** — Testata PA con slim header (ente appartenenza), center header (logo + search), navbar
- **Footer** — Footer istituzionale PA
- **Breadcrumbs** — Percorso di navigazione
- **Megamenu** — Menu espanso multi-colonna
- **Sidebar** — Navigazione laterale
- **BottomNav** — Navigazione mobile bottom
- **Navscroll** — Navigazione scroll-aware
- **Skiplinks** — Accessibilità skip navigation
- **Thumbnav** — Navigazione thumbnails
- **Toolbar** — Barra strumenti
- **Forward/Torna indietro/Torna su** — Navigation helpers

### Components (27)
- **Accordion** — Pannelli espandibili, usa `data-bs-toggle="collapse"`
- **Alert** — Messaggi di avviso con icone, varianti: success, danger, warning, info
- **Avatar** — Immagini profilo circolari con size variants (xs, sm, md, lg, xl)
- **Badge** — Etichette e contatori
- **Buttons** — Pulsanti PA con varianti primary, secondary, outline, dimensioni
- **Card** — Schede contenuto con varianti: simple, article, big, special, teaser
- **Callout** — Box evidenziati per informazioni importanti (success, warning, danger, note)
- **Carousel** — Slider basato su SplideJS
- **Chips** — Tag/filtri interattivi
- **Collapse** — Contenuto espandibile
- **Cookiebar** — Banner gestione cookie GDPR
- **Dimmer** — Overlay oscurante
- **Dropdown** — Menu a tendina
- **Hero** — Banner hero con immagine di sfondo
- **Modale** — Dialoghi modali
- **Notifiche** — Sistema notifiche
- **Overlay** — Pannello overlay
- **Paginazione** — Navigazione pagine
- **Popover** — Tooltip avanzati
- **Progress Indicators** — Barre progresso e spinner
- **Rating** — Valutazione a stelle
- **Sections** — Sezioni contenuto con sfondo
- **Steppers** — Wizard step-by-step
- **Sticky** — Elementi fissi allo scroll (Affix)
- **Tab** — Navigazione a schede
- **Timeline** — Linea temporale eventi
- **Tooltip** — Suggerimenti al passaggio mouse
- **Video Player** — Player video accessibile

### Form (11)
- **Input** — Campi testo con label floating, validazione, helper text
- **Input Numerico** — Stepper numerico
- **Input Calendario** — Date picker
- **Input Ora** — Time picker
- **Autocompletamento** — Ricerca con suggerimenti (Accessible Autocomplete)
- **Upload** — Caricamento file con drag & drop
- **Radio Button** — Selezione singola
- **Select** — Menu selezione
- **Checkbox** — Selezione multipla
- **Toggles** — Switch on/off
- **Transfer** — Lista trasferimento elementi

### Layout & Spacing
- **Griglie** — Bootstrap grid 12 colonne, breakpoints: xs, sm, md, lg, xl, xxl
- **Spaziature** — Margini e padding con scale PA
- **Display, Flex, Float** — Utilities layout standard Bootstrap 5
- **Bordi, Ombreggiature** — Decorazioni
- **Dimensionamento, Proporzioni** — Sizing

### Utilities
- **Colori** — Palette istituzionale PA (primary: #0066CC, complementary, neutral)
- **Colori Custom** — Override palette
- **Icone** — Set icone SVG Bootstrap Italia

## Design Patterns — PA Compliance

### Color Palette (Institutional)
```scss
// Primary
$primary: #0066CC;         // Blu Italia
$secondary: #5C6F82;       // Grigio secondario

// Semantic
$success: #008758;
$warning: #A66300;
$danger: #D9364F;
$info: #979899;

// Neutral
$gray-primary: #5C6F82;
$gray-secondary: #738A9C;
$gray-tertiary: #A9B1B9;
$gray-quaternary: #D4D7DA;
$gray-disabled: #E6E9F2;
```

### Typography
- **Font principale**: Titillium Web (Google Fonts, incluso nel pacchetto)
- **Font serif**: Lora (per testi editoriali)
- **Font monospace**: Roboto Mono
- Scala tipografica PA con classi: `.h1`–`.h6`, `.lead`, `.small`

### Header Structure (Standard PA)
```html
<header class="it-header-wrapper">
  <!-- Slim Header: ente di appartenenza -->
  <div class="it-header-slim-wrapper">...</div>
  <!-- Center Header: logo, nome ente, social, search -->
  <div class="it-header-center-wrapper">...</div>
  <!-- Navbar: navigazione principale -->
  <div class="it-header-navbar-wrapper">...</div>
</header>
```

### Footer Structure (Standard PA)
```html
<footer class="it-footer">
  <div class="it-footer-main">...</div>        <!-- Links principali -->
  <div class="it-footer-small-prints">...</div> <!-- Note legali -->
</footer>
```

## Key Rules

1. **Always use `data-bs-` prefix** for data attributes (Bootstrap 5 convention)
2. **Use `it-` prefix** for Bootstrap Italia specific classes
3. **Italian language** for content, labels, ARIA attributes when building PA sites
4. **Accessibility first** — WCAG 2.1 AA compliance required for PA
5. **GDPR compliance** — Always include Cookiebar component
6. **Responsive** — Mobile-first, test all breakpoints
7. **Fonts** — Always load Titillium Web via `loadFonts()` or CSS `@font-face`
8. **Icons** — Use Bootstrap Italia SVG icon set, not FontAwesome
9. **SASS customization** — Override via `$variables` before importing, never edit source
10. **JS initialization** — Use `data-bs-toggle` attributes or explicit JS: `new ComponentName(element)`

## Class Naming Conventions

- Bootstrap standard: `.btn`, `.card`, `.alert`, `.nav`, etc.
- Bootstrap Italia extensions: `.it-header-wrapper`, `.it-footer`, `.it-hero-wrapper`
- Sizing: `-xs`, `-sm`, `-md`, `-lg`, `-xl`
- Colors: `-primary`, `-secondary`, `-success`, `-warning`, `-danger`
- States: `.active`, `.disabled`, `.show`, `.fade`

## SCSS Customization

```scss
// Override variables BEFORE import
$primary: #0066CC;
$font-path: '/fonts';

// Import Bootstrap Italia
@import 'bootstrap-italia/src/scss/bootstrap-italia';
```

## Common Mistakes to Avoid

1. Don't use Bootstrap standard CDN — use Bootstrap Italia specific bundle
2. Don't forget `loadFonts()` — Titillium Web won't load automatically
3. Don't use `data-toggle` — use `data-bs-toggle` (Bootstrap 5)
4. Don't mix Bootstrap Italia with standard Bootstrap CSS — conflicts
5. Don't skip slim header in PA sites — required by guidelines
6. Don't use custom colors outside PA palette without justification
7. Don't forget `lang="it"` on `<html>` element
