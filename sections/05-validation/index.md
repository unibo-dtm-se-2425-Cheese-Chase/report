---
title: Validation
has_children: false
nav_order: 6
---

# Validation

## Testing approach

A structured testing strategy was adopted to ensure that CheeseChase met all functional and non-functional requirements. Automated testing using Python’s `unittest` framework was combined with manual acceptance testing to validate full gameplay functionality.

A semi–Test-Driven Development methodology was followed: early unit tests guided the implementation of the model and controller logic, with additional tests added as new features were introduced. The `unittest` framework was selected for its simplicity, Python integration, and compatibility with `unittest.mock`, enabling the use of test doubles to isolate components from the Pygame graphical layer.

---

## Testing (automated)

A total of 168 automated tests were developed across the model, controller, and view layers. Each module had a dedicated test file, ensuring thorough and maintainable validation aligned with functional and non-functional requirements.

- Model layer: validated Entity, Node, Cheese, Cat, Mouse, and Animator classes for movement, collision, goal seeking, and state transitions (FR1–FR7)  
- Controller layer: tested EventsManager, LevelManager, GameController, and Pauser for input handling, pausing, scoring, and level progression (FR3–FR10)  
- View layer: confirmed rendering logic in GameView, including background updates and entity visibility (NFR1–NFR3)

Mocks and patches were used to simulate dependencies, providing reproducible and isolated results without requiring a game window or real-time input.

Automated test success rate: 100%  
Measured total coverage: 97% line coverage across all modules

### Unit testing

Unit tests were written for all major classes to validate individual methods and behaviours. These tests confirmed correct initialization, state transitions, timing behaviour, and updates under both standard and edge-case conditions.

Examples include:
- Entity movement and speed adjustment (FR1, FR2)  
- Pause timing and callback management (FR10)  
- LevelManager score/life resets and level transitions (FR8, FR9)  
- Mouse and Cat goal logic and collision reactions (FR4–FR7)

All unit tests passed successfully, confirming stability of each module in isolation.

### Integration testing

Integration tests validated communication between components and the correct flow of data across the MVC architecture. These tests confirmed correct interactions among the player, game entities, and game controllers.

Examples include:
- Mouse, Cats, and Cheese: scoring, collisions, and frightened mode logic (FR3–FR7)  
- GameController and EventsManager: input handling, pause/resume behaviour, and state management (FR8–FR10)  
- LevelManager and GameController: seamless level resets and restarts (FR8, FR9)

Mocks were used to simulate timers, inputs, and game events.

Integration test success rate: 100%

### System testing

System testing validated CheeseChase as a fully functioning game. Full automation was limited due to Pygame’s graphical environment, but extended integration tests and manual sessions confirmed system-level behaviour.

Tests confirmed:
- Proper startup and level loading (FR8)  
- Correct player movement, collisions, scoring, and transitions (FR1–FR10)  
- Consistent performance and responsiveness (NFR1–NFR3)

All system tests were executed in a clean virtual environment to ensure repeatability.

System test success rate: 100%

---

## Acceptance tests (manual)

Manual testing was completed to verify all functional and non-functional requirements.

The testing process included:
- Installing and starting the game using the instructions in the Deployment section  
- Trying different gameplay settings  
- Playing several full games to observe movement, collisions, scoring, and general behaviour as described in the User Guide  

Criteria assessed:
- FR1–FR10: player control, collision handling, cheese collection, frightened mode, enemy behaviour, life loss, scoring, level transitions, game-over sequence, and pause/resume  
- NFR1–NFR5: stable performance, responsive input, consistent graphics, modular design, and absence of data collection

All manual tests produced the expected results.

Acceptance test success rate: 100%
