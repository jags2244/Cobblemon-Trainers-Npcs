**TrainerNPCs**

TrainerNPCs is a Fabric mod for Cobblemon servers that allows server owners to create trainer NPCs and command NPCs.

Trainer NPCs start Cobblemon trainer battles using the Radical Cobblemon Trainers API, allowing servers to create gyms, story battles, and progression systems.

Command NPCs can run commands when interacted with, making them useful for things like healing, warps, and quests.

NPCs are optimized for server performance:

NPCs cannot move

NPCs cannot be damaged

NPCs look at nearby players

NPCs despawn when chunks unload and respawn when chunks reload

**Dependencies**

**Server**

Required mods:

Fabric Loader

Fabric API

Cobblemon

Radical Cobblemon Trainers API (RCT API)

TrainerNPCs Server

**Client**

Required mods:

Fabric Loader

Fabric API

TrainerNPCs Client

**Commands**

**Trainer NPC Commands**

Command	Description

/trainernpc create <npc_id> <trainer_id>	Creates a trainer NPC linked to an RCT trainer.

/trainernpc spawn <npc_id>	Spawns the trainer NPC at your location.

/trainernpc remove <npc_id>	Deletes the trainer NPC.

/trainernpc text <npc_id> <text>	Sets the text displayed above the NPC.

/trainernpc skin <npc_id> <username>	Sets the NPC skin using a Minecraft username.

/trainernpc reload	Reloads trainer NPC configuration files.

**Trainer Progression Commands**

Command	Description

/trainernpc require <npc_id> set all <trainer>	Player must defeat the listed trainer(s) before challenging this one.

/trainernpc require <npc_id> set any <trainer>	Player must defeat any one of the listed trainers.

/trainernpc require <npc_id> clear	Removes trainer requirements.

/trainernpc require <npc_id> message <text>	Sets the message shown when requirements are not met.

**Trainer Reward Commands**

Command	Description

/trainernpc rewards <npc_id> sethand	Sets the reward to the item in your hand.

/trainernpc rewards <npc_id> addhand	Adds the held item to the reward list.

/trainernpc rewards <npc_id> clear	Removes all rewards from the trainer.

/trainernpc rewards <npc_id> once	Makes rewards claimable once per player.

/trainernpc rewards <npc_id> cooldown <time>	Sets reward cooldown per player (example: 1h, 30m).

**Trainer Battle Rules**

Command	Description

/trainernpc rules <npc_id> format singles	Sets the battle format to singles.

/trainernpc rules <npc_id> format doubles	Sets the battle format to doubles.

/trainernpc rules <npc_id> itemusage default	Uses default item rules.

/trainernpc rules <npc_id> itemusage no_items	Disables bag items in battle.

/trainernpc rules <npc_id> itemusage held_only	Allows held items only.

/trainernpc rules <npc_id> itemusage limited	Limits item usage.

/trainernpc rules <npc_id> levelcap <level>	Sets a level cap for the battle.

**Command NPC Commands**

Command	Description

/npc create <npc_id>	Creates a command NPC.

/npc spawn <npc_id>	Spawns the NPC at your location.

/npc remove <npc_id>	Deletes the NPC.

/npc text <npc_id> <text>	Sets the text displayed above the NPC.

/npc skin <npc_id> <username>	Sets the NPC skin.

/npc setcmd <npc_id> <command>	Sets the command that runs when the NPC is interacted with.

/npc addcmd <npc_id> <command>	Adds another command to run.

/npc clearcmd <npc_id>	Removes all commands from the NPC.

/npc reload	Reloads NPC configurations.

**Example Usage**

Create a gym leader:

/trainernpc create rock_gym rock_trainer

/trainernpc spawn rock_gym

Require Rock Gym before Grass Gym:

/trainernpc require grass_gym set all rock_gym

Create a healer NPC:

/npc create healer

/npc spawn healer

/npc setcmd healer pokeheal

