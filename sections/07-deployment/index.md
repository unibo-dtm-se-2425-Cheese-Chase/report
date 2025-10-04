---
title: Deployment
has_children: false
nav_order: 8
---

# Deployment

This section explains the operations needed to install and run CheeseChase on the user’s machine.  Since the project is a standalone desktop game built with Python, deployment is simple and requires no server-side setup.

---

## User installation

To run the game, users need a Python environment (version 3.9 or later) installed on their computer.  
The software is distributed as a Python package on PyPI under the name `CheeseChase`.

First, update `pip` to the latest version by running python -m pip install --upgrade pip.

Then install the game with pip install CheeseChase.

These commands automatically install the required dependencies, such as Pygame and NumPy.

Once the installation is complete, the game can be started directly from the command line by running python -m CheeseChase.


No further configuration is required: the game runs immediately after installation, with no need to create configuration files or set environment variables.  All game data (scores, levels, and lives) is stored only in memory during a play session and resets when the game restarts.

CheeseChase works on Windows, macOS, and Linux, as long as the machine can run Python and Pygame.

---

## Server-side installation

CheeseChase does not require any server-side installation.  It runs entirely on the user’s local machine and needs no external servers, databases, or middleware.  The game state (Jerry’s position, cat status, and collected cheese) is maintained in memory during execution.

This architecture keeps deployment lightweight and accessible.  Users only need a modern Python environment and basic hardware capable of running Pygame applications.
