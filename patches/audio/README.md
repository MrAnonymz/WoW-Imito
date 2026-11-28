# Android PCM playback adapter

This directory contains the complete modified `com.winlator.alsaserver.ALSAClient`
source used in this release and the change from the preceding implementation.
It derives from Winlator/WoW Mobile (LGPL-2.1); the original licence is retained
in `LGPL-2.1.txt` at the repository root.

Upstream projects: https://github.com/brunodev85/winlator and
https://github.com/marcocastignoli/wow-mobile .

Place `ALSAClient.java` at `app/src/main/java/com/winlator/alsaserver/` in the
Android source tree. It uses the existing AudioDriverConfigDialog, KeyValueSet,
Mathf and SysVSharedMemory interfaces from that tree and the Android SDK.
The patch is against the included `ALSAClient.before.java`, not an unspecified
upstream revision.

The negotiated PCM/shared-memory size is kept separate from Android's effective
playback-buffer size. Underrun recovery grows within reserved capacity and never
shrinks the current playback buffer or changes the shared-memory protocol.
Additional buffering trades some latency for tolerance to scheduling delays.

Validation: 22 host buffer invariants and 10,223,736 pointer/partial-write checks.
On a Galaxy S26, an eight-second delayed-write fixture for each transport reduced
the Android underrun counter from 39 to 0. This used silent generated PCM and is
not a subjective audio-quality or all-device performance claim.
