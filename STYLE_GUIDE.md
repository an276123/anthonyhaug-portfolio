# anthonyhaug.com — Style Guide v1
*Last updated: July 2026. Source of truth for all site edits.*

## Design POV (one sentence)
Monochrome structure, glassmorphic surfaces, and hairline scaffolding — with all the color and emotion carried by soft background orb blooms in pink/indigo/lavender.

---

## Color

### Core palette
| Token | Hex | Use |
|---|---|---|
| Primary | `#000000` | Headlines, primary buttons, key text |
| Ink | `#191c1d` | Body text on light surfaces |
| Muted | `#4c4546` | Secondary text, captions |
| Outline | `#7e7576` | Faint captions, hairline-adjacent text |
| Neutral surface | `#f8f9fa` | Page background base |
| White | `#ffffff` | Card fills, button text on dark |

### Accents (color pops — orbs, labels, diagram strokes)
| Token | Hex | Use |
|---|---|---|
| Pink (bright) | `#fc79bd` | Orbs, glows, diagram accents |
| Pink (deep) | `#a43073` | Text-on-light accent (AA-safe), badges, BPMN gateway |
| Pink (pale) | `#ffd8e7` | Soft orb washes |
| Indigo (bright) | `#7073ff` | Orbs, diagram accents |
| Indigo (text-safe) | `#4f46e5` | Eyebrow labels, purple text on white (AA-safe) |
| Lavender | `#c0c1ff` | Large ambient orbs |

### Contrast rules (non-negotiable)
- Text on white must hit **4.5:1** minimum (WCAG AA). `#a43073` and `#4f46e5` pass; `#fc79bd` and `#7073ff` do NOT — those two are for orbs/decoration/large diagram strokes only, never body-size text.
- Badges: white text on `#a43073`. Never pink-on-pink.

---

## Typography
All type is clean sans or mono. **No serifs, ever.**

| Role | Face | Spec |
|---|---|---|
| Display / H1 | Geist | 48px desktop / 32px mobile, weight 600, letter-spacing -0.04em, line-height 1.1 |
| Card & section titles | Geist | 24px, weight 500, -0.02em (large feature cards may go 30–36px weight 600, tracking-tight — never the full -0.04em display squeeze) |
| Body | Geist | 16px, weight 400, line-height 1.6 |
| Eyebrow / kicker | Geist | 14px, weight 700, UPPERCASE, +0.12em tracking, color `#4f46e5` |
| Labels / captions / numbering | JetBrains Mono | 12px, weight 500, +0.05em, often UPPERCASE |

Acceptable substitutes if Geist ever becomes unavailable: Inter, Söhne, General Sans. Mono substitute: IBM Plex Mono.

---

## Shape & radius
| Element | Radius |
|---|---|
| Buttons / CTAs | Full pill (`999px`) |
| Cards / glass panels | Sharp-ish (2–8px) — the pill buttons pop *because* the cards stay architectural |
| Diagram task nodes | 8px |

## Surfaces & effects
- **Glass cards:** `rgba(255,255,255,0.4)` fill, `blur(24px)` backdrop, 0.5px `rgba(0,0,0,0.1)` border.
- **Hairlines:** 0.5–1px at 8–10% black opacity. Structure is drawn, not boxed.
- **Orbs:** huge radial gradients (600–1200px), blur 100–160px, opacity 15–30%. Always behind content, `pointer-events: none`.
- **Dark section:** one per page max (Skills grid), pure black with accent orbs.

## Motion
- Orb parallax: fine-pointer devices only, disabled under `prefers-reduced-motion`.
- Hovers: subtle — translate-y on buttons, border/bg shifts on cards. No spins, no bounces.
- **Interaction color rule:** indigo `#4f46e5` is the ONLY hover/focus/active accent — buttons, card borders, links, all of it. Pink is never interactive; it stays ambient (orbs) and data (charts, diagram branches). One color per job.

## Voice & content rules
- Case studies: employer-anonymized ("a commercial P&C insurance carrier"), outcome-led, defensible numbers only.
- Buttons say what they do ("Email Anthony," not "Submit").
- Every number on the page must be interview-defensible.

## Component inventory
Sticky glass header · hero (eyebrow + display H1 + pill CTAs with pop-color hovers) · philosophy band (badge + display quote) · glass case-study cards with ghost numerals · inline SVG BPMN diagram · black skills grid · contact block · footer (© + LinkedIn/Email).

## Removed by design (do not resurrect without a reason)
- Stats/KPI strip — redundant once the case-study grid grew to six cards; the cards ARE the stats.
- Right side rail — covered footer content on desktop.
- "Built for Production · Est. 2004" tagline.
- Resume nav button (no destination = no button).
