# WoW Imito 1.3.0

## New: Vanilla & The Burning Crusade

**Play Vanilla 1.12.1, The Burning Crusade 2.4.3 and Wrath of the Lich King 3.3.5a on Android.** Use the complete client required by your server. Touch controls, inventory actions and the movable interface are available across all three versions.

## Changes

- Added **Grimfall client support**, including in-app game updates.
- Launcher backgrounds and expansion titles now follow your selected **Vanilla, TBC or WotLK** client.
- **Update WoW Imito from the launcher.** A new-version notice lets you download the update now or leave it for later.
- **Choose how clients are found.** Automatic search is on by default. Turn it off in Settings to use the small search button instead.
- **Make the controls your own.** Open **Move Touch UI** in the in-game menu, drag individual controls and save your layout. **Defaults** restores the original layout; **Mirror** swaps its sides.
- Added compact **pet and class panels**, with visible active commands, stances and modes.
- Inspect **item stats and compare equipped gear** from the inventory. **Sell** is available while a merchant is open.
- **ECO mode now limits the game to 40 FPS** to reduce workload and help your battery last longer.

## Fixes & improvements

- Fixed a memory-access bug associated with reported **Error #132** crashes on Retroid and Warmane clients.
- Fixed a reproduced crash when entering the world with OpenGL, along with garbled text caused by unsupported graphics features.
- Improved handling of graphics-memory allocation failures.
- Improved crash reports so future reports retain more useful details about game errors.
- Fixed the character-name keyboard for Grimfall and improved login-keyboard detection at lower resolutions.
- Fixed initial hardware prompts staying hidden behind the loading screen in original and modified clients.
- Fixed the Wrath Rebuffed update loop and improved interrupted-download recovery. Updates now complete in the launcher before the game starts.
- Fixed a previous failed update leaving the game on a slower graphics fallback. The app rechecks supported graphics after a completed client update, with protection against repeated failing retries.
- Preserved player settings between the login screen, entering the world and reloading the UI.
- Kept touch controls available when using minimap buttons and expanded their support across Vanilla, TBC and WotLK.
- Added a compact experience bar and removed hidden original buttons that intercepted touches.
- Improved update-progress readability and reduced flickering between download and installation messages.

Further performance improvements are in active development.

> **For players who reported crashes:** fixes are included, but confirmation on every affected device is still pending. If the problem returns, update to **1.3.0** and send a fresh report through **Settings > Game crash report**.

## Performance — HD 1280 × 720

Average FPS at low graphics settings:

| Client | Samsung Galaxy S26 | Samsung Galaxy S21 FE |
| --- | ---: | ---: |
| **Vanilla 1.12.1** | **~60 FPS** | **~60 FPS** |
| **The Burning Crusade 2.4.3** | **~60 FPS** | **~56 FPS** |
| **Wrath of the Lich King 3.3.5a** | **~60 FPS** | **~51 FPS** |
| **CoA / Descension** | **~60 FPS** | — |
| **Wrath Rebuffed** | **~60 FPS** | — |
| **Project Epoch Reborn** | **~60 FPS** | **~52 FPS** |
| **Grimfall client (3.3.5a)** | **~60 FPS** | — |

Measurements were taken in **starting locations**. Crowded cities such as Dalaran, Orgrimmar and Stormwind may run at lower FPS. Results vary with device, temperature, settings and addons; **—** means not measured on that device. Wrath Rebuffed was measured with **Original WoW** text rendering.

**[Download APK](https://github.com/MrAnonymz/WoW-Imito/releases/download/v1.3.0/WoW-Imito-Public.apk)**
