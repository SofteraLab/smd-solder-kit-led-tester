<p align="center">
  <a href="https://www.softeralab.com/">
    <img src="docs/assets/images/uk/logo.png" alt="Softera Lab" width="96">
  </a>
</p>

<h1 align="center">LED & BAT Tester · SK-15</h1>

<p align="center"><strong>Набір Softera Lab — тестер світлодіодів і батарейки CR2032</strong></p>

<p align="center">
  <a href="README.md"><img alt="EN" src="https://img.shields.io/badge/EN-README.md-F97316?style=flat-square"></a>
  <a href="https://www.softeralab.com/"><img alt="Сайт" src="https://img.shields.io/badge/softeralab.com-09090B?style=flat-square&labelColor=18181B"></a>
  <a href="https://www.instagram.com/softeralab/"><img alt="Instagram" src="https://img.shields.io/badge/Instagram-09090B?style=flat-square&labelColor=18181B"></a>
  <a href="https://www.youtube.com/@SofteraLab"><img alt="YouTube" src="https://img.shields.io/badge/YouTube-09090B?style=flat-square&labelColor=18181B"></a>
  <img alt="CR2032" src="https://img.shields.io/badge/CR2032-3V-09090B?style=flat-square&labelColor=F97316">
</p>

<p align="center"><strong>Мови:</strong> <a href="README.md">English</a> · Українська (ця сторінка)</p>

<p align="center">
  <img src="docs/assets/images/uk/banner.jpg" alt="LED & BAT Tester" width="720">
</p>

Навчальний набір, який після збірки стає інструментом: перевірка LED, батарейки CR2032 і прозвонка дротів. Сторінка для покупця та учасників курсу пайки.

Це **не open-source проєкт**. Виробничі файли публічно не викладаються.

> © Softera Lab. All rights reserved. Копіювання плати без письмового дозволу заборонене.

## Як працює

<p align="center">
  <img src="docs/assets/images/uk/how-it-works.jpg" alt="Блоки схеми" width="720">
</p>

1. **Батарейка CR2032 3V** — джерело живлення  
2. **AMS1117 LDO** — стабільні **1.5 V**  
3. **Перемикач 1.5 \| 3V** — напруга для LED TEST  
4. **Три режими** — LED TEST · прозвонка · кнопка + LED  

## Про набір

**Solder-Kit-SMD-Led-Tester-SK15** — двостороння плата [Softera Lab](https://www.softeralab.com/).

| Зона | Що є |
| --- | --- |
| **BAT TEST** | R1, R2, D1, кнопка Test, контакти 3V +/- |
| **LED TEST** | Площадки THT **3 mm / 5 mm** і SMD **0402, 0603, 0805, 1206** (полярність +) |
| **Живлення** | Тримач CR2032, AMS1117-1.5, перемикач 1.5 V \| 3 V |
| **Прозвонка** | Площадки TEST на другій стороні |
| **Бонус** | Лінійка 0–3 cm на краю плати |

Мікроконтролера немає.

<p align="center">
  <img src="docs/assets/images/uk/board-overview.jpg" alt="Огляд плати" width="720">
</p>

<p align="center">
  <img src="docs/assets/images/uk/board-back.jpg" alt="Друга сторона — LDO і прозвонка" width="720">
</p>

## Характеристики

| Параметр | Значення |
| --- | --- |
| Product | LED & BAT Tester · SK-15 |
| Повна назва | Solder-Kit-SMD-Led-Tester-SK15 |
| Живлення | CR2032, 3 V |
| Стабілізатор | AMS1117-1.5 → 1.5 V |
| Напруга LED TEST | Перемикач **1.5 V \| 3 V** |
| Площадки LED | 3 mm, 5 mm, 0402, 0603, 0805, 1206 |
| Режими | LED TEST, прозвонка, кнопка + LED |
| МК | Немає |

## Комплектація та номінали

<p align="center">
  <img src="docs/assets/images/uk/kit-contents.jpg" alt="Комплектація" width="720">
</p>

1. **R1, R2, R3** — 220 Ω (код 221)  
2. **D1** — LED  
3. **C1, C2** — 0.1 µF (100 nF), 0805  
4. **U1** — AMS1117-1.5, LDO, SOT-223  
5. Тримач **CR2032 3V**  
6. Перемикач **1.5V \| 3V**  
7. Кнопка **Test**  
8. Площадки **LED TEST** — 3 mm, 5 mm, 0402, 0603, 0805, 1206  

Корпуси на шовкографії звіряйте з карткою комплектації вашої ревізії.

## Навчальні схеми

### Кнопка + LED + батарейка

<p align="center">
  <img src="docs/assets/images/uk/schematic-button-led.jpg" alt="Схема кнопки" width="720">
</p>

Натиснув кнопку — коло замкнулось — LED світиться. Відпустив — гасне.  
`I = (3V − Vf) / 220Ω`

### Прозвонка дротів

<p align="center">
  <img src="docs/assets/images/uk/schematic-continuity.jpg" alt="Схема прозвонки" width="720">
</p>

Торкніться кінців дроту до площадок **TEST**. Цілий дріт — LED світиться. Обрив — не світиться.

### LDO AMS1117 — 1.5 V

<p align="center">
  <img src="docs/assets/images/uk/schematic-ldo.jpg" alt="Схема LDO" width="720">
</p>

Лінійний стабілізатор знижує **3V → 1.5V** для чутливих LED (з C1 / C2 0.1 µF).

## Збірка коротко

Повний порядок: [docs/02-getting-started.md](docs/02-getting-started.md).

<p align="center">
  <img src="docs/assets/images/uk/assembly-order.jpg" alt="Порядок збірки" width="720">
</p>

1. Припаяй **R1, R2, R3** (220 Ω)  
2. Припаяй **D1** (LED) — **полярність!**  
3. Припаяй **C1, C2** (0.1 µF)  
4. Припаяй **U1 AMS1117** (SOT-223)  
5. Припаяй кнопку **Test** і перемикач **1.5V\|3V**  
6. Припаяй тримач **CR2032**  
7. Встав батарейку → перевір **LED TEST** і прозвонку  

## Посилання

| Матеріал | Де |
| --- | --- |
| English README | [README.md](README.md) |
| Огляд плати | [docs/01-hardware-overview.md](docs/01-hardware-overview.md) |
| Збірка | [docs/02-getting-started.md](docs/02-getting-started.md) |
| Користування | [docs/03-usage.md](docs/03-usage.md) |
| Несправності | [docs/04-troubleshooting.md](docs/04-troubleshooting.md) |
| Сайт | [softeralab.com](https://www.softeralab.com/) |
| Курс пайки | [сторінка курсу](https://www.softeralab.com/course-basic-soldering/) |
| Контакти | [Контакти](https://www.softeralab.com/our-contacts/) · support@softeralab.com |
| Instagram | [instagram.com/softeralab](https://www.instagram.com/softeralab/) |
| YouTube | [youtube.com/@SofteraLab](https://www.youtube.com/@SofteraLab) |

## Авторське право

© Softera Lab. All rights reserved.

Публічні матеріали можна переглядати. Копіювати чи виготовляти плату без письмового дозволу Softera Lab заборонено.
