# parasite-eve-pc-recomp
## Parasite Eve (1998) — Native Windows x64 Release (v1.0.0)

This is a pre-compiled native Windows x64 runtime build for **Parasite Eve** (NTSC-U / `SLUS-00662`), based on the `PSXRecomp` static recompilation framework. No CMake, Clang, or Visual Studio installation is required to run this release!

### Legal Notice
**No copyrighted assets are included in this release.** To play the game, you must supply your own legally dumped `SLUS_006.62` executable and `.bin`/`.cue` disc images from your personal copy of *Parasite Eve*.

### Quick Start Guide
1. Download and extract the attached archive (`ParasiteEve_PC_v1.0.zip`) into any folder.
2. Create a clean directory without special or Cyrillic characters (e.g., `C:\PE\`).
3. Place your legally dumped Disc 1 and Disc 2 files into `C:\PE\` and rename them to:
   * `pe1.bin` and `pe1.cue`
   * `pe2.bin` and `pe2.cue`
   *(Make sure the `.cue` files reference the exact `.bin` filenames inside).*
4. Extract `SLUS_006.62` from Disc 1 and place it into `C:\PE\`.
5. Open PowerShell or Command Prompt in the folder containing `PSXRecomp.exe` and run:

```powershell
./PSXRecomp.exe --elf "C:/PE/SLUS_006.62" --disc "C:/PE/pe1.cue" --disc "C:/PE/pe2.cue" --audio-backend sdl
```

*(Tip: You can create a Windows desktop shortcut with this command for one-click launching).*

### Included Enhancements
* **PGXP Geometry Correction:** Fixes PS1 polygon jitter and texture warping.
* **2x Internal Resolution:** Enabled by default via the included `settings.toml`.
* **Dual-Disc Ready:** Seamless disc switching support pre-configured via launch arguments.
