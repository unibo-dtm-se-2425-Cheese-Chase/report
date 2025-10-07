---
title: CI/CD
has_children: false
nav_order: 9
---

# CI/CD

This section describes the continuous integration and continuous deployment (CI/CD) workflow of the CheeseChase project. 
It explains what is automated, why automation was chosen, and how it has been set up.

---

## What is automated

The project uses **GitHub Actions** to automate both testing and releases.

Every time new code is pushed to the `master` branch, the project’s tests run automatically on different operating systems (Linux, macOS, Windows) and with several Python versions.  This makes sure the game works in many environments before changes are accepted.

After all tests succeed, the workflow also takes care of creating a new release.  It builds the game package, decides the correct version number, creates a tag, and publishes the new version so users can install it.

---

## Why

Automation saves time and reduces mistakes.  Developers do not need to manually run tests, create version numbers, or upload new packages as everything happens automatically. This keeps the release process consistent and makes sure each published version has been tested first.

---

## How

The automation is set up using two workflow files stored in the `.github/workflows/` folder:

- check.yml runs the tests every time new code is pushed or reviewed.
- deploy.yml handles the release process by building the game package and uploading it when a new version is ready.

The system checks the messages written in each commit.  If a commit says `fix`, it makes a small update; if it says `feat`, it creates a new feature release; and if it says `BREAKING CHANGE`, it creates a major new version.  This way, the version number is updated automatically depending on the type of change.

---

## Relevant details

- Secrets and authentication: The access keys for publishing to PyPI are stored safely as GitHub organization secrets.  
  The PYPI_USERNAME is set to `__token__`, and the PYPI_PASSWORD is a secure token generated in the developer’s PyPI account.  
  GitHub also stores the RELEASE_TOKEN secret, which allows the workflow to create tags and releases automatically and push them to the repository.

- Versioning: The project follows Semantic Versioning. This means updates are labeled as major, minor, or patch releases depending on the importance of the change.

- Dependencies: The workflow uses Node.js and a helper package that links commit messages to version numbers and automatically creates release notes.

---

Thanks to this setup, developers only need to push their changes with correctly written commit messages. The system tests the game, decides the right version, and publishes it, making the process fast, reliable, and easy to maintain.
