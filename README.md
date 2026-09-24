# Business Site Template

<p>
  <img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" alt="HTML5">
  <img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white" alt="CSS3">
  <img src="https://img.shields.io/badge/No%20Build%20Step-4CAF50?style=for-the-badge" alt="No Build Step">
</p>

<p>
  <a href="https://padou-dev.github.io/business-site-template/">
    <img src="https://img.shields.io/badge/Live%20Preview-2fa89f?style=for-the-badge&logo=googlechrome&logoColor=white" alt="Live Preview">
  </a>
</p>

A generic, static one-page marketing site for a local residential service business
(originally built for an electrician, easy to retarget to any similar trade). No
real business info, no real logo — every identifying detail is a placeholder so
this is safe to keep in a public repo.

## File structure

```
business-site-template/
├── index.html          all page content and markup
└── css/
    └── style.css         all styling (colors, layout, fonts, responsive rules)
```

There are no logo image files — the nav, hero, and footer each show a dashed-border
"Your Logo" placeholder box instead (see `.logo-placeholder` in `css/style.css`).

## Using this template

1. **Drop in a logo.** Replace each `<div class="logo-placeholder ...">` in
   `index.html` with an `<img>` tag pointing at your own logo file. Keep the three
   spots (nav, hero, footer) and size the image to roughly match the placeholder
   it's replacing.
2. **Recolor it.** All the colors are CSS variables at the top of `css/style.css`:
   - `--ink` / `--ink-soft` — the dark background sections (nav, hero, "why us", footer)
   - `--paper` — the light background sections
   - `--accent` / `--accent-deep` — buttons, links, icons, highlighted text
   Change those few values to re-theme the entire site — nothing else needs editing.
3. **Rewrite the copy.** Search `index.html` for:
   - `YOUR BUSINESS NAME` / `Your Business Name` — swap in the real name everywhere
   - `[PHONE NUMBER]`, `[EMAIL ADDRESS]`, `[SERVICE AREA / CITY, STATE]`,
     `[Business Address, City, State]`, `[Hours]`, `[Your License / Certification #]`
   - The city names in the service-area list (`[City One]` … `[City Five]`)
   - The six service cards and four "why us" points — these are written for a
     residential electrician; swap in whatever services/selling points fit your
     trade (plumbing, HVAC, landscaping, etc.) — the layout doesn't need to change.
   - The "Reviews" section — replace the sample cards with real reviews once you
     have them (each is marked "Sample layout — not a real review" so nothing
     fake ships by accident).

## Contact form note

The "Request a Free Estimate" and "Call" / "Email" buttons use `tel:` / `mailto:`
links — no backend required. If you'd rather have a real embedded form, a free
drop-in service like Formspree or Web3Forms works with Cloudflare Pages without
any server code — just point a `<form>`'s `action` at their endpoint.
