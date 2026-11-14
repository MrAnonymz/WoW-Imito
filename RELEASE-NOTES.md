# WoW Imito 1.5.2

## Dual-screen handhelds

- Added a live minimap, chat, quest tracker and player/target information for a separate second display.
- The HUD adapts to the second screen’s available space, with readable panels and subtle backgrounds.
- Switch between the HUD, target controls, trackpad and keyboard. Reopen the display chooser after Cancel or Disconnect.
- Restore the main-screen interface when disconnecting or changing display settings.

## Touch UI

- Moved Draw / sheath weapons from the game menu to a small sword button. Move and resize it in Touch UI, then save your layout.
- Moved Friends into the game menu and updated the tutorial.
- Added a gear icon and a wider, responsive game menu with up to three columns to reduce scrolling.
- Added touch controls for removing glyphs and deleting items, with confirmation before removal.
- Fixed blank action icons when a macro references a texture unavailable in the selected client.

## WoW Forever

- Added support for selecting an existing WoW Forever installation on internal storage or an SD card. Battle.net handles verification and updates; removing app setup keeps the selected game files.
- Existing WoW Forever installations now appear in automatic client search.

## Graphics drivers

- Added per-client imports of compatible Android Vulkan drivers (.zip and .wcp) for classic clients, with compatibility checks and an option to return to Automatic.

## Languages

- Added Spanish for the app and Imito Touch UI. Select Español in Options; English remains the default.
- Offline patch notes now follow the language selected in the app.
- Completed translations for loading messages, dialogs, controller guides and Touch UI across all supported languages.
- Translations are AI-assisted. Please report incorrect wording through Report a problem or a GitHub issue.

## Fixes

- Fixed original-client startup when the runtime loader path differs from the current Android app installation or profile.
- Applied the same loader handling to Wine child processes.
- Fixed startup failing after disabling optional addons such as NotPlater in Wrath and The Burning Crusade.
- Detect missing or invalid required client libraries before launching the game.
- Detect games that exit before their first frame instead of continuing to wait for Wine's desktop.
- Improved startup reports with loading stages and concise library and graphics failure details.
- Improved keyboard activation for login and newly created addon text fields. A movable keyboard button starts in the top-left corner when automatic activation is unavailable.
- Corrected graphics cache paths for original clients and kept startup available when optional cache storage is unavailable.
- Corrected missing graphics capabilities on devices using the VirGL fallback.
- Fixed graphics synchronization errors that could leave original clients waiting during startup.
- Fixed unwanted cursors during touch play while preserving mouse and controller controls.
