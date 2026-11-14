# Vortek fixes in WoW Imito 1.5.5

`vortek-imito6-1.5.5-source.zip` contains the complete current Vortek host
production subtree, matching unchanged revision-6 guest sources, the changed
Java buffer integration and runtime diagnostics, retained licenses, and focused
verification fixtures. `provenance155.json` records canonical and public source
hashes. `imito155-host.patch` is incremental to the host snapshot in the
preserved `vortek-imito6-source.zip`, rather than to pristine upstream Vortek.

The guest originates from [brunodev85/vortek at b1730c5](https://github.com/brunodev85/vortek/tree/b1730c5).
The Android host and Java integration come from the application's
[Winlator](https://github.com/brunodev85/winlator) /
[WoW Mobile](https://github.com/marcocastignoli/wow-mobile) tree.
Original copyright notices and LGPL 2.1 license texts are retained. The new
integration modifications and supplied fixtures use the same license.

## 1.5.5 changes

- Filter native window-system extensions that this virtual swapchain does not
  implement; preserve supported device capabilities and their reported versions.
- Record precise native device-creation errors before a game window exists.
- Translate virtual `PRESENT_SRC_KHR` layouts to native `GENERAL` layouts when
  decoding image barriers, render-pass attachments, dynamic rendering and other
  image-layout fields. The guest protocol and other layouts are unchanged.
- Check Android hardware-buffer dimensions, layers and channel format before
  image import. Replace a cached RGBA/BGRA buffer when the requested format
  changes, allocating its replacement before retiring the previous texture.

The focused tests execute production decoding/extension functions with
controlled boundaries. They do not demonstrate that every Mali device-loss
report is fixed or establish game FPS on the reporting hardware. The paired
queue/fence protocol introduced in 1.5.4 remains in place.

## Build and verification

The host still builds in the Android app with NDK 24.0.8215888, CMake 3.22.1,
the matching `winlator`/`libadrenotools` targets, Android and log dependencies.
The archive includes its CMake project and Vulkan headers; it is a component
source snapshot rather than a standalone APK project. Java source paths under
`host/java/` correspond to `app/src/main/java/` in that application.
The unchanged guest uses the ARM64 glibc sysroot and development headers
described in the preserved 1.5.4 section below. Public source substitutions are
listed in the manifest. Existing source notices are retained.

After extracting the archive, run the focused native fixtures with Python 3.9+
and a C compiler. Set `CC` to its executable, or put `cc`, `clang`, `gcc` or
`zig` on PATH; Zig is invoked with `zig cc`.

```sh
python verification/test-vortek-device-extensions.py
python verification/test-vortek-swapchain-contract.py
python verification/test-vortek-ahb-format.py
```

The second accepts `--baseline` to reproduce the invalid old layout decoding
and is expected to fail in that mode. Generated fixture output stays under the
extracted archive's `verification/results/` directory. The public package omits
local compiled test binaries and operator-specific test launchers from the
host's `tests/` directory; its C test sources are retained.
The AHB fixture also executes the production Java buffer-replacement methods;
it requires JDK 17, available through `JAVA_HOME` or `java`/`javac` on PATH.

## Preserved 1.5.4 source history

# Vortek paired presentation changes

Vortek is by brunodev85 and contributors, licensed under LGPL 2.1. The guest source is based on [brunodev85/vortek at b1730c5](https://github.com/brunodev85/vortek/tree/b1730c5). The Android host is the Vortek renderer in the application's Winlator/WoW Mobile source tree. Original license texts and source copyright notices are retained.

`vortek-imito6-source.zip` contains the complete modified guest source, the complete modified Vortek host subtree (including Vulkan headers), its build files, focused verification scripts and build evidence. `provenance.json` gives source and binary SHA256 hashes. These are the actual canonical build inputs; public packaging performs the equal-length identifier substitutions documented in that manifest. The guest revision is `2.1-enorial6` before that transformation and `2.1-wrathrt6` in the public edition.

`imito-paired-present-host.patch` shows the changes against the previously prepared public host. `imito-paired-present-guest.patch` shows the new presentation protocol and zero-capacity enumeration changes against the preceding local guest revision. These patches are incremental to the existing application changes, not standalone patches against pristine upstream b1730c5. The full source snapshot includes those earlier changes.

The former guest sent only `VkPresentInfoKHR`, omitted the queue identity, and returned success without a reply. The host published the image without consuming the present wait semaphores. The new appended opcode 355 sends the actual queue and receives a result. The host consumes all present waits in one submission and waits for that submission's fence before publishing. Existing opcode numbers remain unchanged. The old one-way opcode remains readable and does not emit an unexpected reply. The runtime version change causes existing classic game containers to replace the old guest library before using this protocol.

Fence waits check cancellation every 50 ms and stop after at most five seconds. There is no added per-frame `vkDeviceWaitIdle` or `vkQueueWaitIdle`. On a terminal error after submission, the virtual context stops and retains pending GPU allocations until Android process retirement; a timeout is not treated as proof that a real driver has already stopped accessing them. A racing transport shutdown can yield `DEVICE_LOST` to the guest; the bounded startup note records the original failing stage/result. Enumeration now honors the caller's image capacity and returns `VK_INCOMPLETE` for short buffers, including a non-null zero-capacity buffer.

Build integration uses the application's existing NDK 24.0.8215888, CMake 3.22.1 and ARM64 glibc sysroot. The guest CMake project needs the sysroot's standard C, Xlib and Vulkan development headers. `build/linux-arm64.cmake` records the actual toolchain configuration, including 16 KiB ELF segment alignment. `verification/build_vortek_timeline_guest.py --revision 6` records the exact build/repack steps when placed at its original application repository path. The original revision-5 archive supplies unchanged configuration files; only `usr/lib/libvulkan_vortek.so` is replaced. The host CMake project builds inside the Android native project with the existing `winlator`, `libadrenotools`, Android and log dependencies. These platform/toolchain dependencies are not duplicated in this source snapshot.

Verification exercises the actual host/guest functions with a deterministic driver, capacity sentinels, allocation/wait failures, cancellation and pending-resource cleanup. The saved old host reproduces invalid repeated binary semaphore signals; the new sequence passes. A separate real system-Vulkan test on Samsung SM-G990B2/Adreno 660 completed 128 frames with two binary wait semaphores and two swapchain entries. This test did not render game pixels or establish Mali game performance. The shared AHB/GLES consumer-release coordination predates this change and is not claimed to be fully redesigned or verified by this fix.
