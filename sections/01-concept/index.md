---
title: Concept
has_children: false
nav_order: 2
---

# Concept

CheeseChase is a desktop application with a graphical user interface.  
It offers interactive graphics and animations, making it easy and enjoyable to play.  
The game works as a real-time system, where the main loop updates the game logic and visuals about 30 times per second, ensuring smooth and responsive gameplay.

From a use case perspective, the players are casual gamers who use a desktop or laptop computer.  
They interact with the game continuously during each session, since it is a fast-paced, arcade-style experience.  
The main way of interacting is through the keyboard:  
- The arrow keys move Jerry (the mouse) up, down, left, or right through the maze.  
- The spacebar lets the player pause or resume the game at any time.

The game does not store any permanent data.  
Information such as the current level, the score, and the number of lives is kept only in memory during gameplay.  
Once the game ends or is restarted, all values are reset. No accounts or external storage are required.

There are two main roles in the system:  
- Player: controls Jerry and tries to level up by collecting cheese and avoiding cats.  
- System: runs the background processes: animating characters, checking collisions, updating the score, and enforcing the game rules.
 




