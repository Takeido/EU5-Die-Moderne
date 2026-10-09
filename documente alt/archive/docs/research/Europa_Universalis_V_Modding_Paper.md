Europa Universalis V Modding: A Practical
                                Research Paper
Foundations, File Structure, Scripted Content, Localization, Map Work, Debugging, and
                                          Compatibility

                                    Prepared for: Paul Tesnow
                                        Date: 18 June 2026

Abstract
This paper summarizes the current public knowledge required to begin modding Europa
Universalis V, a grand strategy game developed by Paradox Development Studio and published
by Paradox Interactive. It focuses on practical mod development: how local mods are structured,
where files belong, how metadata works, how scripted content is organized, how localization
connects script keys to visible text, how load order and replacement behavior affect
compatibility, how to debug with logs and generated script documentation, and what makes map
modding different from ordinary script modding. The paper is not a replacement for the official
wiki pages or the game-generated script_docs output; rather, it is a consolidated orientation
paper that explains the major systems and gives a safe workflow for new and intermediate
modders.

1. Introduction
Europa Universalis V continues Paradox Interactive’s tradition of highly moddable grand strategy
games. The official EU5 wiki describes mods as changes that alter existing game behavior or add
new features, while also noting that some systems remain hardcoded, including areas such as
migration logic, battle casualty logic, and map modes [1]. Therefore, EU5 modding is best
understood as powerful but bounded: modders can change many script-defined systems, data
definitions, interface elements, graphics, audio, localization, and map data, but not every engine-
level behavior.

The game itself is built around hundreds of countries and societies in a detailed historical world
with deep diplomacy, economic simulation, military systems, and logistical depth [2]. From a
modding perspective, this means that a mod can range from a small balance tweak to a total
conversion with new countries, populations, religions, goods, events, interface work, and map
changes. The goal of this paper is to collect the essential information needed to plan and build
such a mod safely.

                  Europa Universalis V Modding Paper — Prepared 18 June 2026
2. What EU5 Modding Can Change
The EU5 modding documentation separates modding areas into several broad groups. Important
areas include core documentation such as defines, effects, scopes, triggers, modifiers, variables,
GUI script, and localization; scripted content such as actions, disasters, events, missions,
modifiers, scripted GUI, setup, and situations; scripted types such as advances, buildings,
countries, cultures, diplomacy, estates, goods, institutions, laws, pops, religions, traits, units, and
wargoals; map work such as terrain and map data; graphical work such as 3D models, interface,
graphical assets, fonts, and flags; audio work such as music and sound; and support topics such as
AI, console commands, checksum, mod structure, load order, and troubleshooting [3].

This taxonomy matters because most EU5 mods are not one kind of file. A country mod may
require country definitions, setup files, population setup, culture and religion definitions, flags,
localization, and sometimes events or missions. A total conversion may require almost every
category. A compatibility patch may only need careful use of load order and injection rules.

3. Local Mod Folder and Metadata
Local mods are placed in the user documents path: %USERPROFILE%/Documents/Paradox
Interactive/Europa Universalis V/mod. Each local mod has its own folder. Workshop mods are
stored separately under Steam/steamapps/workshop/content/3450310 [4]. Modders should never
edit base game files directly, because game updates can overwrite them; instead, the local mod
mirrors the base game’s folder structure [5].

A working mod requires a .metadata folder containing metadata.json. The metadata file supplies
the launcher with information such as mod name, id, version, supported game version, short
description, tags, dependencies, and custom data such as replace_paths. The .metadata folder
should also contain thumbnail.png for launcher and workshop display [4].

Example minimum folder structure:
MyMod/
 .metadata/
  metadata.json
  thumbnail.png
 in_game/
  common/
  events/
  localization/
 loading_screen/
  common/
 main_menu/
  localization/

                  Europa Universalis V Modding Paper — Prepared 18 June 2026
4. Top-Level Folder Structure
EU5 mods mirror the base game game folder. The top-level mod folders should be in_game,
loading_screen, and main_menu. Inside them, the modder creates the relevant subfolders such as
common, localization, events, gui, gfx, or setup as needed [4]. This structure is important because
many systems load only from their expected location.

Table 1. Common EU5 modding areas and likely folders
 Goal                             Typical folders                   Notes
 Add or alter events              in_game/events/                   Use namespaces and localized
                                                                    title/description keys.
 Add countries                    in_game/setup/countries/ and      Countries need definitions
                                  setup/start/                      and setup/history.
 Add text                         localization/<language>/          Use l_<language> header and
                                                                    one-line key-value entries.
 Change defines                   loading_screen/common/            Defines can often be changed
                                  defines/                          individually.
 Map conversion                   in_game/map_data/ and             Requires strict image formats
                                  gfx/terrain2/                     and often map editor
                                                                    workflow.
 Interface modding                <top_folder>/gui/                 GUI type/template load
                                                                    behavior has special rules.

5. Recommended Tools and Working Practices
The EU5 wiki recommends using a code editor with syntax highlighting and search support.
Visual Studio Code can use Paradox Highlight and CWTools; IntelliJ can use Paradox Language
Support; Notepad++ is possible but less powerful [5]. For serious work, source control is strongly
recommended. Git allows a modder to track changes, revert broken experiments, and collaborate,
while GitHub Desktop can make Git more approachable for beginners [6].

Good formatting is not cosmetic in Paradox scripting. Proper indentation makes bracket nesting
readable, allows code folding, and helps find errors. Comments beginning with # should be used
to explain difficult logic or temporarily disable code. Modders should search the base game code
for similar patterns before inventing new structures. Finally, avoiding unnecessary overwrites
reduces conflicts and makes compatibility easier [6].

6. Debugging and Generated Documentation
EU5 supports -debug_mode as a Steam launch option. Debug mode activates the console and in-
game developer tools, and it hotloads many mod file changes without restarting the game, though
some files such as on_action are not fully covered [5]. The console can be opened with ~ when
debug mode is active. The console commands script_docs and dump_data_types generate
technical documentation for effects, triggers, scopes, GUI script, and data types. The wiki

                  Europa Universalis V Modding Paper — Prepared 18 June 2026
describes these generated files as the most reliable technical documentation available to modders
[5][6].

The main diagnostic file is error.log in Documents/Paradox Interactive/Europa Universalis V/logs.
When a mod fails, the safest workflow is to reproduce the issue with only the target mod enabled,
read error.log from top to bottom, fix the earliest root error first, and repeat. Many later errors
are symptoms caused by the first broken file or missing key.

7. Load Order, Overwrites, Injection, and Compatibility
Load order is one of the most important compatibility topics in EU5. If a mod file has the exact
same filename and path as a base game file, the mod file completely overwrites the base file; if
the modded file contains less content, only the modded content is loaded [7]. If two mods provide
the same filename and path, the launcher playset order decides which mod overwrites the other:
lower mods in the list overwrite higher ones [7].

Files that do not share identical names and paths are generally loaded in ASCII order. If multiple
files define the same type, the later-loaded definition wins, unless special rules apply. EU5 also
provides database entry modes such as INJECT, REPLACE, TRY_INJECT, TRY_REPLACE,
INJECT_OR_CREATE, and REPLACE_OR_CREATE for many common folders. These modes allow a
mod to alter existing objects without replacing the full original object [7].

There are important exceptions. GUI types and templates use a first-loaded-wins rule. Events also
use a first-loaded-wins rule, and event subfolders are loaded after files in the main event folder.
Defines can often replace a single define without replacing a whole category. On actions can
append further on_actions, events, or random_events, but cannot replace trigger and effect blocks
without replacing the whole file. Localization replacement uses a special replace folder, because
later loaded localization keys do not simply overwrite earlier keys [7].

8. Localization
Localization turns internal script keys into visible game text. In EU5, localization connects keys
such as a country tag, event title key, situation description key, or action name key to a language-
specific string. A localization entry uses a one-line key-value format such as key: "Localized text".
A complete localization file begins with l_<lang>: and then one or more indented entries [8].

Localization can reuse keys by inserting $key$ inside another localized string. This reduces
maintenance: if a repeated name changes, the modder changes only the original key. EU5
localization also supports formatting syntax beginning with # and ending with #!, and custom
formatting is defined in GUI text formatting files [8].

                  Europa Universalis V Modding Paper — Prepared 18 June 2026
Example localization snippet:
l_english:
 my_event.1.title: "A New Charter"
 my_event.1.desc: "The estates gather to debate $my_law_name$."
 my_law_name: "the Maritime Charter"

9. Event Modding
EU5 event files belong in the events folder or a subfolder. Event files normally contain one or
more namespaces, optional inline scripted triggers and scripted effects, and the events
themselves [9]. Event ids should use the namespace.integer format, where the integer is greater
than 0 and less than 10000. Without a namespace, event ids may overlap and fail to fire as
intended [9].

A typical event includes a type such as country_event, localized title and description keys,
optional historical information, a trigger block, and options. Inline scripted triggers and effects
are scoped to the event file and must not overlap with global scripted triggers or effects [9].

10. Country and Setup Modding
Countries are base playable elements. A country needs both a country definition and
setup/history. Country definitions are located under the setup/countries area and include
information such as tag, map color, culture definition, and religion definition. Start setup is
handled under setup/start and determines ownership, control, cores, and other starting-state data
[10].

Setup modding is described as creating a savefile-like starting state for the game to open. Because
some setup documentation has been marked as needing verification or updated from pre-release
versions, modders should cross-check current base game files and generated documentation
before relying on older examples [11].

11. Actions, Effects, Triggers, and Scopes
Action modding creates new interactions between countries and other game-world objects. The
official action modding page describes common syntax shared by many action types, especially
the interaction target system, which helps create interactions that both players and AI can use
[12]. More broadly, most scripted content depends on effects, triggers, and scopes. Effects change
game state; triggers test whether conditions are true; scopes determine what object a script block
is operating on. Because available effects and triggers can change with patches, the safest source
for exact syntax is the game-generated script_docs output.

                  Europa Universalis V Modding Paper — Prepared 18 June 2026
12. Map Modding
Map modding is more fragile than ordinary script modding. The map documentation warns that
image file formats must be respected exactly; wrong color mode, bit depth, layers, or alpha
channels can make the game or map editor crash or misbehave [13]. EU5 includes a map editor
launched with -map_editor, and the wiki notes that it requires high resources, especially 32 GB of
RAM or more [13].

The map editor is necessary for heightmap and terrain texture work, but not for the location map
or rivers map [13]. Heightmap and terrain texture data are refined through terrain cache files
such as heightmap.bin, heightmap.info, materials.bin, and materials.info, created by baking
decals in the editor. A decal can include up to sixteen 8-bit grayscale PNG mask files without
transparency, a 16-bit grayscale bitmask, and a 16-bit grayscale heightmap image [13].

Location data uses files in in_game/map_data. The core location image is locations.png, an
uncompressed 8-bit RGB image without transparency, with a default resolution of 16384 x 8192.
Every color in locations.png must be defined in named_locations/00_default.txt or the game may
crash. Ports, definitions, location templates, and default.map all contribute to the final map
structure [13].

13. Publication and Maintenance
Publishing a mod is not only a technical upload. A maintained mod should include a clear version
number, supported_game_version, thumbnail, short description, tags, compatibility notes,
dependencies, and a changelog. The supported_game_version field can use a wildcard such as
1.0.* to indicate compatibility with hotfixes in that minor version range [4].

A good maintenance workflow is: keep a clean copy of the mod, use Git, test with a minimal
playset, check error.log before release, update supported_game_version after testing patches,
avoid overwriting entire vanilla files unless necessary, and document which base game systems
the mod touches. For large mods, create compatibility patches rather than forcing every user into
one load order.

14. Beginner Workflow
1. Create the mod folder using the in-game mod tools or manually under Documents/Paradox
Interactive/Europa Universalis V/mod.

2. Add .metadata/metadata.json and thumbnail.png.

3. Mirror only the needed parts of the base game folder structure.

4. Enable -debug_mode in Steam launch options.

                  Europa Universalis V Modding Paper — Prepared 18 June 2026
5. Use script_docs and dump_data_types to generate the most reliable current technical
references.

6. Make one small change, launch the game, and inspect error.log.

7. Add localization keys for every player-visible script key.

8. Use injection or replacement modes where possible instead of full file overwrites.

9. Test with no other mods first, then test expected compatibility cases.

10. Version the mod, document dependencies, and only then publish or share it.

15. Conclusion
Europa Universalis V modding is best approached as structured data and script editing within a
strict folder and load-order system. The safest practice is to mirror the base game folder
structure, avoid direct edits to vanilla files, use a capable editor, enable debug mode, read
error.log, generate script documentation from the current game version, and minimize
destructive overwrites. Scripted content, localization, country setup, and actions form the
foundation of most gameplay mods, while map work is a more specialized discipline requiring
exact image formats and careful use of the map editor. A successful EU5 mod is therefore not only
creative; it is also carefully organized, well-documented, and maintained against ongoing game
updates.

References
[1] Europa Universalis 5 Wiki. “Modding.” https://eu5.paradoxwikis.com/Modding

[2] Paradox Interactive. “Europa Universalis V.”
   https://www.paradoxinteractive.com/games/europa-universalis-v/about

[3] Europa Universalis 5 Wiki. “Europa Universalis 5 Wiki.”
   https://eu5.paradoxwikis.com/Europa_Universalis_5_Wiki

[4] Europa Universalis 5 Wiki. “Mod structure.” https://eu5.paradoxwikis.com/Mod_structure

[5] Europa Universalis 5 Wiki. “Modding: Getting started and tools.”
   https://eu5.paradoxwikis.com/Modding

[6] Europa Universalis 5 Wiki. “Modding: Best practices, debugging, and tools.”
   https://eu5.paradoxwikis.com/Modding

[7] Europa Universalis 5 Wiki. “Mod files load order.”
   https://eu5.paradoxwikis.com/Mod_files_load_order

                  Europa Universalis V Modding Paper — Prepared 18 June 2026
[8] Europa Universalis 5 Wiki. “Localization.” https://eu5.paradoxwikis.com/Localization

[9] Europa Universalis 5 Wiki. “Event modding.” https://eu5.paradoxwikis.com/Event_modding

[10] Europa Universalis 5 Wiki. “Country modding.”
   https://eu5.paradoxwikis.com/Country_modding

[11] Europa Universalis 5 Wiki. “Setup modding.” https://eu5.paradoxwikis.com/Setup_modding

[12] Europa Universalis 5 Wiki. “Action modding.” https://eu5.paradoxwikis.com/Action_modding

[13] Europa Universalis 5 Wiki. “Map modding.” https://eu5.paradoxwikis.com/Map_modding

                 Europa Universalis V Modding Paper — Prepared 18 June 2026
