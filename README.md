Imperium creates a unique new way to play Rust, first used on servers such as Rust Factions and The Lost Isles. Claim land, fight wars, and battle for supremacy!

At its heart, Imperium adds the idea of "territory" to Rust. The game is divided into a grid of tiles matching those displayed on the in-game map. Players can create factions, and these factions can claim these tiles of land and levy taxes on resources harvested therein. Factions can declare war on one another and battle for control of the territory.

To allow you to restrict PVP only to certain areas, Imperium can also add zones around monuments and events like airdrops and heli crashes. These appear in-game as domes over the areas, and you can choose to block PVP damage outside of these domes.

Imperium is extremely configurable, leading to a wide range of game modes. Here are some ideas!

* Create a RP/PVE server where players can claim land to avoid being raided, and PVP is restricted to monuments and events.
* Create a server similar to PVE-Conflict in Conan Exiles, where player structures can't be raided but PVP is allowed everywhere.
* Create a more traditional PVP server, but factions can claim land and have to declare war on one another in order to raid.

## Permissions

* `imperium.factions.admin`
* `imperium.claims.admin`
* `imperium.badlands.admin`
* `imperium.pins.admin`
* `imperium.factions`
## Chat Commands
**Commons**
* `/help` Show Imperium plugin help
* `/map` Show Imperium map
* `/pvp` Toggle pvp on and off (Can hurt only other players with pvp mode on)

**Creating and managing factions**
* `/faction create FACTION_NAME` Create faction with name
* `/faction invite PLAYER` Invite a player to your faction
* `/faction join NAME` Join a faction if has been invited
* `/faction show` Show information about your faction
* `/faction leave` Leave current faction
* `/faction promote PLAYER` Promote a faction member to manager role
* `/faction demote PLAYER` Demote a faction manager to member role
* `/faction kick PLAYER` Remove a member from your faction
* `/faction disband forever` Permanently disband your faction
* `/faction help` Show help about the faction command

**Claiming and managing land**

For server admins
* `/claim assign FACTION_NAME` Start interaction to assign claim to specified faction **(Admin only!)**
* `/claim delete XY` Delete any claim on the specified land **(Admin only!)**

For players
* `/claim` or `/claim add` Start interaction to claim the land you are on
* `/claim remove` Start interaction to remove claim on the land you are on
* `/claim hq` Start interaction to set land as headquarters
* `/claim cost XY` Show cost to claim the specified land
* `/claim give FACTION_NAME` Give land to another faction
* `/claim list` Show a list of claimed land
* `/claim rename XY` Rename the specified land
* `/claim upkeep` Show the land scrap upkeep (if claim upkeep is enabled in the configs)
* `/claim help` Show help about the claim command

**Managing taxes**
* `/tax chest` Start interaction to set faction's tax chest
* `/tax rate XX` Set faction tax rate percentage
* `/tax help` Show help about the tax command

**Declaring war against other factions**
* `/war declare FACTION_NAME` Declare war against the specified faction
* `/war end FACTION_NAME` Ask (or accept) to end the war with the specified faction
* `/war help` Show help about the war command

## What's new in 2.0.0?
**Fixes:**
* Land areas will now correctly align with the in-game map grid
* Plugin now uses icons from /data/ImperiumImages. Download [this image pack](https://github.com/vicbarbosa/rust-imperium-images/archive/refs/heads/master.zip) and put ImperiumImages folder inside your server's data folder and everything should work.

**New features**
* Claimed areas now show in the in-game map as colored circles.
* Support for underground badlands (to allow pvp inside tunnels and underwater labs)
* Option for faction leaders to decide if their own land allows unrestricted pvp with `/faction badlands` command
* Land upgrading. Leaders and Managers can upgrade land level to increase bonuses in that land with `/upgrade land` command
* War option to require admins to approve or deny wars with in-game commands `/war admin approve`, `/war admin deny` and `/war admin pending`
* War option to allow Shop Front peace: If leaders from both enemy factions perform any trade in a shop front, the war will be over
* War option to require defenders to approve or deny wars with in-game commands  `/war approve`, `/war deny` and `/war pending`
* War option to require scrap payment to declare war (To discourage pointless wars)
* War option to protect noob factions from wars. Default value is 24 hours (86400 seconds)
* War option to require defender members online in order to declare war (To discourage offline raiding)
* MapGridYOffset parameter to adjust the vertical land grid (This is a hacky solution to fix some cases where the land is generated with a offset of 1 grid) 

**WORK IN PROGRESS**

Some config options already exists but they don't do anything for now because I'm still working on it so ignore the following in your config file:

*`war priorAggressionRequired`
*`war spamPreventionSeconds`
*`upgrade maxProduceBonus`
*`upgrade maxRecruitBotBuffs`
*`recruiting enabled`

**Features planned for the future**
Allied bot recruiting, procedural storytellying, land passive resource produce with specific resources per type of land, optional Faction Karma system to encourage roleplaying and other interesting conflicts.

**KNOWN ISSUES**
* Configs from previous versions are not compatible
* Data from previous versions are not compatible
* The plugin might spam a OnEntityTakeDamage error when you first start the server. If this happens just run oxide.reload Imperium and everything should work

[Donations ](https://www.paypal.com/donate/?token=kS3ubEttzXAW5nN07ZuubIvdge3i2pj7zSM2YzaCd9mj_oFI6JQikZi72Wtfe1u7HUnKY3DoUsQRjvjH&locale.x=US) are appreciated, but never required.

## Credits
- **chucklenugget**, the original author of this plugin 
- **Orange**, the previous maintainer
- Huge thanks to the authors of Zone Manager, Lusty Map and Dynamic PVP, which inspired and guided my work on Imperium. Also a huge thanks to Disconnect and Gamegeared, the admins of The Lost Isles and Rust Factions, who contributed countless ideas to Imperium and were patient as I shook out the bugs.
- Special thanks to 2022 testers Danilão and AguaRaiss