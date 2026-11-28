# Wine runtime module provenance

The 32-bit patch library is the unmodified WineHQ Wine 10.0 i386 build:

- Package: https://dl.winehq.org/wine-builds/ubuntu/pool/main/w/wine/wine-stable-i386_10.0.0.0~jammy-1_i386.deb
- Package SHA-256: `ba98e66b67f3e1a6b962f3f77d1d21fd6f72b5ce822a916bc973e93325b38ab0`
- `mspatcha.dll` SHA-256: `8f5746010c93ea17a4ad823f3fa00279794996fa4d61cfd9f2464fcd840d04ff`
- Source: https://gitlab.winehq.org/wine/wine/-/tree/wine-10.0/dlls/mspatcha
- Licence: LGPL-2.1-or-later.

The 32-bit OLE DB prefix uses the same `msdasql.dll` as the matched Wine runtime:

- SHA-256: `968193369e4aa6b2f0b5fced8bbabeb7138780d33cfeea7e94f28c88b32797bd`
- Source: https://github.com/The412Banner/proton-wine/tree/c74acb09d51b447f5d5ac56c87608d3ec565a767/dlls/msdasql
- Licence: LGPL-2.1-or-later.

The integration was checked on Android/Wine/FEX with 2,149 patch/export checks
and 40 checks of upgrades to existing application-owned runtime links. User
files and custom library overrides are preserved. These checks do not assert
support for arbitrary external ODBC databases.
