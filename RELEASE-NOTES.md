# WoW Imito 1.0.0-public

First public Android release for using your own WoW 3.3.5a (12340) client with touch controls.

- Android 12+ and ARM64.
- Automatic hardware checks and Vulkan/OpenGL selection.
- Choose an existing client folder or download your own direct ZIP link.
- Streaming extraction, storage checks, background downloading and pause/resume.
- Shared default folder: **Internal storage/WoW-Imito/Client**.
- Set realm in Settings; sign in inside the game.
- Graphics presets, resolution options, touch controls and optional addons.

Included but **OFF by default**: Bagnon, NotPlater, OmniCC, Titan Panel, Immersion,
AtlasLoot Enhanced, GearScoreLite, Deadly Boss Mods, SexyMap and X-Perl UnitFrames.
Enable desired addons from **AddOns** at character selection; reload the UI after
changing activation in-game. MoveAnything and MinimapButtonBag are **ON by default**.

Download **WoW-Imito-Public.apk** below. You need your own complete game client; the APK does not contain it. Read the repository README for requirements and setup.

This is a production build with debugging, USB diagnostics and benchmark mode disabled. Compatibility and performance vary by device; 60 FPS is not guaranteed. Please report reproducible issues using the repository's bug-report form.

Validation includes a full local client transfer and reaching the game login screen on a physical device, plus targeted tests of the final shared-folder and storage-check changes. The public release was not validated in the game world on every device, and physical SD-card testing remains outstanding.

Verify the APK against **SHA256SUMS.txt**. Keep the existing app installed when applying future public updates.
