TrainerNPCs

A Fabric 1.21.1 server/client mod that adds configurable trainer NPCs and command NPCs designed for Cobblemon servers.
It integrates with Radical Cobblemon Trainers API (RCT API) to allow fully customizable trainer battles, progression systems, rewards, and NPC interactions.

TrainerNPCs lets server owners create Pokémon-style gyms, story progression, healing NPCs, quest NPCs, and more — all configured in-game with commands.

Features
Trainer NPCs

Create NPC trainers that players can battle using their Cobblemon team.

Features include:

Custom trainer teams

Configure IVs, EVs, moves, abilities, and level

Optional level scaling to match the player’s highest Pokémon

Custom battle rulesets

Singles / Doubles battle formats

Item usage rules

Level caps

Multiple players can challenge the same trainer at the same time

Cooldown or one-time rewards

Per-NPC reward items

Trainer defeat tracking per player

Gym / Progression System

TrainerNPCs supports trainer progression so players must defeat certain trainers before challenging others.

Example progression:

Rock Gym → Grass Gym → Electric Gym

Commands allow you to require that a player defeats one trainer NPC before battling the next.

Example:

/trainernpc require grass_gym set all rock_gym

If a player hasn't defeated the required trainer, the battle is blocked and a configurable message is shown.

Command NPCs

Create normal NPCs that run commands when right-clicked.

Examples:

/pokeheal

/pc

/warp spawn

quest or dialogue commands

Commands run as the interacting player, ensuring compatibility with permissions and other mods.

NPC Customization

NPCs support several customization options:

Player skins by username

Formatted overhead text

Look at nearby players while standing still

Spawn at the command executor

Cannot be damaged by players

Do not appear in the player tab list

Formatting codes are supported:

&l&dGrass Gym Leader
Server Friendly

TrainerNPCs is designed to be safe for public servers.

NPCs cannot be damaged

Commands run as players (not console)

Interaction anti-spam protection

Permission support via LuckPerms / Fabric Permissions API

Server-side data validation

NPCs automatically despawn when chunks unload and respawn when the area loads again, preventing unnecessary entity load.

Requirements

Server:

Fabric Loader

Fabric API

Cobblemon

Radical Cobblemon Trainers API (RCT API)

Client:

Fabric Loader

Fabric API

TrainerNPCs Client Mod

Building

Requires Java 21.

Build the project:

./gradlew build

Output jars:

server/build/libs/trainernpcs-server.jar
client/build/libs/trainernpcs-client.jar
Example Commands

Create and spawn a trainer:

/trainernpc create rock_gym rock_trainer
/trainernpc spawn rock_gym

Require another trainer to be defeated:

/trainernpc require grass_gym set all rock_gym

Create a command NPC:

/npc create healer
/npc spawn healer
/npc setcmd healer pokeheal
Planned Improvements

GUI trainer editor

Dialogue system

Quest system

Datapack trainer templates

Advanced reward pools
