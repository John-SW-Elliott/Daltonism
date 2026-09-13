<div align="center">

<img src="loja/icone_512.png" alt="Daltonismo app icon" width="120">

# Daltonismo

**See how each type of color vision deficiency perceives color, take a screening
test, and choose combinations that work for everyone.**

9 languages · works fully offline · no accounts, no tracking, no permissions

</div>

---

## What it does

Four tools that usually live in four different places:

| | |
| --- | --- |
| **Simulator** | Any color, across all 8 vision types, with severity adjustable from 10% to 100% |
| **Screening test** | Six questions, then a percentage match against each type |
| **Accessible guide** | Color pairs with a verdict, a 20-color palette analyzed for likely confusions, and recommended substitutes |
| **Adjuster** | Fine-tune a color and see its distortion measured, plus an automatic accessible suggestion |

> [!IMPORTANT]
> The screening test is **indicative and is not a clinical diagnosis**.
> Color vision deficiency is diagnosed by an eye doctor using calibrated
> instruments such as Ishihara plates and an anomaloscope. If the result
> suggests anything, or if you already struggle with colors, see a professional.

## Why the numbers can be trusted

Most color-blindness filters apply a matrix and stop there. This one doesn't:

- Simulation uses the dichromacy matrices from **Machado, Oliveira & Fernandes
  (2009)**, applied in **linear RGB** — the sRGB gamma encoding is removed
  before the computation and reapplied afterwards. Skipping that step makes
  every result systematically too light, which is the most common flaw in
  simulators.
- Intermediate severities come from linear interpolation with the identity, the
  usual approximation of the paper's own intermediate matrices.
- Achromatopsia uses physical Rec.709 luminance in linear space, not a naive
  average of the channels.
- Color differences are measured in **ΔE2000 (CIEDE2000)**, not RGB distance.
  Below ~2 the difference is imperceptible; above ~25 the colors are clearly
  distinct.
- Contrast follows the **WCAG 2** ratio, computed on the *perceived* colors when
  judging a pair, and on the original color when checking conformance.

The implementation is checked against published anchors: pair 1 from **Sharma et
al. (2005)** yields ΔE2000 = 2.0425, and the neutral axis L50→L60 yields 9.4707.

## Designed for the people who use it

- **Status is never signalled by green and red.** Verdicts use teal, amber and
  burnt orange, always paired with a dot *and* a word — the exact mistake this
  app exists to help you avoid.
- **Every color code copies with one tap**, and every field accepts a pasted hex
  in any common form.
- **Nothing is hidden behind a gesture**: a side drawer lists every section, and
  the tab strip fades at the edges when there is more to reach.
- The screening test is fully usable by keyboard and reports honest progress
  before you can run it.

### The icon had to pass its own test

The three colors in the mark were not picked by taste. A search maximized the
smallest ΔE00 separation between the circles across **all eight vision types**,
while requiring at least 4.5:1 contrast against the background. The result holds
a minimum ΔE00 of **15.9**, in the worst case — achromatopsia, where only
lightness separates anything.

The earlier mark scored **0.4** under achromatopsia: two of the circles
collapsed into the same gray. The logo of a color-blindness app was unreadable
to part of its own audience.

## Privacy

Nothing leaves your device. There is no account, no login, no advertising, no
analytics, and the app requests **no permissions at all** — it has no access to
the internet, your files, camera, contacts or location.

The app stores only your preferences (language, theme, selected vision type) in
its own local storage. Your screening answers exist only while the screen is
open and are never saved. Android's automatic cloud backup is switched off, so
even those preferences aren't copied anywhere without you knowing. The app's own
backup is manual, started by you, in an open format.

[Full privacy policy](loja/politica/index.html)

## Languages

Português · English · Italiano · 日本語 · Español · Français · Deutsch · 中文 · 한국어

Fully translated in all nine — interface, color names, vision-type names and
long-form explanations. A **System** option follows your device's language and
keeps up if you change it while the app is open.

## References

- Machado, G. M., Oliveira, M. M., Fernandes, L. A. F. (2009). *A
  Physiologically-based Model for Simulation of Color Vision Deficiency.*
  IEEE Transactions on Visualization and Computer Graphics.
- Sharma, G., Wu, W., Dalal, E. N. (2005). *The CIEDE2000 Color-Difference
  Formula: Implementation Notes, Supplementary Test Data, and Mathematical
  Observations.* Color Research & Application.
- W3C. *Web Content Accessibility Guidelines (WCAG) 2.*

## License

PREENCHER_LICENCA

---

<div align="center">
<sub><em>Daltonismo</em> is Portuguese for color blindness.</sub>
</div>
