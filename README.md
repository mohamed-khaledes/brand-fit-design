# brand-fit-design

**A lightweight, inspiration-led frontend design skill for Claude Code.**
It asks about your business and for the sites you love, then designs a page that fits *your*
business, not a template and not the usual AI-generated look.

Most design skills decide the look for you. Some pick from a fixed kit, some roll random
palettes, and some fall back on the same cream, serif and terracotta page every time. The result
can be polished and still feel like it belongs to someone else's business. `brand-fit-design`
starts from the other end: your business and your references come first, and every design
decision has to trace back to one of them.

---

## How it works

```
1. Intake      →  asks about the business + 2-5 inspirations, then waits
2. Study       →  opens each reference, screenshots it, writes a short digest
3. Brief       →  palette, type, layout, motion, each tagged with its source; one OK from you
4. Build       →  in your project's own stack, tokens first
5. Critique    →  screenshots at desktop + phone beside the references, fix, report
```

### 1. Intake: it asks before it designs

In one message, it asks for:

| | |
|---|---|
| **The business** | what you sell, to whom, where, the one main action, the price level |
| **Inspirations** | 2-5 links or images (sites, Dribbble/Behance shots, Figma, competitors) and *what* you like about each |
| **Anti-inspirations** | looks you don't want, or what every competitor does |
| **Your material** | logo, brand colours, fonts, real photos, copy, prices |
| **Feel + language** | three words for the feel; the page language (RTL supported) |

**No inspirations?** It proposes three distinct directions for your trade, each with
reference sites, a swatch and a type pairing, and you pick or mix them. Say "just go" and it
picks the best fit and explains why.

### 2. Study the references

It extracts **principles, never assets**: palette relationships, type character, density,
grid, image style, shape language, motion and tone. It notes what your references have **in
common** (that's your taste) and never copies their code, copy, photos, logos or signature
effects.

### 3. A traceable brief

Every choice is tagged with where it came from: `[biz]`, `[ref: name]` or `[dev]`. The brief
is checked against a list of common AI-default looks, then you get **one** "build with this
direction?" checkpoint.

### 4-5. Build and critique

It builds in your stack (static HTML, React, Next.js, Vue, Svelte, Astro, Tailwind), takes
screenshots at desktop and phone widths, compares them with your references, fixes what drifted
(two rounds at most), and reports every assumed fact and stand-in photo you need to replace.

### It remembers

The brief is saved to `.design/brief.md` in your project, with a log of what was tried and
rejected. The next session reads it and skips the questions you've already answered.

---

## Install

### As a Claude Code plugin

```bash
/plugin marketplace add mohamed-khaledes/brand-fit-design
/plugin install brand-fit-design@brand-fit-design
```

### Manually

Copy the skill folder into your personal skills folder (or into a project's `.claude/skills/`):

```bash
git clone https://github.com/mohamed-khaledes/brand-fit-design.git
cp -r brand-fit-design/skills/brand-fit-design ~/.claude/skills/
```

On Windows (PowerShell):

```powershell
git clone https://github.com/mohamed-khaledes/brand-fit-design.git
Copy-Item -Recurse brand-fit-design\skills\brand-fit-design "$env:USERPROFILE\.claude\skills\"
```

Start a new Claude Code session afterwards so the skill is picked up.

## Usage

Just ask for a page. The skill triggers on requests like:

- "Make a landing page for my car dealership"
- "Redesign our clinic's homepage, it looks generic"
- "Restyle this pricing page so it feels like our brand"

Or call it by name: `/brand-fit-design`.

**Tip:** the more specific your inspirations, the better. "I like the photography on site A
and the big type on site B" beats "make it modern".

---

## What's inside

```
skills/brand-fit-design/
├── SKILL.md                      # the flow and the rules
├── references/
│   ├── intake.md                 # the questions, and the 3-directions fallback
│   ├── reading-references.md     # how to digest a reference site or image
│   └── checklist.md              # business kinds, AI-default looks, writing rules, final check
└── templates/
    └── design-brief.md           # saved to .design/brief.md in your project
```

No scripts, no dependencies, no hooks. Screenshots use whatever browser tool your Claude Code
session has (the built-in browser, Playwright, or headless Chrome).

## Compared with the skills it grew from

| | tasteskill | frontend-design | **brand-fit-design** |
|---|---|---|---|
| Where the look comes from | randomly dealt from a built-in kit | the model's own distinctive take | **your business + your references** |
| Asks for inspirations | no | no | **yes, first** |
| Size | ~380-line skill + scripts, kits, a gate hook | ~70 lines | ~140 lines + 3 short references |
| Browser check | required, blocking gate | optional | screenshots + critique, non-blocking |
| Remembers decisions | per-build history files | no | `.design/brief.md` |

## Credits

`brand-fit-design` merges ideas from two skills:

- [tasteskill](https://github.com/Leonxlnx/taste-skill) by Leonxlnx (MIT): the business-kind
  rules (photos for places and products, real UI for software, effects only for technical
  subjects), the house rules for heroes, edges and motion, and the copy tells.
- [frontend-design](https://github.com/anthropics/claude-plugins-official) by Anthropic
  (Apache 2.0): the plan-review-build-critique process, the list of AI-default looks and the
  writing guidance.

## License

[MIT](LICENSE)
