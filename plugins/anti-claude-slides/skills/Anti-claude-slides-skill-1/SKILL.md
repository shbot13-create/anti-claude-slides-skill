---
name: Anti-claude-slides-skill-1
description: Build dense, bounded-cell fact-card slides — institutional, credible, flat, Montserrat on ivory, navy/gray/teal/gold, single-title headers (no subtitles), sparing monochrome Lucide icons — following a STRICT hard-rule spec. Use when creating, generating, designing, building, or reviewing slides, decks, presentations, one-pagers, briefings, profile cards, comparisons, timelines, status boards, or metric readouts. Outputs self-contained 1280×720 HTML. NO templates — every slide is composed fresh from tokens + primitives, gated by a checklist. This is the anti-Claude deck style — restrained, anchored, never generic AI slop.
---

# Anti-claude-slides-skill-1

A slide-making **system governed by hard rules**. The rules below are NON-NEGOTIABLE — they are the
binding contract, not guidance. Every rule must hold on every slide, in any arrangement. This skill
**generates** slides from content and **reviews** existing slides, for any topic.

## ⚠️ Rule 0 — NO STARTER SLIDES. Compose fresh, every time.
This skill ships **zero template / starter slides on purpose.** Do NOT look for one, copy one, or
re-fill a previous slide. Build each slide **fresh** from the tokens + flat primitives in
`assets/tokens.css`, arranged to fit the slide's job, and gated by `checklist.md`. (This is also what
keeps the output from looking generated/same-y — no demo residue, no copy-paste sameness.)
**One deliberate exception:** the deck **cover** (`assets/cover.html`) — a cover is a title slide, not a
fact-card — see **THE COVER** below. Every *content* slide still has no starter, ever.

## What you start from
- `assets/tokens.css` — the exact palette + sizes + flat primitive building blocks (a band, a chip, a
  rail field, a metric, a source foot…). **Inline it** into every delivered slide. These are ELEMENTS,
  not layouts. You assemble the layout.
- `checklist.md` — the audit gate. Run it on every slide before delivering, and as the rubric in review.
- `assets/cover.html` — the **one** sanctioned starter slide: a deck **cover** (see **THE COVER** below).
  The ONLY file you copy from; every *content* slide is still composed fresh from primitives (Rule 0).

---

# THE HARD RULES (verbatim spec — all of these MUST hold)

## Typography (the exact spec)
**Font: Montserrat only** — one family for everything; hierarchy comes from **weight + size + color**,
never a second typeface.

| Role | Size | Weight | Color |
|---|---|---|---|
| Slide title | 30px (≈2× body) | light, 300–400 | navy/ink |
| Body / prose / bullets | 15px | 400 (700 for the bold spine) | ink |
| Rail values, metric labels | 14px | 400 / 700 name | ink / gray |
| Keys, chips, tags (UPPERCASE) | 12px | 600 | gray (on panel) / white (on navy) |
| Source foot | 11px (≈0.7× body) | 400 italic | muted |
| Metric number | ≤30px (restrained, ~30–34) — **never above title size** | 600 | navy — never black, never on a colored chip |

**DO:** keep to these 3–4 sizes; sentence-case by default; Title Case only for proper nouns; ALL-CAPS
only for labels/tags; italic only for cited titles; acronyms expanded-then-`(PARENTHESIZED)` on first use.
**The header is ONE title** — the title alone, a single title element (wrapping to a 2nd line is fine).
**DON'T:** add a 2nd font family, a 4th size, a big-and-bold/centered title, type shadows/outlines/wide
tracking, or color-for-emphasis (**bold weight does emphasis**). **No subtitle/definer/eyebrow** — nothing
above the title, nothing below it; framing/scope info lives in content cells, never in the header.

## Format & density
**DO**
- Make every slide a **dense bounded-cell fact-card**: title + label gutters/keystrips + bounded panels
  + a right rail of key→value fields + a source foot.
- **Fill the frame (1280×720)** at fact-card density; content zones flex to occupy full height.
- Keep every region a **bounded cell** (faint `--panel` fill or a `--hair` hairline).
- Vary the content/arrangement **by job** (profile, compare, metrics, status, timeline…).

**DON'T**
- Don't leave empty/dead space or build a sparse slide (pull-quote, lone axis, half-empty grid).
- Don't let anything overflow the frame — cap rows/cells, size to fit; **no box outside 1280×720**.
- Don't invent a divergent layout — **if it isn't a fact-card grid, it's wrong.**
- Don't float a label as a heading — labels live in **bounded gray cells**.

## Signal & color (one signal = one meaning)
**DO**
- navy = structure/ink · gray = secondary/inactive · muted = tertiary.
- **teal (`#2F8F86`) = ACTIVE only** — current / selected / best / positive (one unified meaning).
- **gold (`#A9853F`)** = caveat / link / the thin 2px accent rule / scope tag.
- Ground ivory `#FAFBFC`; navy `#33485A`; emphasize with **bold weight in the same ink**.

**DON'T**
- Don't reuse a signal for a second job (no "gold = active," no two teal meanings).
- Don't mark **more than one teal element per comparison axis** (one row-winner, one current node).
- Don't use **red/amber/green** (a decline is gray ▼; "at risk" is a small **gold tag**).
- Don't color text for emphasis or use gold as a "premium" wash.

## Flatness
**DO**
- Stay **flat**: ivory ground, square corners, hairlines/fills for edges.

**DON'T**
- Don't add shadows, gradients, glows, photos (except the deck **cover's** one bounded image — see
  **THE COVER**), rounded marketing pills, icon rainbows, 3D. (Sparing **monochrome Lucide icons** are
  the ONE sanctioned icon form — see **Icons**.)
- Don't use **pure white `#FFFFFF`**, or **a rule beneath the title**.
- Don't put a metric number on a colored chip or above title size (that's a KPI dashboard).

## Icons (slight & functional — content slides ONLY)
**DO**
- Use **Lucide stroke icons** only — `<i data-lucide="name" class="icon"></i>` plus the Lucide CDN script
  (`<script src="https://unpkg.com/lucide@latest"></script>` + `lucide.createIcons()` at the end of
  `<body>`); size via the `.icon` primitive (~1.25em).
- Keep every icon **monochrome via `currentColor`** — it inherits its cell's text color and so obeys the
  signal system (gray in a keystrip, white on a navy chip; teal/gold ONLY when the cell itself carries
  that signal).
- Put each icon **beside the text label it reinforces** (keystrip, chip, band, rail field name, state row,
  flow step) — wayfinding, not decoration.
- Stay **slight: ≤ 1 icon per labeled region, ≤ 6 per slide**; the same concept gets the same icon
  deck-wide.

**DON'T**
- **Never on the COVER** — the icon allowance is content-slides-only; the cover carries **zero icons**.
- Don't float an icon without a label, use an icon to replace words, or park decorative icons in corners.
- Don't use multicolor/filled icon blobs, emoji, a second icon set, or two different icons for one
  concept — and never recolor an icon for emphasis (color comes from the cell's signal, not the icon).

## Credibility & honesty (anchor-or-cut)
**DO**
- **Anchor every cell/value/figure** to a date, a fully-named authority `(ACRONYM)`, or an *italic*
  dated document title.
- End with **one quiet italic muted `Source:` foot**; links underline-only.
- Keep parallel units **identical** (same template, equal counts, matched phrasing) so they compare.

**DON'T**
- Don't leave a claim unanchored ("experts say," "recently," a bare logo).
- Don't show N/A / — / TBD, invent values, or pad cards with filler — **bend the schema to the data.**
- Don't paste a raw URL or default-blue link, or cite "various/internal."

## Reading & scope
**DO**
- Build for **layered reading**: title → bold-only skim → full detail; **label every region.**
- **One slide, one job;** re-derive labels/fields from this subject.

**DON'T**
- Don't put two subjects/arguments on one slide — **split it.**
- Don't reuse a template's demo labels as the schema (**residue test:** if a label only fits the demo's
  topic, replace it). *(Moot here — there are no templates — but the residue test still applies to any
  content you carry over.)*

---

# THE COVER — the ONE sanctioned exception to Rule 0
A deck needs a title slide, and a cover is **not** a fact-card. The cover is the **single** reusable
template this skill ships: **`assets/cover.html`**. It is the **only** slide you start from a file.
**Swap three slots only — title, date, image — and leave everything else.** Never copy this layout into
a content slide, and never add a second "template."

**Structure (locked):** a left ivory text column (title + date) and a right **full-bleed** image column,
bounded top and bottom by the **gold 2px accent rule**. ~55% text / ~45% image.

**Exempt on the cover ONLY (nowhere else):**
- **Rule 0** — the cover *is* the one reusable starter.
- **Fact-card density / fill-the-frame / no-dead-space** — a cover is deliberately airy; the left column
  breathes. Do **not** "fill" it with fact-card cells.
- **The no-photo clause of Flatness** — the cover carries **one** bounded photo (the right column).
- **Bounded-cell structure / right rail / `Source:` foot** — a cover has none of these.

**Still binding on the cover (do NOT bend):**
- **Montserrat only.** Ivory ground `#FAFBFC` on the text column — **never pure `#FFFFFF`**.
- **Title:** navy/ink, **light (300)**, **left-aligned**, sentence/entity case, **at the title size** —
  **not enlarged, not centered, not recolored** (no gold title, no 4th size, **no rule beneath it**).
- **Gold = the 2px accent rule only** — it appears solely as the two frame bars. **Nothing else is gold.**
- **Square corners**; no shadow / gradient / glow / rounded card on the chrome.
- **Date** is one quiet gray label, **honestly anchored** (a real date — no "TBD," no placeholder month).
- **One slide, one job:** a cover names the deck. No bullets, no agenda, no second subject.
- **Zero icons.** The icon allowance (see **Icons**) is content-slides-only — no icon anywhere on the cover.

**Image — sourcing process (simple; never auto-fabricate filler):**
1. **Ask the user for an image.** If they provide one (path or URL), embed it **raw** (no filter),
   framed by the gold bars.
2. **If none is provided → the navy fallback.** Leave the image column as a flat **`--navy`** panel
   (still bounded by the two gold bars) — a clean, simple cover, fully within the core Flatness rule.
3. **Online search or AI-generation happen ONLY if the user explicitly asks** — and stay subject to brand
   guardrails (license-safe, text/logo-free, no recognizable real public figure).

The template ships in the **navy-fallback** state; supplying an image is a one-line swap — uncomment the
`<img>` in `.cover-media` and set its `src` (base64-embed it for a self-contained file). The shipped
`cover-sample.jpg` is just an example you can point that `<img>` at. Audit with **§8** of `checklist.md`
(not §0/§2's density gates).

---

# MODE A — Generate
*(Need a **cover**? Start from `assets/cover.html` per **THE COVER** — swap title/date/image, audit with
§8. The steps below are for **content** slides, composed fresh.)*
1. **Name the job in one sentence:** "a scanner must walk away knowing ___." One slide, one job. If it
   answers two questions, it's two slides.
2. **Pick the fact-card arrangement that fits the job** (profile / compare / metrics / status / timeline
   / etc.) — *arrangement*, not a template. It is ALWAYS a bounded-cell fact-card grid (Rule 0 +
   Format & density). Decide the regions: title, label gutters/keystrips, bounded panels, a right rail
   of key→value fields, a source foot. Let content zones flex to fill 1280×720.
3. **Assemble from `assets/tokens.css` primitives** — inline the file, compose the elements (band, chip,
   panel, rail/field, metric, dot, tag, spine-list, source). Pour in the subject's real content;
   re-derive every label/field from the subject. Optionally add **a few Lucide icons** beside region
   labels where they aid wayfinding — within the **Icons** caps (≤ 1 per region, ≤ 6 per slide).
4. **Anchor everything** (date / named authority / italic dated title). One quiet `Source:` foot.
5. **Self-audit — mandatory gate:** run **every** item in `checklist.md`; fix each violation before
   presenting.
6. **Render and LOOK — mandatory:** screenshot the HTML headless and inspect it (catch overflow, dead
   space, and density failures the static read misses — measure the bottom gap if unsure). Re-render
   after fixes.
7. **Deliver** the self-contained `.html` (tokens inlined). Offer a screenshot and, for many slides, a
   bundled navigable `deck.html`.

## MODE B — Review / audit
Read the target (HTML / image / description) + `checklist.md`. Walk **every** element; report each
violation as **element → what's wrong → fix**, citing the rule. Separate hard rule-breaks from judgment
calls. Apply fixes on request, then re-audit.

---

# Render & verify (how to screenshot)
Render with ANY headless Chromium and capture an exact 1280×720 frame. Resolve the browser for the
platform — use the first that exists (set it as `$CHROME`):
- **macOS:** `/Applications/Google Chrome.app/Contents/MacOS/Google Chrome`
- **Linux:** `google-chrome` · `chromium` · `chromium-browser`
- **Windows:** `C:\Program Files\Google\Chrome\Application\chrome.exe`
- **Fallback (any OS, no Chrome):** `npx playwright screenshot --viewport-size=1280,720 slide.html out.png`
```
"$CHROME" --headless=new --disable-gpu --hide-scrollbars --force-device-scale-factor=1 \
  --window-size=1280,720 --default-background-color=FAFBFCFF \
  --screenshot=out.png "file://ABSOLUTE/PATH/slide.html"
```
Dead-space test (objective): the lowest row with ink should sit near the bottom margin (~row 678/720).
A large bottom gap = a sparse slide → grow/redistribute content until the frame is filled.
Icon test: every `data-lucide` name must show a rendered glyph — a bad name renders NOTHING (an empty
gap beside its label). Fix the name and re-render. (Headless Chrome runs the Lucide script; if the CDN
was unreachable, re-render with network access before judging.)

# Output contract
- Self-contained `.html`, exactly **1280×720**, Montserrat via Google Fonts link, icons (if any) via the
  Lucide CDN script + `lucide.createIcons()` at the end of `<body>`, `assets/tokens.css` **inlined**.
  Nothing overflows the frame. One `Source:` foot. Passes `checklist.md` with no exceptions.
- **Source-foot guard (common failure):** `.source` is full-width and pinned to the bottom
  (`margin-top:auto`). Every content column / rail / panel MUST end **above** it — a rail or panel that
  runs to the frame edge will overprint the source band. Cap rail fields / trim padding until the
  content clears the source line, and confirm in the render (no ink overlapping the foot).
