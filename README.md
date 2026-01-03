# 🚦 Green Means Go | Traffic Strategy Game

A strategic card-based traffic management game where you optimize vehicle flow to achieve target scores. Built with vanilla HTML, CSS, and JavaScript.

![Game Banner](https://img.shields.io/badge/Status-Active-success) ![License](https://img.shields.io/badge/License-MIT-blue)

## 🎮 Game Overview

**Green Means Go** is a turn-based strategy game where you manage traffic flow by strategically placing different types of vehicles and traffic control units. Your goal is to maximize your daily score by creating efficient traffic sequences while avoiding congestion penalties.

## 🎯 How to Play

### Objective
- **Reach the target score** each day by strategically placing 5 units in the lane
- **Day 1 Target**: 80 points
- Each subsequent day increases the target by 70 points
- Fail to meet the target = Game Over!

### Game Mechanics

#### 📋 Available Units

| Unit | Type | Base Value | Description |
|------|------|------------|-------------|
| **Sedan** 🚗 | Base | 15 pts | Stable, reliable flow |
| **Transit** 🚌 | Base | 25 pts | High value but risky (congestion penalty) |
| **Signal** 💡 | Multiplier | - | Doubles the next 2 units (2 charges) |
| **Enforcer** 🛡️ | Stabilizer | - | Blocks the next penalty |
| **Upgrade** ⏱️ | Extender | - | Adds +1 charge to the next Signal |

#### 🎲 Gameplay Flow

1. **Select 5 units** from your hand to fill the lane
2. **Click "Execute Protocol"** to resolve the traffic flow
3. **Watch the scoring** as each unit is processed sequentially
4. **Meet the target** to advance to the next day

### 🧮 Scoring Rules

#### Base Scoring
- **Sedan**: +15 points (always stable)
- **Transit**: +25 points (high reward, high risk)

#### Special Mechanics

**🚌 Bus Congestion Penalty**
- When two **Transit** units are placed back-to-back:
  - The second Transit suffers a **-15 penalty** (25 - 15 = 10 points)
  - Can be blocked by placing an **Enforcer** before the buses

**💡 Signal Multiplier**
- Doubles the score of the next **2 base units**
- Works on the **net value** (after penalties are applied)
- Example: Signal → Transit (25×2=50) → Transit (10×2=20) = 70 pts

**⏱️ Upgrade Extender**
- Extends the **next Signal's charges** by +1
- Example: Upgrade → Signal → 3 units get doubled instead of 2

**🛡️ Enforcer Protection**
- Blocks the **next congestion penalty**
- Consumed after blocking one penalty

#### 🌟 Strategy Bonus
- **Diversity Bonus**: Use 4 or more different unit types = **+25 points**

## 🎨 Features

- **Modern UI Design**: Sleek dark theme with neon accents
- **Sound Effects**: Procedural audio feedback for all actions
- **Smooth Animations**: Visual feedback for card placement and scoring
- **Progressive Difficulty**: Increasing targets each day
- **Strategic Depth**: Multiple viable strategies and combos

## 🚀 Getting Started

### Prerequisites
- Any modern web browser (Chrome, Firefox, Safari, Edge)
- No installation required!

### Running the Game

1. **Clone or download** this repository
2. **Open `index.html`** in your web browser
3. **Start playing!** No build process needed

```bash
# Option 1: Open directly
open index.html

# Option 2: Use a local server (optional)
python3 -m http.server 8000
# Then visit: http://localhost:8000
```

## 🛠️ Technical Details

### Technologies Used
- **HTML5**: Semantic structure
- **CSS3**: Modern styling with CSS variables, gradients, and animations
- **Vanilla JavaScript**: No frameworks, pure ES6+
- **Lucide Icons**: Beautiful open-source icon library
- **Web Audio API**: Procedural sound generation

### File Structure
```
Game/
├── index.html          # Main game file (HTML + CSS + JS)
├── how_to_play.html    # Dedicated instruction page
└── README.md           # This file
```

### Browser Compatibility
- ✅ Chrome/Edge 90+
- ✅ Firefox 88+
- ✅ Safari 14+
- ✅ Opera 76+

## 🎓 Strategy Tips

### Beginner Strategies
1. **Safe Play**: Use mostly Sedans with occasional Transits
2. **Signal Boost**: Place Signals before high-value units
3. **Avoid Penalties**: Don't place Transits back-to-back without protection

### Advanced Strategies
1. **Enforcer Combo**: Enforcer → Transit → Transit = 50 points (no penalty!)
2. **Extended Signal**: Upgrade → Signal → 3 Transits = massive points
3. **Diversity Bonus**: Mix 4+ different units for +25 bonus
4. **Calculated Risk**: Use back-to-back Transits when you can afford the penalty

### Example High-Score Combo
```
Upgrade → Signal → Transit → Transit → Sedan
= 0 + 0 + 50 + 20 + 30 + 25 (diversity) = 125 points!
```

## 🐛 Known Issues

None currently! If you find a bug, please report it.

## 📝 Version History

### v1.2 (Current)
- ✅ Added dedicated "How to Play" page
- ✅ Integrated help link in main menu
- ✅ Optimized vehicle flow logic

### v1.1
- ✅ Fixed Timer/Upgrade logic bug
- ✅ Fixed bus congestion penalty calculation
- ✅ Improved police protection feedback
- ✅ Added lightbulb icon to Signal card
- ✅ Enhanced user feedback messages

### v1.0
- Initial release
- Core game mechanics
- Sound effects and animations

## 🤝 Contributing

This is a personal project, but suggestions and improvements are welcome!

## 📄 License

MIT License - Feel free to use and modify for your own projects.

## 🎮 Python Version

A command-line Python version (`game.py`) is also included for reference. Run it with:

```bash
python3 game.py
```

## 👨‍💻 Author

Created with ❤️ as a strategic card game experiment.

---

**Enjoy the game and may your traffic always flow green!** 🚦💚
