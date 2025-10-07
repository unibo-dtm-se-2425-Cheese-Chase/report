---
title: User guide
has_children: false
nav_order: 10
---

# User Guide

This section explains how to use *CheeseChase* from the player’s point of view, assuming the game has already been installed on the computer.  
The game is designed to be simple and requires only a keyboard to play.

---

## Starting the game

Once the package is installed, open a terminal and run: python -m CheeseChase
This command launches the game’s main module and opens the game window.  
No extra configuration or setup is required as the game starts immediately.

![Starting the game](/pictures/Starting_the_game_.jpg)

---

## Controls

The game is controlled entirely with the keyboard:

- Arrow keys: Move Jerry (the mouse) up, down, left, or right through the maze.  
- Spacebar: Pause or resume the game. When paused, a clear “Pause” message appears on the screen.

![Game Pause](/pictures/Game_Pause_.jpg)

---

## Gameplay

The goal is to help Jerry collect all the cheese pieces in the maze while avoiding the cats.

- Regular cheese increases the score.  
- Special cheese makes the cats vulnerable for a short time, allowing Jerry to chase them away and earn extra points.  
- If a cat catches Jerry while it is not vulnerable, Jerry loses one life.  
- The player starts with a limited number of lives, shown at the bottom of the screen.  
- The game ends in victory if all cheese pieces are collected or all cats are chased away.  
- The game ends in defeat if Jerry loses all lives.

![Game Play](/pictures/Game_Play_.jpg)

---

## Display and interface

The main game window shows:

- The maze, where Jerry and the cats move.  
- The score and level at the top of the screen.  
- The remaining lives as small mouse icons at the bottom.  
- Additional on-screen messages (e.g., “Ready”, “Pause”, “Game Over”, “Victory”) to guide the player.

![Display and user interface](/pictures/Display_and_userinterface_.jpg)

---

## Ending and restarting

When the game ends, a message will appear showing either Victory or Game Over.  
To play again, simply restart the program by running:  python -m CheeseChase

![The end](/pictures/The_end_.jpg)
