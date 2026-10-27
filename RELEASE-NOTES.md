# WoW Imito 1.2.0

27 October 2026

## Changes

- **Significantly improved performance**, including CoA / Descension and Wrath Rebuffed. More optimizations are in active development.
- **Automatic hardware setup** selects graphics and performance settings suited to your device.
- **Game crash report** at the top of Settings sends diagnostics directly from the app. Add your own description if you want — no GitHub sign-in is needed.
- **Choose your controls** in AddOns: touch UI or ConsolePort. Connecting a controller no longer changes your choice automatically.
- **Six item quick slots:** spell sets A and B now each have their own three item slots.
- Added **Razer Kishi V2** button labels and a control guide.
- Verified compatibility with standard WotLK on **Warmane** and with **Project Epoch Reborn**.

## HD performance

Average FPS at **1280 × 720 (HD)** with **low graphics settings**:

| Client version | Samsung S26 | Samsung S21 FE |
| :--- | ---: | ---: |
| **Standard WoW WotLK 3.3.5a** | **~60 FPS** | **~41 FPS** |
| **CoA / Descension** | **~60 FPS** | — |
| **Wrath Rebuffed** | **~60 FPS** | — |
| **Project Epoch Reborn (3.3.5a)** | **~60 FPS** | **~52 FPS** |

FPS was measured in **starting locations**. Crowded cities such as **Dalaran, Orgrimmar and Stormwind** may run at lower FPS. Results vary by device and enabled addons; these are averages, not guaranteed minimums. **—** means not tested on that device.

CoA / Descension was tested on a local test realm. For Project Epoch Reborn, use a complete client updated with its official launcher.

## ECO mode

> **ECO mode is strongly recommended for longer play sessions.** Its **30 FPS limit** reduces CPU and GPU workload and helps save battery, so you can play longer on a single charge. The benefit varies by device and game settings.

**ECO caps the game at 30 FPS** to reduce workload and help save battery. In Samsung S26 CoA test, CPU load was approximately **31% lower** and GPU load **47% lower** than at 60 FPS. These are workload reductions, not measured battery-life gains.

## Fixes

- Improved keyboard support for authenticator codes and custom login screens.
- Fixed Android Back closing the game when hiding the keyboard.
- Fixed touch UI remaining visible alongside ConsolePort.
- Fixed ECO mode losing its 30 FPS limit after graphics changes.
- Fixed a frame-limit conflict that could keep FPS below the selected limit.
- Smoothed icon edges and cleaned up button frames. Target is red, jump is light blue and item slots use darker frames.

## Text rendering

For **Wrath Rebuffed**, choose **Settings > Text rendering > Original WoW** for the performance option used in these tests. Choose **Rebuffed: safe/full** if you prefer its enhanced text. Restart the game after changing this setting. Standard WotLK, CoA / Descension and Project Epoch Reborn need no change here.

**[Download APK](https://github.com/MrAnonymz/WoW-Imito/releases/download/v1.2.0/WoW-Imito-Public.apk)** · **[Setup & addons](https://github.com/MrAnonymz/WoW-Imito#start-playing)** · **[Report a problem](https://github.com/MrAnonymz/WoW-Imito/issues/new/choose)**
