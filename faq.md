<!-- TITLE: FAQ -->
<!-- SUBTITLE: Frequently Asked Questions! -->


# How do I load custom songs?

Use the mod manager by Umbranox! 
Follow the instructions in the [beginners-guide](beginners-guide).

# Where do I find custom songs?

## Beat Saver
Nearly all custom songs are stored on Beat Saver!
Here you can also upload your own beatmaps to share with others.
Note that the Ingame Downloader Plugin loads songs directly from Beat Saver!
https://beatsaver.com/

## Beast Saber
Find reviews and playlists on Beast Saber!
https://bsaber.com/

## Discord
We also have a designated channel on the Modding Group Discord!
[#finished-maps](https://discordapp.com/channels/441805394323439646/442342190060929055/)

# How do I load other plugins?

Only manually approved mods uploaded to modsaber.ml are included in the mod manager.
(If you don't have any mods yet, run the mod manager from [beginners-guide](beginners-guide).)

If you'd like to add another mod that isn't included in the mod manager, you have to place the mod manually in the following directories:

.dll plugins go in this directory
Steam:
`steamapps\common\Beat Saber\Plugins`

Oculus:
`hyperbolic-magnetism-beat-saber\Plugins`

Asset replacement plugins go in this directory
Steam:
`steamapps\common\Beat Saber\Beat Saber_Data`

Oculus:
`hyperbolic-magnetism-beat-saber\Beat Saber_Data`

# Custom sabers?

## How do I use custom sabers?
Using custom sabers: Here is a video tutorial https://youtu.be/dUzyochSTt4
(Add link to #beginners-guide section here)

## How do I make custom sabers?
Making custom sabers:
Here is a written tutorial:
https://bs.assistant.moe/Sabers/
And here is a video tutorial:
https://www.youtube.com/watch?v=mhMeR9CEUjk

# Custom avatars?

## How do I use Custom Avatars?
Using custom avatars: Follow the instructions included with the plugin
https://github.com/xyonico/CustomAvatarsPlugin/releases/latest

Use Page Up / Page Down to switch avatars in game.
Use the Home key on your keyboard to toggle your avatar in first person view

## How do I make Custom Avatars?
Making custom avatars: Here is a full body avatar tutorial by Assistant https://bs.assistant.moe/Avatars/

# Multiplayer?

Here is a guide to setup the multiplayer plugin: https://bs.assistant.moe/Multiplayer/

# My game updated and now none of my mods are working!
Each time the game updates it is possible that mods will stop working and need to be updated.
The devs realize this, so when the game updates and you run it for the first time, everything in the Plugins folder is moved into the `Incompatible Plugins` folder. **Leave those plugins in there!**

To get mods back, simply **run the mod manager again.**
The mod manager only includes mods that have been proven to be compatible with the latest version of the game!

Get the mod manager from the [beginners-guide](beginners-guide).

# Should I use wrist weights when I play?

***DO NOT USE WRIST WEIGHTS!***
You will only hurt yourself. Besides, a lightsaber wouldn't be heavy, it's made of *light.*
Please read this comment for more information https://www.reddit.com/r/Vive/comments/8g9jgs/beat_saber_has_now_released/dya1yl7/

# My game will not load!

You may have a popup on your desktop asking about your Beat Saver auth token to vote on songs at the end of the game.
If you don't care to vote on songs, simply click "Cancel" and the popup will not appear again.

# My game launches, then instantly closes!

Check your plugins folder for `BeepBoop.dll`. This was a troll plugin designed to do exactly that.
Simply delete the dll file to fix it.

# "Your audio file name is wrong" message in the Edit Saber

The 3D editor only supports .ogg files. You have to convert your file to ogg using a converter, such as audacity.
If you simply change the file extension to .ogg, it will not work.

# How do I delay a song so that it doesn't start right when the level loads?

Currently this isn't possible in Beat Saber. For now you have to edit the song in an audio editor (such as Audacity) to add silence at the beginning of the track.

# I tried to install mods via the Mod Installer but it gives me an error that it can't find the IPA.exe.

Try installing the song injector separately, then try running the mod installer again. https://github.com/xyonico/BeatSaberSongInjector/releases

# I want to double the BPM of my song, is there an easy way to do that?

Here is a python 3 script that will multiply the BPM and _time values in your json file by any given factor:
https://cdn.discordapp.com/attachments/442372806705938434/447910905972523008/beat-saber-time-multiplier.zip

