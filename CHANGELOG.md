# Changelog

All notable changes to these presets will be documented in this file.

## [4.1.2] - 2025-07-20
### Added
- Added two new pixel hashes to `ReshadeEffectShaderToggler.ini` to ensure that effect packages no longer render on top of NPC speech bubbles. This minor update further improves UI clarity during gameplay. 

## [4.1.1] - 2025-07-17
### Changed
- Updated `pSSDOFadeEnd` to `0.350000` and `pSSDOFadeStart` to `0.100000` for `PPFX_SSDO.fx` in all presets. This adjustment ensures that shadows rendered by SSDO gradually fade closer to the player's character than before, resulting in more natural shadow transitions.

## [4.1.0] - 2025-07-17
### Added
- **REST (ReshadeEffectShaderToggler) is now required** for all presets. This add-on ensures that ReShade effects no longer affect the Guild Wars 2 UI.
- REST can be downloaded from [https://github.com/4lex4nder/ReshadeEffectShaderToggler](https://github.com/4lex4nder/ReshadeEffectShaderToggler).
- Updated the installation instructions and required effect packages/add-ons list in the README to include REST and copying your working ReshadeEffectShaderToggler.ini into the Guild Wars 2 folder.
- With this change, all effect packages used by the presets will no longer affect the UI, providing a cleaner and more immersive experience.

## [4.0.0] - 2025-07-16
### Added
- Introduced **Always On - Medium** and **Always On - Low** presets, each available in DOF (Depth of Field) and No DOF variants.
- These new presets are designed to expand accessibility for users with lower-spec hardware, those seeking higher FPS, or anyone preferring a more minimal ReShade experience.
- **Performance:**
  - Always On - Medium: Offers approximately 10-20 more FPS compared to Always On - High.
  - Always On - Low: Offers approximately 20-40 more FPS compared to Always On - High.
- All Always On presets now cover a wider range of hardware and performance needs, making them suitable for both high-end and lower-end systems, as well as users prioritizing smooth gameplay.

---

## [3.0.0] - 2025-07-08
### Added
- Released **Photo Mode - Ultra**: a major overhaul and next-generation upgrade to the First Person photo preset, designed for maximum visual fidelity and screenshot artistry.

### Changed
- **Cinematic Visuals:** Ultra delivers a painterly, dreamlike look with soft, diffused lighting, pronounced god rays, and lush, harmonious color grading. Volumetric fog and advanced bloom effects create a magical, ethereal atmosphere perfect for fantasy screenshots.
- **Atmosphere & Depth:** The new effect stack enhances depth and immersion, with subtle haze and light scattering that make environments feel alive and three-dimensional.
- **Technique Overhaul:** Ultra introduces a revised and expanded set of effects, including new cinematic shading, advanced bloom layers, volumetric fog, reflective bump mapping, and multiple anti-aliasing methods. Several older effects were removed or replaced for a cleaner, more modern look.
- **Sharpening & Noise:** Sharpening and denoising are carefully balanced for clarity without harshness, with new sharpening methods and reduced noise for a cleaner, more photographic image.
- **Artistic Focus:** Every frame is tuned for screenshot artistry—colors are vivid but balanced, details are crisp without harshness, and the overall presentation is clean and free of distracting artifacts.

### Notes
- **Performance:** Ultra is more demanding than previous presets and is intended for high-end screenshots and showcase moments, not regular gameplay. For everyday use, continue to use the Always On or standard Photo Mode presets.

---

## [2.1.0] - 2025-07-07
### Added
- Created `EFFECTS.md` with a comprehensive breakdown of all effect packages and shaders used in the presets. Includes purpose, key settings, and tips for tweaking visuals or performance.

### Changed
- Expanded and clarified the "FOV & Camera Tips" section in `README.md` with more detailed advice on camera controls, composition, and screenshot techniques.
- Updated hardware recommendations and performance notes in `README.md` for both Photo Mode and Always On presets.

---

## [2.0.0] - 2025-07-07
- Renamed the existing Standard - First Person Photos and Standard - Third Person Photos presets to Photo Mode - First Person and Photo Mode - Third Person for clarity.
- Introduced a new set: Always On presets. The first release includes High spec variants:
  - Always On - High - DOF (Depth of Field enabled)
  - Always On - High - No DOF (Depth of Field disabled)
- Always On presets are designed for high performance (60+ FPS) on modern hardware:
  - CPU: Intel Core i7-13700HX or AMD Ryzen 7 7735HS
  - GPU: NVIDIA GeForce RTX 4050 (6GB VRAM) or AMD Radeon RX 7600M
  - RAM: 16 GB DDR5
  - Storage: SSD with 10+ GB free
  - OS: Windows 10/11 64-bit
  - Performance Target: 1080p @ 60+ FPS with all effects enabled
- User testing on a system with Intel i7-8700K, 32GB RAM, and RTX 2080 Ti reported:
  - Without DOF: 90-75 FPS
  - With DOF: 80-60 FPS
- Always On presets deliver roughly double the FPS of the Photo Mode presets, making them ideal for everyday gameplay with high visual fidelity. 

---

## [1.0.0] - 2025-07-01
- Initial public release of Elora's Personal Presets for Guild Wars 2
- Includes First Person and Third Person photo presets
- Full README with setup instructions and required shaders list 