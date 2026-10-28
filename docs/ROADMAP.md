# Development roadmap

*Updated October 28, 2026*

The first target is **stable two-player Fallout 4 co-op**. The checkpoints below keep real game results separate from offline work.

## M1 — Safe test foundations

- [x] Build and run the Fallout 4 networking foundation.
- [x] Connect two real clients and verify separate player identities in the menus.
- [x] Read changing local player position and rotation in a loaded solo-host world (**REAL PASS**).
- [ ] Prove that the test guest cannot alter original saves or game settings (**BLOCKED / NOT VERIFIED**).

## M2 — Two-PC data and shared-world entry

- [x] Transfer 97 pose samples between two physical PCs and verify the exact values (**DATA TRANSFER REAL PASS**).
- [ ] Verify a complete, clean two-PC diagnostic session (**previous overall attempt FAILED**).
- [ ] Verify the revised disconnect-marker process in a new live run (**offline tests passed; live test NOT RUN**).
- [ ] Validate a compatible, host-controlled shared world and safe guest entry (**NOT VERIFIED**).

The completed transfer used a limited transport path. It did not verify full game-network isolation, world entry, character spawning, or movement application.

## M3 — Remote character and movement

- [x] Prepare a local diagnostic actor module and its supporting checks (**OFFLINE PASS**).
- [ ] Create, observe, and remove one local diagnostic actor in an approved solo-host test (**NOT RUN**).
- [ ] Spawn the second player's character in the shared world (**NOT RUN**).
- [ ] Synchronize basic movement and orientation between players (**NOT RUN**).
- [ ] Extend to gameplay interactions, combat, NPCs, inventory, and quests (**NOT VERIFIED**).

## Public release

- [ ] Validate save protection, connection recovery, and supported versions.
- [ ] Verify the features advertised for the first playable build.
- [ ] Provide installation instructions, required attribution, and licenses.

**No public playable build is available.** Passing a network or offline test never implies that the whole game mode works.

[README](../README.md) · [Changelog](../CHANGELOG.md) · [Development diary](DEVELOPMENT-TRACKER-EN.md) · [Issues](https://github.com/PawPaw228/Fallout-Together-Signal_111/issues)
