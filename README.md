# VictoryPointShuffler

A mod for **Sid Meier's Civilization III: Conquests** that randomly places Victory Point locations on new random maps, making them function as genuine VP victory mechanics rather than fixed scenario placements.

Built on top of [C3X](https://github.com/maxpetul/C3X) by **maxpetul and contributors**, which is a code-injection framework that patches the Civ3 Conquests executable at runtime to add quality-of-life features and bug fixes.

## What it does

When you start a new random map game, Victory Point locations are shuffled to random positions on the map instead of appearing at their default locations. The shuffle updates both the game's internal VLOC objects (which govern gameplay and scoring) and the tile rendering data, so VP locations work correctly for both display and victory conditions.

## Based on C3X

The underlying infrastructure — executable patching, config system, and the majority of the codebase — comes from [C3X (Civ3Augments)](https://github.com/maxpetul/C3X), developed by **maxpetul** and other contributors. All credit for that work belongs to them.

This project adds the Victory Point shuffle feature on top of C3X. If the C3X authors request it, this repository will be taken down.

## Supported versions

- Steam
- GOG
- PCGames.de

## How to install

1. Clone or download this repository into the `Conquests` folder of your Civ 3 installation (e.g. `Sid Meier's Civilization III Complete/Conquests/VictoryPointShuffler`).
2. Run `RUN.bat` from that folder. The patcher uses [TCC (Tiny C Compiler)](https://bellard.org/tcc/) bundled in the `tcc/` folder — no external tools needed.

## Configuration

The included `default.c3x_config.ini` has been set to fully vanilla Civ 3 defaults — all C3X quality-of-life features are disabled. This is intentional: enabling them can cause **desyncs in multiplayer games**.

If you want access to C3X's QoL features for singleplayer, install [C3X](https://github.com/maxpetul/C3X) separately rather than enabling options in this config. Do not modify `default.c3x_config.ini` here.
