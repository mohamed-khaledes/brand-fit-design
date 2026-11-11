---
name: brand-fit-design
description: >-
  Lightweight, inspiration-led frontend design. Before designing anything it asks the developer
  about the business and for 2-5 inspirations (sites, screenshots, Dribbble/Behance/Figma shots,
  competitors) that fit it, studies them, turns them into a short design brief traceable to the
  business and the references, gets a quick OK, then builds and critiques the page against those
  references. Merges the business-first rules of tasteskill with the distinctive-direction process of
  frontend-design, without dice-rolled palettes, kits or blocking gates. Use whenever the user asks to
  build, design, redesign, restyle or polish a landing page, website, product page, app screen or UI
  for a business, in static HTML/CSS or inside React, Next.js, Vue, Svelte, Astro or Tailwind, or says
  a page looks generic, templated, "AI-made" or "not like our business".
---

# Brand-fit design

Design the page this specific business would ship, in the visual family of references the developer
chose, not a template and not the model's house style. Every design decision must trace back to one
of three sources: **the business** (what it sells, to whom, where), **the references** the developer
gave, or **the developer's own words**. A choice with no source is a default; replace it.

## The flow

1. **Intake** – ask, then wait (section 1).
2. **Study the references** – write a digest (section 2).
3. **Brief** – tokens, layout, principles; review against defaults; one OK (section 3).
4. **Build** – in the project's stack, to the brief (section 4).
5. **Critique** – screenshots beside the references, fix, report (section 5).

Keep the brief in the project at `.design/brief.md` (template: `templates/design-brief.md`). If it
already exists, read it first: skip the questions it already answers and only ask what is missing or
what the new request changes.

## 1. Intake: ask before designing

Do not write a palette, a layout or a line of code before this step is answered. Ask everything in
**one message** (use the AskUserQuestion tool for the multiple-choice parts when available, plain
text for the rest). Full question set and follow-ups: `references/intake.md`. The essentials:

- **The business:** what is sold, who buys it, where (online / a place / a region), the one main
  action (Book a table, Start a trial, Order, Get a quote), and the price level or positioning.
- **Inspirations (the important one):** 2-5 links or images that fit the business, and for each
  *what* they like about it (colour? type? layout? photography? the feel?). Competitors count.
- **Anti-inspirations:** a site or look they dislike or that their competitors all share.
- **Own material:** logo, brand colours, fonts, real photos, product screenshots, real copy, prices,
  address, hours. Brand assets always beat references.
- **Feel in three words** and the **audience's language/direction** (RTL for Arabic, etc.).

If the developer has **no inspirations**, don't build from nothing: propose **three distinct
directions** grounded in their trade (each with a name, 2-3 well-known reference sites in that
industry or a neighbouring one, a 4-colour swatch, a type pairing and one sentence on the feel) and
let them pick or mix. If they say "just go", pick the direction that fits the trade best, say which
and why, and carry on.

## 2. Study the references

For each reference: open it (browser tool, web fetch, or read the image), take a screenshot of the
first screen and one inner section where you can, and write a short digest. How to read a reference
and the digest format: `references/reading-references.md`.

Extract **principles, never assets**: palette relationships, type character and scale, density and
whitespace, grid and alignment, image style (crop, light, people or product), shape language
(radius, borders, shadows), motion temperament, copy tone. Then mark what is **common** across the
references (that is the developer's taste) and what is **unique** to one (pick only what fits).

Never copy a reference's code, copy, photographs, logo or signature effect. The page must read as
the same *family*, not a clone.

## 3. The design brief

Write it into `.design/brief.md` and show a compact version to the developer:

- **Business line:** kind, what is sold, buyer, main action (the kind table is in
  `references/checklist.md`; it sets what visuals fit: photographs for places and physical
  products, the real UI for software, effects only where the subject is technical).
- **Palette:** 4-6 named hex values with roles (ground, surface, ink, muted, accent, optional
  second accent). Brand colours first; otherwise derived from the references' common palette.
- **Type:** one or two families with roles and a scale. Chosen to match the references' character,
  never the face you would use on any project.
- **Layout:** the hero treatment (the most characteristic thing in this business's world: a photo,
  the product, the live UI, a headline set large...), then one line per section: its one idea and
  its picture. An ASCII wireframe for the hero and one key section.
- **Shape and motion:** radius, borders/shadows, the one orchestrated motion moment, hover answers.
- **Traceability:** each of the above tagged `[biz]`, `[ref: name]` or `[dev]`.
- **The one bold thing:** where this page spends its boldness. Everything else stays quiet.

**Review before building.** Check the brief against the AI-default list in
`references/checklist.md`. Ask: "would I produce this same brief for any other business in this
trade?" Revise anything that would be, and say what you changed and why.

Then ask for **one OK** ("Build with this direction?") with the option to adjust. Skip the wait only
if the developer said earlier to go ahead without stopping.

## 4. Build

- **Stack:** build inside the existing project and its conventions (framework, CSS approach,
  components). An empty folder gets a single static `index.html` with inline or one linked CSS file.
- **Tokens first:** put the palette, type scale, spacing and radius in CSS custom properties (or the
  project's theme/Tailwind config) and use only them.
- **Content:** the developer's real copy and material. Missing copy follows the writing rules in
  `references/checklist.md`: plain, specific, the buyer's words. Never invent reviews, customers,
  figures or awards; mark any assumed fact (hours, prices) in a comment for the developer.
- **Pictures:** real photos/screens the developer gave; otherwise clearly-marked stand-ins of the
  same kind of thing (Unsplash/Pexels search, credited in the footer), listed in the report. Never a
  drawn look-alike of a real logo.
- **House rules kept from tasteskill:** the hero alone on the first screen and saying what is sold,
  for whom, with one hard fact and the main action inside it; equal left and right content edges;
  no captions explaining pictures; one button style pair, one card style, one radius scale; real
  full-colour icons for real products; no fade-in on every section, no parallax text, no scroll
  hijacking; hover answers on buttons, links and linked cards; the hero enters once.
- **Quality floor (unannounced):** responsive down to 360px, visible keyboard focus, alt text,
  labels on fields, `prefers-reduced-motion` respected, text contrast AA, no sideways scroll.

## 5. Critique and report

1. Screenshot the page at desktop (1440) and phone (390) with whatever browser tool is available
   (the built-in browser, Playwright, or a headless Chrome command). If none is available, say so.
2. Put each screenshot beside the reference digests and judge honestly:
   - Same family as the references? Name what matches and what drifted.
   - Does it look like **this** business? Would a customer know what is sold in 3 seconds?
   - Any item from the AI-default list? Any section that is a generic card grid?
   - Remove one accessory: cut the decoration that serves nothing.
3. Fix and reshoot, two rounds at most unless the developer asks for more.
4. **Report:** the direction in one line, how each reference shaped it, the palette and type, what
   was assumed, every stand-in picture the developer should replace, and what was not checked.
   Update `.design/brief.md` with anything decided during the build, plus a "tried / rejected" note
   so the next pass doesn't repeat it.

## Never

- Designing before the intake is answered (unless the developer explicitly said to skip it).
- Copying a reference's code, text, photographs, logo or signature effect.
- Ignoring the developer's brand assets in favour of a reference.
- Shader effects, 3D scenes or glowing gradients on a business whose subject isn't technical.
- Invented testimonials, logos of customers, figures, or "trusted by" strips.
- Violet/lavender or the cream + terracotta look unless the brand or references actually call for it.
