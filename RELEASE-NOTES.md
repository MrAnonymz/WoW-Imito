# WoW Imito 1.4.1

## Highlights

- **More responsive touch controls after loading and reloading.** Jump and Target become usable as their positions are confirmed. Completing the rest of the layout no longer interrupts an unchanged held Jump or pending Target tap.
- **Camera and runtime fixes.** Corrected a runtime calculation error behind reproduced camera drift and incorrect character facing. Improved CoA/Descension's first Target response after a UI reload.
- **Performance and responsiveness improvements.** Faster touch-control readiness across Vanilla, TBC and Wrath, plus runtime fixes for camera movement and reduced background profiling work in supported Rebuffed clients.

## Fixes and improvements

- Redesigned **Options** with grouped settings, consistent controls and a clearer controller guide. **Report a problem** is highlighted at the top, and the update button names the selected client.
- Refreshed **Game reports** and issue categories with clear action buttons and descriptions.
- Corrected garbled text while preparing addons.
- Optional **automatic app updates** in Options, with Android confirmation when required.
- Improved app-update cancellation and recovery after storage errors or screen recreation.
- Options and reports remain available before selecting a client.
- Corrected the status shown after selecting a client when automatic discovery is off.
- Disabled unsupported game updates for standard **Vanilla, TBC and Wrath** clients.
- Turning on **Eco mode** opens a choice of **30, 40, 50 or 60 FPS**. Your choice is saved, and turning Eco off restores your normal FPS setting.
- Improved camera dragging after using action buttons and the Objectives tracker.
- Quest notifications now fit within the **Objectives** tracker.
- Improved recovery after device sleep and temporary graphics stalls.
- Corrected game-window activation after returning to the app.
- Physical-mouse buttons are released on focus loss, pointer-capture loss and cancelled input, without releasing buttons held by other input devices.
- Corrected mouse and gamepad event handling, fixed input interruptions caused by long controller names, and prevented system fingerprint inputs from being detected as game controllers.
- Fixed CoA custom spellbook assignment accidentally casting the selected spell, and corrected TBC addon loading.
- The second spell row starts off for new profiles. Existing choices are preserved, and its tutorial lesson practices both turning it on and off before **Save & reload**.
- Fixed **Friends** and **Pin** positioning and overlap with native chat tabs.
- CoA video options now preserve the selected FPS setting.
- Updated the Wrath Rebuffed performance fix for the current client.
- Replace an equipped bag, quiver or ammo pouch through **Equip bag**, with confirmation for occupied slots and the game's normal item and capacity rules.
- Prevented unintended item moves in **Vanilla** when another item or spell is selected.
- Drag supported quest text and other scrollable dialog backgrounds without picking up items or changing their native controls.
- Fixed macro icon selection, clipped assignment buttons and touch handling in native lists.
- Auction windows now fit the screen, keeping their tabs and auction controls accessible.
- Tap the app name and version to read **release notes offline**, with clearer headings, spacing and a performance table.
- Improved game startup, cancellation and shutdown, including cleanup after incomplete startup.
- Long game starts now show the latest startup stage and offer **Keep waiting** or **Cancel startup** after one minute.
- File operations resume after returning from Android storage-access settings.
- Added progress and cancellation during ZIP verification, with safer interrupted imports and verified reuse of renewed download links.
- Fixed graphics-memory compatibility checks and corrected the compression library's layout for Android devices using 16 KB pages.
- Improved diagnostic information for delayed controls and runtime failures.

**Open or resume the tutorial: Menu > Touch UI > Show tutorial.**

## Measured performance

**FPS: standing / camera movement**

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
