# 👑 Queens Puzzel

[![GitHub Pages](https://img.shields.io/badge/demo-live-green)](https://sweco-nllars.github.io/QueensGame/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Een logische puzzel-app geïnspireerd door LinkedIn's Queens game. Train je logisch denkvermogen met verschillende moeilijkheidsniveaus!

## 🎮 [Speel Nu](https://sweco-nllars.github.io/QueensGame/)

![Queens Game Screenshot](docs/screenshot.png)

## 📜 Spelregels

**Doel:** Plaats precies één koningin (👑) in elke rij, kolom én gekleurd gebied.

| Regel | Beschrijving |
|-------|--------------|
| 🔲 Rijen | Elke rij mag maar 1 koningin bevatten |
| 🔳 Kolommen | Elke kolom mag maar 1 koningin bevatten |
| 🎨 Gebieden | Elk gekleurd gebied mag maar 1 koningin bevatten |
| ⚔️ Aanraken | Koninginnen mogen elkaar NIET raken (ook niet diagonaal) |

## 🎯 Bediening

| Actie | Resultaat |
|-------|-----------|
| Tik 1x | Plaats een ✕ (markering) |
| Tik 2x | Plaats een 👑 (koningin) |
| Tik 3x | Maak cel leeg |

## 🏆 Moeilijkheidsniveaus

| Niveau | Raster | Hints | Beschrijving |
|--------|--------|-------|--------------|
| 🌱 Beginner | 4×4 - 5×5 | 3 | Perfect om te leren |
| ⭐ Makkelijk | 5×5 - 6×6 | 2 | Basis strategieën |
| ⭐⭐ Gemiddeld | 6×6 - 7×7 | 1 | Logisch redeneren |
| ⭐⭐⭐ Moeilijk | 7×7 - 8×8 | 0 | Gevorderd |
| 👑 Expert | 8×8 - 9×9 | 0 | Uitdagend |
| 🏆 Meester | 9×9 - 10×10 | 0 | Voor echte puzzelaars |

## ✨ Features

- ✅ 6 moeilijkheidsniveaus (4×4 tot 10×10)
- ✅ Willekeurig gegenereerde puzzels
- ✅ Hint systeem voor beginners
- ✅ Undo functie
- ✅ Timer
- ✅ Statistieken & win-streaks
- ✅ Fout-highlighting
- ✅ Confetti animatie bij winst
- ✅ PWA - installeerbaar op telefoon
- ✅ Offline support
- ✅ Donker thema
- ✅ Responsive design

## 📱 Installeren op je Telefoon

### Als PWA (Aanbevolen)
1. Open [de app](https://sweco-nllars.github.io/QueensGame/) in Chrome
2. Tik op het menu (⋮) rechtsboven
3. Kies "Toevoegen aan startscherm" of "App installeren"
4. De app verschijnt als een normale app!

### Als Android APK
Zie [BUILD.md](BUILD.md) voor instructies om een APK te bouwen.

## 🛠️ Lokaal Draaien

```bash
# Clone de repository
git clone https://github.com/sweco-nllars/QueensGame.git
cd QueensGame

# Start een lokale server
python3 -m http.server 8080
# of
npx serve .

# Open in browser
open http://localhost:8080
```

## 💡 Tips & Strategieën

1. **Begin met kleine gebieden** - Als een gekleurd gebied maar 1 cel heeft, moet daar de koningin!
2. **Elimineer rijen/kolommen** - Als je een koningin plaatst, markeer alle cellen in die rij en kolom met ✕
3. **Check diagonalen** - Vergeet niet dat koninginnen ook diagonaal niet mogen raken
4. **Werk systematisch** - Begin bovenaan en werk naar beneden
5. **Gebruik hints** - In beginner/makkelijke niveaus krijg je hints om te leren

## 🔧 Technologie

- Pure HTML/CSS/JavaScript
- React 18 (via CDN)
- Geen build stap nodig
- PWA-ready
- LocalStorage voor statistieken

## 📁 Project Structuur

```
QueensGame/
├── index.html          # Hoofdapplicatie
├── manifest.json       # PWA configuratie
├── icons/
│   ├── icon-192.png    # App icoon (klein)
│   └── icon-512.png    # App icoon (groot)
├── README.md           # Dit bestand
├── BUILD.md            # APK build instructies
└── LICENSE             # MIT License
```

## 🤝 Bijdragen

Bijdragen zijn welkom! Open een issue of pull request.

## 📄 Licentie

MIT License - zie [LICENSE](LICENSE) bestand.

---

Gemaakt met ❤️ en 👑
