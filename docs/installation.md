---
title: Installation Instructions
parent: Home
nav_order: 4
permalink: /gw2-reshade-eloras-personal-presets/#installation-instructions
---

## Installation Instructions

1. Download Presets
   - Download the latest release from [My Release Page](https://github.com/AlteredM1nd/gw2-reshade-eloras-personal-presets/releases).
   - You can either download the `.ini files` beginning with `Elora's Personal Presets` from the `Assets` section of the latest release by clicking on them individually along with the `ReshadeEffectShaderToggler.ini` or click `Source code (zip)` to download my entire repository as a `.zip file` containing everything which you will then have to extract (unzip) by clicking on the `.zip` file in your `File Explorer`, clicking on the `Extract All` button, and then clicking on the `Extract` button.
   - Copy all files beginning with `Elora's Personal Presets` along with `ReshadeEffectShaderToggler.ini` into your Guild Wars 2 game folder `C:\Program Files\Guild Wars 2` (default for standalone launcher players) or `C:\Program Files (x86)\Steam\steamapps\common\Guild Wars 2` (default for Steam players).

2. Download and Install ReShade 6.5.1
   - Download the latest version of the ReShade installer (ReShade 6.5.1 with full add-on support) and run it. ([Download here](https://reshade.me/#download))
   - Select your `Gw2-64.exe` (Guild Wars 2 executable), it may not appear on the default list of applications, and if so, click `Browse...` and navigate to the Guild Wars 2 folder and select it `C:\Program Files\Guild Wars 2` (default for standalone launcher players) or `C:\Program Files (x86)\Steam\steamapps\common\Guild Wars 2` (default for Steam players) and then click `Next`.
   - Choose `Microsoft DirectX 10/11/12` and then click `Next`.
   - Choose `Install ReShade and effects` and then click `Next`.
   - Click `Browse...`, navigate to and select `Elora's Personal Presets - Photo Mode - Ultra.ini` (since this uses the most effect packages, it will install all the effect packages used in all my presets) and then click `Open`.
   - It will automatically select all of the effect packages used by my presets for installation, if this is sufficient for you, then you can click `Next` and it will begin downloading the required effect packages. If you would like to give yourself more options for experimenting, you can instead click `Uncheck All` and then click `Check All`, this will install every available effect package in the ReShade repository which will give you a lot of room for experimenting with new effect packages.
   - On the `Select add-ons to install:` screen, select `ReshadeEffectShaderToggler (REST) by 4lex4nder` and click `Next`
   - Click `Finish`.

3. Rename dxgi.dll to d3d11.dll
   - In `C:\Program Files\Guild Wars 2` (default for standalone launcher players) or `C:\Program Files (x86)\Steam\steamapps\common\Guild Wars 2` (default for Steam players) rename the `dxgi.dll` to `d3d11.dll`, this change is required since the update to DX11 in order for ReShade to recognize Guild Wars 2 and initialize during launch.

4. Launch Guild Wars 2
   - Launch Guild Wars 2.
   - Press the `Home` button on your keyboard to open the `ReShade Menu` (this keybind can be modified in the `ReShade Settings Menu`).
   - Select the desired preset from the `dropdown menu at the top` to activate it.

5. Set a Toggle Key (optional)
   - Navigate to the `Settings` tab in the `Rehsade Menu`.
   - Bind a key for `Effect Toggle Key`.
   - Use your new keybind to turn the current preset on and off whenever it suits you.

6. Tweak Settings (optional)
   - If you like how I have things set up then you can skip this, but if you'd like to simply use my preset as a foundation for more changes you're more than welcome to do that. At the end of the day, this is your game, you should enjoy the way that it looks, and it should suit your preferences. Modify sliders and toggle effects until everything is just right for you. If you need to revert back, you can always just download this preset again. Alternatively, you can create a new preset based on mine using the `Add A New Preset` (Plus Icon) button in the top right hand corner of the `Reshade Menu` and put a checkmark in the `Inherit Current Preset` checkbox - this way the original preset remains untouched and you get a brand new copy to modify to your heart's content!

> Note:
> - Additional information on each effect package along with tips for tweaking them yourself (should you choose to do so) can be found in [EFFECTS.md](../EFFECTS.md).