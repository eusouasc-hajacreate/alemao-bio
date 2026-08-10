---
name: Alemão Diesel — Link na Bio
description: Gunmetal-lab link-in-bio for a diesel fuel-injection training brand.
colors:
  ink: "#0b0c0e"
  grafite: "#121417"
  grafite-2: "#1a1d21"
  border-subtle: "#24262a"
  prata: "#a8bac2"
  cinza-aco: "#5a6167"
  quase-branco-cta: "#e2e6e8"
  branco-titulo: "#f2f3f4"
  cinza-medio: "#7a8287"
  cinza-legenda: "#707576"
typography:
  display:
    fontFamily: "Anton, sans-serif"
    fontSize: "26px (31px from 480px up)"
    fontWeight: 400
    lineHeight: 1.1
    letterSpacing: "0.2px (0.3px from 480px up)"
  body:
    fontFamily: "Inter, sans-serif"
    fontSize: "11.5px–12px"
    fontWeight: 400
    lineHeight: normal
    letterSpacing: "0.2px"
  label:
    fontFamily: "Inter, sans-serif"
    fontSize: "10.5px–11.5px"
    fontWeight: 600
    lineHeight: normal
    letterSpacing: "2.5px–3px"
rounded:
  card: "14px"
  circle: "50%"
  page-desktop: "22px"
spacing:
  page-padding-mobile: "32px 16px 28px"
  page-padding-desktop: "44px 16px 36px"
  card-gap: "14px (16px from 480px up)"
  hero-margin: "24px (30px from 480px up)"
components:
  card:
    backgroundColor: "{colors.grafite}"
    rounded: "{rounded.card}"
  card-hover:
    backgroundColor: "{colors.grafite}"
  cta-badge:
    backgroundColor: "{colors.quase-branco-cta}"
    rounded: "{rounded.circle}"
  social-btn:
    backgroundColor: "{colors.grafite-2}"
    rounded: "{rounded.circle}"
---

# Design System: Alemão Diesel — Link na Bio

## Overview

**Creative North Star: "The Curitiba Lab at Night"**

The system reads like the real Common Rail service lab it points back to: a dim, cool-lit
workshop where the only bright things are brushed-metal tool faces and a single white
work-lamp. Nothing here is decorative gold or trophy-shop chrome — the metallic accent
is functional, the way a torque wrench or a socket set is functional. Backgrounds sit in
a blue-black gunmetal, never a true black; panels are near-invisible slabs distinguished
by a hairline edge, not a frame. Typography carries the weight instead of ornament: one
extra-heavy condensed display face stands in for the embossed lettering on real workshop
signage.

This identity replaces an earlier gold-and-rivets "instrument plate" identity (Archivo
Black display, gold `#fcd414` accents, riveted card corners, bronze-to-gold hairline).
That version is retired; do not blend gold back in anywhere, including hover/focus
states, icon fills, or shadows.

**Key Characteristics:**
- Blue-black gunmetal ground, never pure black, never warm.
- Prata (`#a8bac2`) is the *only* accent — icons, hairline, focus rings, hover borders. Nothing else is tinted.
- Cards are thin-edged slabs, not bordered boxes: the border is nearly invisible at rest.
- One extra-condensed, extra-heavy display face, always set in caps.
- The single saturated color anywhere on the page is WhatsApp's own brand green, and it appears only inside the WhatsApp card's own photography/UI, never as a page-chrome token.

## Colors

A near-monochrome gunmetal system with exactly one accent hue (cool silver-gray) and no saturated brand color of its own.

### Primary
- **Prata / Metálico** (`#a8bac2`): the system's only accent. Used for the logo-adjacent hairline divider, all social icon fills, card hover/focus borders, and the focus-visible ring. Never fills a large area — it is always a line, an icon, or a thin edge.

### Neutral
- **Preto Base** (`#0b0c0e`): page background. A cool, slightly blue black — never `#000` or a warm black.
- **Grafite** (`#121417`): card and panel fill, sitting one step up from the page background.
- **Grafite 2** (`#1a1d21`): the social-icon circle fill, one step up again from card grafite, for a subtle third layer.
- **Borda Sutil** (`#24262a`): the resting border color on cards and social buttons. Deliberately close in value to grafite — the edge should read as a seam, not a frame.
- **Cinza-Aço** (`#5a6167`): the outer stops of the hairline gradient and its end-dots; a structural, not decorative, gray.
- **Quase-Branco CTA** (`#e2e6e8`): fill for every circular arrow CTA. Reads as brushed metal / a lit surface against the dark ground, paired with an ink-colored stroke icon.
- **Branco Título** (`#f2f3f4`): the one high-emphasis text color, reserved for the wordmark.
- **Cinza Médio** (`#7a8287`): secondary headline text (the tagline directly under the wordmark).
- **Cinza Legenda** (`#707576`): captions, footer text, least-emphasis copy.

### Named Rules
**The One-Accent Rule.** Prata is the only hue-bearing color token in the chrome. If a new element needs emphasis, give it prata or give it more size/weight — never a second accent color.

**The No-Gold Rule.** `#fcd414` (and its bronze/tan/beige family) is retired system-wide, including inline SVG `stroke`/`fill` attributes baked into markup, not only CSS. Grep for those hex values before shipping any change to this page.

## Typography

**Display Font:** Anton (fallback: sans-serif)
**Body Font:** Inter (fallback: sans-serif) — unchanged from the prior identity; kept because it matches the body copy observed on the brand's confirmed reference site.

**Character:** Anton is extra-condensed and extra-heavy by construction — it supplies its own visual weight, so it is never additionally bolded and always set in caps (source copy is typed upper-case rather than relying on `text-transform`, so a mixed-case string dropped into a `.hero__name`-class element will render mixed-case; type it in caps). Inter stays purely a workhorse body/label face — it never appears at display scale.

### Hierarchy
- **Display** (400, 26px→31px, line-height 1.1): the wordmark only (`.hero__name`). One instance per page.
- **Label** (600, 10.5–11.5px, letter-spacing 2.5–3px, uppercase): eyebrow-style text — tagline under the wordmark, footer brand line. Always `{colors.cinza-medio}` or `{colors.cinza-legenda}`, never full white.
- **Body** (400, 11.5–12px): the subhead line ("Cursos 100% online · acesso imediato") and footer copyright. `{colors.cinza-legenda}`.

### Named Rules
**The Single Display Instance Rule.** Anton appears exactly once per viewport — the wordmark. Course names and headlines that appear to use it are baked into the card photography, not live type; do not add a second live Anton element without a reason strong enough to justify a second focal point.

## Layout

Single-column, mobile-first, capped at `--page-max: 460px` at every breakpoint — this page never widens into a multi-column desktop layout; desktop only adds a framing card (border + radius) around the same 460px column and centers it in the viewport. Spacing scales in one step at 480px (more breathing room, larger type) and again at 640px (the outer frame appears). Vertical rhythm is a single stacked flow: hero → card list → social row → footer, each block separated by a fixed margin rather than a grid.

## Elevation & Depth

Hybrid: cards carry a real soft shadow (ambient, not structural) for lift off the page background; everything else is flat, distinguished by the grafite/border-subtle tonal steps rather than shadow.

### Shadow Vocabulary
- **Card rest** (`box-shadow: 0 10px 24px rgba(0,0,0,0.45), inset 0 0 0 1px rgba(255,255,255,0.02)`): default lift under every card.
- **Card hover** (`0 12px 28px rgba(0,0,0,0.5), 0 0 0 1px rgba(168,186,194,0.3)`): adds a prata-tinted outer ring on top of the rest shadow; the border color itself also shifts to prata.
- **CTA badge** (`0 4px 10px rgba(0,0,0,0.35)`): a plain dark ambient shadow — no colored glow, unlike the retired gold version.

## Shapes

Rounded rectangles throughout: 14px on cards, 22px on the desktop outer frame, full circles (50%) on every button (CTA badge, social icons). No sharp corners, no cut corners, no rivets or corner ornaments — the retired identity's riveted-corner motif is gone; the card edge is now a single hairline border and nothing else.

## Components

### Buttons (circular CTA)
- **Shape:** full circle, 34px (36px from 480px up).
- **Fill:** `{colors.quase-branco-cta}`, flat, no gradient.
- **Icon:** a chevron arrow, stroke color `{colors.ink}` (`#0b0c0e`), 2.6px stroke width, round caps/joins.
- **Shadow:** plain dark ambient shadow (see Elevation).
- One per card, bottom-right, 12px inset (14px from 480px up).

### Social Icon Buttons
- **Shape:** full circle, 44px, border `{colors.border-subtle}`, fill `{colors.grafite-2}`.
- **Icon:** single-color SVG fill, `{colors.prata}`.
- **Hover:** border shifts to `{colors.prata}`, background gains a faint prata tint (`rgba(168,186,194,0.08)`).
- **Focus-visible:** 2px `{colors.prata}` outline, 3px offset.

### Cards / Containers
- **Corner Style:** 14px radius, `overflow: hidden`.
- **Background:** `{colors.grafite}`.
- **Border:** 1px `{colors.border-subtle}` at rest → `{colors.prata}` on hover/focus, per the shadow vocabulary above.
- **Internal content:** each card's visible content is a single baked photographic banner (16:9); the DOM carries a visually-hidden text label for accessibility rather than live overlaid type. New cards should follow the same pattern — do not add live text on top of card photography.

### Navigation
No traditional nav; the card list itself is the primary navigation, one destination per card, external links only (`target="_blank" rel="noopener"` on every one).

## Do's and Don'ts

### Do:
- **Do** keep prata as the only hue-bearing token; every other color is neutral gunmetal/gray.
- **Do** set Anton only in caps, only for the wordmark.
- **Do** use the near-invisible border-subtle edge as the card's resting state; let prata appear only on hover/focus.
- **Do** keep card photography as real, on-brand studio/workshop photography — never illustration or generic stock.
- **Do** describe every course as "100% online" in any new copy (binding brand rule from PRODUCT.md, not a visual one, but it constrains what a redesigned card may claim).

### Don't:
- **Don't** reintroduce `#fcd414` gold, `#71440c` bronze, `#b38c67` tan, or `#c3b2a6` beige anywhere — CSS custom properties, inline styles, or SVG attributes.
- **Don't** add rivets, bolt marks, or corner ornaments to cards — that motif belongs to the retired identity.
- **Don't** add a second accent color; a new functional color (like WhatsApp's green) stays confined to third-party photography/UI captures, never becomes a page-chrome token.
- **Don't** bold or italicize Anton, or set it in mixed case — its condensed weight is the whole effect.
- **Don't** widen this page past `--page-max` (460px) on desktop; the framing card, not a wider column, is the desktop treatment.
