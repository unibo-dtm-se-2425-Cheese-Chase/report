---
title: Development
has_children: false
nav_order: 5
---

# Development

## DVCS Conventions

The project uses Git on GitHub as a distributed version control system.  
Development follows a simple but structured workflow.

The main branch always contains stable code.  

Commit messages follow the Conventional Commits style: `type(optional context): short description`.  For example: `feat(model): add MazeData loader`.  
This makes it easy to understand which part of the project a change affects and also supports automatic versioning and changelog generation during the release process.

Issues are used to track bugs, enhancements, and planned improvements, creating a clear backlog of work and improving collaboration.

This lightweight workflow was chosen because it balances clarity and speed, making it efficient even for a small development team.

---

## Implementation Details

Since CheeseChase is a local, single-player desktop game, many concerns typical of distributed systems are intentionally avoided to keep the project simple and fast:

- Network protocols: none are needed; all interactions happen locally on the user’s computer.  
- Data representation: the game state is stored as Python objects in memory, so serialization is not required.  
- Databases: not used. Information such as the score, lives, and character positions only exists during a play session and is kept in memory.  
- Authentication and authorization: not applicable, as there are no user accounts or online features.

Avoiding these elements keeps the game lightweight, fast, and easy to deploy.

---

## Technological Details

The project is developed in Python 3.12.4, chosen for its clear syntax, wide adoption, and suitability for rapid prototyping.

The main dependencies are:

- Pygame: provides multimedia functionality such as graphics rendering, keyboard input handling, sound effects, and sprite animation.  
- NumPy: simplifies loading and processing maze layouts, which are stored as text files and converted into efficient 2D arrays.

All sprites, fonts, and audio assets are stored locally with the game, making the project fully self-contained and requiring no external services or APIs.

This technology stack was selected because it ensures:

- Accessibility: Python and Pygame are easy to install and widely supported.  
- Performance: NumPy improves efficiency when managing maze data.  
- Portability: with all resources bundled locally, the game can run on any compatible desktop without additional setup.

The team follows the PEP 8 coding style for clarity and consistency.  
Using an IDE such as VS Code is recommended, as it provides automatic formatting, error checking, and integrated Git support to simplify development.

