# WoW Imito 1.5.6

## Graphics and startup

- Fixed WotLK startup on Mali-G52 r1 when the bundled Vulkan driver passes its initial check but cannot open a Direct3D display. The launcher selects the working graphics profile automatically.
- Fixed black tiles on the WotLK login screen with the affected Mali-G925 driver. The launcher automatically selects the working graphics profile.
- Fixed a black screen before the first frame on Mali-G57. Vanilla now reaches the world on the Galaxy A15 with the bundled PanVK driver.
- Corrected swapped red and blue channels on Mali-G615.
- If PanVK loses the device after the first frame, the launcher tests another buffer layout. If it also fails the check, the next launch uses the next compatibility profile.
- Fixed shared-texture synchronization in VirGL. Vortek now waits for the previous frame’s texture read before reusing its buffer.
- Fixed VirGL startup and in-game command handling when Android refuses to create or restore a graphics context. Failed commands no longer submit a frame fence.
- Vortek reuses completed frame-copy commands and releases failed allocations when rebuilding the display.
- Fixed the rejection of compatible Turnip packages on Adreno. Five affected driver packages now pass import and the Vulkan startup check.
- After a graphics failure the launcher can try another profile on the next run. Your imported driver is kept.
- Fixed a startup crash when a Vulkan driver returned a different number of extensions on the second query.
- Fixed corruption when passing Vulkan driver names and descriptions from Android to the Windows client.
- Fixed graphics helper libraries that could fail to load on Android phones with 4 KB pages. The same libraries also support 16 KB pages.

## Display and performance

- TBC and WotLK start at 800 × 450 on lower-end devices. The in-game picker offers higher resolutions, including modes that match the phone’s aspect ratio.
- Vanilla keeps the selected resolution after restarting.
- Restored the faster DXVK profile on affected Galaxy S26 devices that retained an older fallback after updating.
- On Galaxy S26 with Xclipse 960, Forever’s optional 60 FPS Eco mode scales the 3D scene separately from the interface. Eco 40 remains the default.
- On lower-performance devices Vanilla starts at 800 × 480 with ground clutter disabled. Saved resolution and ground-clutter settings take precedence.
- Fixed the Vanilla resolution menu showing just one option on wide phones. It now includes supported 4:3, 16:9 and full-display modes.

## Touch controls and controllers

- Fixed the touch joystick disappearing in ghost form. In WotLK you can close chat over the corpse prompt, keep your draft and move again.
- Restored controller jumping in Vanilla and OctoWoW. Pick up a spell, item or macro and press a face button to assign it to the selected action layer.
- In TBC, holding a controller modifier while tapping Assign Spell now binds the spell to the intended slot. The assignment button clears the warlock pet tab.
- Fixed the menu and bags opening chat in TBC. Repositioned controller hints that covered other controls in Vanilla and TBC.
- Fixed ConsolePort activation in WotLK so the left stick, camera and action buttons work in game.
- The keyboard button can enter text in the WotLK character deletion dialog.
- The map, menu, backpack and chat icons now use muted colors. Draw/sheath, target and jump have new symbols.
- Walk/run uses a boot. Autorun uses two footprints and an A badge. The Write button stays legible at lower resolutions.

## Forever and audio

- Fixed Forever’s touch controls disappearing when combat restricted access to action counts, cooldowns or range checks.
- On the tested Adreno 829 driver, Forever can pass texture uploads directly to Vulkan when the driver and graphics layers both support the compressed formats.
- Fixed audio playback position overflowing after roughly three hours of stereo sound.

## Using a second screen

- Connect the second display before starting the game. The HUD shows the live minimap, chat, quest log and player and target information.
- Switch to Targets to select party members, Trackpad to move the pointer or scroll with two fingers, or Keyboard to type.
