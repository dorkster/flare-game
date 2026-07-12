# Contributing to Flare: Empyrean Campaign

Thanks for your interest in contributing to Flare: Empyrean Campaign.

This repository contains game data for the FLARE engine. The engine source lives at https://github.com/flareteam/flare-engine.

## Before You Start

- For engine bugs or engine features, use the flare-engine repository.
- For campaign, art, data, translation, packaging, or mod issues, use this repository.
- Keep pull requests focused. Small, independent changes are easier to review and merge.
- Avoid unrelated formatting changes in content files.

## Reporting Issues

When reporting a bug, include:

- FLARE engine version
- Operating system
- Enabled mods and their order
- Steps to reproduce
- Expected result
- Actual result
- Screenshots or save files when useful

## Pull Request Guidelines

Good pull requests usually:

- Touch the smallest practical set of files
- Have a clear title, such as `fix: correct missing collision in map`
- Explain the player-visible effect of the change
- Mention how the change was tested
- Avoid mixing content, balance, art, translation, and build changes in one PR

If a change affects gameplay balance, describe the reasoning and test it in game when possible.

## Game Data Style

Most game data uses simple INI-style text files.

- Preserve existing line endings and formatting style.
- Prefer existing naming patterns in nearby files.
- Keep comments useful and remove obsolete TODOs only when the issue is actually solved.
- Do not rename or move assets unless every reference is updated.

## Maps and Tiled Sources

Runtime maps live under `mods/*/maps/`.

Tiled source files live under `tiled/`. If changing map layout, keep exported runtime maps and Tiled sources in sync when applicable.

## Art and Audio

Use open formats where possible:

- Images: PNG or JPG as appropriate
- Audio: OGG
- Source art: Blender, XCF, or other editable formats when available

Large binary changes are harder to review. Keep them focused and explain their source/license.

## Translations

Translation files live under each mod's `languages/` directory.

When changing translatable strings, keep translation impact in mind. Do not manually update all translations unless you are intentionally doing a translation update.

## Packaging

Packaging-related files live in `distribution/` and `CMakeLists.txt`.

Packaging changes should be tested with a local install when possible, and should avoid changing runtime game content unless necessary.

## Licenses

The FLARE engine is released under GPL version 3 or later.

Art and data files for Flare: Empyrean Campaign are released under CC-BY-SA 3.0 or later unless otherwise noted.

By contributing, you agree that your contribution may be distributed under the relevant project license.
