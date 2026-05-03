# Portfolio — Yuan Zhuang (2026)

Product designer portfolio website. Premium, editorial, product-first aesthetic inspired by Wealthfront's marketing site visual language.

## Project files

```
Portfolio 2026/
├── index.html              # Homepage (hero section built; work/about/footer TBD)
├── design-system-gallery.html  # Design system reference page (Foundations + Shared components)
└── CLAUDE.md
```

## Design direction

- **Aesthetic:** Premium fintech meets editorial design studio. Dark-first hero, clean light content sections below.
- **Tone:** Confident, minimal, product-focused. Typography carries personality.
- **Font pairing:** DM Serif Display (display headlines, weight 400) + Inter (all UI/body)
- **Google Fonts import:**
  ```
  https://fonts.googleapis.com/css2?family=DM+Serif+Display:ital@0;1&family=Inter:wght@300;400;500;600;700&display=swap
  ```

## Design tokens (CSS custom properties)

All pages must declare these in `:root`. Never use raw values — always reference tokens.

```css
/* Backgrounds */
--color-bg-base:       #FAFAF8   /* warm off-white, default page bg */
--color-bg-surface:    #FFFFFF   /* cards and modals only */
--color-bg-subtle:     #F4F2ED   /* alternate section fill */
--color-bg-dark:       #0D0B18   /* hero, footer */
--color-bg-dark-mid:   #1A1730   /* dark section variant */
--color-bg-dark-card:  #241F38   /* cards on dark surfaces */

/* Text */
--color-text-primary:    #0D0B18
--color-text-secondary:  #6B6774
--color-text-tertiary:   #A39EAD
--color-text-inverse:    #FFFFFF
--color-text-inv-dim:    #BDB8CC   /* secondary text on dark bg */

/* Accent — electric violet, used sparingly */
--color-accent:        #7C5CFC
--color-accent-hover:  #6544EA
--color-accent-light:  #EEE9FF   /* tint for tags/chips */
--color-accent-dark:   #A68DFF   /* accent on dark surfaces */

/* Semantic */
--color-success: #1DB87A
--color-warning: #F5A623
--color-error:   #E5484D

/* Borders */
--color-border-subtle:  #EDEAE3
--color-border-default: #D9D5CC
--color-border-dark:    #2E2945
--color-border-accent:  #7C5CFC

/* Shadows */
--shadow-xs:    0 1px 2px rgba(13,11,24,0.05)
--shadow-sm:    0 2px 8px rgba(13,11,24,0.07)
--shadow-md:    0 4px 20px rgba(13,11,24,0.09)
--shadow-lg:    0 8px 40px rgba(13,11,24,0.11)
--shadow-xl:    0 16px 64px rgba(13,11,24,0.14)
--shadow-glow:  0 0 52px rgba(124,92,252,0.28)   /* CTA/hero accent glow */

/* Border radius */
--radius-xs: 2px  --radius-sm: 4px   --radius-md: 8px
--radius-lg: 12px --radius-xl: 16px  --radius-2xl: 24px
--radius-3xl: 32px --radius-pill: 9999px

/* Spacing — 8px base grid */
--space-1: 4px   --space-2: 8px   --space-3: 12px  --space-4: 16px
--space-5: 20px  --space-6: 24px  --space-8: 32px  --space-10: 40px
--space-12: 48px --space-16: 64px --space-20: 80px --space-24: 96px
--space-30: 120px --space-40: 160px
```

## Typography scale

| Token name    | Font               | Size (clamp)        | Weight | Tracking  |
|---------------|--------------------|---------------------|--------|-----------|
| Display 2XL   | DM Serif Display   | clamp(72–120px)     | 400    | -0.03em   |
| Display XL    | DM Serif Display   | clamp(56–88px)      | 400    | -0.03em   |
| Display LG    | DM Serif Display   | clamp(40–64px)      | 400    | -0.025em  |
| Headline      | Inter              | clamp(28–40px)      | 700    | -0.02em   |
| Title LG      | Inter              | 24px                | 600    | -0.01em   |
| Title         | Inter              | 20px                | 600    | -0.01em   |
| Body LG       | Inter              | 18px / lh 1.75      | 400    | —         |
| Body          | Inter              | 16px / lh 1.65      | 400    | —         |
| Body SM       | Inter              | 14px / lh 1.6       | 400    | —         |
| Caption       | Inter              | 13px                | 500    | +0.01em   |
| Label         | Inter              | 11px, UPPERCASE     | 600    | +0.08em   |

## Layout

- Max-width content: **1200px**
- Max-width full-bleed: **1440px**
- Gutter desktop: **24px** / mobile: **16px**
- 12-column grid
- Section vertical padding: `80px–160px`
- Body copy max-width: ~65ch (≈ 6 of 12 columns)

## Section background rhythm

Pages alternate: `bg-base` → `bg-subtle` → `bg-dark`. Never use `bg-surface` as a section background — it's for cards only.

## Component conventions

- Buttons: always `border-radius: var(--radius-pill)`. Primary = accent fill. Secondary = outlined. Never two primary buttons side-by-side.
- Tags/chips: accent variant for categories, neutral for metadata.
- Cards: `border-radius: var(--radius-xl)` (16px) standard, `--radius-3xl` (32px) for image/mockup containers.
- Nav: fixed 64px height. Transparent on dark hero, frosted glass (`backdrop-filter: blur`) on scroll.
- All interactive elements animate with `transition: all 0.2s ease` as default.

## Motion

- Enter: `cubic-bezier(0.0, 0.0, 0.2, 1)` (ease-out)
- Exit: `cubic-bezier(0.4, 0.0, 1, 1)` (ease-in)
- Durations: 150ms hover color, 200ms button/card, 350ms reveals, 500ms hero only
- Always include `@media (prefers-reduced-motion: reduce)` fallback

## Content — Yuan Zhuang

- **Role:** Product Designer
- **Location:** SF Bay Area
- **Headline:** "Designing thoughtful products that simplify complex decisions."
- **Bio:** "I'm Yuan, a product designer with 4+ years building user-centered tools and AI-powered products through research, empathy, and data-driven thinking."
- **Stats:** 4+ years experience · 20+ products shipped · 3 companies
- **Photo:** `/Users/yuanzhuang/Desktop/My photo/BCEEFD59-DE2F-468D-9CCD-A1A4279CF9E8.JPG`
  - Referenced in index.html as: `../../My photo/BCEEFD59-DE2F-468D-9CCD-A1A4279CF9E8.JPG`

## Build status

| Page / Section              | Status      |
|-----------------------------|-------------|
| Design system gallery       | ✅ Complete (Foundations + Shared components) |
| Homepage — Nav              | ✅ Built    |
| Homepage — Hero             | ✅ Built    |
| Homepage — Work/Projects    | ⬜ Not started |
| Homepage — About preview    | ⬜ Not started |
| Homepage — Testimonials     | ⬜ Not started |
| Homepage — Contact CTA      | ⬜ Not started |
| Homepage — Footer           | ⬜ Not started |
| Case study page             | ⬜ Not started |
| About page                  | ⬜ Not started |

## Git / hosting

- **GitHub repo:** https://github.com/zhuangyuan829/Portfolio-YuanZ
- **Branch:** `main`
- To deploy via GitHub Pages: Settings → Pages → Deploy from branch → main
- Live URL (once Pages enabled): `https://zhuangyuan829.github.io/Portfolio-YuanZ/`
