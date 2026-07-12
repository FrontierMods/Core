# Frontier Mods

_last updated: Jul 12, 2026_

Frontier Mods is a collection of mods for _Cataclysm: Dark Days Ahead_. They're designed to work separately or in conjunction with one another; patches will be provided to bridge functionality between Frontier mods, should their content overlap.

The goal of Frontier Mods is to create an ecosystem of independent, compatible, and ultimately synergetic mods which augment the gameplay by grounding the game in reality and expanding the options available to the player.

_DDA_'s engine does not allow adding extensive functionality via mods; it does, however, permit creating a large amount of content.

Implenenting author-driven expansion of content – independently of (though sometimes in line with) the goals of the base game – is the foundation of Frontier Mods.

## Game Version Support

The mods are designed to be compatible with the latest stable release only.

Current version supported: **0.I**.

## Mod IDs and Compatibility

As of v2.0.0, Core uses the slash-based Frontier Mods ID system, and its former submods live in standalone repositories:

| Mod                                     | Old ID               | New ID      | Location                                                            |
| --------------------------------------- | -------------------- | ----------- | ------------------------------------------------------------------- |
| Frontier Mods Core                      | `frontier_core`      | `frontier`  | this repository                                                     |
| Materials Library (was Core: Materials) | `frontier_materials` | `materials` | [FrontierMods/Materials](https://github.com/FrontierMods/Materials) |
| Item Audits (was Core: Audits)          | `frontier_audits`    | `audits`    | [FrontierMods/Audits](https://github.com/FrontierMods/Audits)       |

This is a **breaking change**: worlds and mods that reference the old IDs must update their mod lists and dependencies.

For mods compatible with version **0.H**, refer to the [`0.H` branch](https://github.com/FrontierMods/Core/tree/0.H).

# Frontier Core

**Frontier Core** is the base mod for the entirety of the Frontier Mods collection. It contains features, changes, and bug fixes used by most mods of the umbrella/brand.

## Auditing

⚠️ Item audits now live in the standalone [Item Audits](https://github.com/FrontierMods/Audits) mod.

## Materials

⚠️ The materials library now lives in the standalone [Materials Library](https://github.com/FrontierMods/Materials) mod.

# Frontier Mods Extra

[Frontier Mods Extra](https://github.com/FrontierModsExtra) are mods that don't fit into the Frontier ecosystem. Extra mods are developed by the same author.

These are usually smaller mods, often experimental in nature. Their goal is to speculate and explore, without affecting larger, more-cohesive mods.

Extra mods may be absorbed into main Frontier mods later.

# List of Mods

_crossed-out features are currently unavailable but are planned_

_mods may move in and out of focus at random intervals_

## In Focus

_these mods are receiving the most attention at this moment_

- **[Armory](https://github.com/FrontierMods/Armory)**:

  - adds a variety of real-life military gear
  - significantly expands tactical gear modularity
  - ~~adds decoration options for military and civilian clothing~~

- **[Loadout](https://github.com/FrontierMods/Loadout)**:

  - adds a variety of real-life firearm attachments
  - overhauls existing attachments to specific models, with their own limitations
  - adds a handful of improvised attachments
  - enhances magazines and add magazine modding

- **[Remedy](https://github.com/FrontierMods/Remedy)**:

  - revamps the medical system
  - adds new health effects and treatment tools

## Out of Focus

_no changes to these mods are expected at this time, but they are not abandoned and may be focused again in the future_

- **[Dapper](https://github.com/FrontierMods/Dapper)**:

  - revamps existing clothing
  - expands the clothing and accessory options available to the player
  - adds a variety of civilian storage options (backpacks, fanny packs etc.)

- **[Comforts](https://github.com/FrontierMods/Comforts)**:

  - adds a variety of common personal items to enrich and flourish one's survival

- **[Handload](https://github.com/FrontierMods/Handload)**:

  - remodels existing calibers based on real-life data
  - revamps cartridge components into distinct items
  - allows crafting custom rounds using the new components
  - ~~introduces new calibers~~

- **[Recharge](https://github.com/FrontierMods/Recharge)**:

  - adds extra options for portable energy storage
  - ~~overhauls energy supply, storage, and demand values for tools, automotive components, personal devices, and more~~
  - ~~expands battery types and sizes~~
  - ~~replaces generic batteries with device-appropriate variants~~

- ~~[Gunstore](https://github.com/FrontierMods/Gunstore)~~:

  - reimplements guns as distinct, separate objects, while following the latest base-game trends (like modular AR-15 rifles)
  - adjusts each gun to have realistic gun slots, and adds some of the basic attachments to make outfitting a gun realistic
  - models replaceable gun attachments (like AR-15-style stocks) as default gunmods, allowing their replacement by the player

- ~~[Computation](https://github.com/FrontierMods/Computation)~~:

  - adds a variety of computational devices, i.e. smartphones and personal computers
  - expands available options for using such devices
  - provides platform for computer-assisted design for use in personal crafting recipes

- ~~[Workshop](https://github.com/FrontierMods/Workshop)~~:

  - adds basic and advanced home workshop tools
  - ~~provides framework for 3D-printing items~~

- ~~[Toolkit](https://github.com/FrontierMods/Toolkit)~~:

  - adds basic and advanced portable tools, including compact EDC options

- ~~[Prepper](https://github.com/FrontierMods/Prepper)~~:

  - adds equipment for survival and nomad lifestyle

- ~~[Synthesis](https://github.com/FrontierMods/Synthesis)~~ (name pending):

  - revamps existing bionics
  - adds a set of new and advanced bionics

- ~~[Forma](https://github.com/FrontierMods/Forma)~~:

  - revamps select mutations tree and paths to acquiring the mutations
  - models potential health effects while undergoing mutations changed by the mod

## Extra

- **[Weight](https://github.com/FrontierModsExtra/Weight)**: makes carried weight directly affect stamina expenditure and fatigue buildup
- **[Playing Cards](https://github.com/FrontierModsExtra/PlayingCards)**: adds collectable enchanted playing cards to the world, each card with its own effect
- **[Hellfire](https://github.com/FrontierModsExtra/Hellfire)**: adds the ability to call airstrikes on a designated target, provided you can find the rare military tablet with access to the drone
- **[Bullseye](https://github.com/FrontierModsExtra/Bullseye)**: unbalanced mod that makes every ranged weapon hit (almost) perfectly on every shot
- **[Proficiencies](https://github.com/FrontierModsExtra/Proficiencies)** `[WIP]`: adds _Escape from Tarkov_-style firearm proficiencies, separated by platform

## Archived

- ~~**[Gunsmith](https://github.com/FrontierMods/Gunsmith)**~~:

_not coming: desirable implementation requires too much effort for a single developer_

_reworked into lighter Loadout and Gunstore (see above), which retain some of the modding features and add different options_

- overhauls gunmodding by making it as close to real life as possible
- introduces hundreds of real-life parts for existing firearms
- adds gunsmithing tools necessary for many of the gunmodding processes
- expands on the skills and proficiencies required to construct and mod guns
- adds decoration options for firearms

# Notes

Many of the mods also include notes and reference documents. These were written during development and shared with other modders for the purposes of expanding the arsenal of ideas.

# Donate

Frontiers Mods are developed by a single dedicated person.

While the mods themselves confer no overhead costs – such as, for example, hosting – each takes a considerable amount of time to research, develop, and polish, to say nothing of the post-release support.

You can support the project by donating to it. The quickest way to do it is via the links in the sidebar. Alternatively, check out [DONATE.md](documentation\DONATE.md) for a way to contribute to the project. You can give a one-time donation or support the project continuously via subscriptions. Donating earns you an opportunity to leave your mark in any of Frontier Mods; see [DONATE.md](documentation\DONATE.md) for details.

## Supporters

Supporter suggestions are tracked in [this table](https://docs.google.com/spreadsheets/d/1hzIu-enqmCW8pQzS0lfJ8N449k1GNmESi7rPMj7Cyfg/).

### 30 €

- Crow
- G4R5vb5r3H ×2

## License

MIT
