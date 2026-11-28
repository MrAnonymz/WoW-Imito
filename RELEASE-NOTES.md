# WoW Imito 1.5.14

- Fixed the joystick stopping when loot or bags close during a movement gesture.
- Fixed action bar 4 moving to the right after mounting or changing pet state; custom positions and sizes are preserved.
- Added Turnip compatibility settings for Adreno 710/720/732 and Samsung devices with Adreno 740.
- Adjusted texture decoding on Qualcomm GPUs and Box64 memory mappings on Mali, while retaining existing GPU-specific fixes.
- Fixed audio-buffer recovery that could worsen crackling after an underrun; playback now has room to adapt under load.
- Problem reports retain the latest touch-control readback failure details without adding continuous logging.
- Forever reports now retain recent launcher errors and observed startup phase timings, including failures after a long login.
- If a problem persists in 1.5.14, send a fresh in-app report immediately after it occurs, with the screen or error you see.
