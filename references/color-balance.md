# Color balance — roles, ratios, and pop

Companion to [`color-scheme`](../skills/color-scheme/SKILL.md). Encodes the before→after teaching from `media/color-scheme/`.

## Why “flat” fails

Two well-chosen neutrals (or a calm duo pulled from a photo) can feel finished—but **without a scarce accent**, the eye has no focal punch. The fix is not more color; it is **one** hotter/cooler/brighter note on the thing that matters.

| Failure | Fix |
| --- | --- |
| Muddy / same-value greys | Separate dominant field vs structural dark (text/image) |
| Rainbow chrome | One accent; mute status colors |
| Accent everywhere | Cap accent at ~5–10% of painted UI |
| Accent fights the hero | Extract accent from light, glow, or fabric already in the photo |
| Purple-AI default | Subject-grounded accent; ban unearned violet kit |

## Ratio models

### Classic light UI — ~60 / 30 / 10

| Share | Job | Example (Sage–Walnut–Amber) |
| --- | --- | --- |
| **~60%** | Quiet field | Warm cream / off-white bg |
| **~30%** | Structure + mood | Walnut type + Sage in furniture/soft panels |
| **~10%** | Pop | Amber on *alive* (+ optional solid CTA) |

Charcoal–Silver–Red follows the same shape: Silver field ~60%, Charcoal type/structure ~30%, Signal Red ~10% (keyword + one hero-tied plane).

### Dark luxury — ~80 / 15 / 5

| Share | Job | Example (Jet–Amethyst–Cyan) |
| --- | --- | --- |
| **~80%** | Canvas | Jet `#050505` |
| **~15%** | Mood in imagery | Amethyst in blooms/depth—not purple buttons |
| **~5%** | Sparkle | Cyan on edges/highlights only |

Dark schemes fail when the “secondary” becomes saturated chrome. Keep amethyst (or brand deep) **in the picture**; keep sparkle tiny.

## Where accent may live

**Allowed (pick few):**

1. One headline keyword (italic or weight change optional)
2. Primary CTA fill or strong outline
3. Small icon, underline, or focus-adjacent mark
4. At most **one** accent plane that continues a color already in the hero (red strip beside the rock; cyan edge on petals)

**Forbidden as accent abuse:**

- Full-width section washes
- Every card border / badge / chart series
- Nav + logo + buttons + links all accented
- Gradient headline + matching gradient button kit

## Imagery ↔ palette

1. Sample 3–5 regions from the hero (fabric, wood, sky, glow, shadow).
2. Name them; promote one quiet field, one structure, one pop.
3. If the photo already “contains” the accent (golden hour, neon edge, signal light), UI accent should **rhyme**—not invent a fourth mood.

## Contrast quick rules

| Pair | Target |
| --- | --- |
| Body / UI text on bg | ≥ 4.5:1 (WCAG AA) |
| Large display text | ≥ 3:1 |
| Accent keyword on light | Prefer display size; if <4.5:1, don’t use for body/links |
| Accent CTA | Text on accent button must pass AA |
| Focus | Visible ring; don’t rely on color alone for errors/success |

## Token checklist

```text
--bg        dominant field
--surface   raised quiet plane (neutral)
--text      primary type (secondary structure)
--muted     secondary type / hints
--border    hairline neutral
--accent    ONE pop hue
```

No `--accent-2` unless the brief explicitly requires dual-brand systems—and even then, UI still picks **one** focus accent per view.

## Reference pairs

| Pair | Paths |
| --- | --- |
| Sage–Walnut → Amber | [before](../media/color-scheme/sage-walnut-before.jpg) · [after](../media/color-scheme/sage-walnut-amber-after.jpg) |
| Jet–Amethyst → Cyan | [before](../media/color-scheme/jet-amethyst-before.jpg) · [after](../media/color-scheme/jet-amethyst-cyan-after.jpg) |
| Charcoal–Silver → Red | [before](../media/color-scheme/charcoal-silver-before.jpg) · [after](../media/color-scheme/charcoal-silver-red-after.jpg) |
