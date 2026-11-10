# Music Plus 0.9.4

- Search/album: Title · Artist · Views · Duration. Artist: Title · Views · Album · Duration. Personal playlists: Title · Artist · Album · Duration.
- Numeric K/M/B sorting; missing Views show — and sort last. No invented counts or album links for counters.
- Ctrl/Shift-click multi-selection and bulk Add/Remove (50-action chunks, max 500 selected).
- Add picker has cover previews, titles and known track counts; one click adds, no bottom Add button.
- Duplicate video-ID warning before adding another copy; bulk prompt can include/skip/cancel duplicates.
- Confirmed playlist mutations reconcile short-lived stale list responses. Refresh Library also reloads the current collection.
- Triple-click selects full text. Playing artist is selectable. Only direct text clicks select words; artwork/blank row double-click still plays.
- Selecting the currently playing song does not restart it.
- Hover underline is limited to the artist under the pointer. Normal hover cursor; I-beam during selection. No text tooltip notes/playing-title hover background.
- Paste YouTube/YouTube Music/youtu.be song links in Search to resolve exactly that video ID.
- Bounded per-account artist/album page cache; artist endpoint reuse; cover fetching does not block page-open completion.
- Audio disk cache: 32 tracks/256MiB policy; redundant intermediate files removed. No audio-byte RAM cache or background updater added.

Use Settings > Check for updates, or fully exit the app and extract/overwrite this complete ZIP.
Existing local data stays in %LOCALAPPDATA%\MusicPlus8.

Build and 83 fixture/policy checks passed. Windows UI/updater/live YouTube API and latency are
still unverified in the Linux build environment. Cold playback still requires network download
and native remux; no measured speed improvement claimed. First duplicate check of an uncached
playlist may need to page that target playlist. Source stays private; this repository stores binaries only.
