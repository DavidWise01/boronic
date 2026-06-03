# Boronic Core

*An 8×8×8 boron-nitride processor, stacked in light and material — and made explorable.*

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=flat-square)](LICENSE)
[![concept](https://img.shields.io/badge/hardware-concept-46c8ff?style=flat-square)](#what-it-is)
[![lattice](https://img.shields.io/badge/8%C3%978%C3%978-512%20nodes-2fd6c0?style=flat-square)](#architecture)
[![material](https://img.shields.io/badge/hBN%20%2B%20WS%E2%82%82-2D%20materials-ffce3a?style=flat-square)](#architecture)

**→ Run it: [davidwise01.github.io/boronic](https://davidwise01.github.io/boronic/)**

A processor stacked in boron. An **8×8 grid, eight layers deep** — **512 nodes** — a
microplasma chamber over piezoelectric films, a **hexagonal boron-nitride (hBN)** lattice,
and **tungsten-disulfide (WS₂) quantum dots**, driven by real, live 512-bit math.

---

## What it is

A **concept and an interactive simulation** — a way to think with the eyes about a processor
built from 2D materials: an hBN lattice as the substrate, WS₂ quantum dots as the active
sites, piezoelectric films to drive them, and a microplasma chamber on top.

**Kept honest:** hBN and WS₂ are real materials, and the **512-bit math runs live** in your
browser (eight 64-bit layer-words `L0–L7` composing into `CORE[511:0]`). But the microplasma
drive, the optics, and the performance are a **visualization of the design** — not
measurements of a fabricated, benchmarked chip. The concept render in
[`assets/`](assets/boron_single_chip.jpg) labels its materials conceptually.

---

## Architecture

`8 × 8 × 8 = 512`. Each layer is an 8×8 array (one 64-bit word); eight layers close the tower.

**The stack, top → bottom:**

| | Layer | Material |
|---|---|---|
| `L7` | Microplasma Chamber | blue plasma plume · amber core ring |
| `L6` | 12 nm Piezo | piezoelectric drive film |
| `L5` | Electrostatic Gate | field control |
| `L4` | Nano-Piezo Array | actuating pillars |
| `L3` | Optical Piezo | photo-mechanical coupling |
| `L2` | Hexagonal Boron Nitride | hBN lattice · the substrate |
| `L1` | Tungsten Disulfide Quantum Dots | WS₂ · the active sites |
| `L0` | Circuit Base | cyan trace interconnect |

---

## The demo

[`demos/core.html`](demos/core.html) — a single self-contained HTML file (vanilla
canvas/JS, no dependencies, runs offline). The eight layers explode into an isometric tower
of 512 glowing nodes; the microplasma chamber fires at the top. Controls: **plasma
containment · piezo drive · coupling/coherence · output gain**, a `.01 FINE` toggle, an
`⚡ IGNITE` boost, and an 8-way layer selector. Live `L0–L7` words, `CORE[511:0]` hex, and an
XOR checksum update in real time.

---

```
ROOT0-ATTRIBUTION-v1.0
Project: BORONIC CORE — 8×8×8 boron-nitride processor concept
Architect: David Lee Wise / ROOT0 / TriPod LLC
AI Collaborator: AVAN (Claude / Anthropic)
License: MIT
```
