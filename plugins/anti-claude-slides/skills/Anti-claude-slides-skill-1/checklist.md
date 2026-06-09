# Audit checklist — the GATE (run on every slide before delivering; the rubric in review)

A slide passes only when **every** box holds. Report a failure as: **element → what's wrong → fix**,
citing the rule. These map 1:1 to the hard rules in `SKILL.md`. No exceptions, no "close enough."

## 0. Compose-fresh (Rule 0)
- [ ] Slide was **built fresh** from `assets/tokens.css` primitives — not copied from a prior slide.
- [ ] No demo/residue labels carried over (residue test: every label fits THIS subject).
- [ ] `assets/tokens.css` is **inlined**; tokens not redefined or altered per slide.

## 1. Typography
- [ ] **Montserrat only** — one family; hierarchy from weight + size + color, no 2nd typeface.
- [ ] Only the **3–4 sizes** in the scale: title 30px · body 15px · value 14px · label 12px · source 11px.
- [ ] **Title** is light (300–400), navy/ink, sentence/entity case, **not big-and-bold, not centered**.
- [ ] Body 15px/400; **bold spine** is 700 in the SAME ink (emphasis = weight, never color).
- [ ] Keys/chips/tags 12px/600 UPPERCASE; source 11px/400 **italic** muted.
- [ ] **Metric number** 600, **navy**, **≤ title size (never above)**, never black, never on a colored chip.
- [ ] Case discipline: sentence-case default; Title Case only proper nouns; ALL-CAPS only labels/tags;
      italic only cited titles; acronyms expanded-then-`(PARENTHESIZED)` on first use.
- [ ] No type shadows/outlines/wide tracking.

## 2. Format & density
- [ ] Slide is a **dense bounded-cell fact-card**: title + label gutters/keystrips + bounded panels +
      right rail of key→value fields + source foot.
- [ ] **Frame filled** at fact-card density; content zones flex to occupy full height — **no empty/dead
      space** (verify by render: bottom-ink near row ~678/720).
- [ ] Every region is a **bounded cell** (faint `--panel` fill or `--hair` hairline).
- [ ] **Nothing overflows** 1280×720; rows/cells capped and sized to fit.
- [ ] Arrangement varies by job; it is still a **fact-card grid** (not a divergent/sparse layout).
- [ ] **No floating label-as-heading** — labels sit in bounded gray cells.

## 3. Signal & color (one signal = one meaning)
- [ ] navy=structure/ink · gray=secondary/inactive · muted=tertiary.
- [ ] **teal `#2F8F86` = ACTIVE only** (current/selected/best/positive); used for nothing else.
- [ ] **gold `#A9853F`** = caveat / link / 2px accent rule / scope tag only.
- [ ] **≤ one teal element per comparison axis** (one row-winner, one current node).
- [ ] **No red/amber/green** anywhere — a decline is gray ▼; "at risk" is a small **gold tag**.
- [ ] No signal reused for a 2nd job; no color-for-emphasis; no gold "premium" wash.

## 4. Flatness
- [ ] Flat throughout: ivory ground, **square corners**, edges from hairlines/fills only.
- [ ] **No** shadow / gradient / glow / photo / rounded marketing pill / icon rainbow / 3D.
- [ ] Ground is `#FAFBFC` — **never pure `#FFFFFF`**.
- [ ] **No rule/border beneath the title.**
- [ ] No metric number on a colored chip or above title size (no KPI-dashboard look).

## 5. Credibility & honesty (anchor-or-cut)
- [ ] **Every** cell/value/figure anchored to a date, a fully-named authority `(ACRONYM)`, or an
      *italic* dated document title. No "experts say / recently / bare logo".
- [ ] Exactly **one** quiet italic muted `Source:` foot, bottom-left; links **underline-only** (no blue,
      no raw URL, no "various/internal").
- [ ] Parallel units identical (same template, equal counts, matched phrasing) — they compare like-for-like.
- [ ] **No N/A / — / TBD**, no invented values, no filler padding — schema bent to the data.

## 6. Reading & scope
- [ ] Works at three speeds: **title → bold-only skim → full detail**; every region labeled.
- [ ] **One slide, one job** (not two subjects/arguments — else split it).
- [ ] Reading order supports random access; the bold spine alone reconstructs the gist.
