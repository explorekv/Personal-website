# CLAUDE.md — iam.kavya Personal Website

This file is the source of truth for working on this project.
Read it fully before making any changes. Update it whenever something significant changes.

---

## Who This Site Is For

**Owner:** Kavya (GitHub: explorekv, email: explorekv@gmail.com)
**Site name:** `iam.kavya`
**Live URL:** https://explorekv.github.io/Personal-website/
**GitHub repo:** https://github.com/explorekv/Personal-website

Kavya is **not a developer** and does not want to write or learn code.
All code must be written by Claude. Minimize permission prompts where possible.

---

## About Kavya

Kavya is a musician, poet, and writer. She describes herself as deeply introspective,
courageous, curious, and an adventurer into inner spaces. She balances logic and beauty
in all her work and is constantly learning, reflecting, and transforming.

She struggled for a long time with perfectionism and fear of criticism keeping her work
private. This website is her deliberate act of courage, to share what is honest and
of value, especially when it isn't perfect.

### Music
- Trained in **Carnatic classical vocal** from age 5, with a dedicated teacher for 10 years
- Performed with **Sounds of Isha USA** (2016–present), a volunteer musician group
- Has a YouTube channel: **Kavya's Music** — cover songs in multiple Indian languages and genres
- Currently learning **North Indian classical** (Khayal and Dhrupad)
- Goal: take listeners on a journey of feeling a range of emotions, and healing

### Poetry
- Uses metaphor frequently
- Themes: relationships, spirituality, the human condition
- Goal: readers feel and heal along with her

### Blog
- Has been writing for years but not posted publicly
- Topics: being better humans, living a healthy and beautiful life
- Goal: honest writing, no filter

---

## Folder Structure

```
personal-website/
├── index.html          # Homepage — the only page currently built
├── style.css           # All styles for the entire site (single stylesheet for now)
├── DESIGN-SYSTEM.md    # Visual design reference: colors, fonts, components, tone
├── CLAUDE.md           # This file
└── .claude/
    └── launch.json     # Ruby HTTP server config for local preview on port 8080
```

Pages to build in the future (not yet created):
- `music.html` — YouTube links, performance history
- `poetry.html` — poem listing and display
- `blog.html` — essay listing
- `post-template.html` — single poem or essay view

---

## Design Choices

Full details live in `DESIGN-SYSTEM.md`. Summary below.

### Color Palette — Peacock Blue-Green + Warm Gold
Kavya's chosen palette. Do not substitute.

| Role             | Hex       | CSS Variable     |
|------------------|-----------|------------------|
| Primary deep     | `#00515f` | `--teal-deep`    |
| Primary main     | `#007a8c` | `--teal`         |
| Primary mid      | `#009db3` | `--teal-mid`     |
| Primary light    | `#b8e5ec` | `--teal-light`   |
| Gold accent      | `#b8923a` | `--gold`         |
| Gold light       | `#f5ecd9` | `--gold-light`   |
| Page background  | `#f8f6f2` | `--bg`           |
| Body text        | `#1c1c1c` | `--text`         |
| About section bg | `#00515f` | (hardcoded)      |
| Footer bg        | `#003340` | (hardcoded)      |

### Fonts — Two fonts only, never add others
- **Cormorant Garamond** (Google Fonts) — headings, logo, blockquotes, italic feature text. Weights: 300, 400, 600 + italic
- **Inter** (Google Fonts) — body text, nav, buttons, labels. Weights: 300, 400, 500

### Type Scale — 4 sizes only
| Name    | Variable          | Value                      |
|---------|-------------------|----------------------------|
| Display | `--size-display`  | clamp(3.5rem, 7vw, 6.5rem) |
| Heading | `--size-heading`  | clamp(2.2rem, 4vw, 3.2rem) |
| Body    | `--size-body`     | 1.15rem                    |
| Label   | `--size-label`    | 0.8rem                     |

Italic feature text (subtitles and notes) uses Cormorant Garamond at 1.5rem — outside the 4-size scale by exception.

### Layout
- Max content width: **1200px**, centered
- Max readable text width: **720px**
- Horizontal page padding: **2.5rem**
- Section vertical padding: **7rem–8rem**
- Feature sections alternate: text left / visual right, then reversed
- Mobile breakpoints: 860px (stack feature cards), 600px (hide nav links)

### Overall Vibe
Warm, poetic, unhurried. Literary. Rooted in Indian classical tradition.
No bright colours, no stock-photo energy, no marketing language.

---

## Current Homepage Sections (index.html)

1. **Nav** — Fixed, blurred background. Logo `iam.kavya` left, links right (Music, Poetry, Blog, About)
2. **Hero** — Full-viewport. Headline: *"An inner journey, shared."* Button: "Explore my work". Quote: *"I balance logic and beauty in all my work, constantly learning, reflecting, and transforming."*
3. **Intro** — White background. Short bio paragraph. Links to About section.
4. **Explore** — Three feature cards, equal weight. No numbers, no tag pills.
   - **Music** — South Indian Carnatic roots, YouTube (Kavya's Music), Sounds of Isha USA, Khayal & Dhrupad
   - **Poetry** — Metaphor, relationships, spirituality, healing
   - **Blog** — Essays on becoming, healthy and beautiful life
5. **About** — Dark teal background. Full personal story in Kavya's own words.
6. **Footer** — Darkest teal. Logo, nav links, copyright.

---

## Voice & Tone Rules

- Write *toward* the reader, not at them
- Honest about vulnerability — this is always appropriate for this site
- Poetic but never obscure
- No urgency, no hype, no "subscribe now" language
- Reference Indian classical tradition (Carnatic, Khayal, Dhrupad) naturally
- Headlines should read like the opening line of a poem

---

## Workflow Notes

- **No em dashes** — use commas, colons, or periods instead. Kavya's preference.
- **No build tools** — pure HTML and CSS. No npm, no frameworks, no bundlers.
- **Deployment:** GitHub Pages from the `main` branch, root directory
- **To deploy changes:** commit and push to `main` — GitHub Pages auto-publishes
- **Local preview:** Ruby HTTP server on port 8080 (see `.claude/launch.json`)
- **After any accepted visual change:** update `DESIGN-SYSTEM.md` to reflect it
- **Git config:** use `-c user.email="kavya@iam.kavya" -c user.name="Kavya"` when committing
