# WoW Imito 1.5.1

## Controller support

- Added optional **ConsolePort Legacy** controls for original **Vanilla 1.12.1** and **The Burning Crusade 2.4.3**.
- Use four action layers with your selected controller modifiers, assign spells, items and macros, and use the cursor and Android keyboard in game windows.
- ConsolePort Legacy is disabled by default. Enable it in AddOns; disable it and reload to return to Touch UI.

## Languages

- Added **German, Czech, Polish, Russian, Italian, Simplified Chinese, Japanese, Turkish and Arabic**. Change the language in Options to translate the app and Imito Touch UI, including the tutorial. English remains the default.
- Added fonts for all supported languages and right-to-left Arabic text in Touch UI.
- Translations were made with AI and may contain mistakes. Please report incorrect translations through Report a problem or a GitHub issue.

## Controls and convenience

- Added optional **second-screen controls** for Android handhelds with two separate displays: party targets, trackpad, scrolling and keyboard, with the bottom system bar hidden on the control display.
- Added **ConsolePort modifiers** in Options: choose LT/RT, LB/LT or LB/RB.
- Added **Manage add-ons** for each original client and access to Forever addon folders through Android Files.
- Added **Draw / sheath weapons**, **Link quest** and **Chat language** to the in-game menu.
- Added **Socket gems** to touch item actions and equipped-item details. Use **LT + X** for Shift + right-click in controller cursor mode without ConsolePort.
- Added **Switch WoW account** and **Sign out of Battle.net** for Forever. Automatic game launch pauses while you use the official launcher to change accounts.

## Performance and fixes

- Improved original-client graphics defaults and TBC CPU scheduling on phones with different types of CPU cores.
- Reduced graphics cache, video-memory and compiler-worker budgets for entry-level PowerVR GPUs.
- Fixed graphics resource cleanup, shared texture lifetime and texture readback in the VirGL compatibility renderer.
- Fixed overlapping graphics checks and late probe results when starting or resuming the app.
- Fixed controller camera movement triggering unwanted targeting or interaction.
- Added visibility controls for ConsolePort L2/R2 icons and fixed their visibility across bar layouts.
- Updated compatibility with the Wrath Rebuffed diagnostic component and improved startup and native crash reports.
- Enforced Forever's **8 GB physical RAM minimum** before installation or launch; RAM expansion does not count.
- Fixed Forever client detection with different executable filename capitalization and removal-button visibility for fresh or incomplete setups.
- Fixed clipped text on the client setup removal button.
