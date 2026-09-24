---
id: troubleshooting
title: Troubleshooting
sidebar_position: 4
description: Dark LED, wrong polarity and continuity issues on SK-15.
---

<p className="brand-kicker">Fix</p>

# Troubleshooting

| Symptom | Check |
| --- | --- |
| Nothing works | CR2032 inserted, polarity + / −, fresh cell |
| BAT TEST LED dark when pressing Test | D1 polarity, R1/R2 joints, button orientation |
| LED TEST never lights | Switch 1.5 V \| 3 V position, LED polarity on pads, LED size matches footprint |
| Only some LED sizes work | Pads must match package; 0402 needs fine tip and little solder |
| Continuity always off | TEST pads clean, wire ends exposed, R3 / path on second side soldered |
| Continuity always on | Solder bridge between TEST pads |
| Board gets hot | Short near U1 or battery holder — remove cell immediately |

:::caution Battery
Do not leave a shorted board with a CR2032 installed. Remove the cell before rework.
:::

When asking for help, send: kit code **SK-15**, which mode fails, switch position, and a clear photo of both sides.
