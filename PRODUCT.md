# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Stack

static HTML/CSS (no build step, no framework — single `index.html` + `style.css`)

## Users

Two audiences of equal weight, both arriving from Instagram/YouTube/WhatsApp bio links:

- **Mecânicos diesel buscando especialização** — technicians already working with diesel engines who want to specialize in Common Rail, Scania XPI, or Unidade Injetora systems to raise their income.
- **Aspirantes a empreendedor do setor** — people interested in opening a diesel-injection service business or lab, evaluating the franchise/lab model rather than (or in addition to) the technical courses.

## Product Purpose

Alemão Diesel (Método DRV) is a training and services brand for diesel fuel-injection specialization. It exists to route bio-link visitors to its online courses (Unidade Injetora, Common Rail), YouTube channel, and WhatsApp support/franchise inquiries. Success is a completed click-through: course checkout, channel subscription, or a support/franchise conversation started.

## Positioning

Deep technical authority in a narrow mechanical specialty (diesel fuel injection — Common Rail, Scania XPI, Unidade Injetora) delivered as 100%-online training, backed by a real physical service lab (Curitiba) and a franchise path — not a generic "become a mechanic" course.

## Operating Context

- This is a **link-in-bio surface**: a single mobile-first static page, entry point is Instagram/YouTube/WhatsApp bio, not a marketing funnel in itself.
- Each card routes off-site: two courses to their own checkout/landing pages (Hotmart or dedicated landing URLs), one to the YouTube channel, one to WhatsApp.
- No backend, no analytics wiring currently present (`data-link` attributes exist on cards but nothing consumes them yet).

## Capabilities and Constraints

- **Golden rule (binding):** every course must always be described as **"curso online"** (100% online, immediate access) — never as in-person/presencial, in any copy, art, or script.
- Copy frameworks in use: Value Equation / Grand Slam Offer (Hormozi), and PAS (Problema → Agitação → Solução) for sales-page-style copy.
- Real content only: instructor photography is real (studio/workshop), not illustration or stock generic graphics.

## Brand Commitments

- Name: **Alemão Diesel** (Método DRV).
- Logo: fixed symbol — shield with crossed piston and wrench, side wings. Never stretched/distorted; keep protective padding equal to the wing height; minimum size 32px on screen / 15mm print.
- **Visual identity rebranded 2026-08-10** (Manual da Marca v2.0, Aug 2026, `assets/Manual-da-Marca-Alemao-Diesel.md`): this page now runs the cooler gunmetal/silver system referencing the brand's real Curitiba lab signage, replacing the prior gold/bronze-on-black identity — see `DESIGN.md` for the applied tokens. The manual remains the binding source for any further visual work on this or other brand surfaces; treat the old gold identity as legacy/anti-reference.
- Tone of voice: direct, results-oriented ("domine", "vire especialista", "aumente sua renda"), backed by technical proof (system acronyms, vehicle brands, years of experience). Never implies in-person classes, fixed cohorts, or travel.
- Other brand surfaces referencing the same identity (not all in this repo): course artwork (Unidade Injetora, Common Rail), a main hub page, YouTube channel art, and Common Rail lab materials — this repo (`alemao-bio`) covers only the link-in-bio page.

## Evidence on Hand

- Real instructor photography embedded inline in `index.html` (base64) for hero and course cards.
- Real logo asset (`assets/favicon-512.png` and inline in `index.html`).
- Confirmed live links: two Hotmart/landing course checkouts, YouTube channel (`@alemaodiesel9472`), WhatsApp (`wa.me/5541998253542`), Instagram (`instagram.com/alemaodiesel1`).
- Brand reference screenshots described (not stored as images) in the manual, section 06, sourced from `https://alemao-diesel-curitiba.resultadoscomerciais.chatgpt.site/`.
- No testimonials, pricing, or case studies present on this page — do not fabricate any.

## Product Principles

1. Every course mention says "100% online" — never implies presencial delivery.
2. Real photography and real logo only — no generic illustration, no stock icon substitutes for the brand mark.
3. The page is a router, not a pitch — keep it scannable and fast; the actual persuasion happens on the destination pages.
4. Serve both audiences (technical upskilling and franchise/business interest) without one crowding out the other.
5. Follow the current Manual da Marca as the binding visual authority once applied; do not blend it with the superseded gold identity.

## Accessibility & Inclusion

No product-specific requirement established beyond standard web accessibility (contrast, keyboard focus, alt text) already addressed in prior polish work on this page.
