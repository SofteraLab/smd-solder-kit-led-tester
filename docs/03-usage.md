---
id: usage
title: How to use
sidebar_position: 3
description: LED TEST, continuity and button modes on SK-15.
---

<p className="brand-kicker">Use</p>

# How to use

Insert a good CR2032 with correct polarity. Then pick a mode.

## LED TEST

1. Set the switch to **1.5 V** or **3 V**.  
2. Place the LED on the matching pads (**3 mm / 5 mm** or SMD **0402…1206**).  
3. Observe **+** on the silkscreen.  
4. A good LED lights according to voltage and polarity.

Sensitive LEDs often prefer the **1.5 V** position (via AMS1117).

## Continuity (прозвонка)

![Continuity card](./assets/images/en/schematic-continuity.png)

1. Touch both ends of the wire to the **TEST** pads on the second side.  
2. Intact conductor → indicator LED on.  
3. Open wire → LED stays off.

## Button + LED (BAT TEST)

![Button card](./assets/images/en/schematic-button-led.png)

1. Press **Test**.  
2. Circuit closes → onboard LED lights.  
3. Release → LED goes out.  

Current through the LED is limited by **220 Ω**:  
`I = (3V − Vf) / 220Ω`.

## LDO note

![LDO card](./assets/images/en/schematic-ldo.png)

AMS1117-1.5 with **C1 / C2 0.1 µF** provides a stable **1.5 V** rail for the LED TEST path when the switch selects that mode.
