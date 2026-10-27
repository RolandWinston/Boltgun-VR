# Sources, licenses and modifications

Project source is distributed under GPL-3.0-or-later. The complete license is in ../LICENSE. Copyright and license notices in third-party source remain in force.

This distribution builds on local project work and referenced code from [rubocopter/boltgun-vr](https://github.com/rubocopter/boltgun-vr), snapshot c74df9a97f45. Original rubocopter copyright and reuse notices are retained in licenses/upstream-COPYRIGHT_AND_REUSE.md and licenses/upstream-SOURCE-AND-NOTICES.md. Those files describe the historical upstream release; the present package uses the authored low-poly firearm geometry and runtime described here.

Changes in this distribution include Quest controls, authored low-poly firearms and arm presentation, tracked melee and projectile behavior, Volkite/Gravgun corrections, lifecycle and tracking gates, control-file caching, exit ordering, and the portable launch transaction. The corresponding C/C++, Lua and model source is included. The exact distributed file list is in manifest.json.

UEVR API: praydog, MIT; API headers retain the notice. MinHook: Tsuda Kageyu and contributors, BSD-style license in licenses/MinHook-LICENSE.txt. OpenXR headers: Khronos Group, Apache-2.0. Reference notices for GTFO VR code and menu code are retained in licenses/LICENSE-GTFO and licenses/Menu-reference-GPL-3.0.txt.

Chainsword credit: This work is based on “Wh-40k-chainsword” by Kaiser-E, licensed under CC BY 4.0. Source: https://sketchfab.com/3d-models/wh-40k-chainsword-2976e3debf33494a831253b160f7d2c9 . Artist: https://sketchfab.com/Kaiser-E . License: https://creativecommons.org/licenses/by/4.0/ . Adaptations include 95 cm length, grip origin, Unreal axes and 2K texture. The original credit file remains in licenses/chainsword-CREDITS.txt.

The polished firearm geometry was authored in Blender. Official weapon art was used as visual reference only, as listed in source/asset-sources.json. Reference image files and extracted game assets are excluded.

This is an unofficial fan mod. Warhammer 40,000, Boltgun, game assets and related marks remain the property of their respective owners. No affiliation or endorsement is claimed. Players obtain the game, UEVR, VR runtime and Python separately. Game files, user saves and private test logs are not part of this distribution.
