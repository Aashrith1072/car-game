# 🚗 Car Game

A Python turtle graphics game where you navigate a turtle across a busy road while dodging oncoming cars. Each successful crossing increases the level and makes the cars faster!

---

## 🎮 Gameplay

- Control a turtle starting at the bottom of the screen
- Press the **Up Arrow** to move forward
- Dodge the randomly spawning cars coming from the right side
- Reach the top of the screen to complete a level
- Cars get faster with every level you clear
- One collision = **Game Over**

---

## 📁 Project Structure
car-game/
│
├── main.py          # Main game loop, collision detection, level progression

├── player.py        # Player (turtle) movement and finish line detection

├── car_manager.py   # Car spawning, movement, and speed scaling

└── scoreboard.py    # Level display and Game Over screen

---

## 🛠️ How to Run

**Requirements:** Python 3.x — no external libraries needed (turtle is built into Python)

```bash
git clone https://github.com/Aashrith1072/car-game.git
cd car-game
python main.py
```

---

## 🧠 Concepts Used

- Object-Oriented Programming (classes and inheritance with `Turtle`)
- Python `turtle` graphics module for rendering
- Real-time game loop with `time.sleep()` and `screen.tracer(0)`
- Collision detection using `.distance()` method
- Randomized car spawning with probability control (`randint`)
- Progressive difficulty — car speed increases each level

---

## 🗺️ How It Works

| Component | Responsibility |
|---|---|
| `Player` | Moves up on keypress, detects finish line crossing |
| `CarManager` | Spawns random colored cars, moves them left, speeds up on level up |
| `Scoreboard` | Displays current level, shows GAME OVER on collision |
| `main.py` | Ties everything together — game loop, event listening, collision logic |

---

## 📸 Preview

> 600×600 screen. Turtle starts at the bottom centre. Cars spawn from the right in random colors (red, orange, yellow, green, blue, purple) at random vertical positions. Level counter is shown in the top-left corner. Colliding with any car ends the game.

---

## 🐛 Bugs Fixed During Development

- `scoreboard.increase_level` was referenced without `()` — level never increased
- `Turtle("sSquare")` had a typo — cars rendered as arrows instead of rectangles
- `import car_manager` shadowed the `CarManager` instance variable

---

Built as part of the **100 Days of Code** — The Complete Python Pro Bootcamp.
