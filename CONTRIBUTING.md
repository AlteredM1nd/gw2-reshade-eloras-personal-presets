# Contributing to Elora's GW2 ReShade Presets

First off, thank you for considering contributing to this project! Your help is greatly appreciated. Whether you're reporting a bug, suggesting an improvement, or submitting a change, you're helping make these presets better for everyone.

Please take a moment to review this document to make the contribution process easy and effective for everyone involved.

## Table of Contents
- [Code of Conduct](#code-of-conduct)
- [How Can I Contribute?](#how-can-i-contribute)
  - [Reporting Bugs](#reporting-bugs)
  - [Suggesting Enhancements](#suggesting-enhancements)
  - [Submitting Pull Requests](#submitting-pull-requests)
- [Style Guide & Preset Philosophy](#style-guide--preset-philosophy)
- [Pull Request Process](#pull-request-process)

---

## Code of Conduct

This project and everyone participating in it is governed by the Contributor Covenant Code of Conduct. By participating, you are expected to uphold this code. Please report unacceptable behavior to the project maintainers as outlined in the Code of Conduct.

## How Can I Contribute?

### Reporting Bugs
If you find a bug, visual artifact, or an issue with the documentation, please [open a bug report](https://github.com/alteredm1nd/gw2-reshade-eloras-personal-presets/issues/new?assignees=&labels=bug&template=bug_report.md&title=%5BBUG%5D+). We have a template that will guide you through the process of providing the necessary details.

### Suggesting Enhancements
Have an idea for a new preset, a tweak to an existing one, or an improvement to the documentation? We'd love to hear it! Please [open a feature request](https://github.com/alteredm1nd/gw2-reshade-eloras-personal-presets/issues/new?assignees=&labels=enhancement&template=feature_request.md&title=%5BFEATURE%5D+) to share your suggestion. The template will help you structure your idea.

### Submitting Pull Requests
If you have a fix or enhancement you'd like to contribute directly, you can submit a Pull Request. Please follow the Pull Request Process below.

## Style Guide & Preset Philosophy

To maintain a consistent look and feel, please keep the following in mind when making changes:
- **Photo Mode Presets:** The goal is maximum visual fidelity for a cinematic, painterly, and often dreamlike aesthetic. Performance is secondary.
- **Always On Presets:** The goal is to enhance the visuals while maintaining high performance for smooth gameplay. Changes should have a minimal FPS impact.
- **Clarity:** Avoid overly aggressive effects that crush blacks, blow out highlights, or oversaturate colors to the point of looking unnatural.
- **Documentation:** If you add a new shader or make a significant change, please update the `README.md` or `EFFECTS.md` accordingly.

## Pull Request Process

1.  **Fork the repository** and create your branch from `main`. A good branch name is descriptive, e.g., `fix/ssdo-flicker-in-caves` or `feature/new-vintage-preset`.
2.  **Make your changes.** Ensure you've tested them in various in-game locations (e.g., a bright open area, a dark interior, a zone with heavy fog) to check for unintended side effects.
3.  **Update the documentation.** If your changes affect installation, required shaders, or performance, please update the relevant sections in `README.md` or other documentation files.
4.  **Commit your work** with a clear and descriptive commit message.
5.  **Open a Pull Request** to the `main` branch of the original repository.
    - Provide a clear title and description for your PR.
    - Link to any relevant issues (e.g., "Fixes #123").
    - Include **before and after screenshots** to showcase your changes. This is very important for visual projects!

Thank you again for your contribution!