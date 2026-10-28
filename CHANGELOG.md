# Changelog

**Signal 111 is in development. No public playable build is available.**

## October 28, 2026

### Verified in the game

- Captured changing position and rotation from the local player in a loaded solo-host world.
- Recorded 97 limited player-pose samples.
- Sent 97 samples from a host PC through the server to a guest PC over Radmin. The sample order and all six float values per sample matched exactly.

**Limit:** the overall two-PC attempt **failed** during disconnect handling. A guest-side disconnect marker was invalid, and the host later reached a session-hold timeout. The sample transfer passed; the complete run did not. No shared-world entry, remote character spawning, or movement application was verified.

### Passed offline, not in-game

- Fixed and tested the diagnostic disconnect-marker publication process. The new implementation has **not** had a live rerun.
- Built a separate local actor diagnostic module and verified its supporting components offline. It has **not** been loaded into Fallout 4. Actor creation, observation, and removal are **not yet verified in-game**.
- Prepared a review package for one controlled solo-host actor test. The package is not an approved or completed runtime test.

### Still unresolved

- Protection of original saves and game profiles in real test conditions.
- A clean full two-PC session, safe shared-world entry, and remote player synchronization.

## October 26, 2026

- Prepared the first guarded player-position reader and its offline loading-state checks.
- Continued work on test-environment and save protection.
- Improved guest startup checks.

These were offline results at the time. The later October 28 entry records the first successful loaded-world player-position capture.

## October 25, 2026

- Connected two real Fallout 4 clients to one local server.
- Verified separate network player IDs and independent disconnects.
- Both clients remained in the main menus.

## October 24, 2026

- Verified two simultaneous local client connections.
- Tested basic player-reference access from the main menu.

## October 20–21, 2026

- Established the first real Fallout 4 client-to-server connection.
- Started the two-player networking groundwork.

[README](README.md) · [Roadmap](docs/ROADMAP.md) · [Dev log](docs/DEVELOPMENT-TRACKER-EN.md)
