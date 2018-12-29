<!-- TITLE: FAQ -->
<!-- SUBTITLE: Frequently Asked Questions! -->
# FAQ
## After using the mod manager, I can't click anything in game!
Sounds like you pirated the game. If so, go sit in the corner of shame and think about what you've done. Once you've reflected on your mistakes, purchase the game from [Steam](https://store.steampowered.com/app/620980/Beat_Saber/) or [Oculus](https://www.oculus.com/experiences/rift/1304877726278670/) and the mods won't break your game.

## How do I load custom songs?
Follow the instructions in the [Beginners Guide](beginners-guide).

## Where do I find custom songs?
[Beat Saver](https://beatsaver.com/)
[Beast Saber](https://bsaber.com/)

We also have a dedicated channel on the Modding Group Discord: [`#finished-maps`](https://discordapp.com/channels/441805394323439646/442342190060929055/)

## How do I load plugins that aren't in the Mod Manager?

After you have run the Mod Manager, you can then add other plugins / mods in the following directory:

`.dll` plugins go in the directory:
|  |  |
| --- | --- |
| Steam | `steamapps\common\Beat Saber\Plugins` |
| Oculus | `hyperbolic-magnetism-beat-saber\Plugins` |

Asset replacement plugins go in the directory:
|  |  |
| --- | --- |
| Steam | `steamapps\common\Beat Saber\Beat Saber_Data` |
| Oculus | `hyperbolic-magnetism-beat-saber\Beat Saber_Data` |

**Can't find your install directory?** See: [Beat Saber install folder](faq/install-folder)

## Multiplayer?

The official multiplayer has not been released, but you can use the multiplayer mod by Andruzzzhka.
Here is a guide to set up the multiplayer mod: https://bs.assistant.moe/Multiplayer/

## My game updated and now none of my mods are working!
Each time the game updates it is possible *(and very likely)* that your existing will stop working and need to be updated.
The devs realized this, so when the game updates and you run it for the first time, everything in the `Plugins` folder is moved into the `Incompatible Plugins` folder. **Leave those plugins in there!**

To get mods back, simply **run the mod manager again.**
The mod manager only includes mods that have been confirmed to work on the latest version of the game!

Get the mod manager from the [Beginners Guide](beginners-guide).

## How does the scoring system work in Beat Saber?

Check out this video the devs released: https://twitter.com/beatsaber/status/992782948515622913?lang=en

Here is an image of the hitboxes for the notes: https://twitter.com/Split82/status/979365834324889600

## How do I revert to the original sabers after installing custom sabers?

Here are the [original saber models](/uploads/the-originals.saber "The Originals")!


## Should I use wrist weights when I play?
> **DO NOT USE WRIST WEIGHTS!**
{.is-danger}

You will only hurt yourself. Besides, a lightsaber wouldn't be heavy, *it's made of plasma.*
Please read [this comment](https://www.reddit.com/r/Vive/comments/8g9jgs/beat_saber_has_now_released/dya1yl7/) for more information.

## Why are the vote buttons greyed out in game?

To vote on songs, you must have an account on Beat Saver, then input your access token in the modprefs file.

`\Beat Saber\UserData\modprefs.ini`

Change the value for: `apiAccessToken=replace-this-with-your-api-token`

Use the value from your beatsaver account by going to the access tokens page on your profile.
https://gyazo.com/46da60331d8bfabd4833ab85bcb73535

## "Failed to get version info!" in the Mod Manager

This error means that the Mod Manager could not connect to https://modsaber.org
* Check your internet connection
* Check if the website is reachable for you (click the link above)
* Check that your firewall isn't blocking the Mod Manager from accessing the internet

![Mod Manager Error](/uploads/faq/mod-manager-error.png "Mod Manager Error")

## I tried to install mods via the Mod Installer but it gives me an error that it can't find the IPA.exe.
Try installing the [Song Loader](https://github.com/xyonico/BeatSaberSongLoader/releases) on its own, then try running the Mod Manager again.

## I can see my avatar in the menus, but it disappears when I start a song ??
Don't use Ikeiwa's version of the custom avatar plugin, it's outdated! Use [xyonico's](https://github.com/xyonico/CustomAvatarsPlugin/releases), also pinned in the `#model-discussion` channel.
