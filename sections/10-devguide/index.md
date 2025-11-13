---
title: Developer guide
has_children: false
nav_order: 11
---

# Developer Guide

This section explains how new contributors can join the development team and start working on CheeseChase.  It describes how to communicate through GitHub, how to set up the development environment, and the conventions and tools used during development.

---

## Communication and issue reporting

The project is managed entirely on GitHub, which serves as both the code repository and the communication platform.  
Contributors can open issues to report bugs or propose new features, comment on existing discussions, and submit pull requests with code updates.  
All project activity and collaboration happen directly on GitHub, so no external tools are required.

For questions, you can also contact the maintainers:  
francesca.folli2@studio.unibo.it, gaia.bellachioma@studio.unibo.it

---

## Coding conventions and style

The project follows a few clear rules to keep the codebase consistent and readable:

- Code is written in Python 3.12.4, following the PEP 8 style guide.  
- Class names use CamelCase (e.g., `GameController`, `MouseSprites`).  
- Variables and functions use snake_case (e.g., `update_score`, `start_game`).  
- Commit messages follow the Conventional Commits format (for example:  
  `feat(constants): add constants for tiles, colors, directions, objects, cat's modes and texts`,  
  `feat(controller): add GameController to orchestrate game flow`).
  This convention ensures clarity in the commit history and supports automated versioning during releases.


---

## Development environment setup

To start contributing, developers should prepare their local environment as follows:

1. Clone the repository:
     ```bash
   git clone <https://github.com/unibo-dtm-se-2425-Cheese-Chase/artifact.git>
   ```



2. Create and activate a virtual environment:
   ```bash
   python -m venv venv
   venv\Scripts\activate        # On Windows
   source venv/bin/activate     # On Mac/Linux
   ```

3. Install the dependencies:
   ```bash
   pip install -r requirements-dev.txt
   ```

4. Run the test suite to confirm everything works correctly:
   ```bash
   python -m unittest discover -s test -t .
   ```

5. Run the game locally:
   ```bash
   python -m CheeseChase
   ```

---

## Development workflow

If you want to submit a pull request with new features or fixes, please follow these steps:

1. Create a new branch from `main` (or `master`):
   ```bash
   git checkout -b feature-your-branch-name
   ```

2. Make your changes and commit them using the Conventional Commits format:
   ```bash
   git add .
   git commit -m "feat: describe your feature here"
   ```

3. Push your branch to GitHub:
   ```bash
   git push origin feature-your-branch-name
   ```

4. Open a pull request on GitHub from your branch to the `main` (or `master`) branch.

5. Wait for a review. Your pull request will be checked and approved by another team member before merging.

Once your pull request is merged, the CI/CD pipeline will automatically run tests and, if successful, build a new release on PyPI.

---

## Development tools

- Recommended IDE: Visual Studio Code (VS Code)  as it is easy to use and works well with Python and Git.

- GitHub Actions: The project already has workflows set up for testing (`check.yml`) and releases (`deploy.yml`).  As a contributor, ensure all tests pass before opening a pull request. GitHub Actions will handle the rest.
