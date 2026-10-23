# WoW Imito

Play your own **World of Warcraft: Wrath of the Lich King 3.3.5a (build 12340)** client on an Android phone or tablet, with touch controls. The game runs on the device; a PC is not needed while playing.

**[Download the APK](https://github.com/MrAnonymz/WoW-Imito/releases/latest)** · **[Report a problem](https://github.com/MrAnonymz/WoW-Imito/issues/new/choose)**

Maintained by **Mr Anonymz**. This is an unofficial community project and is not affiliated with Blizzard Entertainment.

## What it does

- Adapts movement, camera, action buttons and menus for touch screens.
- Selects a graphics path from the device's capabilities: Vulkan/DXVK where supported, with an OpenGL fallback.
- Uses a client folder you select, or downloads and unpacks your own direct ZIP link without keeping a second complete archive.
- Lets you set your server address. Sign in inside the game; there is no launcher account login or built-in server download.
- Includes graphics presets, a 30 FPS battery-saving option and optional addons.

**The APK does not include the game client.** You must supply a complete, compatible client and a server account. No particular server is required.

## Requirements

| Requirement | Details |
| --- | --- |
| Android | **12 or newer** |
| CPU / operating system | **ARM64 (`arm64-v8a`)**. A 64-bit chip running a 32-bit Android system is insufficient. |
| Graphics | Working OpenGL ES 3.0 support. Vulkan support and driver features are checked automatically. |
| RAM | **6–8 GB recommended** as a starting point. Devices with 4 GB are experimental; this is not a measured universal minimum. |
| Storage | Room for the unpacked client plus **2 GiB reserve**. If a ZIP's unpacked size cannot be determined, the app initially checks a **20 GiB** budget (about 21.5 GB). Larger clients can require more. |
| Game files | Complete Windows WoW **3.3.5a, build 12340**, including `Wow.exe` and `Data`. |
| Connection | Internet access for downloading and connecting to your selected server. |

The runtime needs internal storage even if you keep game files on an SD card. Writable SD folders are supported by the folder selector, but physical SD-card operation has not yet been verified in this public build. Slow cards may increase loading times and stutters.

Android version and ARM64 support alone do not guarantee compatibility or 60 FPS. Performance also depends on the GPU driver, memory, temperature, resolution and scene. Older devices may need **Low specs** and a lower in-game resolution.

## Get started

1. Download `WoW-Imito-Public.apk` from **Releases** and install it. Android may ask you to allow installation from the app you used to download it.
2. Open **Game files** and choose one option:
   - **Copy from a PC:** put the complete unpacked client in **Internal storage → WoW-Imito → Client**. Create the folders if needed. `Wow.exe` and `Data` may be directly there or inside one client subfolder. **Choose folder** opens this same location. Use **Storage** to select another writable folder or an SD card; `Documents` is not mandatory.
   - **Download ZIP:** paste a direct link to a complete ZIP. Allow file access when prompted. The app unpacks into **WoW-Imito/Client**, checks free space and can continue downloading in the background. Use Pause/Resume if needed. Servers without HTTP Range may require rereading the ZIP on resume.
3. After the client is recognised, **PLAY** and the settings gear become available.
4. In **Settings → Set realm**, enter your server's login address. If you do not change it, the client's existing realm address is retained.
5. Tap **PLAY** and sign in inside WoW.

Avoid `Android/data` and `Android/obb` for manually copied clients. Selecting an existing folder does not create a second 18 GB copy. All-files access is needed for the selected client's game files, configuration and addons.

The first preparation applies low graphics, **800 × 450** and a 60 FPS cap. Later ordinary player settings are retained; **Defaults** and **Low specs** explicitly reset graphics. Required runtime settings and bundled addon files are repaired when necessary without rewriting identical content. The initial setup also writes the client's EULA/TOS acknowledgement flags automatically.

## Bundled addons

These optional addons are included but **OFF by default**. Enable only the ones you want:

| Addon | What it adds |
| --- | --- |
| **Bagnon** | Combines your bags into one inventory window. |
| **NotPlater** | Customisable unit nameplates; a 3.3.5a-compatible alternative inspired by Plater. |
| **OmniCC** | Numeric cooldown timers. |
| **Titan Panel** | Information bar, with mobile battery percentage and FPS integration. |
| **Immersion** | An alternative quest and NPC dialogue interface. |
| **AtlasLoot Enhanced** | Browse dungeon, raid and other loot tables. |
| **GearScoreLite** | Equipment score information. |
| **Deadly Boss Mods (DBM)** | Boss encounter warnings and timers. |
| **SexyMap** | Customisable minimap appearance. |
| **X-Perl UnitFrames** | Alternative player, target, party and raid frames. |

**MoveAnything** (move and customise UI frames) and **MinimapButtonBag** (organise minimap addon buttons) are **ON by default**. The touch-control integration is also prepared automatically.

To enable an optional addon, open **AddOns** on the character-selection screen, tick the addon and its required modules, then enter the game. If you change addon activation while already in the world, **reload the UI** (`/reload`) for the change to take effect. Your saved addon choices are preserved on later launches.

On lower-powered devices, start with optional addons disabled and enable them gradually; extra UI processing can reduce FPS.

## Updates and feedback

Install future public APKs as updates; keep your existing installation and game data. Do not uninstall or clear app data as a routine update step.

Before reporting a problem, search [existing issues](https://github.com/MrAnonymz/WoW-Imito/issues). Include your device model, Android version, APK version and steps to reproduce. Screenshots or a short video help. For performance reports, also include resolution, graphics preset, FPS and what was happening in the scene.

**Do not post passwords, account emails, tokens or unredacted personal logs.** Hide account and character details in screenshots if you do not want them public.

## Release integrity and credits

Releases include a SHA-256 checksum. The public APK package is `pub.wowimito` and its signing certificate subject is **`CN=Mr Anonymz`**. Debugging, USB diagnostics and the benchmark mode are disabled in the distributed APK.

This project builds on WoW Mobile, Winlator, Wine, Box64, DXVK and other components. Their names, authors and licence notices remain intact; they are not claims of authorship by Mr Anonymz. See [third-party notices](THIRD-PARTY-NOTICES.txt) and the notices bundled in the app.
