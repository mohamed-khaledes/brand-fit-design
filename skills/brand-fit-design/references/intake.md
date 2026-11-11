# Intake

Ask once, in one message, grouped and short. Skip anything the request, the project files or
`.design/brief.md` already answer, and say what you already know ("I can see it's a Next.js app with
a green logo in /public").

## Look in the project first

Before asking, scan for: a logo and favicon (`public/`, `assets/`), an existing theme or Tailwind
config (brand colours, fonts), a README or landing copy describing the business, existing pages,
real photos or screenshots. Put what you find into the question as a default to confirm.

## The questions

**1. The business** (free text, 2-4 lines is enough)
- What do you sell, and to whom?
- Online, a physical place, or both? Which city/region/market?
- The one thing a visitor should do (book, order, sign up, call, get a quote, visit).
- Positioning: budget, mid, premium, luxury? Young/playful or serious/established?

**2. Inspirations** (the most important answer)
- 2-5 links or images (websites, Dribbble/Behance shots, Figma files, Instagram accounts, competitor
  sites, even a physical shop or packaging photo).
- For each: what do you like about it? (colours / fonts / layout / photos / animation / the feel /
  "everything")
- Tip to the developer: references from **the same industry or a neighbouring one** fit best; a
  great site from an unrelated industry is fine if they name the part they like.

**3. Anti-inspirations** (optional)
- A look you don't want, or what every competitor does that you want to avoid.

**4. Your material**
- Logo, brand colours, brand fonts? Real photos or product screenshots? Real copy, prices, hours,
  address? (Paths or "none yet".)

**5. Feel and language**
- Three words for how it should feel.
- Page language(s); Arabic/Hebrew means an RTL layout and a typeface with good Arabic/Hebrew glyphs.

Suggested multiple-choice items for AskUserQuestion (keep the rest as free text):
- Positioning: Budget / Mid-range / Premium / Luxury
- Theme: Light / Dark / Either
- Density: Airy and calm / Balanced / Dense and information-rich

## When there are no inspirations

Offer three directions that differ on more than colour. For each:

```
A. <name>, e.g. "Market-hall warm"
   Like: <2-3 real, well-known sites in this or a neighbouring trade>
   Palette: #xxxxxx ground · #xxxxxx ink · #xxxxxx accent · #xxxxxx surface
   Type: <display face> + <text face>
   Feel: one sentence (photo-led, big type, tight grid, etc.)
```

Make the three span different axes (e.g. photo-led and warm / type-led and minimal / bold colour
and graphic). Let the developer pick one or mix ("A's photos with C's colours").

## Follow-ups worth one more question

- A reference link won't open (login, blocked): ask for a screenshot.
- References contradict each other (a dark tech site and a pastel bakery): ask which one is
  closer to the business, or which part of each they want.
- Brand colours clash with the references: brand wins; say how you'll adapt the reference's feel
  around them.
