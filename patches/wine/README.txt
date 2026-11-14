Wine10.10 compatibility changes

Wine project and contributors; GNU Lesser General Public License2.1.
Upstream source: https://github.com/wine-mirror/wine/tree/wine-10.10

The source-equivalent patches here cover the bundled Wine10.10 shader
alpha-test selection and null-buffer-map guard. The guard applies only to
the exact verified PE32 build; it returns E_OUTOFMEMORY rather than reporting
a successful map with an invalid address when backing memory is unavailable.
The 1.5.3 patch also handles a failed DISCARD upload mapping by using Wine's
existing glBufferSubData path, with the same ranges, offsets and fence handling.
The normal successful mapping path is unchanged. No game executable is changed.
This does not establish that every device-specific crash is resolved.

Original PE32 SHA256:
d678bb939547d2b7f14b177f7af483ac3e7bda11656d4d4ed3bf71173876cd64
Result PE32 SHA256:
67aa1f16a90d278b29b2be65ab018c778b2a1f7f04e1b30d16adc7e17956160e

Wine copyright and LGPL notices remain applicable. See ../../LGPL-2.1.txt.
