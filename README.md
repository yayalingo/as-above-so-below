# As Above, So Below

> 如在其上，如在其下 — a complex-systems bridge between astrology and science.

An interactive thought experiment. It turns the core argument of the essay
[*占星术、八卦与复杂系统：寻找迷信与科学之间的桥梁*](https://dev.to/sanyaduan/zhan-xing-zhu-ba-gua-yu-fu-za-xi-tong-xun-zhao-mi-xin-yu-ke-xue-zhi-jian-de-qiao-liang-35hm)
into a live, manipulable model — and then gives you the tools to be skeptical of it.

## The idea, in one sentence

The universe and the human body are **the same kind of thing**: coupled,
dynamical complex systems. Astrology and the I Ching are not "directionally
wrong" — they are *too crude*. They are ancient attempts to find measurable
signal correlations inside a complex system, rediscovered today as
multi-agent systems.

## What the project does

Two systems, coupled through a signal bridge:

- **Macro — the celestial system** (left): the Sun, Moon and planets orbit and
  each emits a periodic "signal". The Sun's light is the dominant, established
  driver; the planets are weak, schematic perturbations.
- **Micro — the human system** (right): a small coupled network of six agents —
  the circadian clock (SCN), melatonin, cortisol, mood, energy, and the immune
  system — with the Sun→SCN→melatonin→mood path as the *real* causal chain.
- **The bridge** (center): the signal channel coupling the two.

You can watch **emergent behavior** — mood, energy and melatonin oscillate with
the day/night cycle, and the SCN *entrains* to light (a real complex-systems
phenomenon: synchronization).

### Controls

| Control | What it does |
|---|---|
| Simulation speed | 0.25× – 4× |
| Signal coupling | Strength of the cosmos→body link (0 = decoupled, two independent systems) |
| Noise | Injects randomness into the body network |
| Skeptic mode | Dims the unproven (planetary) paths; highlights the established Sun path |
| Shuffle planet phases | Re-randomizes orbits to show correlation is unstable |
| Reset / Pause | Reset the model / freeze time |

### Live readouts

Mood, Energy, Melatonin, **Circadian sync** (`r(light, SCN)`, the entrainment),
and the headline **`r(Cosmos, Mood)`** correlation.

## The Skeptic Lab

The second tab holds the essay's critical reflection, made interactive:

1. **Correlation ≠ causation** — the causal graph is *known here* (we wrote it).
   The Sun drives mood; the planets contribute nothing. Yet a naive observer can
   still find a nonzero "astrology ↔ mood" correlation, because everything is
   periodic and finite samples produce spurious alignment.
2. **Live correlation** — watch `r(Astrology, Mood)` vs `r(Cosmic, Mood)`. Crank
   the noise or shuffle phases: the astrology number jumps around wildly; the
   Sun's stays high, because it is the real driver.
3. **Overfitting (Barnum oracle)** — a horoscope generator that is vague enough
   to always "fit". That is overfitting, not prediction.
4. **Evidence ladder** — where each claim actually stands: *established*
   (tides, melatonin), *frontier* (geomagnetic ↔ cardiovascular), *speculative*
   (planet → personality).
5. **Survivorship bias** — 24 predictions, filter to "hits only", and watch the
   misses quietly disappear.

## Run it

This is a single self-contained file. No build, no dependencies.

```bash
# just open it
start index.html        # Windows
open index.html         # macOS
```

Or serve it:

```bash
python -m http.server 8000
# http://localhost:8000
```

## Honest disclaimer

This is a **schematic model, not a validation of astrology**. Planetary causal
weights are deliberately set to **zero** here to make the point sharply. In
reality there may be a tiny, still-unproven physical coupling; the essay's
position is exactly that: *"the direction may not be wrong, but the tools are
far too crude."* See the footer of the app for the full disclaimer.

## Structure

```
as-above-so-below/
├── index.html          # the entire interactive experiment (HTML + CSS + JS)
├── README.md           # this file
└── README.zh-CN.md     # 中文说明
```

## Theoretical anchors

Complex systems theory · chronobiology · entrainment/synchronization ·
ReAct multi-agent systems · Barnum effect · multiple-comparisons / data dredging.
