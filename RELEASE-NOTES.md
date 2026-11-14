# WoW Imito 1.5.3

## Graphics

- Automatic graphics selection now prefers Vulkan for classic clients, including the bundled PanVK driver on eligible Mali GPUs. Another graphics path is used if the required checks fail.
- Fixed rejection of valid imported Vulkan driver packages.
- Reused graphics command buffers to reduce repeated memory allocations.
- Fixed a crash when uploading graphics buffers after a failed memory mapping.

## Startup and reports

- Leftover processes from a previous game session no longer interrupt a new launch.
- Improved DXVK startup recovery without interrupting retries handled by DXVK itself.
- Crash reports now identify the failing runtime module more precisely.
