<!-- TITLE: Beginners Guide -->
<!-- SUBTITLE: Getting Started -->

# How to install mods

Beat Saber was not designed with mod support, so it needs to be patchched to enable mods.

> It's not recommended to install mods without knowing what they do, this can lead to undesired behaviors and performance issues. {.is-danger}

> Every time the game updates, you will have to do this process again to get all compatible mods. 
> Since mods are made by volunteers, you may need to wait for your favorite mod to be fixed for the latest game version. Make sure to check the #server-announcements channel in the discord for the latest updates!
{.is-warning}

## Mod Installer ?
The mod repository ModSaber has shut down, and lolPants has left a [message](https://www.modsaber.org/) on the site explaining the situation. We are working on a replacement service and ask for your patience.

The [BeatSaber Mod Manager](https://github.com/beat-saber-modding-group/BeatSaberModInstaller/releases/latest) has been modified to use our new mods repository, [BeatMods](https://beatmods.com/)! There's another installer in the works, but until then feel free to use the modified Mod Manager!

**Run the game at least once** before trying to mod the game! This applies to reinstalling your game too. 

> If your game is **crashing** upon installing mods with the Mod Manager for the first time, try **verifying your files with Steam**, or **reinstalling** the game with Oculus. Some changes had to be made regarding the way IPA works, and some users are missing important game files.
> BSIPA is currently known **incompatible** with certain programs like FaceIt (cs:go matchmaking service). If you're getting any GetThreadContext failed errors, uninstall FaceIt 
{.is-warning}


> Make sure to scroll over to the right to see the Custom Maps pack! If you don't see anything, make sure that the following are correct:
> a) You're scrolling right to actually see the CustomMaps songpack
> b) There actually is a Plugins folder in your install directory
> c) Steam/Oculus is launching Beat Saber from the same installation that mods are in, e.g. mods are on the D drive but steam is launching from the C drive

![Custommaps](/uploads/custommaps.png "Custommaps")

## Manual Installation

**Run the game at least once** before trying to mod the game! This applies to reinstalling your game too. 

1. Download [BSIPA](https://github.com/nike4613/BeatSaber-IPA-Reloaded/releases/latest/download/Release.zip).
2. Navigate to your [install folder.](faq/install-folder) and extract the contents of BSPIA into it.
![Directory Clean](/uploads/directory-clean.png "Directory Clean")
![Directory Ipa](/uploads/directory-ipa.png "Directory Ipa")
3. Double click IPA.exe to patch the game. A console window will pop up, and if there aren't any errors then any mods in the `Plugins` folder will now be loaded when starting the game. If there are errors, you probably didn't follow step 2 correctly.
![Directory Patched](/uploads/directory-patched.png "Directory Patched")
4. Download the mod(s) you wish to install, whether it be from GitHub, the #finished-mods channel, or other sources. **Make sure to download any dependencies required by the mod.**
![Directory Plugins](/uploads/directory-plugins.png "Directory Plugins")
5. Some mods have installation instructions, some don't. Generally you can just drag and drop the zip contents into your beat saber install folder, and the files should go into the corresponding folders. 

> Make sure to scroll over to the right to see the Custom Maps pack! If you don't see anything, you probably installed your mods wrong. Don't panic and don't uninstall the game - delete your Plugins folder and try again.

![Custommaps](/uploads/custommaps.png "Custommaps")
# How to get more songs
The `Song Loader Plugin` enables you to load more songs into the game, but only includes one test song.

## Ingame Downloader
The `BeatSaver Downloader` Plugin allows you to download maps in-game using the `MORE SONGS` menu button on the main menu screen. This pulls maps directly from www.beatsaver.com

## Beat Saver
[Beat Saver](https://www.beatsaver.com) is the central repository that holds nearly all custom songs/maps for Beat Saber.
You can manually place the zip files downloaded from Beat Saver into the `CustomSongs` folder in your Beat Saber directory, use the In-Game Downloader Plugin, or use the OneClick Install button if you're using the [ModSaber Installer](https://www.modsaber.org/).

There are a couple more resources to help you find songs over in the [FAQ](faq#more-songs)

# How to uninstall mods
**Currently the only way to uninstall a mod is to remove the dll from the `Plugins` folder.**
|  |  |
| --- | --- |
| Steam | `\steamapps\common\Beat Saber\Plugins` |
| Oculus | `\hyperbolic-magnetism-beat-saber\Plugins` | 

# Where to go from here
* [Grips and tricks](grips-and-tricks)
* [Making beatmaps](mapping)
* [Custom sabers](models/custom-sabers)
* [Custom avatars](models/custom-avatars)
* [Custom platforms](models/custom-platforms)
* [Setup multiplayer](https://bs.assistant.moe/Multiplayer/)
* [Making mods](modding)

# Have questions?
Visit the [FAQ](faq) or drop by the #support tab in the [discord](https://discord.gg/beatsabermods)!