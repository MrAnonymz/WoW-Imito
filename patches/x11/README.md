# X11 output and connection fixes

This package contains the complete modified X11 output and connection source
used by WoW Imito 1.5.5, plus the supporting headers/interfaces needed by its
focused tests. It is based on the Winlator/WoW Mobile integration in the app;
it is not presented as an unmodified upstream checkout.

## Attribution and license

- Winlator: brunodev85 and contributors,
  https://github.com/brunodev85/winlator and
  https://github.com/brunodev85/winlator-app.
- WoW Mobile: marcocastignoli and contributors,
  https://github.com/marcocastignoli/wow-mobile.
- License: GNU Lesser General Public License, version 2.1. The original
  full license is included as `LICENSE-LGPL-2.1.txt`; existing source notices
  are retained. WoW Imito modifications and test fixtures use the same license.

The archive contains full modified files rather than a patch that assumes an
unidentified clean upstream revision. `provenance.json` identifies each source
input by SHA-256, the exact public source transformation, and archive hashes.
Only the existing public identifier substitutions and line-ending normalization
are applied to production files; the algorithms are identical to the canonical
build inputs.

## Changes

- Nonblocking ordered output preserves short-write and interrupted-write tails.
  A worker waits for socket readiness without holding Java/UI/X-server locks.
- Deferred file-descriptor transfers retain ownership and occur exactly once.
  Socket ownership prevents a closed descriptor being reused by a late writer.
- Queues and builders have explicit bounds, with checked allocation, offsets
  and teardown. A terminal failure closes the connection instead of silently
  accepting truncated protocol data.
- Java array slices and heap ByteBuffer ranges retain the correct byte counts.
- Failed connection initialization releases partial Java/native resources,
  removes failed epoll registrations and clears rejected JNI callbacks.

No renderer downgrade, GPU-specific forced fallback, or guest CPU-flag rollback
is part of these changes. Reproducing these protocol defects does not establish
that they caused every reported freeze on a particular GPU.

## Verification

Extract `x11-imito155-source.zip` to a writable directory. Python 3.9+ and JDK 17
are required for the host tests. Set `JAVA_HOME`, or put `java` and `javac` on
PATH. For the native host fixture set `CC` to a C compiler executable, or put
`cc`, `clang`, `gcc` or `zig` on PATH. A Zig executable is invoked with `zig cc`.

```sh
python tests/test_xoutput_slices.py
python tests/test_xconnector_initialization.py
```

The first executes the production Java methods with JNI write boundaries
captured: offset slices, reply framing, direct/heap buffers, preserved buffer
state and allocation failure. The second executes production Java/native
initialization bodies with controlled allocation, JNI, socket, thread and epoll
failures. It also checks successful initialization and normal cleanup.

For the real-socket native queue fixture, connect an authorized ARM64 Android
12+ test device with USB debugging and specify its serial explicitly:

```sh
python tests/run_xoutput_queue.py --ndk /path/to/android-ndk --adb /path/to/adb --serial YOUR_TEST_DEVICE
```

This uses the NDK ARM64 API31 compiler, installs only a temporary native fixture
under `/data/local/tmp`, runs isolated AF_UNIX sockets, and removes the fixture
afterward. It does not launch, attach to, or modify the game. Tests cover partial
writes, EAGAIN/EINTR, ordered output, exactly-once SCM_RIGHTS, descriptor reuse,
undrained shutdown, peer close, queue limits, allocation failure and canaries.
The supplied fixed native fixture passed on Android; a successful host test is
not a substitute for testing each graphics driver or a complete game session.

`source/app/src/main` files can be integrated at the corresponding paths in the
matching Winlator/WoW Mobile application tree. This focused source archive is
not the complete Android app or an independently buildable APK project.
