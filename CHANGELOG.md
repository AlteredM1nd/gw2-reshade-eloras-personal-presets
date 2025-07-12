# Changelog

All notable changes to these presets will be documented in this file.

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