# 🗡️ CS50 — Legend of Zelda  

[![LÖVE2D](https://img.shields.io/badge/Engine-L%C3%96VE2D-informational)](https://love2d.org/)
[![Language](https://img.shields.io/badge/Language-Lua-blue)](https://www.lua.org/)
[![Course](https://img.shields.io/badge/Course-CS50G-red)](https://cs50.harvard.edu/games/)
[![License](https://img.shields.io/badge/License-MIT-green)](LICENSE)

**Course:** [CS50's Introduction to Game Development](https://cs50.harvard.edu/games/)  
**Assignment:** Legend of Zelda  
**Engine / Language:** LÖVE2D (Lua)  

---

## 📋 Project Overview  

This repository contains my implementation of the **Legend of Zelda** assignment from CS50's Introduction to Game Development.  

🕹️ Inspired by the NES classic, this project enhances the dungeon-crawling adventure with **hearts, pots, and throwable weapons**, expanding gameplay depth and survival mechanics.  

📺 You can also watch my gameplay demo on [YouTube](https://youtu.be/2jVrMHtXrbk?si=89M16LnBJWaZZ5Mi).

---

### What I Implemented  

- ✔️ **Heart Drops** — Enemies sometimes drop **hearts** on defeat. Picking one up restores **a full heart** without exceeding the health cap.  
- ✔️ **Pot Objects** — Randomly spawned **pots** in the dungeon that the player can:  
  - Pick up (changes animation to carrying state).  
  - Cannot swing a sword while carrying.  
- ✔️ **Pot Throwing Mechanic** — While carrying:  
  - Player can **throw the pot** in the direction they face.  
  - Pot travels up to **4 tiles** or until it collides with a wall or enemy.  
  - On hitting an enemy → deals **1 damage** and disappears.  
  - On hitting a wall → disappears.  

---

## 🎬 Gameplay Preview  

![Gameplay Preview](docs/gameplay.gif)  

---

## 🚀 How to Run  

1. Install [LÖVE2D](https://love2d.org/).  

2. Download and unzip the CS50 Zelda distro or clone this repository:  

   ```bash
   git clone https://github.com/huzaifa-gamedev/cs50-legend-of-zelda.git
   cd cs50-legend-of-zelda
   ```  

3. Run the game:  

   ```bash
   love .
   ```  

---

## 🎯 Controls  

- **Arrow Keys (↑ ↓ ← →)** — Move Link.  
- **Spacebar** — Swing sword (if not carrying a pot).  
- **Enter/Return** — Pick up pot (when facing one).  
- **Enter/Return (while carrying)** — Throw pot.  
- **Escape** — Quit game.  

---

## 🧠 Notes on Implementation  

- **Hearts:** Implemented as `GameObject` with `onConsume` callback. Added healing logic with cap at 6 health (3 hearts).  
- **Pot Pickup:** Added **PlayerCarryingPotState** that locks sword usage and updates animations.  
- **Pot Throwing:** Extended `GameObject` with **projectile behavior** using `dx`, `dy`, and max distance logic.  
- **Collision Handling:** Pots interact with **walls** and **enemies**, disappearing or damaging appropriately.  
- **Integration:** Modified `Dungeon`, `Player`, and `GameObject` classes to support new mechanics smoothly.  

---

## ✨ Credits  

- Original skeleton code & assets: CS50's Introduction to Game Development (Harvard). Licensed under [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/).  

---

## 📄 License  

- This implementation: © 2025 Muhammad Huzaifa Karim. Licensed under the [MIT License](LICENSE).  

For more details, see [ATTRIBUTION.md](ATTRIBUTION.md).  

---

## ✍️ Author  

**Muhammad Huzaifa Karim**  
[GitHub Profile](https://github.com/huzaifakarim1)  

---

## 📬 Contact  

For ideas, feedback, or collaboration, feel free to reach out via [GitHub](https://github.com/huzaifakarim1).  

---

© 2025 Muhammad Huzaifa Karim. All rights reserved.  
