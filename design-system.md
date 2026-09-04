# RA Consulting — Brand Guidelines
**v1 · 2026** · Generative AI integration · Diagnostic, pilot, handover

The identity is one mark, one accent and one voice: a gold monogram on midnight, editorial serif over plain sans, and copy that states what happens next. This document is the portable record of the system — everything in it exists as CSS tokens and React components in the design system project.

| | |
| --- | --- |
| **Positioning** | Generative AI integration for companies and founder-led businesses. |
| **Accent** | One gold. Everything else is midnight or warm neutral. |
| **Type** | Instrument Serif · Geist · Space Mono. |
| **Temperament** | Precise, unhurried, low-ornament. No hype. |

---

## 01 · The mark

A falcon rendered as a single continuous gold line, resolving into the letters R and A. It is the only illustrated element in the system — nothing else in RA's visual language is drawn.

### Approved colourways
1. **Gold on midnight** — primary (`assets/logo-mark-gold.png` on the midnight field)
2. **Cream** — single-colour on dark (`assets/logo-mark-cream.png`)
3. **Ink** — paper and print (`assets/logo-mark-ink.png`)
4. **Ink on gold** — accent panels

### Lockups
- **Horizontal** (headers, decks, documents): mark · 1px hairline divider · "RA" in Instrument Serif at 0.06em with a mono uppercase "Consulting" beneath in gold.
- **Stacked** (avatars, covers, stamps): mark above "RA CONSULTING" in Instrument Serif, uppercase, 0.14em tracking.

### Clearspace and minimum size
- Clear margin = **0.5× the mark's height** on every side.
- Sizes: 48px (nav) · 32px (app rail) · **24px floor**. Below 24px the falcon's line closes up and reads as a smudge — use the stacked wordmark instead.

### Rules
**Do**
- Place the mark on the midnight field, on flat cream, or on a photograph dark enough to hold a gold line.
- Use one mark per surface. It is a signature, not a pattern.
- Let the mark carry the gold when the rest of the layout is neutral.

**Don't**
- Recolour the mark outside the four approved colourways, or add a stroke, glow or bevel.
- Rotate, stretch, crop or reconstruct it. The gradient is part of the artwork.
- Set it against a busy image, a light gold panel, or another brand's mark without a dividing rule.

---

## 02 · Colour

Four families. Midnight is the ground, gold is the only bright accent, warm neutrals carry paper surfaces, and the semantic hues are deliberately desaturated so nothing ever competes with gold.

### Midnight — the ground
| Token | Hex |
| --- | --- |
| `--navy-950` | `#030A14` |
| `--navy-900` | `#050F1D` |
| `--navy-800` | `#071426` |
| `--navy-700` | `#0B1E33` |
| `--navy-600` | `#12293F` |
| `--navy-500` | `#1B364E` |
| `--navy-400` | `#2A4A66` |
| `--navy-300` | `#3E6284` |

navy-800 is the default page background; 900 for sunken sections, 700 for raised panels. 300–500 are for hairlines and disabled states, never for large fills.

### Gold — the accent
| Token | Hex |
| --- | --- |
| `--gold-800` | `#5E3F17` |
| `--gold-700` | `#775320` |
| `--gold-600` | `#9C7A2E` |
| `--gold-500` | `#BE9B48` |
| `--gold-400` | `#D8B868` |
| `--gold-300` | `#E8C868` |
| `--gold-200` | `#F3DFA6` |
| `--gold-100` | `#FFF1C0` |

Sampled from the mark's own gradient. gold-500 is the accent on midnight; gold-600 on paper. 300 is the text accent on dark, 700 on light. Gold is never a background for body copy.

### Warm neutrals — the paper side
| Token | Hex |
| --- | --- |
| `--cream-50` | `#FBF9F4` |
| `--cream-100` | `#F4F0E6` |
| `--cream-200` | `#E7E0D1` |
| `--cream-300` | `#D4CBB8` |
| `--stone-400` | `#A79D89` |
| `--stone-500` | `#7D7565` |
| `--stone-600` | `#55503F` |
| `--stone-700` | `#332F26` |

There is no neutral grey in this system. Every light surface, border and secondary text colour is warm — that warmth is what keeps the gold from reading as yellow.

### Semantic
| Hue | Role | Hex |
| --- | --- | --- |
| Jade | success | `#2F8F6B` |
| Steel | info | `#4E7FA8` |
| Ember | warning | `#C7761F` |
| Rust | danger | `#B4442F` |

### Signature gradients
- `--gradient-gold` — the mark, key numerals, accent panels: `linear-gradient(135deg, #9C7A2E 0%, #E8C868 42%, #FFF1C0 62%, #BE9B48 100%)`
- `--gradient-field` — page and hero backgrounds: `radial-gradient(120% 90% at 50% 42%, #0C2136 0%, #071426 55%, #030A14 100%)`
- `--gradient-hairline` — section dividers on midnight, gold fading to transparent at both ends.

These three are the only gradients in the system. No purple, no multi-hue blends.

### Semantic aliases
Components never reference a scale value directly — they reference an alias, and the alias is redefined once under `[data-theme="light"]` to produce the paper theme.

| Alias | Midnight (default) | Paper |
| --- | --- | --- |
| `--bg-base` | navy-800 | cream-50 |
| `--bg-raised` | navy-700 | `#FFFFFF` |
| `--surface-card` | `rgba(255,255,255,.035)` | `#FFFFFF` |
| `--text-primary` | cream-50 | navy-800 |
| `--text-secondary` | cream-50 at 72% | stone-600 |
| `--text-accent` | gold-300 | gold-700 |
| `--accent` | gold-500 | gold-600 |
| `--border-subtle` | cream-50 at 12% | cream-200 |
| `--border-hairline` | gold at 22% | gold-700 at 22% |

---

## 03 · Typography

Three families, each with one job. A serif for what the brand says, a sans for how the product works, a mono for what the system measures.

- **Instrument Serif — display.** Headlines, key numerals, pull quotes. Tight leading (1.04–1.16) and −0.02em tracking. Italic for emphasis, sparingly. Never below 20px and never used for interface labels.
- **Geist — interface and body.** Body sits at 16px in product and 13–14px in dense panels, always with 1.6 leading and a measure of about 64 characters. Weight 300 for standfirsts.
- **Space Mono — labels and data.** Eyebrows, badges, IDs, metrics, table numerals. Mono never sets a sentence.

### Scale
| Token | Size | Leading | Use |
| --- | --- | --- | --- |
| `--text-display-xl` | 56 → 104 | 1.04 | Hero headline, one per page |
| `--text-display-l` | 42 → 72 | 1.04 | Page and section openers |
| `--text-display-m` | 32 → 48 | 1.16 | Sub-sections, dialog titles |
| `--text-display-s` | 28 | 1.16 | Card titles |
| `--text-lead` | 21 | 1.5 | Standfirst under a headline, weight 300 |
| `--text-body` | 16 | 1.6 | Default body |
| `--text-body-s` | 14 | 1.6 | Dense panels, list rows, buttons |
| `--text-caption` | 13 | 1.5 | Hints, table meta, footnotes |
| `--text-micro` | 11 | 1.2 | Mono eyebrows and badges, uppercase, 0.16em |

### The fixed rhythm
Mono eyebrow → serif headline → light sans standfirst → hairline rule → body. Every section opener in every RA surface uses this order.

> **Font substitution:** no vendor font binaries were supplied with the brand artwork. Instrument Serif, Geist and Space Mono are the nearest Google Fonts matches to the mark's monoline geometry. Supply the real licensed families and the system will pick them up from one token file (`tokens/fonts.css`).

---

## 04 · Space, form and depth

The layout system is deliberately tight. Small radii, hairline borders and almost no shadow — closer to a measuring instrument than a consumer app.

### Spacing
4px base with a 2px hairline step for instrument-panel density: **2 · 4 · 8 · 12 · 16 · 20 · 24 · 32 · 40 · 48 · 64 · 80 · 112 · 160**.

Card padding 24, internal stack gap 12, grid gap 24, section rhythm 112. Page gutter 32 (64 on wide marketing pages), container 1240, narrow container 820, prose measure 64ch.

### Corner radii
**2** (xs) · **3** (controls) · **6** (md) · **10** (cards) · **16** (xl) · **pill — tags only**.

### Elevation
- On midnight: flat + hairline, `--shadow-card`, `--shadow-raised`, `--shadow-glow-gold`. Depth reads as a gold-tinted glow, not a drop shadow.
- Cards on midnight carry **no shadow at all** — the hairline does the work. Real shadows (`--shadow-card-paper`) appear only on the paper theme, and only on raised panels and modals.
- Text over imagery gets a protection gradient (`--scrim-bottom` / `--scrim-left`), never a solid capsule.
- Blur (14px, 120% saturation) is reserved for the sticky header and modal scrims.

### Motion and interaction states
| State | Behaviour |
| --- | --- |
| hover | Surfaces lighten one step; interactive cards lift 1px and their border goes gold. Buttons shift fill, never scale. |
| press | Translate down 1px. No scale, no colour flash. |
| focus | 3px gold ring at 55% plus a 1px background-coloured spacer. Never a browser outline. |
| disabled | Opacity 0.42, cursor not-allowed. Colour is unchanged. |
| reveal | Fade plus an 8px rise over 640ms. Once, on entry only. |
| timing | 90 / 160 / 240 / 420 / 640ms on `cubic-bezier(.22,.61,.36,1)`. No bounce, no spring, no looping animation. All durations collapse to 0 under `prefers-reduced-motion`. |

---

## 05 · Iconography

Lucide at 1.5px stroke, injected inline so a glyph is always the same colour as the text beside it (`currentColor`). The falcon is the only illustration; everything else is a line icon.

- **Practice icons** (gold accent): brain-circuit · workflow · database · shield-check · gauge · scan-search
- **Interface icons** (inherit label colour): arrow-up-right · chevron-right · plus · search · download · x
- **Status icons** (semantic hue): circle-check · triangle-alert · octagon-alert · info · clock

**Do**
- Use the sanctioned sizes only: 14 inline with caption text, 18 default, 20 in navigation, 24 in feature blocks.
- Let the icon inherit the colour of the text it sits with. Gold means the icon *is* the accent.

**Don't**
- Use emoji anywhere — not in product, decks, documents or email. The system has no emoji.
- Mix in a second icon library, use filled glyphs, or scale a line icon above 24px.

> **Substitution flagged:** no vendor icon set was supplied. Lucide was chosen because its monoline weight is the closest available match to the falcon's single-stroke construction.

---

## 06 · Voice

RA writes like a practitioner giving a straight answer, not a firm selling a category. Short declaratives, concrete nouns, numbers where they exist, and a willingness to say no.

- **Person.** "We" for the firm, "you" and "your team" for the client. Never "our clients" in second-person copy, never the passive voice to avoid naming who acts.
- **Casing.** Sentence case for everything: headlines, buttons, nav, table headers. Uppercase appears only in mono eyebrows and badges, always with 0.16em tracking. Title Case is never used.
- **Sentence shape.** One idea per sentence. Lead with the outcome, then the mechanism. Headlines run 4–8 words and carry a verb: "Put AI where the work actually happens", not "AI transformation, reimagined".
- **Numbers.** Quantify the commitment, not the ambition. "Two weeks to a diagnostic." "40–120 evaluation cases." "$0.031 per run." Never a percentage without the base it came from.
- **Banned register.** No hype vocabulary — revolutionary, unlock, supercharge, game-changing, seamless, journey, leverage as a verb. No exclamation marks. No rhetorical questions as headlines.
- **Interface copy.** Buttons name the action and its scope: "Book a diagnostic", "Promote", "Re-run evaluation". Hints state a consequence: "Adds two weeks to the diagnostic." Errors say what to do next, never "Oops".

### On brand
> **Put AI where the work actually happens** — We embed generative AI into the workflows your business already runs. A two-week diagnostic, a six-week pilot, and a system your team owns at the end of it.

Verb-led. Names the phases. Ends on ownership, which is the actual promise.

### Off brand
> **Unlock the transformative power of AI** — Our seamless, end-to-end solutions supercharge your digital journey and revolutionise how your organisation innovates.

Nothing is claimed, nothing is measurable, and no one is named as the actor.

### Phrases the brand owns
*Diagnostic, pilot, handover* · *One workflow at a time* · *The handover is the deliverable* · *Built to be handed over, not demoed* · *Where AI actually pays* · *No discovery theatre* · *Field notes*

---

## 07 · Applying the system

Two themes, one token set. Midnight is the default for product and marketing; paper is for anything a client reads at length or prints.

### Layout rules
| Surface | Rule |
| --- | --- |
| Marketing page | 1240px container, 64px gutter, 112px section rhythm. Sections alternate between the midnight field gradient and the sunken navy, separated by a 1px subtle rule. No section carries a shadow. |
| Product shell | 232px left rail on the sunken navy, 64px topbar, 32px content padding. The rail holds the mark, navigation, engagement progress and the user. Active nav is a gold wash with gold text. |
| Header | Sticky, midnight at 82% with a 14px blur, closed by a 1px subtle rule. The only sticky element in the system. |
| Tables | Mono uppercase headers at 11px, 1px row rules, numerals right-aligned in mono. No zebra striping, no vertical rules. |
| Accent budget | **One gold fill per view.** Everything else that needs emphasis uses the gold hairline or gold text. |

### Where the system lives
| Path | Contents |
| --- | --- |
| `styles.css` | The single entry point consumers link. Imports only. |
| `tokens/` | fonts, colors, typography, spacing, radius, elevation, motion, base |
| `components/core/` | Button, IconButton, Icon, Badge, Tag, Card |
| `components/forms/` | Input, Select, Checkbox, Radio, Switch |
| `components/feedback/` | Dialog, Toast, Tooltip |
| `components/navigation/` | Tabs |
| `ui_kits/website/` | Marketing site — home, method, insight, contact |
| `ui_kits/console/` | Client portal — overview, workflows, assistant, governance |
| `assets/` | Falcon mark in gold, cream and ink, plus the original navy lockup |
| `guidelines/` | Specimen cards and the printable brand-guidelines document |
