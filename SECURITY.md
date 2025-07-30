---
title: Security
nav_order: 6
---

# Security Policy

The maintainers of Elora's Personal Presets take the security of this project and its users seriously. While this project consists solely of configuration files (`.ini`) and documentation, and does not include any executable code, we believe in following security best practices.

## Table of Contents
- Supported Versions
- Reporting a Vulnerability
- Third-Party Dependencies
- Our Commitment

---

## Supported Versions

Security updates and support are only provided for the latest version of the presets available on the `main` branch and in the latest official release. We encourage all users to stay up-to-date.

| Version | Supported          |
| ------- | ------------------ |
| Latest  | :white_check_mark: |
| Older   | :x:                |

---

## Reporting a Vulnerability

We appreciate responsible disclosure of any security concerns. If you discover a potential security issue in this project, such as a malicious link in the documentation or a configuration that could exploit a known ReShade vulnerability, please help us by reporting it privately.

**Please do NOT open a public GitHub issue for security vulnerabilities.**

Instead, please contact the project maintainer directly and privately via:
- **Discord:** `alteredm1nd`

When reporting, please include the following information:
- A clear description of the vulnerability.
- The potential impact of the vulnerability.
- Steps to reproduce the issue, if applicable.
- Any other relevant details.

We will do our best to acknowledge your report within 48 hours and will work with you to understand and resolve the issue promptly.

---

## Third-Party Dependencies

These presets require the use of third-party software, including:
- **ReShade:** The core post-processing injector.
- **Shader Packages:** Various `.fx` shader files from different authors (e.g., qUINT, prod80, Zenteon).
- **ReShade Add-ons:** The `ReshadeEffectShaderToggler` add-on.

The security of these third-party components is outside the scope of this project. We are not responsible for vulnerabilities or malicious code within ReShade itself or any of the external shader/add-on repositories.

**We strongly advise you to download these dependencies *only* from their official, trusted sources, which are linked in our `README.md` file.** Avoid downloading them from unverified third-party websites.

---

## Our Commitment

- **No Executables:** This project **only** distributes configuration files (ending in `.ini`) and documentation files (ending in `.md`). We will never include executables (`.exe`), scripts (`.bat`, `.ps1`), or installers in this repository.
- **Authenticity:** To ensure you are using the authentic, untampered presets, please download them directly from the official GitHub repository releases page.

Thank you for helping keep Elora's Personal Presets and its community safe.