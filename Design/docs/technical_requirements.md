# Technical Requirements

This document outlines the software, tools, and technologies that will be used to build the COD4: Modern Warfare replica game. The chosen engine is **Unreal Engine 5** with **C++**, which provides a powerful framework for creating first-person shooters (FPS) with both keyboard/mouse and controller support.

## 1. Game Engine

### Unreal Engine 5
- **Why Unreal Engine?**: Unreal Engine is one of the most widely-used engines for creating high-fidelity FPS games. It provides powerful built-in tools for graphics, physics, AI, and networking, which are ideal for recreating the core mechanics of COD4: Modern Warfare.
- **Language**: Unreal Engine uses **C++** for scripting and gameplay programming, which offers precise control over performance and systems.
- **Version**: Use the latest stable version of Unreal Engine 5 (UE5) to ensure access to modern features and tools like Nanite (for rendering) and Lumen (for global illumination).

### Download & Installation
- Download Unreal Engine from the **Epic Games Launcher**: [https://www.unrealengine.com/en-US/download](https://www.unrealengine.com/en-US/download).
- Installation process: Follow the guided setup in the Epic Games Launcher to install Unreal Engine 5.

## 2. Programming Language

### C++
- **Why C++?**: C++ is the primary language used in Unreal Engine for game logic and mechanics. It allows for optimized performance and flexibility when implementing gameplay features like shooting, AI, health systems, and physics.
- **IDE**: Use **Visual Studio** as the primary integrated development environment (IDE) for C++ coding in Unreal Engine. Visual Studio has full support for Unreal Engine and provides debugging tools.

### Download & Installation
- Download **Visual Studio 2022**: [https://visualstudio.microsoft.com/](https://visualstudio.microsoft.com/).
- During installation, select the **Game Development with C++** workload, which includes Unreal Engine support.

## 3. 3D Modeling Software

### Blender (Free)
- **Why Blender?**: Blender is a free and open-source 3D modeling software, perfect for creating low-poly models, environments, and objects for the game. It also supports asset export in formats like `.FBX` that Unreal Engine natively imports.
- **Usage**: Use Blender to model multiplayer maps, weapons, and environmental objects.
- **Version**: Use the latest stable version of Blender (currently 3.x).

### Download & Installation
- Download Blender from the official website: [https://www.blender.org/download/](https://www.blender.org/download/).

## 4. Texturing and Material Creation

### GIMP (Free)
- **Why GIMP?**: GIMP is a free alternative to Photoshop and can be used to create textures for 3D models. It supports various formats (like PNG, JPEG, etc.) for creating textures to be applied in Unreal Engine.
- **Usage**: Create custom textures for weapons, walls, and environmental objects.
  
### Download & Installation
- Download GIMP: [https://www.gimp.org/downloads/](https://www.gimp.org/downloads/).

## 5. AI Systems

### Unreal Engine's Built-in AI (Behavior Trees, Navigation Mesh)
- **Why Built-in AI?**: Unreal Engine has a powerful AI system built in, which includes **Behavior Trees** for decision-making and **Navigation Meshes (NavMesh)** for pathfinding. These tools are sufficient for creating basic enemy bots that patrol, engage with players, and respawn.
- **Usage**: Implement bot AI using Behavior Trees for decision-making and NavMesh for movement and pathfinding.
  
## 6. Physics Engine

### Unreal Engine Physics System
- **Why Built-in Physics?**: Unreal Engine's physics system handles collision detection, projectile trajectories, and environmental interactions. It is highly optimized and ideal for implementing bullet mechanics, grenade physics, and player-environment interaction.
- **Usage**: Use the built-in physics engine for handling player collision, shooting mechanics, and environmental destruction (e.g., explosives).

## 7. Animation System

### Unreal Engine Animation System
- **Why Built-in Animation System?**: Unreal Engine supports skeletal animations, blend spaces, and animation blueprints, which are ideal for character and weapon animations like running, shooting, reloading, and idle animations.
- **Usage**: Use Unreal’s animation system to handle player movement, weapon handling, and AI animations.

## 8. Input Systems

### Unreal Engine Input System (PC and Xbox Controller)
- **Why Unreal's Input System?**: Unreal Engine’s input system supports both keyboard/mouse and controller inputs out of the box. It allows for easy mapping of controls for different input devices.
- **Usage**: Implement input handling for both PC (keyboard/mouse) and Xbox controllers.
- **Control Mapping**: Use Unreal Engine's Input Manager to map the actions (e.g., shooting, moving) to the respective keys/buttons for both PC and controller inputs.

## 9. Sound and Audio

### Free Audio Tools: Audacity
- **Why Audacity?**: Audacity is a free, open-source audio editing tool that can be used to create and edit sound effects (e.g., gunfire, explosions) for the game.
- **Usage**: Use Audacity to edit and format sound effects and dialogue, and import them into Unreal Engine.

### Download & Installation
- Download Audacity: [https://www.audacityteam.org/download/](https://www.audacityteam.org/download/).

## 10. Version Control

### Git and GitHub
- **Why Git?**: Version control is essential for tracking changes to your project, and Git is the most popular version control system. By using **GitHub**, you can store your project remotely and collaborate if needed.
- **Usage**: Use Git for tracking project progress, saving backups, and managing versions of your code and assets.
- **Git LFS**: Since Unreal Engine projects can contain large assets (3D models, textures, etc.), you’ll need **Git Large File Storage (LFS)** to manage large binary files.

### Download & Installation
- Install **Git**: [https://git-scm.com/downloads](https://git-scm.com/downloads).
- Sign up for **GitHub**: [https://github.com/](https://github.com/).
- Initialize your project with Git and push your repository to GitHub:
  ```bash
  git init
  git add .
  git commit -m "Initial commit"
  git remote add origin <your-repository-url>
  git push -u origin master
