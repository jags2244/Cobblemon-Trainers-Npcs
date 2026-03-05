TrainerNPCs

TrainerNPCs is a Fabric mod for Cobblemon servers that lets server owners create:

Trainer NPCs (start Cobblemon trainer battles using Radical Cobblemon Trainers API)

Command NPCs (run commands when right-clicked, as the player)

NPCs are designed for performance and public servers:

NPCs cannot move

NPCs cannot be damaged

NPCs look at nearby players

NPCs despawn when chunks unload and respawn when chunks load

Trainers support progression (players must defeat earlier gyms before challenging later ones)

Multiple players can challenge the same trainer NPC

Dependencies
Server (Required)

Fabric Loader

Fabric API

Cobblemon

Radical Cobblemon Trainers API (RCT API)

TrainerNPCs (Server)

Client (Required for skins / rendering)

Fabric Loader

Fabric API

TrainerNPCs (Client)

Note: The mod is split into server + client jars. Server jar is required for gameplay. Client jar is required to render player-model NPCs with skins.

Commands
Trainer NPC Commands (/trainernpc)

/trainernpc create <npc_id> <trainer_id> - Creates a trainer NPC linked to the specified RCT trainer ID.
/trainernpc spawn <npc_id> - Spawns the trainer NPC at your current location.
/trainernpc remove <npc_id> - Deletes the trainer NPC and its saved configuration.

/trainernpc text <npc_id> <text> - Sets the text displayed above the NPC (supports Minecraft formatting codes, & will be converted to §).
/trainernpc skin <npc_id> <minecraft_username> - Sets the NPC’s skin to the given Minecraft username.

/trainernpc rules <npc_id> format singles - Sets the trainer battle format to singles (if supported).
/trainernpc rules <npc_id> format doubles - Sets the trainer battle format to doubles (if supported).
/trainernpc rules <npc_id> itemusage default - Uses default item rules.
/trainernpc rules <npc_id> itemusage no_items - Disables bag items in battle.
/trainernpc rules <npc_id> itemusage held_only - Allows held items but blocks bag items.
/trainernpc rules <npc_id> itemusage limited - Limits item usage (server-defined limit).
/trainernpc rules <npc_id> levelcap <number|off> - Sets a level cap for the battle, or disables it.

/trainernpc rewards <npc_id> sethand - Sets the reward to the item you are holding.
/trainernpc rewards <npc_id> addhand - Adds the held item to the reward list.
/trainernpc rewards <npc_id> clear - Clears all rewards for that trainer NPC.
/trainernpc rewards <npc_id> once - Makes rewards claimable once per player.
/trainernpc rewards <npc_id> cooldown <duration> - Makes rewards claimable on a cooldown per player (10s, 5m, 2h, 3d, 1h30m).

/trainernpc require <npc_id> set all <required_npc_id> [more...] - Requires players to defeat ALL listed trainer NPCs before challenging this one.
/trainernpc require <npc_id> set any <required_npc_id> [more...] - Requires players to defeat ANY one of the listed trainer NPCs before challenging this one.
/trainernpc require <npc_id> clear - Removes all progression requirements from the trainer NPC.
/trainernpc require <npc_id> message <text> - Sets the blocked message shown when a player hasn’t met requirements (supports & formatting).

/trainernpc reload - Reloads trainer NPC configurations from disk.

Command NPC Commands (/npc)

/npc create <npc_id> - Creates a command NPC.
/npc spawn <npc_id> - Spawns the command NPC at your current location.
/npc remove <npc_id> - Deletes the command NPC and its saved configuration.

/npc text <npc_id> <text> - Sets the text displayed above the NPC (supports & → §).
/npc skin <npc_id> <minecraft_username> - Sets the NPC’s skin to the given Minecraft username.

/npc setcmd <npc_id> <command> - Sets the command to run when a player right-clicks the NPC (runs as the player, not console).
/npc addcmd <npc_id> <command> - Adds another command to run on interact.
/npc clearcmd <npc_id> - Clears all commands on that NPC.

/npc cooldown <npc_id> <duration|off> - Sets an interaction cooldown per player (30s, 10m, 1h30m, etc.), or disables it.
/npc once <npc_id> on - Makes the NPC usable once per player.
/npc once <npc_id> off - Disables once-per-player restriction.

/npc reload - Reloads command NPC configurations from disk.

Examples

/npc setcmd healer pokeheal - Makes an NPC heal the player’s Cobblemon party on right-click.
/trainernpc require grass_gym set all rock_gym - Requires defeating the Rock Gym trainer before challenging the Grass Gym trainer.
