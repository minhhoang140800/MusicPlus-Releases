# Music Plus — Windows releases

Public binary downloads only. Source is maintained privately.

[Download 0.9.1](packages/MusicPlus-0.9.1-compact-windows-x64.zip)

Exit the old app completely, extract the complete ZIP and overwrite your app folder.
Do not delete %LOCALAPPDATA%\MusicPlus8; it holds your local account/settings/cache.
From 0.9.1: Settings > Check for updates downloads/verifies a newer ZIP and restarts.
No login/token is needed for updates. No background update process.

0.9.1: select/copy text; underline artist/album on hover; on-demand updater; playlist
selection reuses loaded Library; optimistic removal restores on server error.
Audio transfer avoids WPF dispatch per chunk. Speed improvement not measured on a live account.
Windows UI/install helper/live login/audio have not been tested in the Linux build environment.
