# NuStadium: The Pokémon Stadium HD Retexture & UI Overhaul

A visual overhaul of the Nintendo 64 classic *Pokémon Stadium*, designed for use with GLideN64. 

The goal of this project is to modernize the game's UI and textures while strictly preserving the original N64 lowpoly aesthetic. THIS IS NOT A GAMEPLAY HACK. it is a pure visual enhancement designed to make the game look vibrant and appealing on not only modern displays but also be appealing to modern point of views on certain assets of art, all without losing its original retro soul that made generations love Pokémon Stadium.

## Design Philosophy
*   **Retaining of the Lowpoly Feel:** Higher resolutions must not mean losing the original pixel art texture and N64 charm.
*   **Modern Lookability:** Fix the clutter of the original 2000 era UI with better typography, contrast, and visual hierarchy.
*   **Vibrancy:** Correct the color grading and saturation to make the game pop, while remaining faithful to the original palette.

## Repository Structure
This repository is organized to separate game-ready assets from design source files:

*   `/hires_texture/POKEMON_STADIUM/` - The final, game-ready `.png` files redrawn or remixed entirely on IbisPaint X (filenames retain the original CRC hashes for emulator matching).
*   `/source_textures/` - The original, unmodified textures ripped from the game for reference.
*   `/design_files/` - Source files (e.g., `.kra`,but now that ArtCraft Suite came out, `.psd` files too) for the redesigned assets.
*   `/docs/` - Progress notes, layout grids, color palettes and everything else i might need to come back on this project and start from where i left.

## Technical Pipeline (Current Setup)
This project is being developed on a Linux (Nobara) environment using the following workflow:
*   **Emulation:** RMG (Rosalie's Mupen GUI) for gameplay/testing, and RMG v0.2.4 (Portable) specifically for asset extraction.
*   **Ripping Tool:** GLideN64-SceneRipper plugin.
*   **Design Tools:** Krita. \
                      IbisPaint X Mobile. \
                      Adobe Illustrator, Lightroom, Photoshop. \
                      ArtCraft's PhotoCraft, LightCraft, EffectCraft, FigCraft, TextureCraft, MaterialCraft.

---

## Installation & Usage Tutorial

To use this texture pack, you must be running the game on an N64 emulator that supports the **GLideN64** video plugin (such as RMG, Project64, or Mupen64Plus). 

### Step 1: Locate your emulator's Texture Folder
You need to find the `hires_texture` folder for your specific emulator. Here are the common paths:

*   **RMG (Flatpak on Linux):** 
    `~/.var/app/com.github.Rosalie241.RMG/data/RMG/hires_texture/`
*   **RMG (Portable/Windows):** 
    `[Your RMG Folder]/Data/hires_texture/`
*   **Project64:** 
    `[Your Project64 Folder]/Plugin/GFX/GLideN64/hires_texture/`

### Step 2: Create the Game Folder
Inside that `hires_texture` directory, create a new folder named exactly:
`POKEMON_STADIUM`

*(Note: If the folder doesn't work, launch the game and check the emulator's log/console to see the exact internal name it is looking for, though `POKEMON_STADIUM` is standard for the US 1.0 ROM).*

### Step 3: Copy the Files
Download the latest release of this repository (or clone it). 
Copy all the `.png` files from the `hires_texture/POKEMON_STADIUM/` folder in this repo into the folder you just created in Step 2. 
**Do not rename the files.** The filenames are CRC hashes (e.g., `P1S3LL1N0_676767_all.png`) that the emulator uses to match the custom texture to the game's original texture.

### Step 4: Configure the Emulator Plugin
Open your emulator's graphics settings and go to the **Texture Enhancement** tab. Ensure the following boxes are checked:
*   ✅ **Use Texture Pack**
*   ✅ **Use Full Transparencies** (This is crucial for UI elements and particle effects to display correctly).
*   ✅ **Use File Storage instead of Memory Cache** (Recommended for easier swapping of textures).

### Step 5: Clear the Texture Cache (CRITICAL)
If you have played the game before, the emulator has likely saved the original textures in its cache. **If you don't clear the cache, your new textures will not show up.**

1. Close the emulator.
2. Navigate to your emulator's cache folder (For RMG Flatpak, this is usually `~/.var/app/com.github.Rosalie241.RMG/cache/RMG/cache/`).
3. Delete the cache files inside this folder (or just delete the folder for Pokémon Stadium if you can identify it).
4. Relaunch the game. The emulator will take a moment to rebuild the cache using your new PNGs.

---

## License & Legal
This project is licensed under a **Creative Commons Attribution-NonCommercial 4.0 International License (CC BY-NC 4.0)**. 
You are free to share and adapt the custom artwork, but you may not use it for commercial purposes.

*Pokémon and Pokémon Stadium are registered trademarks of Nintendo, Creatures Inc., and GAME FREAK inc. This is a non-profit, fan-made project. No original game ROMs or copyrighted game code are distributed here.*