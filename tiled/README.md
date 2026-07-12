# Editing Maps with Tiled

This directory contains the Tiled source maps (`*.tmx`) used to edit Flare maps.
The game does not load these files directly. Runtime maps are exported as Flare
map text files under `mods/*/maps/`.

## Basic Workflow

1. Open `tiled/flare-game.tiled-project` in Tiled.
2. Open an existing map or one of the template maps, for example:
   - `tiled/grassland/grassland_template.tmx`
   - `tiled/dungeon/dungeon_template.tmx`
   - `tiled/cave/cave_template.tmx`
   - `tiled/snowplains/snowplains_template.tmx`
   - `tiled/ruins/ruins_template.tmx`
3. Edit the map in Tiled.
4. Ensure the `libflare` plugin in Tiled's Preferences menu is enabled.
5. Export the map as a Flare map (`*.txt`) into the matching mod's `maps/`
   directory, for example `mods/empyrean_campaign/maps/arrival.txt`.

The `devlab` mod also contains an in-game mapping tutorial. See the NPC dialog
files under `mods/devlab/npcs/` for the same workflow explained in-game.

It's also recommended to use the [flare-tiled-tools](https://github.com/flareteam/flare-tiled-tools) repository to aid in map creation and editing.

## Tiled Source Maps vs Runtime Maps

Tiled maps can reference several smaller tilesheet images from
`tiled/tilesheets/`. The exported runtime map uses the simpler Flare map format
and points at a single tileset definition in its header, such as:

```ini
tileset=tilesetdefs/tileset_grassland.txt
```

Tileset definition files live in the mods, for example:

- `mods/fantasycore/tilesetdefs/tileset_grassland.txt`
- `mods/fantasycore/tilesetdefs/tileset_dungeon.txt`
- `mods/fantasycore/tilesetdefs/tileset_cave.txt`
- `mods/fantasycore/tilesetdefs/tileset_snowplains.txt`
- `mods/empyrean_campaign/tilesetdefs/tileset_ruins.txt`

Those tileset definitions map tile IDs to the runtime tileset images used by the
engine. They are not generated automatically as part of a normal map edit; use
the existing tileset definitions unless you are intentionally adding or changing
a tileset.

## Automapping Rules

Some tileset folders include `rules.txt` files. These list Tiled automapping rule
maps used while editing, for example:

```txt
rules/grassland_ruleset0.tmx
rules/grassland_ruleset1.tmx
```

These files are editor-side helpers. They are useful when working in Tiled, but
they are not runtime maps loaded by the game.

## Additional Resources

Further information with regards to editing Flare maps can be found on the [flare-engine wiki](https://github.com/flareteam/flare-engine/wiki#mapping).
