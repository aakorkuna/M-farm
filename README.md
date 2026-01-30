# M-farm — Space Farming Simulation Game (C++)

[Українська версія](README.ua.md)

**M-farm** is a space-themed farming simulation game developed in **C++** as a portfolio project.  
The project demonstrates core game development concepts such as **resource management**, **progression systems**, **state persistence (save/load)**, and **mode-based gameplay logic**.

The game challenges the player to build and manage a farm in space under environmental constraints while working toward a clear win condition.

---

## 🎯 Project Goal

The main objective of the game is to **earn 2000 coins** by:
- efficiently managing resources,
- upgrading infrastructure,
- unlocking higher-tier crops,
- balancing environmental parameters (heat and oxygen).

---

## 🧠 Core Gameplay Systems

### 🌱 Farming & Crop Progression
- Crops can only be grown on **dedicated farming plots**.
- Farming plots must be purchased from the in-game shop.
- Each crop has **environmental requirements**:
  - minimum heat level
  - minimum oxygen level
- More advanced crops generate **higher income**, encouraging long-term planning.

---

### ⛏️ Resource System
The game features two mineable resources:
- **Iron**
- **Coal**

Key characteristics:
- Resources **spawn randomly** across the map.
- The player must actively mine them.
- Resources are essential for building infrastructure, especially heat generators.

This system introduces **map exploration** and **resource prioritization** into the gameplay loop.

---

### 🔥 Heat Management System
- Heat is a global environmental parameter.
- Heat level is increased by constructing **heat generators**.
- Heat generators require **iron and coal** to be built.
- Higher heat levels unlock access to more profitable crops.

This creates a **dependency chain** between mining, construction, and farming.

---

### 🌳 Oxygen Management System
- The player can purchase and place **grass tiles**.
- **Trees** can only be planted on grass tiles.
- Trees increase the global oxygen level.
- Oxygen is required to unlock higher-tier crops.

This system encourages **land planning** and adds another strategic layer to progression.

---

### 🛒 Builder Mode & In-Game Shop
- All construction and placement actions are restricted to **Builder Mode**.
- While in Builder Mode, a **shop panel opens on the right side** of the screen.
- The player can purchase:
  - farming plots
  - trees
  - heat generators
  - other game elements
- All tiles, plants, and buildings **can only be placed in Builder Mode**.

This mode-based design helps separate **building logic** from **interaction logic**.

---

### 🌾 Harvest Mode
- To collect crops, the player switches to a **Harvest Mode** using a sickle.
- In this mode, all grown crops can be harvested.
- Harvested crops generate in-game currency.

---

### ⏭️ Day Progression System
- After harvesting, the player presses the **“Next Day”** button.
- The game advances to the next in-game day.
- All planted crops grow automatically.

This creates a clear and repeatable **gameplay loop**:
> build → plant → harvest → advance day → upgrade

---

### 💾 Save & Load System
- The game includes a **persistent save system**.
- Player progress is stored in a `Save.txt` file.
- On game launch, the player can **continue from the last saved state**.

This demonstrates **state serialization** and continuity between sessions.

---

## 🛠️ Technical Details

- **Language:** C++
- **Build system:** Makefile
- **Platform:** Windows
- **Assets:** `resources/`
- **Save file:** `Save.txt`
- **Architecture:** modular design using multiple header/source files

---

## ▶️ Running the Project

### Run prebuilt version
```bash
main.exe
