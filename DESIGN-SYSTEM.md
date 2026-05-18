# iam.kavya — Design System

This document defines the visual identity, tone, and component rules for the website.
Reference it whenever adding new pages, sections, or features so everything stays consistent.

---

## 1. Brand Identity

**Site name:** `iam.kavya`
**Tagline:** *An inner journey, shared.*
**Essence:** Warm, poetic, introspective. Balances logic and beauty.
**Audience:** People who appreciate depth — music listeners, poetry readers, reflective thinkers.

---

## 2. Color Palette

These are the exact colors used throughout the site. Never substitute them.

### Primary — Peacock Teal
| Name         | Hex       | Use                                      |
|--------------|-----------|------------------------------------------|
| `--teal-deep`  | `#0e4f4f` | Headings, dark backgrounds, logo         |
| `--teal`       | `#1a6b6b` | Buttons, links, labels, accents          |
| `--teal-mid`   | `#267a7a` | Hover states, gradients                  |
| `--teal-light` | `#d4eaea` | Soft backgrounds, tags, subtle borders   |
| `--teal-glow`  | `rgba(26, 107, 107, 0.12)` | Glow effects, shadows   |

### Secondary — Warm Gold
| Name          | Hex       | Use                                      |
|---------------|-----------|------------------------------------------|
| `--gold`        | `#b8923a` | Section numbers, eyebrows, italic labels |
| `--gold-light`  | `#f5ecd9` | Warm background washes                   |

### Neutral
| Name    | Hex       | Use                             |
|---------|-----------|---------------------------------|
| `--bg`    | `#f8f6f2` | Page background                 |
| `--text`  | `#1c1c1c` | Body text                       |
| `--muted` | `#666666` | Secondary / descriptive text    |
| `--light` | `#999999` | Captions, notes, fine print     |
| `--border`| `#e2ddd6` | Dividers and card borders       |
| `--card-bg`| `#ffffff` | Card and section backgrounds   |

### Dark (Footer / About)
| Name           | Hex       | Use               |
|----------------|-----------|-------------------|
| About bg       | `#0e4f4f` | About section     |
| Footer bg      | `#0a3a3a` | Footer            |

---

## 3. Typography

Two fonts. Never use any other font on this site.

### Headings — Cormorant Garamond
- **Source:** Google Fonts
- **Weights used:** 300 (light), 400 (regular), 600 (semibold)
- **Styles:** Regular + Italic
- **Used for:** All `<h1>` through `<h3>`, the logo, blockquotes, the `.feature-sub` label
- **Character:** Elegant, literary, timeless

### Body — Inter
- **Source:** Google Fonts
- **Weights used:** 300 (light), 400 (regular), 500 (medium)
- **Used for:** All body text, navigation, buttons, labels, captions
- **Character:** Clean, modern, readable

### Type Scale
| Element              | Font                | Size                     | Weight | Notes                        |
|----------------------|---------------------|--------------------------|--------|------------------------------|
| Site logo            | Cormorant Garamond  | 1.45rem                  | 600    | Color: `--teal-deep`         |
| Hero h1              | Cormorant Garamond  | clamp(3.2rem, 7.5vw, 6.5rem) | 300 | Color: `--teal-deep`     |
| Section h2           | Cormorant Garamond  | clamp(2.4rem, 4vw, 3.6rem) | 300  | Color: `--teal-deep`         |
| About h2             | Cormorant Garamond  | clamp(2.2rem, 4vw, 3rem) | 300    | Color: white                 |
| Feature subtitle     | Cormorant Garamond  | 1.1rem                   | 400    | Italic, color: `--gold`      |
| Body text            | Inter               | 1rem / 0.96rem           | 400    | Color: #444 or #555          |
| Section label        | Inter               | 0.72rem                  | 500    | Uppercase, 0.25em tracking   |
| Nav links            | Inter               | 0.82rem                  | 400    | Uppercase, 0.07em tracking   |
| Buttons              | Inter               | 0.82rem                  | 500    | Uppercase, 0.12em tracking   |
| Feature number       | Inter               | 0.7rem                   | 500    | Uppercase, color: `--gold`   |

---

## 4. Spacing

The site uses a consistent rhythm. Stick to these values.

| Context                        | Value       |
|--------------------------------|-------------|
| Section top/bottom padding     | 7rem – 8rem |
| Max content width              | 1200px      |
| Max readable text width        | 720px       |
| Horizontal page padding        | 2.5rem      |
| Gap between feature text/visual| 5rem        |
| Card internal padding          | 2.5rem 2rem |
| Nav height                     | 64px        |

---

## 5. Components

### Navigation
- Fixed to top, blurred background (`backdrop-filter: blur(10px)`)
- Logo left, links right
- Links are uppercase, small, color `--muted` → `--teal` on hover
- On mobile (< 600px): hide links, show hamburger icon

### Buttons
Two styles only:

**Filled (`.btn`)**
- Background: `--teal`, text: white
- Padding: `0.8rem 2.2rem`
- Uppercase, 0.12em letter-spacing
- Hover: background → `--teal-deep`, lifts 1px

**Outline (`.btn-outline`)**
- Transparent background, border: 1.5px `--teal`, text: `--teal`
- Hover: fills with `--teal`, text turns white
- Used inside feature cards

### Section Labels (`.section-label`)
- All-caps, 0.25em letter-spacing, 0.72rem
- Color: `--teal` on light backgrounds, faded teal-light on dark backgrounds
- Always appears above a heading or block

### Feature Cards (Music / Poetry / Blog)
- Two-column grid: text left, visual panel right (alternates with `.reverse`)
- Visual panel: tall colored block (340px) with a symbol and tag line
- Each section has its own gradient (all teal-based, slightly different hues)
- On mobile: stacks to single column

### Visual Panels (inside feature cards)
| Section | Gradient                                         |
|---------|--------------------------------------------------|
| Music   | `#0e4f4f` → `#1a7a7a` → `#267a7a`              |
| Poetry  | `#1a5f7a` → `#1a6b6b` → `#2d8a6e`              |
| Blog    | `#2c5364` → `#1a6b6b` → `#4a9a8a`              |

### Decorative Circles (hero only)
- Three blurred radial gradients, low opacity (0.10–0.18)
- Positioned absolute, pointer-events none
- Do not replicate elsewhere

### About Section
- Full-width dark background (`#0e4f4f`)
- White heading, body text at 80% white opacity
- Max width 760px centered

### Footer
- Background `#0a3a3a` (darker than About)
- Logo, nav links, copyright — centered column layout

---

## 6. Imagery & Icons

Currently the site uses typographic symbols as icons (♪ ✦ ◎). When real images are added:
- Photography should feel **warm, intimate, slightly desaturated** — not bright or commercial
- Avoid stock photo aesthetics; prefer candid or artistic shots
- Images should complement the teal/gold palette — warm skin tones, earthy backgrounds work well
- Always use `border-radius: 4px` on images (subtle, not pill-shaped)

---

## 7. Voice & Tone

The writing on this site has a distinct voice. Maintain it on all new pages.

- **Introspective, not performative** — writes *toward* the reader, not at them
- **Honest about vulnerability** — perfectionism, fear of being seen, the courage to share
- **Poetic but clear** — uses metaphor, but never obscures meaning
- **Warm and unhurried** — no urgency, no hype, no calls to "subscribe now"
- **Rooted in Indian classical tradition** — reference Carnatic, Khayal, Dhrupad naturally, not as exotic labels

Headlines should feel like the opening line of a poem, not a marketing slogan.

---

## 8. Page Structure Pattern

Every new page should follow this structure:

```
<header>        ← Fixed nav (same on every page)
<main>
  <section>     ← Hero or page title
  <section>     ← Primary content
  <section>     ← Secondary content (optional)
  <section class="about"> ← Dark closing section (optional, use on landing pages)
</main>
<footer>        ← Same on every page
```

Sections alternate between `--bg` (warm off-white) and `--card-bg` (white) backgrounds to create rhythm without needing borders.

---

## 9. What's Coming Next

Planned sections to build (in rough priority order):
1. **Music page** — YouTube embeds / links to Kavya's Music channel, Sounds of Isha performances
2. **Poetry page** — Individual poem display, categories (relationships / spirituality / human condition)
3. **Blog page** — Essay listing with dates and short excerpts
4. **Individual post template** — For single poems and blog essays

Each new section should feel like a natural extension of the homepage — same fonts, same palette, same unhurried pace.
