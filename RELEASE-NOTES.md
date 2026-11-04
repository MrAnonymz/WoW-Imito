# WoW Imito 1.4.0 — QoL Update

## Highlights

- **Rebuilt interactive Touch UI tutorial.** The guide first introduced in **1.3.10** had too many broken and confusing steps, so it has been extensively reworked. Clearer prompts, connected pointers and matching gold highlights now show where to tap. Practice movement, spells, items, macros and UI settings; completed actions move the guide forward automatically.
- **More comfortable mobile windows.** Larger game menus, options, quest and shop windows make text easier to read and buttons easier to tap, while keeping windows within the screen.

## Changes

- **Pin chat while playing.** Open Chat and turn **Pin** on for a compact, readable chat panel. Move or resize it in **Menu > Touch UI**.
- **Resize individual controls.** In **Touch UI**, tap a control and use **−25% / +25%** to adjust it independently. This includes the joystick, spells, item slots and utility buttons. **Default size** restores that control; **Save & reload** keeps the changes.
- Added short descriptions to the game menu entries.
- Improved problem reports with more information about the game session, input, graphics and available crash details.

## Fixes

- Fixed tutorial steps getting stuck, pointing at the wrong button or being covered by other windows.
- Fixed tutorial progress restarting after saving and reloading the UI.
- Fixed a legacy-client Lua error that could prevent the joystick from appearing.
- Fixed the joystick's touch area blocking spell assignment in enlarged windows.
- Fixed labels being cut off in enlarged game menus on older clients.
- Prevented delayed camera gestures from building up into a sudden turn when input processing briefly slows down.
- Widened the **XP bar** and improved tapping across its full area.
- Matched the visible sizes of Menu, Friends and Chat buttons.
- Replaced a repeated spell-assignment lesson with guidance for the second spell row.
- Fixed repeated hardware-change prompts resetting game preferences in the managed runtime.
- Corrected graphics-memory compatibility checks and cleanup when a system driver rejects an allocation.

**Restart the tutorial anytime: Menu > Touch UI > Show tutorial.**

**Report follow-up:** closing older tickets does not confirm that every reported device-specific crash is resolved. If the problem returns, use **Settings > Report problem** in **1.4.0**. Reports now include more complete runtime identification and memory information during startup to help investigate failures that could not be reproduced.
