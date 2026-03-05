🎮 TrainerNPCs

TrainerNPCs is a Fabric 1.21.1 mod that adds fully configurable trainer NPCs and command NPCs for Cobblemon servers.

It integrates with the Radical Cobblemon Trainers API (RCT API) to provide Pokémon-style trainer battles, gym progression systems, rewards, and interactive NPCs.

Perfect for creating:

🏟️ Gym Leaders

📖 Story progression

❤️ Healing NPCs

🎁 Reward trainers

🧭 Quest or utility NPCs

✨ Features
🧑‍🏫 Trainer NPCs

Create NPC trainers that battle players using Cobblemon teams.

Features include:

⚔️ Cobblemon trainer battles

📈 Optional level scaling to player's strongest Pokémon

🎯 Custom IVs, EVs, moves, abilities, and levels

🎮 Singles or doubles battle formats

🎒 Custom item usage rules

🔒 Optional level caps

👥 Multiple players can challenge the same trainer simultaneously

🎁 Rewards after victory

⏱️ Cooldown-based or one-time rewards

🏆 Gym Progression System

Create real Pokémon-style gym progression.

Players must defeat certain trainers before challenging others.

Example progression:

Rock Gym ➜ Grass Gym ➜ Electric Gym

Example command:

/trainernpc require grass_gym set all rock_gym

If a player hasn't defeated the required trainer, the challenge is blocked and a custom message is displayed.

🧍 Command NPCs

Create simple NPCs that run commands when interacted with.

Examples:

❤️ /pokeheal

📦 /pc

🧭 /warp spawn

📜 Quest or dialogue triggers

Commands run as the interacting player, ensuring compatibility with permissions and other mods.

🎨 NPC Customization

TrainerNPCs allows extensive NPC customization.

🧑‍🎤 Player Skins

NPCs can use Minecraft player skins by username, even if that player has never joined the server.

💬 Overhead Text

Add formatted text above NPCs.

Formatting example:

&l&dGrass Gym Leader

Supports Minecraft formatting codes.

👀 Behavior

NPCs:

👁️ Look at nearby players

🚫 Cannot move

🛡️ Cannot be damaged

📋 Do not appear in the player tab list

⚙️ Server-Friendly Design

TrainerNPCs was built with public servers in mind.

Security features include:

🛡️ NPCs are invulnerable

🚫 Commands never run as console

⏳ Interaction anti-spam protection

🔐 LuckPerms compatible permission checks

🧾 Server-side validation of NPC data

NPCs also automatically:

📦 Despawn when chunks unload

🔄 Respawn when the area is loaded again

This keeps entity counts low and improves server performance.

📦 Requirements
Server

Fabric Loader

Fabric API

Cobblemon

Radical Cobblemon Trainers API (RCT API)

Client

Fabric Loader

Fabric API

TrainerNPCs Client Mod

🛠️ Building the Mod

Requires Java 21.

Build using Gradle:

./gradlew build

Output jars:

server/build/libs/trainernpcs-server.jar
client/build/libs/trainernpcs-client.jar
📜 Example Commands
Create a Trainer NPC
/trainernpc create rock_gym rock_trainer
/trainernpc spawn rock_gym
Require another trainer to be defeated
/trainernpc require grass_gym set all rock_gym
Create a Command NPC
/npc create healer
/npc spawn healer
/npc setcmd healer pokeheal
🚧 Planned Features

Future improvements may include:

🖥️ GUI trainer editor

💬 Dialogue system

🧭 Quest framework

📚 Datapack trainer templates

🎲 Advanced reward pools

🎭 NPC animations
