# Crystal's Icarus Mod Source

This readme is only for people who want to modify and/or build my mods. If you just want to use them, see the readme in the root directory.

# Project Setup

I recommend setting up a directory structure like this to get started:
```
IcarusMods (root)
 |- Icarus (project directory)
 |- IcarusMods (git repo)
 |- Staging (intermediate files)
```

## Setup Unreal

Install Unreal 4.27.latest using either the Epic Games Launcher or by building from source if you prefer (and have source access).

Once installed, run the editor and create a new C++ project named "Icarus".

> **The project must be named "Icarus". This is important.**

Save the project nearby where you cloned this git repo, but not inside the repo. (Recommended folder structure above.)

Once the project is created, you will need to create a bunch of C++ class stubs as well as blueprint stubs to imitate classes from the game. Which classes are needed and how to create them is beyond the scope of this document. You will still be able to examine the mod blueprints without doing this, but they will be full of errors due to missing classes.

In the future, I would like to include the necessary class and blueprint stubs in this repo to make things easier.

## Setup directory junctions

Each mod which has assets included in it will have a folder called "Source". This folder needs to be junctioned into your Unreal project in order for the mods to appear in the editor. The target location for each mod should be as follows.

```
[Path to Project]/Content/Mods/[Name of Mod]
```

You can create junctions using the built-in Windows utility `mklink`. The command line should look something like this:

```
mklink /J "[Path to mod in repo]\Source" "[Path to Project]/Content/Mods/[Name of Mod]"
```

## Setup Staging Directory

You will need to create a staging directory for mods which contain assets. This directory will contain a `response.txt` file along with cooked assets that can be packaged into pak files. For now, create the `response.txt` file with content like this:

```
[Full path to staging dir]\InfoMod\*.* ../../../Icarus/*.*
[Full path to staging dir]\ExoticSpawner\*.* ../../../Icarus/*.*
(repeat for each mod that contains assets)
```

Make sure you use the a full, rooted path to your staging directory for each line, such as "D:\IcarusMods\Staging". Relative paths will not work properly.

# Building Mods

Each mod contains a "Package" directory. Zip the contents of this directory to create a mod that can be loaded into Crystal's [Icarus Mod Manager](https://github.com/CrystalFerrai/IcarusModManager) (not to be confused with Jimk72's "Icarus Mod Manager").

If the mod contains Unreal assets (you will see a "Source" directory next to the "Package" directory), you will need to build and package those assets into a pak file which should also be included in the final zip file.

To build the Unreal assets, you will first need to setup an Icarus project as described in the "Project Setup" portion of this document. Then, from inside of the editor, select the File menu -> "Cook Content for Windows".

If the cook is successful, then it will output cooked versions of all of the assets for all of the mods. These files need to be copied to your staging directories, separating out each mod into its own, then package using UnrealPak. UnrealPak is a command line utility which can be found within your Unreal installation at `Engine/Binaries/Win64/UnrealPak.exe`.

I recommend building a batch file that will perform the copying and packaging for you so that you can repeat it easily. Here is an example for InfoMod:

```
set root=[appropriate location for your setup]
set pak=[path to UnrealPak.exe]

:: InfoMod
rd /s /q %root%\Staging\InfoMod
md %root%\Staging\InfoMod

xcopy %root%\Icarus\Saved\Cooked\WindowsNoEditor\Icarus\Content\Mods\InfoMod\*.* %root%\Staging\InfoMod\Content\Mods\InfoMod\*.* /s /y

%pak% %root%\InfoMod\Package\InfoMod_P.pak -Create=%root%\Staging\response.txt

:: ExoticSpawner
(repeat section above but for the next mod that contains assets)
```

Make sure the output pak file always has "_P" at the end of its name so that the game loads it properly.

The final built mod should be a zip file containing the contents of the source "Package" directory and the built pak file. Only mods with assets need a pak file.