<!-- TITLE: Beginners Guide -->
<!-- SUBTITLE: Getting Started -->

# How to install mods

Beat Saber was not designed with mod support, so you have to run one of the installers below to patch the game and enable mods.

> It's not recommended to install mods without knowing what they do, this can lead to undesired behaviors and performance issues. Click the `View Selected Mod Info` button in the ModSaber Installer, or the `More Info` button in the Mod Manager to learn more about a mod.
{.is-danger}

> The mod manager only shows mods compatible with the latest game update.
> Every time the game updates, you will have to run the mod manager to get all compatible mods.
> As all mods are made by volunteers, you may need to wait for your favorite mod to be fixed for the latest game update. Check the #server-announcements channel in the discord for the latest updates!
{.is-warning}

## ModSaber Installer
The new **recommended** mod installer! Both are similar in function, but this one offers richer debugging capabilities if things go wrong.
* Navigate to https://github.com/lolPants/modsaber-installer/releases
* Download `modsaber-installer-setup-{version}.exe` and install it
* Run it! Select what mods you want to install from the list!

Mods are installed into the folder `Plugins` within your Beat Saber install directory.
Can't find where Beat Saber is installed? See [install folder.](faq/install-folder)

## Manual Installation
If you've already used to the installer to patch the game, skip to step 4.
1. Download [IPA](https://www.modsaber.org/mod/illusion-plugin-architecture).
2. Navigate to your [install folder.](faq/install-folder)
3. Drag Beat Saber.exe on top of IPA.exe to patch the game. Any mods in the `Plugins` folder will now be loaded when starting the game.
4. Download the mod you wish to install, whether it be from GitHub, [ModSaber](https://www.modsaber.org/), or the #finished-mods tab in the Discord. Make sure to download any dependencies required by the mod.
5. Some mods have installation instructions, some don't. Generally you can just drag and drop the zip contents into your beat saber install folder, and the files should go into the corresponding folders. 
# How to get more songs
The Mod Manager includes the `Song Loader Plugin`, which enables you to load more songs into the game, but only includes one test song.

## Ingame Downloader
The installers include the `BeatSaver Downloader` Plugin, which allows you to download beatmaps in-game using the `MORE SONGS` menu button on the main menu screen. This pulls maps directly from www.beatsaver.com

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