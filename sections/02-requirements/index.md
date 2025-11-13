---
title: Requirements
has_children: false
nav_order: 3
---

# Requirements
## User Stories

The main persona for this project is a casual gamer playing on a desktop or laptop computer for fun.  
Their primary goal is to control Jerry, collect cheese, avoid cats, and try to win the game.  
The system, on the other hand, must manage the background logic: cat behavior, collision detection, and game state updates.

The following user stories summarize the expected interactions:

- **US1**: As a player, I want to move Jerry using the keyboard so I can navigate the maze.  
- **US2**: As a player, I want to collect cheese to increase my score.  
- **US3**: As a player, I want to eat special cheese to temporarily scare cats and make them vulnerable.  
- **US4**: As a player, I want to avoid cats to prevent losing lives.  
- **US5**: As a system, I want to control the cats so they chase Jerry and react to special cheese.  
- **US6**: As a system, I want to detect collisions between Jerry, cats, and cheese so the game state updates correctly.  
- **US7**: As a system, I want to allow the player to pause and resume the game using the spacebar.  
- **US8**: As a system, I want to advance to the next level once all cheese is collected.

---

## Requirements Analysis

The following requirements define what the game must do, without prescribing how it is implemented.  
They are divided into functional requirements (FR), non-functional requirements (NFR), and implementation requirements (IR).  
Each requirement includes acceptance criteria to help validate the system.

---

### Functional Requirements (FR)

| ID | Description | Acceptance Criteria |
|----|-------------|---------------------|
| **FR1** | The player must be able to control Jerry using the arrow keys. | Jerry moves immediately in the chosen direction when an arrow key is pressed. |
| **FR2** | The maze must be displayed and constrain Jerry’s movement. | Jerry cannot pass through walls: the maze correctly limits movement. |
| **FR3** | The maze must contain regular cheese pieces that can be collected. | When Jerry collects a cheese piece, it disappears and the score increases. |
| **FR4** | At least one special cheese must exist and make cats vulnerable for a limited time. | After Jerry eats special cheese, cats enter a visible vulnerable state and can be chased. |
| **FR5** | The game must include four cats, including Tom, moving autonomously. | All cats are visible: they move on their own and follow AI behavior rules. |
| **FR6** | Jerry must lose a life if touched by a non-vulnerable cat. | A life counter decreases and the game state updates accordingly. |
| **FR7** | Jerry can chase away cats when they are vulnerable. | Cats disappear or return to their spawn point: points are awarded. |
| **FR8** | The game must end in defeat if Jerry loses all lives. | A “Game Over” message or screen is displayed when no lives remain. |
| **FR9** | The game must allow pausing and resuming via the spacebar. | All game entities stop moving: a pause message appears, and resume works correctly. |

---

### Non-Functional Requirements (NFR)

| ID | Description | Acceptance Criteria |
|----|-------------|---------------------|
| **NFR1** | The game should run smoothly on standard desktop systems. | No noticeable input lag or frame drops on modern hardware. |
| **NFR2** | Keyboard input should be processed immediately. | Player movement responds with no perceptible delay. |
| **NFR3** | Graphics and animations should render consistently. | No flickering, tearing, or visual glitches are observed. |
| **NFR4** | The game architecture should be modular and extensible. | New levels or power-ups can be added with minimal changes due to the MVC structure. |
| **NFR5** | The game must not collect or store user data. | No files are saved to disk: no personal information is requested. |

---

### Implementation Requirements (IR)

| ID | Description | Justification | Acceptance Criteria |
|----|-------------|--------------|---------------------|
| **IR1** | The game must be implemented in Python 3.12.4 using the Pygame library. | Python and Pygame offer simple syntax, multimedia support, and are beginner-friendly. | All components (logic, rendering, input) run correctly using Python and Pygame. |
| **IR2** | The game must run locally on a desktop environment. | Offline execution ensures accessibility and easy testing. | The game works without internet connection or external authentication. |
| **IR3** | The system must follow the Model-View-Controller (MVC) pattern. | MVC separates logic, input handling, and rendering: improving maintainability. | Controllers, models, and views are clearly separated in the codebase. |
| **IR4** | NumPy must be used to load maze layouts from text files. | NumPy simplifies efficient management of 2D level data and future extensions. | Maze files load correctly and produce the intended layouts. |

---

## Glossary

- **Maze**: The grid that defines walls and paths where Jerry and the cats move.  
- **Cheese**: Collectable items: regular cheese increases score, while special cheese makes cats vulnerable.  
- **Vulnerable state**: A temporary condition where cats can be chased away.  
- **Lives**: The number of attempts Jerry has before the game ends.  
- **Defeat**: The condition under which the game ends unsuccessfully.  
