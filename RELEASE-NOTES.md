# WoW Imito 1.5.7

Please update to 1.5.7 and retry the steps from your original report. If the problem persists, send a new in-app report immediately afterward and include the previous issue number if you have it.

## Classic client graphics

- Fixed WotLK failing to start on wide displays when the Mali Vulkan driver supported the game window size but the app rejected widths above 2,048 pixels.
- Classic clients use exact Vulkan texture decoding on the affected Mali-G720 r1 driver to avoid block artifacts on the Poco X7 Pro. This also covers a manually imported copy of the same driver.
- Fixed black tiles on the WotLK login screen with the affected Mali-G720 driver. Classic clients now select the working graphics profile automatically.
- On the Mali-G615, G1-Ultra and G720 driver revisions that repeatedly lost the first frame, classic clients now test linear Vulkan presentation before launch and use OpenGL ES if that test fails.
- If the bundled Mali Vulkan driver loses the device after the first frame, classic clients now remember to try a different buffer layout on the next launch even if the game closes immediately.
- The classic renderer retries a failed first frame or resize. Previously it could keep showing the loading screen even after the game supplied valid frames.
- Classic Vulkan clients keep the last visible frame if the first image copy fails or the game window changes during the copy.
- VirGL and Gladio now keep the previous image visible if the first OpenGL frame fails. The next valid frame replaces it without clearing the game window first.
- VirGL avoids switching OpenGL contexts twice for every consecutive batch of game commands. It still checks that the GPU has finished the earlier work.
- The in-game resolution menus in TBC and WotLK now offer standard sizes such as 800 × 450 alongside modes fitted to the phone and its full display resolution.
- VirGL now uploads every requested cube-map face and compressed texture layer. Smaller mip levels of vertically flipped textures also update at the correct position.
- VirGL now reads back every requested face or layer into its own rows. This preserves neighbouring texture data when a game reads part of a texture.
- Fixed incomplete lists of screen formats and presentation modes during classic Vulkan startup. The game can retry graphics initialization after an interrupted connection.
- Fixed two ways classic Vulkan clients could freeze while waiting for the GPU. A system signal no longer drops the frame notification, and a shortage of worker threads no longer blocks the game command needed to finish the wait.
- Fixed VirGL copying the wrong part of a texture when the source and destination use different faces, offsets or mip levels. Region copies now allocate only the pixels they need.
- Fixed the classic loading screen covering an already-rendered login window when Wine mapped or identified it late. VirGL and Gladio now report the first completed frame even if the game draws that screen only once.
- Fixed classic OpenGL ES rendering that could stall when loading a new area. Visibility queries now read the result from the context and buffer location where the game requested it.
- Fixed classic Vulkan startup failing when a driver provided the required core capabilities under Vulkan 1.1 but omitted optional extension names. If the driver fails to enumerate a graphics adapter, the client now receives the startup error.
- Fixed classic clients freezing while waiting for a graphics buffer or an already-signalled Vulkan fence. Vulkan and Gladio now return a reply even when there is no file descriptor to transfer.
- Classic Vulkan startup now preserves the features DXVK requests. Checking support for transform feedback could previously enable unrelated graphics options during device creation.
- Fixed a classic Vulkan memory allocation error when several game buffers share one allocation. If the driver cannot export that memory, automatic mode now retries with a supported Android import.
- Classic Vulkan now reports which shared synchronization handles it can actually export. This avoids selecting an unsupported import path and requesting the wrong handle type at startup.

## Forever graphics and performance

- Fixed incorrect colours and transparency in compressed Forever textures on the affected Mali-G925 driver.
- Forever now uses exact texture decoding on the affected Mali-G1-Ultra driver to preserve colours and transparency when copying textures.
- Forever now loads its Vulkan texture compatibility layer on PowerVR drivers that lack native BC compression and correctly registers the Adreno 829 texture path.
- Forever now keeps the last image when a window subscribes to frame updates. Software and Vulkan frames can replace each other without leaving a black window or losing part of the picture.
- Forever keeps the last pending frame valid when the game resizes its window and now displays software image updates sent directly to a Vulkan window. If the first Vulkan frame fails to load, the previous image stays visible and the next frame can still be displayed. Equal-sized login and game windows now switch to the front window when it presents its first frame.
- Forever preserves the rest of the window when Vulkan updates only a rectangle. Importing a shared graphics buffer in classic clients and Forever no longer allocates a second full-size pixel buffer.
- If Android reports low memory or stopped the previous Forever session for that reason, the next launch reduces shader compilation and runtime cache memory.
- Forever keeps Battle.net available when Android cannot read the game process list. Replacing the game window during login or a resize now also cancels the pending exit check.
- Forever now processes a burst of window changes in one rendering update. Closing a dialog or an old login window while the game remains visible no longer starts the game-exit check.
- Forever now starts at 600p on 8 GB devices when no valid resolution is saved. Existing resolutions and later changes are kept.

## Installation, client files and networking

- Selecting a classic client folder now works even if it still contains an unused Battle.net manifest or Forever directory.
- A complete classic client now appears in the library even if the folder was previously saved as Forever and still contains a valid manifest from an unfinished Battle.net install.
- WotLK keeps the language selected in Config.wtf if its archives are intact. When a language patch is truncated, it uses another complete installed language or names the damaged file before launch.
- After the WotLK #121 crash caused by an unreadable survey table, the launcher can use another installed language that contains the table and uses the same realm.
- If OctoWoW finds a missing or damaged audio or video library when you press Play, you can open the official repair directly from the error message, even after a recent update check.
- The launcher reads just the version data when identifying classic clients, reducing memory use with large game executables. Checks before Play also read the executable and its required libraries in small blocks.
- Classic clients can retry graphics startup while the English or Spanish Direct3D acceleration error is still on screen.
- Classic clients now wait for the launcher’s folder scan to finish before retrying a failed graphics startup. Switching clients cancels the retry.
- Forever replaces an incomplete cached Battle.net installer on the next setup attempt, including interrupted downloads larger than 1 MB. The setup window is now visible when Battle.net needs input during installation.
- Interrupted Battle.net installations now use a complete launcher in either installation folder or return to official setup.
- On dual-stack networks, Forever now reports a usable IPv4 DNS server to Windows apps even when Android lists an IPv6 server first.
- Modified WotLK clients that use the older version signature now keep their WotLK identity through Play, graphics driver selection and add-on management. Previously a folder could pass validation and then fail when opening the game.
- Update WoW Forever now opens Battle.net so you can resume a paused download or finish an update. The app also respects a paused download when you press Play.
- Classic clients use less memory while checking and installing bundled addons. An unrelated addon with the same folder name as an old Imito addon no longer blocks Play.
- Classic clients start with Imito’s touch controls and MoveAnything. Choose other bundled add-ons in Options → Add-ons. Existing selections and saved character settings are preserved.
- Play preserves an imported optional add-on with its own descriptor, even when its folder has the same name as a bundled add-on.

## Touch and controller input

- Fixed a native crash when copying the on-screen pointer image, including images with padding at the end of a row.
- Fixed the joystick disappearing when the dungeon corpse notice overlapped a movement button. Ghosts can keep walking while the notice is visible.
- The joystick stays available while looting. Tapping a loot row selects the item even when the loot window opens over the joystick.
- The joystick, autorun, walk/run and jump now become available as soon as the game reports each button’s position, even if another button is missing. An incoming layout update no longer interrupts a held movement button whose position is unchanged.
- Fixed sudden camera turns when a second finger touches the screen during a drag. Sliding two fingers together now keeps the zoom steady.
- Wrath touch controls keep receiving combat and menu updates if a cooldown, cursor or display hook throws a Lua error.
- Forever touch controls return when a native panel fades out. Restricted game panels no longer interrupt the touch interface.
- Forever now restores missing or truncated touch UI scripts at launch and preserves saved addon choices.
- In Vanilla, OctoWoW and TBC, the native Key Bindings screen now accepts the four controller face buttons. Saved assignments survive reopening the menu and reloading the UI.
