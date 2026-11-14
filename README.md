[English](README.md) · [Deutsch](docs/readme/README.de.md) · [Čeština](docs/readme/README.cs.md) · [Polski](docs/readme/README.pl.md) · [Русский](docs/readme/README.ru.md) · [Italiano](docs/readme/README.it.md) · [Español](docs/readme/README.es.md) · [简体中文](docs/readme/README.zh-CN.md) · [日本語](docs/readme/README.ja.md) · [Türkçe](docs/readme/README.tr.md) · [العربية](docs/readme/README.ar.md)

<h3 align="center">☕ Support development</h3>

<h3 align="center">If you enjoy WoW Imito, you can help keep development going: **[Buy Me a Coffee](https://buymeacoffee.com/mranonymz)** · **[Donate via Stripe](https://buy.stripe.com/fZu7sM8Gm4UA2XGaOIbII01)**</h3>

<table align="center">
  <tbody><tr>
    <td align="center"><img width="180" height="180" alt="Donation QR code" src="https://github.com/user-attachments/assets/03e67232-7b00-475d-a5e5-cfd65cc6d4d7" /></td>
    <td align="center"><img width="158" height="180" alt="QR" src="https://github.com/user-attachments/assets/5fa4f4ed-4d05-4425-9198-6bd32894773e" /></td>
  </tr></tbody>
</table>

<h3 align="center">Supporter thanks</h3>

<p align="center">Thank you for supporting WoW Imito! A good latte makes fixing bugs a little more enjoyable and a little less stressful.</p>

<table align="center">
  <thead><tr><th>Supporter</th></tr></thead>
  <tbody><tr><td><strong>Amunkyinatuxedo9</strong></td></tr></tbody>
</table>

![WoW Imito — Your Azeroth. Anywhere.](assets/wow-imito-banner.jpg)

# WoW Imito

**Your Azeroth. Your character. Now on Android.**

Run original and custom **World of Warcraft** clients on Android phones, tablets and handhelds — including **WoW Forever with official Battle.net login and updates**. Use **Imito Touch UI or a controller**, with a **live second-screen HUD** on dual-screen handhelds. See the [supported clients](#compatibility) for Vanilla, TBC, WotLK and server-specific versions. No PC is needed while playing.

**[Download APK](https://github.com/MrAnonymz/WoW-Imito/releases/latest)** · **[Latest patch notes](https://github.com/MrAnonymz/WoW-Imito/releases/latest)** · **[All releases](https://github.com/MrAnonymz/WoW-Imito/releases)**

> [!IMPORTANT]
> **Found a bug? Open Settings > Report problem in WoW Imito.** Describe what happened and what you were doing when the problem occurred. The app includes device and game details in the report to help investigate the cause.
>
> For **feature requests or support for another device or game client**, choose **Other** and describe what you would like added.
>
> If WoW Imito cannot open, [create a GitHub issue](https://github.com/MrAnonymz/WoW-Imito/issues/new/choose) and include your device model, Android version, app version and the error you see.

## Start playing

**Requires Android 12+, an ARM64 processor and 64-bit Android. Forever requires 8 GB RAM or more.** Game files and server accounts are not included.

1. Install WoW Imito and open it.
2. Copy the complete client required by your server to internal storage or an SD card, or download a ZIP through **Game files**. For **Forever**, select it in the client list; official Battle.net handles sign-in, downloads and updates. First setup may take a few minutes.
3. Select the detected client and confirm its server address when prompted. Use **Game files** to select a folder manually or **Settings > Set realm** to change the server.
4. Tap **PLAY**, sign in and choose your character.

App updates are offered automatically, using smaller delta downloads when available. Enable **Options > Support > Automatically update WoW Imito** for automatic downloads and installation; Android may still require permission or confirmation. Tap the app name/version in the launcher for offline patch notes.

<details>
<summary><strong>Hardware & storage</strong></summary>

**Snapdragon 888-class performance and 6 GB RAM** are suggested starting points for classic clients. Graphics support and performance vary by device.

| Client | Suggested free storage before installation |
| --- | --- |
| Vanilla / TBC | 8 GB / 12 GB |
| Standard WotLK | 22 GB |
| Wrath Rebuffed | 30 GB |
| CoA / Descension community client | 50 GB |

Storage needs vary by client and updates. Use the complete client required by your server, an internet connection and your own account.

</details>

## Features & controls

- **Imito Touch UI:** movable, resizable controls and pinnable chat. Open **Menu > Touch UI > Show tutorial** to learn the controls; **Save & reload** keeps your layout.
- **Controllers & addons:** ConsolePort and optional addons, with availability depending on the game client; setup details below.
- **Dual-screen handhelds:** live minimap, chat, quests and player/target information on a separate display. Enable **Options > Controller > Second-screen controls**; use **Displays** to reconnect. Trackpad and keyboard views are also available.
- **Performance options:** ECO limits of **30, 40, 50 or 60 FPS**, **Low specs**, and Android Vulkan driver imports (**.zip / .wcp**) under **Options > Graphics > Graphics driver** for classic clients. The app checks the driver before applying it. **Automatic** remains the default.
- **Languages:** English, German, Czech, Polish, Russian, Italian, Spanish, Simplified Chinese, Japanese, Turkish and Arabic. **Options > Game > Language** changes the app, Touch UI and offline patch notes. English is the default; AI-assisted translations may contain mistakes — please report them.

> [!TIP]
> **ECO 30–40 FPS is strongly recommended for Forever** to reduce CPU/GPU load and temperatures. Performance depends on your device, settings and scene.

<a name="compatibility"></a>

## Supported clients & devices

<details>
<summary><strong>Supported & tested clients</strong></summary>

| Client | In-game testing | Game updates |
| :--- | :--- | :--- |
| **World of Warcraft - Forever (8 GB+ RAM)** | ✅ Tested | Official Battle.net login, downloads and updates |
| **WoW Vanilla 1.12.1** | ✅ Tested on a local test realm | Use your server's usual update method |
| **The Burning Crusade 2.4.3** | ✅ Tested on a local test realm | Use your server's usual update method |
| **Wrath of the Lich King 3.3.5a** | ✅ Tested | Use your server's usual update method |
| **Warmane WotLK 3.3.5a** | ✅ Tested | Use your server's usual update method |
| **[CoA / Descension community client](https://coa-development.org/)** | ✅ Tested on a local test realm | Direct updates in WoW Imito |
| **[Wrath Rebuffed](https://whitemane.gg/en)** | ✅ Tested | Direct updates in WoW Imito |
| **[Project Epoch Reborn (3.3.5a)](https://project-epoch.org/)** | ✅ Tested | Direct updates in WoW Imito |
| **Grimfall (3.3.5a)** | ✅ Tested | Direct updates in WoW Imito |
| **OctoWoW (Vanilla)** | ✅ Tested in game | Direct updates in WoW Imito |
| **Triumvirate (3.3.5a)** | ✅ Tested in game | Direct updates in WoW Imito |

Use your server's complete client. The CoA entry refers to the community distribution, not a confirmed test of the official Ascension service.

For supported game updates, use **PLAY** or **Settings > Update [client name]**. Standard Vanilla, TBC and Wrath use your server's update method. For Rebuffed performance, try **Settings > Text rendering > Original WoW**.

</details>

<details>
<summary><strong>Supported & confirmed devices</strong></summary>

Check marks indicate successful in-game testing, not guaranteed FPS. Other devices may work too.

| Device | Confirmed working |
| :--- | :---: |
| **Samsung Galaxy S26 (SM-S942B)** | ✅ |
| **Samsung Galaxy S21 FE (SM-G990B2)** | ✅ |
| **Samsung Galaxy S23 Ultra** | ✅ |
| **Samsung Galaxy S26 Ultra** | ✅ |
| **Motorola Edge 70 Max** | ✅ |
| **AYN Odin 2** | ✅ |
| **POCO X7 Pro** | ✅ |
| **Google Pixel 10 Pro XL** | ✅ |
| **Samsung Galaxy Z Fold7** | ✅ |
| **Samsung Galaxy S25 (SM-S931B)** | ✅ |
| **Samsung Galaxy Tab S6 LTE (SM-T865)** | ✅ |
| **OnePlus Nord CE 3 Lite** | ✅ |
| **Redmi Note 11 (Snapdragon 680)** | ✅ |
| **POCO F3** | ✅ |
| **POCO F8 Ultra** | ✅ |
| **POCO X6 5G (23122PCD1G)** | ✅ |
| **HONOR X8d (LNA-LX3)** | ✅ |
| **AYN Thor** | ✅ |

[Confirm your device](https://github.com/MrAnonymz/WoW-Imito/issues/new?template=device-confirmation.yml) to help grow this list. The Pixel 10 Pro XL confirmation used the player's custom graphics settings.

</details>

<details>
<summary><strong>FPS measurements</strong></summary>

**Classic clients — [1.4.1](https://github.com/MrAnonymz/WoW-Imito/releases/tag/v1.4.1), HD 1280 × 720, Low graphics. Standing / camera movement:**

| Client | S21 | S26 |
| --- | --- | --- |
| Vanilla 1.12.1 | 105.5 / 75.5 | 174.5 / 128.5 |
| The Burning Crusade 2.4.3 | 102 / 77.5 | 191 / 120 |
| Wrath of The Lich King 3.3.5a | — | 135.5 / 123 |
| Wrath 3.3.5a (Warmane) | — | 110.5 / 84 |
| Wrath Rebuffed | — | 100.5 / 73 |
| Grimfall | — | 150 / 117 |
| Project Epoch Reborn | — | 95.5 / 84 |
| OctoWoW | 102 / 92 | 163.5 / 124.5 |
| Triumvirate | — | 177.5 / 133 |
| CoA / Descension | — | 102 / 86.5 |

**Forever — [1.5.0](https://github.com/MrAnonymz/WoW-Imito/releases/tag/v1.5.0), HD, Low graphics, 85% render scale, ECO off:**

| Client | S26 standing | S26 camera movement |
| --- | ---: | ---: |
| World of Warcraft - Forever | 46.0 FPS | 55.9 FPS |

Results vary with hardware, graphics settings, addons, scene complexity and temperature.

</details>

<details>
<summary><strong>Addons & controller setup</strong></summary>

Optional addons are **OFF by default**; enable them in **AddOns** on character selection. Availability depends on the client:

**Bagnon, ConsolePort, LoseControl, NotPlater, OmniCC, Titan Panel, Immersion, AtlasLoot Enhanced, GearScoreLite, Deadly Boss Mods, SexyMap and X-Perl UnitFrames.**

**MoveAnything** and **MinimapButtonBag** are **ON by default**. Use **/reload** after changing addons in game.

On Wrath, choose **Imito Touch UI** or **ConsolePort**, and keep **WoW Imito Input** enabled. Connecting a controller does not change this choice. Original Vanilla and TBC offer optional **ConsolePort Legacy**; disable it and reload to return to Touch UI.

</details>

## Gameplay screenshots

![WoW Imito gameplay](assets/screenshots/gameplay-01.png)

![WoW Imito quest dialogue](assets/screenshots/gameplay-02.png)

![WoW Imito inventory](assets/screenshots/gameplay-03.png)


---

Maintained by **Mr Anonymz**. Unofficial community project, not affiliated with Blizzard Entertainment or the listed servers. [Third-party credits and licences](THIRD-PARTY-NOTICES.txt) · [Logo credits](assets/clients/CREDITS.txt).
