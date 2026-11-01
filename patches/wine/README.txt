Wine10.10 compatibility changes

Wine project and contributors; GNU Lesser General Public License2.1.
Upstream source: https://github.com/wine-mirror/wine/tree/wine-10.10

The source-equivalent patches here cover the bundled Wine10.10 shader
alpha-test selection and null-buffer-map guard. The guard applies only to
the exact verified PE32 build; it returns E_OUTOFMEMORY rather than reporting
a successful map with an invalid address when backing memory is unavailable.
This does not establish that every device-specific crash is resolved.

Original PE32 SHA256:
d678bb939547d2b7f14b177f7af483ac3e7bda11656d4d4ed3bf71173876cd64
Result PE32 SHA256:
89fe49b8ae1f6f2953d5b461c6b77443e8c5fe71266a2568ec19a424b1c74f06

Wine copyright and LGPL notices remain applicable. See ../../LGPL-2.1.txt.
