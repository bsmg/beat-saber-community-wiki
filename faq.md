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
[Beat Drop](https://bsaber.com/beatdrop/) is a desktop application that allows you to download songs, and create playlists as well! Created by StarGazer1258.

### Bootleg BeatSaver Search
An [external search engine](http://bootleg-beatsaver.com/) that enables more advanced searching functionality to help you find songs on BeatSaver, by Zeekin.

### Beat Saber Songs
Another [external search engine](https://beatsaber-songs.herokuapp.com/) with more advanced searching functionality to help you find songs on BeatSaver, by rorekk.

We also have a dedicated channel on the Modding Group Discord: [`#finished-maps`](https://discordapp.com/channels/441805394323439646/442342190060929055/)

## How do I make a beatmap?

See [mapping](../mapping)!

## How do I install playlists?
Place the playlist file into `Beat Saber/Playlists` and select it in-game, then hit download. You can create playlists using BeatDrop.

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

To get mods back, simply **run the installer again**
The BeatMods repository only includes mods that have been confirmed to work on the latest version of the game!

If you're confused by any of this, visit [Beginners Guide](beginners-guide).

## How does the scoring system work in Beat Saber? How does global ranking work?
We have sections on the [grips and tricks](grips-and-tricks) page dedicated to the scoring and ranking systems, check them out!

## Why are the vote buttons greyed out in game?

To vote on songs, you must have an account on Beat Saver, then input your access token in the modprefs file.

`\Beat Saber\UserData\modprefs.ini`

Change the value for: `apiAccessToken=replace-this-with-your-api-token`

Use the value from your beatsaver account by going to the access tokens page on your profile.
https://gyazo.com/46da60331d8bfabd4833ab85bcb73535


## My menus are blank and I have nothing to click on!
If the main window in your game is blank, your save file likely got corrupted.

To fix it, navigate to:
`%AppData%\..\LocalLow\Hyperbolic Magnetism`

Delete or rename the Beat Saber folder to something else. When you re-enter the game, it'll recreate the save file and should load the main menu properly.

## How did you run the invitational (2018) stream?

Megalon made a 6-part writeup in the discord in early July 2018, and the following link to those posts in the BSMG discord:

1. [Setup RTMP server and connections](https://discordapp.com/channels/441805394323439646/441805394323439648/463600705811251200)
2. [Recieve the streams in OBS](https://discordapp.com/channels/441805394323439646/441805394323439648/463603246842511362)
3. [OBS workflow and tips](https://discordapp.com/channels/441805394323439646/441805394323439648/463606263926751233)
4. [Creating the UI](https://discordapp.com/channels/441805394323439646/441805394323439648/463615913405448192)
5. [The Live Score display](https://discordapp.com/channels/441805394323439646/441805394323439648/463621857913077770)
6. [Audio and music](https://discordapp.com/channels/441805394323439646/441805394323439648/463651616235716619)

       