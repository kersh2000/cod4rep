# Game Design Document (GDD)

## Overview
This document serves as the blueprint for the COD4: Modern Warfare replica game project, outlining all aspects of game design, including core gameplay mechanics, level design, AI behavior, and features. The game will be developed using **Unreal Engine 5** with **C++**, and will support both **PC (keyboard/mouse)** and **Xbox One controllers**.

### References:
- [Core Gameplay Mechanics](./core_gameplay_mechanics.md)
- [Game Features](./game_features.md)
- [Technical Requirements](./technical_requirements.md)
- [Map Layout Sketches](./assets/map_sketches)

---

## 1. Game Overview

The game replicates key aspects of *Call of Duty 4: Modern Warfare*, focusing on multiplayer map design and AI-controlled enemy bots. The project will aim to recreate the core gameplay mechanics of the original game, including movement, shooting, health regeneration, perks, and killstreaks. The game will feature a first-person perspective, dynamic AI, and single-player vs bots as the main gameplay mode.

### Game Modes:
- **Team Deathmatch (vs AI Bots)**: Players engage in a deathmatch against AI-controlled bots with predefined score limits.
- **Free-for-All (vs AI Bots)**: Players compete individually against AI bots.

### Game Flow:
1. Players will spawn in random locations on the map.
2. The objective is to achieve the highest number of kills, earning points toward killstreak rewards (UAV, Airstrike, Helicopter).
3. AI bots will patrol the map, engage in combat, and respawn after being killed.

---

## 2. Core Gameplay Mechanics

The game will follow the core gameplay mechanics outlined in the [Core Gameplay Mechanics](./core_gameplay_mechanics.md) document. Key mechanics include movement, shooting, health regeneration, and basic AI behavior.

### Movement:
- **Keyboard/Mouse**: WASD for movement, Shift to sprint, etc.
- **Xbox One Controller**: Left thumbstick for movement, Left thumbstick button (L3) to sprint, etc.
  
### Shooting and Weapon Mechanics:
- Players can aim down sights, fire weapons, throw grenades, and perform melee attacks.
- Both primary and secondary weapons can be equipped, with attachments like silencers or scopes.

---

## 3. Game Features

The game features are based on the classic COD4 gameplay elements such as perks, killstreaks, and custom loadouts. Detailed feature descriptions are available in the [Game Features](./game_features.md) document.

### Perks:
- Players can choose from three perk categories (Blue, Red, Yellow) that enhance gameplay.
- Perks like **Stopping Power**, **Sleight of Hand**, and **Last Stand** will be implemented to allow players to customize their playstyle.

### Killstreak Rewards:
- **UAV (3 kills)**: Reveals enemy positions on the minimap.
- **Airstrike (5 kills)**: Calls an airstrike to a target location.
- **Helicopter (7 kills)**: Summons a helicopter that patrols and kills enemies.

### Custom Loadouts:
- Players can select primary and secondary weapons, grenades, and perks before each match.
- Weapons can include assault rifles, SMGs, sniper rifles, etc.

---

## 4. Level Design

### Overview:
The map design will replicate the simple, iconic layouts of COD4 multiplayer maps with a focus on balanced combat zones, open areas, and choke points. One key map will be designed for this project.

### Map Features:
- **Multiple Levels**: Include both ground-level and elevated platforms for players to navigate.
- **Cover Points**: Walls, crates, and vehicles will be scattered throughout the map to provide cover.
- **Open Areas**: Large areas for long-range combat (sniper-friendly).
- **Choke Points**: Narrow corridors and doorways to encourage close-quarter combat.

### Map Layout Sketches:
We will design and implement one multiplayer map, starting with a rough 2D sketch and translating it into a 3D environment. The map will include:

- **Spawn Points**: Designated areas for player and bot respawns.
- **Combat Zones**: Areas where the majority of the action will take place.
- **Choke Points**: High-traffic areas designed for close-quarters combat.
  
### References:
- [Map Sketches](./assets/map_sketches): Folder containing 2D map layout sketches and concept designs.

### Sketch Example:
![Map Layout Example](./assets/map_sketches/map_concept1.png)

- This sketch shows the rough layout of the primary map, which includes open areas for long-range encounters, a central building for close-quarters combat, and elevated areas for snipers.

---

## 5. AI Design

### AI Behavior:
- Bots will patrol the map and engage players when they come within line of sight.
- Bots will use basic cover-seeking behavior and throw grenades.
- AI will prioritize certain objectives, such as defending areas or chasing after players.

### AI Technical Design:
- Bots will navigate the map using **Unreal Engine's NavMesh** system.
- Bot decision-making will be handled using **Behavior Trees**.
- The bots will have different difficulty levels, adjusting accuracy and aggressiveness.

---

## 6. User Interface (UI)

### Heads-Up Display (HUD):
- **Health Bar**: Shows the player’s current health and will flash when health is low.
- **Ammo Counter**: Displays the current ammo count for the player’s weapon.
- **Killstreak Counter**: Displays the number of kills the player has accumulated and shows killstreak rewards when earned.

### Minimap:
- The minimap will display player and bot positions, along with key objectives (e.g., airstrikes, spawn points).

### Menus:
- A simple start menu that includes options for selecting game modes, loadouts, and exiting the game.
- In-game menu to pause, view stats, and change loadouts during matches.

---

## 7. Technical Requirements

### Software & Tools:
- Unreal Engine 5 with C++
- Visual Studio 2022 for C++ development
- Blender for 3D modeling
- GIMP for texture creation
- Git for version control

Detailed setup can be found in the [Technical Requirements](./technical_requirements.md) document.

### Hardware Requirements:
- **Minimum**: CPU: Intel i5, GPU: GTX 970 or equivalent, RAM: 8GB
- **Recommended**: CPU: Intel i7, GPU: RTX 2060 or equivalent, RAM: 16GB

---

## 8. Art and Assets

### 3D Models:
- **Environment Models**: Low-poly walls, crates, buildings, and vehicles created using Blender. These will be textured using simple materials with a mix of baked textures for optimized performance.
  
### Textures:
- **Weapons and Environment Textures**: Created using GIMP, applied to 3D models for walls, floors, and objects. The game will use realistic, yet performance-friendly textures, inspired by the industrial military theme of COD4.

### Animation:
- **Player Animations**: Basic animations for running, shooting, reloading, and melee.
- **Bot Animations**: Animations for idle, patrol, firing, and death.

---

## 9. Sound Design

### Sound Effects:
- **Gunshots**: Realistic weapon firing sounds.
- **Explosions**: Grenades, airstrikes, and vehicle explosions.
- **Footsteps**: Different sounds for walking/running on various surfaces (e.g., concrete, grass).
  
### Music:
- Minimal background music to keep the atmosphere intense and immersive.
  
### Tools:
- **Audacity** for editing and formatting sound effects.

---

## 10. Milestones

### Milestone 1: Core Mechanics Prototype (3-4 Weeks)
- Basic player movement, shooting, and respawn system.

### Milestone 2: Map Design and Bot AI (5-7 Weeks)
- Completion of the primary multiplayer map.
- Implementation of bot AI, including patrol, attack, and respawn behavior.

### Milestone 3: Full Gameplay Loop and Polishing (8-12 Weeks)
- Final implementation of perks, killstreaks, and UI.
- Polishing animations, sound, and visual effects.

---

## 11. Version Control & Collaboration

### Git for Version Control:
- The project will use Git to track all changes and manage versions.
- The repository will be hosted on GitHub with regular commits after each feature implementation.

- **Repository Link**: [GitHub Repository](https://github.com/your-repository-url)

---

## 12. References

- **[Core Gameplay Mechanics](./core_gameplay_mechanics.md)**
- **[Game Features](./game_features.md)**
- **[Technical Requirements](./technical_requirements.md)**
- **[Map Layout Sketches](./assets/map_sketches)**
- **[Git Repository](https://github.com/your-repository-url)**

---

