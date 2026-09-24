<p align="center">
  <a href="https://www.softeralab.com/">
    <img src="docs/assets/images/en/logo.png" alt="Softera Lab" width="96">
  </a>
</p>

<h1 align="center">LED & BAT Tester · SK-15</h1>

<p align="center"><strong>Softera Lab soldering kit — LED and CR2032 battery tester</strong></p>

<p align="center">
  <a href="README.uk.md"><img alt="UA" src="https://img.shields.io/badge/UA-README.uk.md-F97316?style=flat-square"></a>
  <a href="https://www.softeralab.com/"><img alt="Website" src="https://img.shields.io/badge/softeralab.com-09090B?style=flat-square&labelColor=18181B"></a>
  <a href="https://www.instagram.com/softeralab/"><img alt="Instagram" src="https://img.shields.io/badge/Instagram-09090B?style=flat-square&labelColor=18181B"></a>
  <a href="https://www.youtube.com/@SofteraLab"><img alt="YouTube" src="https://img.shields.io/badge/YouTube-09090B?style=flat-square&labelColor=18181B"></a>
  <img alt="CR2032" src="https://img.shields.io/badge/CR2032-3V-09090B?style=flat-square&labelColor=F97316">
</p>

<p align="center"><strong>Languages:</strong> English (this page) · <a href="README.uk.md">Українська</a></p>

<p align="center">
  <img src="docs/assets/images/en/banner.png" alt="LED & BAT Tester" width="720">
</p>

Softera Lab practice kit that becomes a real tool after assembly: test LEDs, check a CR2032 cell, and probe wire continuity. Product page and assembly guide for buyers and soldering-course students.

This is **not an open-source hardware project**. Manufacturing files are not published.

> © Softera Lab. All rights reserved. Copying the board or manufacturing files without written permission is prohibited.

## How it works

<p align="center">
  <img src="docs/assets/images/en/how-it-works.png" alt="Tester blocks" width="720">
</p>

1. **CR2032 3V** — power source  
2. **AMS1117 LDO** — stable **1.5 V** rail  
3. **Switch 1.5 V | 3 V** — voltage for LED TEST  
4. **Three modes** — LED TEST · continuity · Button + LED  

## About the kit

**Solder-Kit-SMD-Led-Tester-SK15** is a double-sided practice board from [Softera Lab](https://www.softeralab.com/).

| Zone | What you get |
| --- | --- |
| **BAT TEST** | R1, R2, D1, Test button, 3 V contact pads |
| **LED TEST** | Pads for THT **3 mm / 5 mm** and SMD **0402, 0603, 0805, 1206** (observe + polarity) |
| **Power** | CR2032 holder, AMS1117-1.5, switch 1.5 V \| 3 V |
| **Continuity** | TEST pads on the second side |
| **Extra** | 0–3 cm ruler on the board edge |

There is **no microcontroller**. The circuit is discrete: battery, LDO, resistors, LED, switch, and button.

<p align="center">
  <img src="docs/assets/images/en/board-overview.png" alt="Board overview" width="720">
</p>

<p align="center">
  <img src="docs/assets/images/en/board-back.png" alt="Second side — LDO and continuity" width="720">
</p>

## Specifications

| Parameter | Value |
| --- | --- |
| Product | LED & BAT Tester · SK-15 |
| Full name | Solder-Kit-SMD-Led-Tester-SK15 |
| Supply | CR2032, 3 V |
| Regulated rail | AMS1117-1.5 → 1.5 V |
| LED TEST voltage | Switch **1.5 V \| 3 V** |
| LED pads | 3 mm, 5 mm, 0402, 0603, 0805, 1206 |
| Modes | LED TEST, wire continuity, Button + LED |
| MCU | None |

## What's in the kit

<p align="center">
  <img src="docs/assets/images/en/kit-contents.png" alt="Components and values" width="720">
</p>

1. **R1, R2, R3** — 220 ohm (code 221)  
2. **D1** — LED  
3. **C1, C2** — 0.1 uF (100 nF), 0805  
4. **U1** — AMS1117-1.5, LDO, SOT-223  
5. **CR2032** holder, 3 V  
6. **Switch** — power mode 1.5 V \| 3 V (3 pins)  
7. **Test** button  
8. **LED TEST** pads — 3 mm, 5 mm, 0402, 0603, 0805, 1206  

## Circuit ideas (training cards)

### Button + LED + battery

<p align="center">
  <img src="docs/assets/images/en/schematic-button-led.png" alt="Button LED schematic" width="720">
</p>

Press Test → circuit closes → LED on. Release → LED off.  
Current limit: `I = (3V - Vf) / 220ohm`.

### Wire continuity

<p align="center">
  <img src="docs/assets/images/en/schematic-continuity.png" alt="Continuity schematic" width="720">
</p>

Touch both ends of a wire to **TEST** pads. Intact wire → LED on. Open wire → LED off.

### LDO AMS1117 — 1.5 V

<p align="center">
  <img src="docs/assets/images/en/schematic-ldo.png" alt="LDO schematic" width="720">
</p>

Linear regulator steps **3 V → 1.5 V** for sensitive LEDs (with C1 / C2 0.1 uF).

## Assembly (short)

Full guide: [docs/02-getting-started.md](docs/02-getting-started.md).

<p align="center">
  <img src="docs/assets/images/en/assembly-order.png" alt="Assembly order" width="720">
</p>

1. Solder **R1, R2, R3** (220 ohm)  
2. Solder **D1** LED — **polarity!**  
3. Solder **C1, C2** (0.1 uF)  
4. Solder **U1 AMS1117** (SOT-223)  
5. Solder **Test** button and **1.5 V \| 3 V** switch  
6. Solder **CR2032** holder  
7. Insert battery → check **LED TEST** and continuity  

## Links

| Item | Where |
| --- | --- |
| Ukrainian README | [README.uk.md](README.uk.md) |
| Hardware overview | [docs/01-hardware-overview.md](docs/01-hardware-overview.md) |
| Assembly | [docs/02-getting-started.md](docs/02-getting-started.md) |
| How to use | [docs/03-usage.md](docs/03-usage.md) |
| Troubleshooting | [docs/04-troubleshooting.md](docs/04-troubleshooting.md) |
| Website | [softeralab.com](https://www.softeralab.com/) |
| Soldering course | [course page](https://www.softeralab.com/course-basic-soldering/) |
| Contact | [Contacts](https://www.softeralab.com/our-contacts/) · support@softeralab.com |
| Instagram | [instagram.com/softeralab](https://www.instagram.com/softeralab/) |
| YouTube | [youtube.com/@SofteraLab](https://www.youtube.com/@SofteraLab) |

## Copyright

© Softera Lab. All rights reserved.

Public materials may be viewed. You may not copy, manufacture, redistribute, or commercially use the board design without written permission from Softera Lab.
