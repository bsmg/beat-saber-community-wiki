<!-- TITLE: Beginners Guide -->
<!-- SUBTITLE: Getting Started -->

# How to install mods

## Preface
> This guide is for PC-modding on Windows. 
> If you have a Quest, check out the tutorial on [BeastSaber](https://bsaber.com/beaton/).
> If you're on Linux, check out [QBeat](https://github.com/geefr/beatsaber-linux-goodies/blob/master/README.md)


Beat Saber natively supports custom songs, so if that's all you're looking for, you don't require more mods! It's a wise idea to install `SongCore` though, as this mod expands upon the base game functionality to improve loading times and provide functionality for other mods like the in-game downloader, custom leaderboards, playlists, etc.

>By choosing to use mods, you understand that:
> - You may experience problems that don't exist in the vanilla game. 99.9% of bugs, crashes, and lag are due to mods.
> - Mods are subject to being broken by updates and that's normal - be patient and respectful when this happens, as modders are volunteers with real lives.
> - Beat Games aren't purposefully trying to break mods. They wish to work on the codebase and sometimes this breaks mods, but they are not out to kill mods.
> 
> Do not attack the devs for issues related to mods, and vice versa - modders and devs are two separate groups. Just don't be a jerk ok
{.is-danger}

Every time the game updates, you will have to do this process again to get all compatible mods. 
Since mods are made by volunteers, you may need to wait for your favorite mod to be fixed for the latest game version. Make sure to check the #server-announcements channel in the discord for the latest updates!

If you run into problems at any point, please head to the [support page](support#1-4-no-mods-in-game) and see if you can identify what went wrong before asking in the discord server. Chances are, your answer is on that page!

## Installers

### Mod Assistant

**This is the current recommended installer for mods.**

**Run the game at least once** before trying to mod the game! This applies to reinstalling your game too. 

A simple Beat Saber Mod Installer similar to the mod manager, but with additional features such as mod removal and version checking! Get it on [Assistant's GitHub](https://github.com/Assistant/ModAssistant/releases/latest)

![Modassistant](/uploads/modassistant.png "Modassistant")

### BeatDrop

**Run the game at least once** before trying to mod the game! This applies to reinstalling your game too. 

BeatDrop 2 is an iTunes / Spotify-like song manager, downloader, playlist creator and mod installer / manager for Beat Saber, all rolled up into a single beautiful and easy to use app. [Get it over on StarGazer's GitHub!](https://github.com/StarGazer1258/BeatDrop/releases). Here's a [short tutorial](https://www.notion.so/BeatDrop-2-Tutorial-e6a98d87b14a4621bd0941c5f8953be9) that explains how it works.

![Beatdrop 800](/uploads/beatdrop-800.jpg "Beatdrop 800")

Note that BeatDrop is still in development and currently lacks mod updating functionality, but it's highly recommended for song and playlist management. Stay tuned for the addition of more features! To update mods, simply uninstall the mod and redownload it to get the latest version, or use an alternative method to update your mods.

# How to get more songs
## Ingame Downloader
The `BeatSaver Downloader` Plugin allows you to download maps in-game using the `MORE SONGS` menu button on the `MODS` menu screen. This pulls maps directly from www.beatsaver.com

## Beat Saver
[Beat Saver](https://www.beatsaver.com) is the central repository that holds nearly all custom songs/maps for Beat Saber.
To install songs downloaded from the site, unzip them into a folder and place it into `Beat Saber/Beat Saber_Data/CustomLevels`.  You can also use the In-Game Downloader plugin.

There are a couple more resources to help you find songs over in the [FAQ](faq#more-songs)

# How to uninstall mods
**Currently the only way to uninstall a mod is to remove the dll from the `Plugins` folder.**
|  |  |
| --- | --- |
| Steam | `\steamapps\common\Beat Saber\Plugins` |
| Oculus | `\hyperbolic-magnetism-beat-saber\Plugins` | 


# Manual Installation
Only resort to this if you absolutely know what you're doing, the installer is the recommended way to install mods.

**Run the game at least once** before trying to mod the game! This applies to reinstalling your game too. 

1. Download [BSIPA](https://github.com/beat-saber-modding-group/BeatSaber-IPA-Reloaded/releases).
2. Navigate to your [install folder.](faq/install-folder) and extract the contents of BSPIA into it.
![Directory Clean](/uploads/directory-clean.png "Directory Clean")
![Directory Ipa](/uploads/directory-ipa.png "Directory Ipa")
3. Double click IPA.exe to patch the game. Any mods in the `Plugins` folder will now be loaded when starting the game. If there are errors, you probably didn't follow step 2 correctly.
![Directory Patched](/uploads/directory-patched.png "Directory Patched")
4. Download the mod(s) you wish to install, whether it be from GitHub, the #finished-mods channel, or other sources. **Make sure to download any dependencies required by the mod.**
![Directory Plugins](/uploads/directory-plugins.png "Directory Plugins")
5. Some mods have installation instructions, some don't. Generally you can just drag and drop the zip contents into your beat saber install folder, and the files should go into the corresponding folders. 

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