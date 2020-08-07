## Doug's toybox
This is a place I talk about things

### Posts

1. [Smash Arena](#smash-arena)
2. [Idea for a new game](#idea-for-a-new-game)
3. [Class Expansion](#class-expansion)
4. [Starting Building](#starting-building)
5. [Old Activities](#old-activities)
5. [Player (and Monster) Statistics](#player-and-monster-statistics)

### Player (and Monster) Statistics
From a stats perspective the game is fair in that both players and enemies have the same stat types and they apply the same to both of them. For the players most of their stats come from gear choices and some from player progression; for enemies they are implicit (for now, ideas for random weapons or armour for enemies, allows things like disarms and armour breaking; but that's a future topic).
Like the game it was inspired by AQ and also Path of Exile, a resist system exists, needing a fire resist set against strong fire enemies is an intended choice but without a cap like found in PoE, instead all gear will have resists and balanced such that the maximum resist attainable will still be a good amount above 0. This creates a system where players might want to look for certain pieces to survive longer in various enemy type environments or certain weapons to greater damage tough opponents. 
As follows the remaining stats exist to allow players to increase in strength certain aspects of their character, but none that all characters want as much of as possible:
* Strength: Melee Damage
* Dex: Ranged Damage
* Int: Magic Damage
* Endurance: Health Points
* Spirit: Unique to each resource combination (see class expansion topic)
* Crit: Chance of greater effect (on things other than damage too hopefully)
* Initiative: Stat that allows uncontested free initial turns or chances to go again after a turn finishes
* Overload: Critical effect or multiplier
* Favour: Buff and Debuff Strength

Gear with various combinations of these stats are interesting to a varied basis of characters and most pieces of gear will have many stats. I worry that with this many stats as well as unique effects on gear as well as Resistance there is too much entropy in gear design, potentially fixed by only certain pieces of gear having certain stats if it becomes and issue; however it does allow for a LOT of gear to be created which is definitely a goal.

[Back to the top](#posts)
### Old Activities
Recently Google Sites shut down and was going to migrate to some new service and prompted me to save some old site I had from 10th grade english class. Looking over it I found a piece of art I had done back then, I made many pieces like it but lost almost all of them as I got older and transferred computers. I made a lot of art in this electronic abstract style and its really nice to have a copy of some of it back again. 
![dougart1](https://i.imgur.com/ZGBghbZ.jpg)

[Back to the top](#posts)
### Starting building
After looking into engines like Unity or RPG maker, since the game is 2d and not graphically intensive I decided to build in JS in HTML5 Canvas and build my own game engine. Not the easiest choice but I've never built a game from scratch without a prebuilt engine and I was willing to do the work to learn and plan it all out. As of now the basic turn based-combat system is integrated as well as most stats and resistances, as well as coding for allowing unique effects on items (things like rings that grant thorns or damage type conversion), the buff and debuff system is done as well, next to do is figure out essential UI functionality and the skill system. Here's an early look at the stats page (graphics temporary as hell)

![early stats page](https://i.imgur.com/BxFjY9G.png)

Done are gear switching and applying stats, the basic framework for attack coding and stat and resistance scaling as well.

[Back to the top](#posts)
### Class Expansion
So I have the ideas for most of the classes, Mana and Energy is a Cultist, Combo Points + Totems is undead themed, Rage and Mana is a Wild Mage, etc...
After those ideas I started thinking of skills and ways to uniquely interact with their unique resource combination, for example Wild Mages can spend large amounts of rage and mana for Powerful Effect and must balance mana use with rage generation. But from there I wanted slightly more uniqueness besides some skills and the resource so I started working on a statistic found on gear that would change the effect based on the players' class. Similar to something like Mastery in wow (but not exclusively damage oriented). For example Ranges (Totem + Energy) gain a stacking damage buff each turn they don't use a damaging skill based on this stat, Pure Mages (mana + mana) have the costs of their spells increased but also the damage, Barbarians (Rage+Rage) gain health regeneration. This is a cool effect in a game with  no class-gear exclusivity allow different pieces of gear to matter differently to different classes, or even different builds among the classes.

[Back to the top](#posts)
### Idea for a new game
I've been looking recently for a more modern game similar to one I played when I was younger: AdventureQuest. The game was a simple concept of open world adventuring with a simple combat system (mostly 1. Equip gear 2. Attack). Though it wasn't complicated, the sheer amount of content and decision making you had access to as a player kept me coming back; things like "Where will I get a better fire weapon" or "How do I get strong enough to defeat this werewolf?" were fun problems to solve given the amount of content (as tools) I had access too. I couldn't find anything similar; most similar games (jrpgs mainly) control whole parties, or are not open world, or some other issues that made them non-enticing.

I've always loved games that allow for tons of power-level wise character choise, games like Rift, Guild Wars 1, Runes of Magic, Custom hero maps in Warcraft 3 or Dota, and Path of Exile. I loved choosing a path, theorycrafting other character choices to make and tuning them as I actually played through the games, so for this I wanted something similar. Since Dual-class systems accomplish this so well I started there and elected 5 Resource types: 
* Rage (built by generating attacks or being hit)
* Energy (Builds over time), 
* Mana (Starts full but is spent on spells, not easily regained)
* Combo points (built and spent with effects based on how many are spent)
* Totems (Have certain # of types and can have only one of each, do different things and may have duration)

Then I wanted to allow the player to select any two of these and have a class waiting for them, as well as allow them to select one twice to greater focus that archetype. Though these abilities are nothing new to RPGS, most don't allow cross contamination to this extent though some experimentation has been dont in other games (rogues in many games have CP and Energy, Death Knights in wow have have Energyish and Rage, Bards in Rift have a totem like system and Energy). The reason I think this is not done in other games to this extent is that they can be very complicated if done intricately, and most other games involve a complicated combat system which they don't want to distract from. This game I'm thinking of would not have that and be turn and stats-based so complicated systems like this I think would work better.

[Back to the top](#posts)
### Smash Arena
So my friends and I often play games in Garry's Mod, most notably TTT. However I was interested in a game that I couldn't quite find, one that allows the fun pacing of games like quake and other arena based shooters with the accessibility of a game like Super Smash Bros. Seemed like a natural fit to transfer the "Knock enemies to their death" free for all style to a FPS setting. 

So I started designing the game and what a map would look like but the most important thing was the weapons players had. They have to be fun to use and versitile and unoptomized enough to create lasting gameplay. and I eventually settled on four: a bat that knocks enemies flying away, a shotgun that fires physics-enabled skins, a harpoon launcher, and a charging hitscan laser that sends enemies flying based on their vector difference from the shooter. Combined with the crist movement from the source engine, bunnyhopping and physics-based simulation the game is simple but fun and with good movement. Not a lot of a work, but a fun simple project to play with friends.
Mapmaking is done in Hammer and weapon and gamemode scripting is done in Lua.

![gmod blog picture](https://i.imgur.com/uTMcJeI.jpg)

[Back to the top](#posts)
