# Crystal's Icarus Mod Releases

This folder contains the latest downloadable releases for all of the mods.

# Usage

Mods need to be installed using [Icarus Mod Manager](https://github.com/CrystalFerrai/IcarusModManager). Once installed, just play the game and enjoy. Whenever the game updates, run the mod manager and press the install button to integrate the mods with the latest game data. The mods themselves do not need to be updated most of the time, only installed again.

If you play with other mods not designed for the mod manager, it is recommended that you load them into the mod manager anyway. Then, place any of my mods after those to ensure they merge properly. Failure to do this may result in conflicts between mod manager mods and other mods.

# Mod Details

## Deep Ore Fast

Increases the mining speed of the biofuel and electric deep ore mining drills.

* Biofuel drill: +0% -> +75%
* Electric drill: +33% -> +100%

[Download Here](https://github.com/CrystalFerrai/IcarusMods/raw/main/Release/DeepOreFast.zip)

## Exotic Spawner

**The game now has its own exotic respawning mechanic in open world, so this mod is no longer needed. However, there are some differences with how the mod works that might be preferable for some people.**

Spawns 3 exotics veins in open world propsects containing 200-400 exotics each at random locations. Once a vein is fully emptied, another one will automatically spawn a short while later (10 minutes or less) at a new location. Once all possible vein locations have spawned - there are around 70 per map - new veins will stop spawning.

**This mod only functions in open world prospects, not missions or outposts.**

You can press F7 to access a menu with advanced commands. From here, you can clear the map of all radar scans to clean up after many scans have been completed. You can also remove all depleted exotics veins, allowing new ones to later spawn in their place. These commands work regardless whether you are in an open world prospect or not. However, new veins will only spawn in open world.

How does this mod differ from the vanilla exotic respawning?
* This mod spawns deposits with slightly more exotics on average. 200-400 vs vanilla 100-300.
* This mod looks for empty deposits and respawns them every 10 minutes vs vanilla every 3 hours.
* This mod has no fancy visual effects for respawning like the vanilla game does.
* This mod only respawns exotics deposits, not exotics cave voxels which the vanilla game also respawns.
* Clearing radar scans from the map can be done manually at any time using the mod. The vanilla game clears them automatically when it spawns new deposits, and no other time.
* Removing depleted deposits can be done manually at any time using the mod. The vanilla game removes them automatically when it spawns new deposits, and no other time.

This mod does not explicitly prevent the vanilla respawn mechanics from happening. However, the vanilla event only runs when there are less than 3 exotic deposits present, and this mod always spawns a new one when there are less than 3. So the vanilla event usually will not happen as a result.

[Download Here](https://github.com/CrystalFerrai/IcarusMods/raw/main/Release/ExoticSpawner.zip)

## Recipe Tweaks

Tweaks various recipes to balance against time and resource availability.

* Concrete Mix now produces 4 instead of 1 and takes half as long to process.
  * This can be overridden by the Extra Concrete mod if you want a lesser bonus.
* Refined wood takes half as long to process.
* Steel bloom creates 2 steel ingots instead of 1.
* Copper wire output is doubled.

[Download Here](https://github.com/CrystalFerrai/IcarusMods/raw/main/Release/RecipeTweaks.zip)

## Fast Pickup

Reduces the action hold time for picking up deployables from 3 seconds to 0.5 seconds.

[Download Here](https://github.com/CrystalFerrai/IcarusMods/raw/main/Release/FastPickup.zip)

## Extra Concrete

The concrete mix recipe now produces 2 concrete at no extra cost.

[Download Here](https://github.com/CrystalFerrai/IcarusMods/raw/main/Release/ExtraConcrete.zip)

## Hide Geometry Screen

Prevents the game from displaying the "Preparing Geometry" screen, allowing you to see things loading in behind it. Intended to help people diagnose cases where the screen gets stuck and never closes.

[Download Here](https://github.com/CrystalFerrai/IcarusMods/raw/main/Release/HideGeometryScreen.zip)

## Info Mod

This mod assists with gathering information about things in the game world. This is primarily intended to assist with data mining and bug reporting efforts.

The mod will display your current character position and rotation at the top left of the screen. This display can be toggled off/on by pressing \[Ctrl + Numpad 6\].

Pressing \[Numpad 6\] will perform a scan for locations and other details of various objects in the world and open a fullscreen overlay showing the results. This overlay auto-refreshes data every 10 seconds while it remains open. It also provides buttons to toggle location markers for objects on the game map and compass. (This overlay only functions if the mod is installed by the current host or dedicated server.)

Pressing \[Alt + Numpad 6\] will start a continuous scan of whatever your game camera is currently looking at. It will display some information in the middle of your screen about your target such as actor class and material type.

[Download Here](https://github.com/CrystalFerrai/IcarusMods/raw/main/Release/InfoMod.zip)

## Lantern Fuel
Inrcreases the fuel that a lantern can hold from 1000 to 2500 and increases the biofuel lamp fuel from 2000 to 2500 to match the lantern.

[Download Here](https://github.com/CrystalFerrai/IcarusMods/raw/main/Release/LanternFuel.zip)

## Loadout

Increases loadout and drop ship slots from 15 to 20.

[Download Here](https://github.com/CrystalFerrai/IcarusMods/raw/main/Release/Loadout.zip)

Warning: Do not run the game without this mod if any of your loadouts or dropships currently have more than 15 items in them as the extra items may be lost.

## More Power
Increases power output and lowers fuel consumption for generators.

**Power Output**

* Biofuel generator: 5000 -> 10000
* Waterwheel: 2000 -> 4000
* Solar panel: 6000 -> 12000
* Wind Turbine: 1750 -> 3500

**Power Storage**

* Basic Battery: 1500 -> 3000
* Advanced Battery: 10000 -> 20000

**Fuel Consumption**

A full can of biofuel will last 8 hours 20 minutes in a generator, double the vanilla time of 4 hours 10 minutes.

[Download Here](https://github.com/CrystalFerrai/IcarusMods/raw/main/Release/MorePower.zip)

## No Plant Fatigue
Removes plant fatigue from crop plots for all plants except "strange plants". Note that the Fatigue debuff will still appear, but it will stay at -100%, meaning it does not do anything.

[Download Here](https://github.com/CrystalFerrai/IcarusMods/raw/main/Release/NoPlantFatigue.zip)

## Red Exotics Mission

Adds a new mission to the Prometheus map called "HARVEST: Red Exotics". This is an exploration mission (30 days, no objectives) that is accessible after completing the fourth story mission. This new mission contains 10 red exotic trees for harvesting.

[Download Here](https://github.com/CrystalFerrai/IcarusMods/raw/main/Release/RedExoMission.zip)

## Lava Cooler

Reduces the ambient heat around lava pools. It still gets very hot, but stays within a range that can be mitigated via gears, buffs, etc. By default, lava areas can reach temperatures of 130C (even though the in-game UI caps at 90C). This mod brings that down to a maximum of around 90C.

[Download Here](https://github.com/CrystalFerrai/IcarusMods/raw/main/Release/LavaCooler.zip)
