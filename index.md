---
title: Home
layout: home
has_children: false
nav_order: 1
---

# Cheese-Chase

### Authors

- Francesca Folli - [frafo227295](https://github.com/frafo227295)
- Gaia Bellachioma - [gaia-bellachioma](https://github.com/gaia-bellachioma)

## Abstract

Cheese-Chase is a modern remake of the classic arcade game Pac-Man, reimagined in the world of Tom & Jerry. The player controls Jerry, represented in the code by the Mouse class, and must move through a maze collecting cheese while avoiding four cats. The project is built in Python with the Pygame library and follows the Model-View-Controller (MVC) pattern, which helps keep the game’s logic, graphics, and input separate and well organized.

The game features two types of collectables: regular cheese, which increase the player’s score, and special cheese, which changes how the cats behave. When the mouse eats a special cheese, the cats become “vulnerable” for a short time, shown by a change in their sprites. In this state, the mouse can chase them away for extra points. If the mouse collides with a cat that is not vulnerable, he loses a life. The player begins with 5 lives, and the game ends in defeat if the mouse runs out of lives.

Technically, the game aims to provide smooth and responsive gameplay. Pygame’s event system handles keyboard input, and the central GameController coordinates updates to characters, the maze, and the score each frame. Sprite animations are managed by classes such as MouseSprites and CatSprites, which update the mouse’s and the cats’ appearance based on their movement and state. The maze layout is stored in text files and created at runtime by the MazeSprites and NodeGroup classes, which also handle walls and valid movement paths.

The system is modular and easy to extend. Each game element is written as its own class, making it simple to add new features, extra levels, or different power-ups. Game constants and external files also make it easy to adjust settings without rewriting the core code. For players, the game remains straightforward: they control the mouse with the arrow keys and get immediate feedback when scoring points, eating a special cheese, or losing a life.

Therefore, Cheese-Chase combines a nostalgic concept with modern programming practices. It keeps the simple fun of Pac-Man while adding the playful theme of Tom & Jerry. At the same time, the project shows how object-oriented design, modular code, and a lightweight framework like Pygame can be used to recreate and update classic arcade gameplay.

## Disclaimer

During the preparation of this work, the authors used ChatGPT to support the integration of pre-existing code retrieved from GitHub with the original project code.

In particular, the tool was used to assist in adapting external implementations related to the maze structure and the collision handling between entities, ensuring that these elements were correctly aligned with the project’s architecture.

ChatGPT was also used to support the testing phase, helping refine test cases, clarify testing strategies, and improve the clarity and consistency of some sections of the written report.

All AI-assisted suggestions and reused code fragments were reviewed, adapted, and validated by the authors.

The authors take full responsibility for the final implementation and for the accuracy and completeness of this report.
