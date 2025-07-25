# Effect Packages & Shaders Explained

This page provides a detailed breakdown of all the effect packages and shaders used in Elora's Personal Presets for Guild Wars 2 ReShade. For each effect package, you'll find:
- **What the package is for**
- **What each shader does**
- **Typical settings/sliders and what they control**
- **Tips for tweaking for visuals or performance**

---

## Table of Contents
1. [qUINT by Marty McFly](#quint-by-marty-mcfly)
2. [Zenteon Shaders](#zenteon-shaders)
3. [prod80 Shaders](#prod80-shaders)
4. [ReShade Repository Shaders](#reshade-repository-shaders)
5. [Other Notable Shaders](#other-notable-shaders)

---

## qUINT by Marty McFly
A suite of advanced post-processing effects designed for realism and cinematic visuals. [qUINT GitHub](https://github.com/martymcmodding/qUINT)

### MartysMods_MXAO.fx (MXAO)
- **Purpose:** Adds ambient occlusion for realistic shadowing in crevices and around objects.
- **Key Settings:**
  - `Sample Radius`: How far AO spreads from edges.
  - `Sample Quality`: Higher = better quality, lower = faster.
  - `AO Amount`: Strength of the effect.
  - `Debug View`: Visualize AO mask.
- **Tips:** Lower quality for performance, increase radius for softer AO.

### qUINT_dof.fx (DOF)
- **Purpose:** Depth of Field, blurs background/foreground for a photographic look.
- **Key Settings:**
  - `Focal Plane`: Where the image is sharpest.
  - `Blur Amount`: How strong the blur is.
  - `Bokeh Shape/Quality`: Style and quality of out-of-focus highlights.
- **Tips:** Lower quality for gameplay, increase for screenshots.

### MartysMods_LAUNCHPAD.fx
- **Purpose:** Utility for managing and toggling qUINT effects.
- **Key Settings:**
  - `Enable/Disable` toggles for various qUINT effects.
- **Tips:** Use to quickly enable/disable qUINT suite features.

---

## Zenteon Shaders
A collection of modern, performance-friendly post-processing effects. [Zenteon Shaders GitHub](https://github.com/Zenteon/Reshade-Shaders)

### Zenteon_Framework.fx
- **Purpose:** Core framework for Zenteon shaders, may provide global toggles or shared settings.

### ZN_LC.fx (Local Contrast)
- **Purpose:** Enhances local contrast for a sharper, more detailed look.
- **Key Settings:**
  - `Strength`: How much contrast is added.
  - `Radius`: Area affected by the contrast boost.
- **Tips:** Too high can cause halos; adjust for subtlety.

### Zenteon_Sharpen.fx
- **Purpose:** Sharpening filter for crisper visuals.
- **Key Settings:**
  - `Strength`: Sharpening intensity.
  - `Clamp`: Prevents over-sharpening artifacts.
- **Tips:** Use moderate values to avoid noise.

### Zenteon_XenonBloom.fx
- **Purpose:** Bloom effect for glowing highlights.
- **Key Settings:**
  - `Threshold`: Brightness level to start bloom.
  - `Intensity`: Strength of the glow.
- **Tips:** Lower threshold = more bloom; too much can wash out image.

---

## prod80 Shaders
A set of high-quality color grading and bloom effects. [prod80 GitHub](https://github.com/prod80/prod80-ReShade-Repository)

### PD80_02_Bloom.fx
- **Purpose:** Adds bloom (glow) to bright areas.
- **Key Settings:**
  - `Threshold`: Minimum brightness for bloom.
  - `Intensity`: Bloom strength.
  - `Radius`: Spread of the bloom.
- **Tips:** Lower intensity for subtlety; adjust threshold to control what glows.

### PD80_04_Color_Temperature.fx
- **Purpose:** Adjusts color temperature (warmth/coolness) of the image.
- **Key Settings:**
  - `Temperature`: Warmer (red/orange) or cooler (blue) tones.
  - `Tint`: Green/magenta shift.
- **Tips:** Use to match lighting mood or correct color cast.

---

## ReShade Repository Shaders
Official and community shaders included with ReShade. [ReShade Shaders GitHub](https://github.com/crosire/reshade-shaders)

### AmbientLight.fx
- **Purpose:** Adds a soft ambient light/glow to the scene.
- **Key Settings:**
  - `Strength`: Intensity of the effect.
  - `Color`: Tint of the ambient light.
- **Tips:** Good for brightening dark scenes.

### MagicBloom.fx
- **Purpose:** Simple, fast bloom effect.
- **Key Settings:**
  - `Threshold`, `Intensity`, `Radius` (see above).
- **Tips:** Use for a dreamy or fantasy look.

### Vibrance.fx
- **Purpose:** Boosts color intensity without oversaturating skin tones.
- **Key Settings:**
  - `Vibrance`: Amount of color boost.
  - `RGB Balance`: Adjust which colors are boosted.
- **Tips:** Subtle values prevent cartoonish look.

### Reinhard.fx
- **Purpose:** Tone mapping for more natural highlights and shadows.
- **Key Settings:**
  - `Exposure`: Brightness control.
- **Tips:** Use to prevent blown-out highlights.

### SmartDeNoise.fx
- **Purpose:** Reduces image noise/grain.
- **Key Settings:**
  - `Strength`: How much noise is removed.
  - `Sensitivity`: How aggressively noise is detected.
- **Tips:** Too high can blur details.

### CAS.fx (Contrast Adaptive Sharpening)
- **Purpose:** Sharpening filter that adapts to contrast.
- **Key Settings:**
  - `Sharpness`: Intensity of sharpening.
- **Tips:** Good for upscaled or blurry images.

### NeoSSAO.fx
- **Purpose:** Screen-space ambient occlusion (shadows in crevices).
- **Key Settings:**
  - `Radius`, `Intensity`, `Quality`.
- **Tips:** Lower quality for performance.

### HexLensFlare.fx
- **Purpose:** Simulates lens flares from bright lights.
- **Key Settings:**
  - `Intensity`, `Threshold`, `Color`.
- **Tips:** Use sparingly for realism.

### PPFX_SSDO.fx
- **Purpose:** Screen-space directional occlusion (advanced AO).
- **Key Settings:**
  - `Quality`, `Radius`, `Intensity`.
- **Tips:** More realistic than basic AO, but more demanding.

### GloomAO.fx
- **Purpose:** Another ambient occlusion shader, often softer.
- **Key Settings:**
  - `Strength`, `Radius`.

### FGFXLargeScalePerceptualObscuranceIrradiance.fx
- **Purpose:** Large-scale ambient occlusion and lighting.
- **Key Settings:**
  - `Strength`, `Scale`.

### LocalContrast.fx
- **Purpose:** Enhances local contrast (see also ZN_LC.fx).
- **Key Settings:**
  - `Strength`, `Radius`.

### Quark_Local_Contrast.fx
- **Purpose:** Another local contrast enhancer.
- **Key Settings:**
  - `Strength`, `Radius`.

### Quark_Xenon_Bloom.fx
- **Purpose:** Bloom effect variant.
- **Key Settings:**
  - `Threshold`, `Intensity`, `Radius`.

### BloomingHDR.fx
- **Purpose:** High dynamic range bloom effect.
- **Key Settings:**
  - `Threshold`, `Intensity`, `HDR Mode`.

### lilium__rcas_hdr.fx
- **Purpose:** Robust contrast adaptive sharpening for HDR.
- **Key Settings:**
  - `Sharpness`, `HDR Mode`.

### pCamera.fx
- **Purpose:** Camera simulation (exposure, vignette, etc.).
- **Key Settings:**
  - `Exposure`, `Vignette`, `Film Grain`.

### pColors.fx
- **Purpose:** Color grading and correction.
- **Key Settings:**
  - `Saturation`, `Contrast`, `Gamma`, `Lift`, `Gain`.

### Shading.fx
- **Purpose:** Adds stylized shading and lighting to enhance the painterly or cartoon-like look of the scene.
- **Key Settings:**
  - `ShadingIntensity`: Strength of the shading effect.
  - `SamplingArea`: Area over which shading is calculated.
- **Tips:** Use for a more artistic, less photorealistic look.

### VolumetricFog.fx
- **Purpose:** Simulates volumetric fog and light scattering for atmospheric depth and god rays.
- **Key Settings:**
  - `Intensity`, `Radius`, `SampleCount`, `Exposure`, `Gamma`.
- **Tips:** Increase intensity and sample count for denser, more dramatic fog; lower for subtle haze.

### ReflectiveBumpmapping.fx
- **Purpose:** Adds reflective bump mapping for enhanced surface detail and subtle reflections.
- **Key Settings:**
  - `FresnelMult`, `ReliefHeight`, `SampleCount`.
- **Tips:** Use moderate values to avoid overly shiny or artificial surfaces.

### cDLAA.fx (Contrast-aware Directionally Localized Anti-Aliasing)
- **Purpose:** Advanced anti-aliasing technique for reducing jagged edges while preserving detail.
- **Key Settings:**
  - `ContrastThreshold`, `PreserveFrequencies`.
- **Tips:** Use with other AA for best results in screenshots.

### DFTAA.fx (Directional Filtering Temporal Anti-Aliasing)
- **Purpose:** Temporal anti-aliasing to smooth out shimmering and flickering in motion.
- **Key Settings:**
  - `EdgeThreshold`, `Lambda`.
- **Tips:** Best for video or animated scenes; may slightly blur stills.

### DTAA.fx (Directional Temporal Anti-Aliasing)
- **Purpose:** Another temporal anti-aliasing shader for reducing aliasing artifacts over time.
- **Key Settings:**
  - `blendRate`, `mixRate`.
- **Tips:** Combine with other AA for maximum smoothness.

### GaussianBlur.fx
- **Purpose:** Applies a soft blur to the image, useful for dreamy or atmospheric effects.
- **Key Settings:**
  - `BlurRadius`, `BlurStrength`.
- **Tips:** Use sparingly to avoid loss of detail; great for soft focus or haze.

### GBloom.fx
- **Purpose:** Adds an additional bloom layer for glowing highlights and enhanced fantasy lighting.
- **Key Settings:**
  - `BloomIntensity`, `BloomSaturation`, `BlurRadius`, `LuminanceThreshold`.
- **Tips:** Stack with other bloom effects for a magical, ethereal look.

---

## ReshadeEffectShaderToggler Addon
A ReShade 5+ addin that allows you to apply ReShade effects to specific render targets or shader groups based on a key press. Its primary purpose is to ensure that effect packages (like bloom, DOF, AO, etc.) are not rendered on top of the in-game UI, menus, or HUD elements, preserving UI clarity while keeping the visual enhancements for the game world.

- **Purpose:** Prevents ReShade effects from affecting the UI by toggling effects only for the game world.
- **How it works:**
  - Lets you create toggle groups for shaders that draw the UI or HUD.
  - When the UI is visible, the addon disables selected effects for those UI elements.
  - Configuration is done in-game via the ReShade Addons tab, where you can mark shaders associated with the UI and assign them to toggle groups.
  - Saves its configuration to `ReshadeEffectShaderToggler.ini` for reuse.
- **Typical Use Case:**
  - Open the ReShade overlay, go to the Addons tab, and use the Shader Toggler area to create a new toggle group.
  - Mark shaders responsible for the UI using the provided hotkeys (see the addon's documentation for details).
  - Assign a toggle key or let the addon automatically manage toggling based on UI visibility.
  - Save the group to persist your settings.
- **Reference:** [ReshadeEffectShaderToggler on GitHub](https://github.com/4lex4nder/ReshadeEffectShaderToggler)

---

## Tips for Tweaking
- **Performance:** Lower quality, radius, or sample count for AO and DOF effects to improve FPS.
- **Visuals:** Increase bloom, vibrance, and color grading for a more stylized look.
- **Sharpening:** Use moderate values to avoid noise and artifacts.
- **Color Grading:** Adjust temperature, tint, and vibrance to match your taste or the scene's mood.

---

## References
- [ReShade Shader List & Docs](https://reshade.me/docs)
- [qUINT by Marty McFly](https://github.com/martymcmodding/qUINT)
- [prod80 Shaders](https://github.com/prod80/prod80-ReShade-Repository)
- [Zenteon Shaders](https://github.com/Zenteon/Reshade-Shaders)
- [ReShade Shaders](https://github.com/crosire/reshade-shaders)

---

This guide should help you understand and tweak every effect in Elora's Personal Presets. For more details, see the official shader documentation or the [ReShade forums](https://reshade.me/forum/). 