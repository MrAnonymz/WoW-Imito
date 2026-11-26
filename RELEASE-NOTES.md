# WoW Imito 1.5.12

- Rebuffed updates: reduced memory use when validating large update lists, preventing the reproduced memory-exhaustion failure.
- Rebuffed: extended the frame-recorder workaround to the current official client component.
- Touch controls: prepare the pointer as soon as a spell or item button is pressed, improving first-tap activation.
- Forever: reconnect action buttons that become available after the touch UI first loads.
- Extra action bars now stay clear of buff and debuff icons as those displays change size or visibility.
- Correctly recognize disabled extra bars while enabling the three action bars used by touch pages A, B and C.
- Graphics detection can continue through a bound service when Android blocks a background service start.
- Forever: Reload can stop and restart the tracked Battle.net installer if its normal shutdown gets stuck.
- Forever: extended accurate texture decoding to the affected Mali-G615 and PanVK driver versions.
- Fixed stale images in redirected game windows when their rendering texture is replaced, resized or destroyed.
- Removed an unused 32-bit scripting tool from the Forever runtime after a Windows Defender detection; updates also remove its old managed links.
- Prevent returning to the launcher when a temporary game-named process exits while another game process from the same session is still running.
- Forever: fixed a missed game-exit notification that could leave a black screen after the game window closes.
- Forever: fixed black and stale image areas with the affected Mali-G1-Ultra and PanVK driver combination.
- Forever: fixed occasional stale frames on the affected Xclipse driver by waiting for Vulkan rendering to finish before copying the image.
- Classic clients: fixed a startup crash when querying GPU memory through Vortek.
- Removed unused development files from the public app package.
- Reports now include specific Wine startup errors and existing render/Touch UI counters to help identify failures before entering the world.
- Action bars 4 and 5 use a single centered row with slightly larger touch targets. Fixed bars moving over touch controls after opening the spellbook or bags.
- Added a return to WoW Imito after updating, with an Open notification when Android requires a tap.
- Touch UI: fixed overlapping chat captions and missing profession labels. Pinned chat defaults above the joystick, and extra-bar icons scale together with their frames.
- Forever: confirm your WoW account once, then launch automatically with that account after Battle.net restores it. Use the account option in Settings to choose again.
- Classic clients: avoid the bundled PanVK path that corrupts textures on the reported Mali-G52 driver combination.
- Game files: download complete OctoWoW, Triumvirate and Grimfall clients from official sources, with background progress, pause and resume.
- Existing clients on the phone or SD card are offered before a new download. Normal updates reuse the selected client and preserve its settings.
- Launcher dialogs: balanced button placement, clearer primary actions and missing translations in Game files, client selection and storage dialogs.
- Forever: added a targeted frame-synchronization workaround for black or flickering login screens on the reported Mali-G720/PanVK combination.
- The launcher guide now shows the complete-client download option and matches the updated Game files buttons.

If a problem persists after updating to 1.5.12, please send a new report from that version and describe what happened.
