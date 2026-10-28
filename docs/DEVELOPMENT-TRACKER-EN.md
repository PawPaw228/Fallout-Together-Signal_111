# Signal 111 — Dev log

*Updated October 28, 2026*

[English](DEVELOPMENT-TRACKER-EN.md) · [Русский](DEVELOPMENT-TRACKER-RU.md) · [Español](DEVELOPMENT-TRACKER-ES.md) · [Português (Brasil)](DEVELOPMENT-TRACKER-PT-BR.md) · [简体中文](DEVELOPMENT-TRACKER-ZH-CN.md)

[README](../README.md) · [Roadmap](ROADMAP.md)

## October 28 — Real player coordinates and a two-PC data test

I captured the local player's changing position and rotation in a loaded Fallout 4 solo-host world. The native read-only test passed. A later limited recording produced 97 pose samples.

I then tested a connection between **two physical PCs**. The host sent those 97 samples through the server to the guest. Their order and all six position/rotation values per sample matched exactly.

**The data transfer passed, but the whole attempt failed.** The guest reported an invalid disconnect marker, and the host later timed out. This test did not put two characters in the same world or move a remote character.

I reproduced a diagnostic marker-publication problem and tested its fix offline. The updated path has **not** been retested in a real two-PC session.

Separately, I built an experimental module for creating, observing, and removing one local actor. Its supporting checks passed offline. It has **not** been loaded into the game, so actor creation and deletion remain unverified.

## October 26 — Getting ready for the world

I prepared the guarded player-position reader and continued working on protecting existing saves. These were offline steps at the time; the first real in-world capture came later.

## October 25 — Two real network identities

Two real Fallout 4 clients connected to one local server and received separate network player IDs. Both stayed in the menus. One client could disconnect without dropping the other.

## October 24 — Two connected game clients

I verified simultaneous local client connections and basic player-reference access from the menu.

## Next

Verify safe test-profile isolation, check the revised two-PC disconnect handling in a complete session, then test one local diagnostic actor before moving toward shared-world character spawning.

**There is no playable co-op build yet.**

[Changelog](../CHANGELOG.md) · [Issues](https://github.com/PawPaw228/Fallout-Together-Signal_111/issues)
