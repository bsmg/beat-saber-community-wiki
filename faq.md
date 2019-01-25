<!-- TITLE: FAQ -->
<!-- SUBTITLE: Frequently Asked Questions! -->
# FAQ
## I just got the game, how do I get started?
Check out our [beginner's guide](beginners-guide)!

## How do I get more songs?
If you don't like using [beatsaver](https://www.beatsaver.com) to find songs, here are some other tools to help you out!

### Beast Saber
[Beast Saber](https://www.bsaber.com) is a review site that aims to curate all of the songs on Beat Saver! You can also download playlists, follow mappers, find songs using advanced sorting methods and more. Created by elliotttate.

### Beat Drop
[Beat Drop](https://bsaber.com/beatdrop/) is a desktop application that allows you to download songs, and create playlists as well! Created by Stargazer.

### Bootleg BeatSaver Search
An [external search engine](http://bootleg-beatsaver.com/) that enables more advanced searching functionality to help you find songs on BeatSaver, by Zeekin.

### Beat Saber Songs
Another [external search engine](https://beatsaber-songs.herokuapp.com/) with more advanced searching functionality to help you find songs on BeatSaver, by rorekk.

We also have a dedicated channel on the Modding Group Discord: [`#finished-maps`](https://discordapp.com/channels/441805394323439646/442342190060929055/)

## How do I make a beatmap?

See [mapping](../mapping).

## How do I load plugins that aren't in the Mod Installer?

After you have run the ModSaber Installer, you can then add/delete other mods in the following directory:

`.dll` plugins go in the directory:
|  |  |
| --- | --- |
| Steam | `steamapps\common\Beat Saber\Plugins` |
| Oculus | `hyperbolic-magnetism-beat-saber\Plugins` |


## How does the multiplayer mod work?

The official multiplayer has not been released, but you can use the multiplayer mod by Andruzzzhka.
Here is a guide to set up the multiplayer mod: https://bs.assistant.moe/Multiplayer/

## My game updated and now none of my mods are working!
Each time the game updates it is possible *(and very likely)* that your existing will stop working and need to be updated.
The devs realized this, so when the game updates and you run it for the first time, everything in the `Plugins` folder is moved into the `Incompatible Plugins` folder. **Leave those plugins in there!**

To get mods back, simply **run the installer again.**
Both the modsaber installer and the mod manager only includes mods that have been confirmed to work on the latest version of the game!

Get the installer from [Beginners Guide](beginners-guide).

## How does the scoring system work in Beat Saber? How does global ranking work?
We have sections on the [grips and tricks](grips-and-tricks) page dedicated to the scoring and ranking systems, check them out!

## Should I use wrist weights when I play?
> **PLEASE DO NOT, UNLESS YOU'RE A TRAINED PROFESSIONAL**
{.is-danger}

In which you'd know why not to use wrist weights. Besides, a lightsaber wouldn't be heavy, *it's made of plasma.*
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

## My menus are blank and I have nothing to click on!
If the main window in your game is blank, your save file likely got corrupted.

To fix it, navigate to:
`%AppData%\..\LocalLow\Hyperbolic Magnetism`

Delete or rename the Beat Saber folder to something else. When you re-enter the game, it'll recreate the save file and should load the main menu properly.