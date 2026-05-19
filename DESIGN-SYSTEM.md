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
| `--teal-deep`  | `#00515f` | Headings, dark backgrounds, logo         |
| `--teal`       | `#007a8c` | Buttons, links, labels, accents          |
| `--teal-mid`   | `#009db3` | Hover states, gradients                  |
| `--teal-light` | `#b8e5ec` | Soft backgrounds, subtle borders         |
| `--teal-glow`  | `rgba(0, 122, 140, 0.14)` | Glow effects, shadows    |

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

### Type Scale — 4 sizes only
| Name            | Variable          | Value                      | Used for                                        |
|-----------------|-------------------|----------------------------|-------------------------------------------------|
| Display         | `--size-display`  | clamp(3.5rem, 7vw, 6.5rem) | Hero h1 only                                    |
| Heading         | `--size-heading`  | clamp(2.2rem, 4vw, 3.2rem) | All h2s, About heading                          |
| Body            | `--size-body`     | 1.15rem                    | All paragraphs, intro, descriptions             |
| Label           | `--size-label`    | 0.8rem                     | Nav, buttons, section labels, captions, footer  |

**Italic text** (feature subtitles and notes) uses Cormorant Garamond at 1.5rem.
- Subtitles (`.feature-sub`): color `--gold`, italic, weight 600 — e.g. *"A journey of emotion and healing through sound"*
- Notes (`.feature-note`): color `--teal`, italic — e.g. *"Singing in multiple Indian languages..."*
- The selector must be `.feature-text .feature-sub` (not just `.feature-sub`) due to CSS specificity — `.feature-text p` would otherwise override it.

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
- **No em dashes** — use commas, colons, or periods instead

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
