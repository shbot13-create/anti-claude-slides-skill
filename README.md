# Anti-Claude Slides

A Claude Code **skill** that builds dense, **bounded-cell fact-card slides** — institutional, credible,
restrained, and flat. Montserrat on ivory; a four-signal palette (navy / gray / **teal** / **gold**);
no shadows, no gradients, no marketing slop. It **generates** slides from your content and **reviews**
existing slides, for any topic, as self-contained **1280×720 HTML**.

It is governed by a **strict hard-rule spec** (typography, density, one-signal color, flatness,
anchor-or-cut credibility, layered reading). There are **deliberately no template slides** — with a single
exception, the deck **cover** (a title slide, not a fact-card) — every slide is composed *fresh* from a
tokens file + flat primitives, then gated by an audit checklist. That's the
"anti-Claude" part: restrained and anchored, never generic AI deck output.

## What it enforces (the short version)
- **Typography:** Montserrat only; 3–4 sizes (title 30px / body 15px / value 14px / label 12px / source
  11px); light title, bold-weight emphasis (never color), metric numbers ≤ title size and never on a chip.
- **Density:** every slide a dense fact-card grid that fills the frame — no dead space, nothing overflowing 1280×720.
- **Color = one meaning:** teal `#2F8F86` = active/best/positive only (≤1 per comparison axis); gold
  `#A9853F` = caveat/link/rule/tag only; no red/amber/green.
- **Flat:** ivory `#FAFBFC` ground (never pure white), square corners, hairline/fill edges, no rule under the title.
- **Credibility:** every value anchored to a date / named authority / cited document; one quiet `Source:` foot.
- **Cover:** the one sanctioned template — a title-slide cover (`assets/cover.html`) with a navy/light
  title, a date, and a side image; a flat **navy** panel is the fallback when no image is provided.

Full rules live in [`SKILL.md`](plugins/anti-claude-slides/skills/Anti-claude-slides-skill-1/SKILL.md);
the audit gate is [`checklist.md`](plugins/anti-claude-slides/skills/Anti-claude-slides-skill-1/checklist.md);
the palette + sizes + primitives are in
[`assets/tokens.css`](plugins/anti-claude-slides/skills/Anti-claude-slides-skill-1/assets/tokens.css);
the deck **cover** template is
[`assets/cover.html`](plugins/anti-claude-slides/skills/Anti-claude-slides-skill-1/assets/cover.html).

## Install

### Option A — via the plugin marketplace (one command)
In Claude Code:
```
/plugin marketplace add shbot13-create/anti-claude-slides-skill
/plugin install anti-claude-slides@shbot-skills
```
Update later with `/plugin marketplace update`.

### Option B — manual (copy the skill folder)
```bash
git clone https://github.com/shbot13-create/anti-claude-slides-skill
cp -R anti-claude-slides-skill/plugins/anti-claude-slides/skills/Anti-claude-slides-skill-1 \
      ~/.claude/skills/
```
The skill is then invocable in any Claude Code session.

## Use
Just ask Claude Code to build or review slides — e.g. *"make a profile fact-card for X"*,
*"a comparison slide of these 4 options"*, *"review this slide against the rules"*. The skill activates
on slide/deck/presentation/one-pager work. Output is a self-contained `.html` you can open in any browser
or print to PDF.

### Rendering a slide to PNG (optional)
The skill builds HTML; to screenshot it, use any headless Chromium:
```bash
"$CHROME" --headless=new --disable-gpu --hide-scrollbars --force-device-scale-factor=1 \
  --window-size=1280,720 --default-background-color=FAFBFCFF \
  --screenshot=out.png "file://$PWD/slide.html"
```
(`$CHROME` = your Chrome/Chromium path; or `npx playwright screenshot --viewport-size=1280,720 slide.html out.png`.)

## Requirements
- Claude Code (recent version with plugin support).
- Internet access for the Montserrat web font (slides reference Google Fonts).
- Optional: a headless Chromium for screenshots.

## License
[MIT](LICENSE).
