---
title: Troubleshooting & FAQ
parent: Home
nav_order: 8
---

## Troubleshooting & FAQ

**Q: The preset looks wrong, or some effects are missing!**
- Double-check that all required .fx files are present (see above for links).
- Make sure your in-game graphics settings match the recommendations.
- Try reloading the preset in the ReShade menu.
- If depth-based effects (like MXAO or DOF) don't work, try switching between windowed and fullscreen, or check the "Copy depth buffer before clear operations" option in ReShade's settings.
- If you see a black screen or crash, ensure your GPU drivers are up to date and that you are using ReShade 6.5.1.

**Q: My game is running slowly!**
- Some effects (like MXAO, SSDO, and high-quality DOF) are demanding. Disable or lower their quality in the ReShade menu if needed.
- For gameplay, toggle off the most demanding effects or use the Always On preset tier (High, Medium, or Low) that achieves the framerate that works best for your system.
- Lower your in-game resolution or reduce supersampling for better performance.

**Q: Where do I get missing shaders?**
- Most are included with the standard ReShade install. For third-party shaders, use the links above or check the [ReShade forums](https://reshade.me/forum/) or the shader author's GitHub.

**Q: Guild Wars 2 won't launch with ReShade, or ReShade doesn't appear?**
- Make sure you renamed `dxgi.dll` to `d3d11.dll` in your GW2 folder (see Installation Instructions).
- Some overlays (Discord, Steam, etc.) can interfere—try disabling them.

**Q: The Depth of Field is reversed, why is that?**
- Click on the `Edit global preprocessor definitions` button from the `ReShade Menu` and change `RESHADE_DEPTH_INPUT_IS_REVERSED` from `1` to `0` and click on the `Apply` button.

**Q: My UI is blurry when I use any of the Photo Mode or Always On - DOF Presets, how do I fix that?**
- In order for your UI to not be affected by `qUINT_dof.fx` the `REST add-on` is required. You can rerun the ReShade installation and follow the steps in the Installation Instructions to ensure that the REST add-on is installed and then ensure that my `ReshadeEffectShaderToggler.ini` is placed into your `Guild Wars 2 Game Folder` which is `C:\Program Files\Guild Wars 2` (default for standalone launcher players) or `C:\Program Files (x86)\Steam\steamapps\common\Guild Wars 2` (default for Steam players)

**Q: Why is everything except the UI very dark?**
- This will happen when using `ReshadeEffectShaderToggler.ini` files designed for other presets that don't utilize the same effect packages or for older versions of ReShade - my preset has it's own `ReshadeEffectShaderToggler.ini` that has been configured for my current effect package load order and won't cause this issue. Please download the `ReshadeEffectShaderToggler.ini` from my repo and replace it with the `ReshadeEffectShaderToggler.ini` that is currently in your `Guild Wars 2 Game Folder` which is `C:\Program Files\Guild Wars 2` (default for standalone launcher players) or `C:\Program Files (x86)\Steam\steamapps\common\Guild Wars 2` (default for Steam players)