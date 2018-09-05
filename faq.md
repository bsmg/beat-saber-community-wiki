<!-- TITLE: FAQ -->
<!-- SUBTITLE: Frequently Asked Questions! -->

# FAQ

## How do I load custom songs?

Use the mod manager by Umbranox! 
Follow the instructions in the [beginners-guide](beginners-guide).

## Where do I find custom songs?

Beat Saver   : https://beatsaver.com/
Beast Saber : https://bsaber.com/
We also have a designated channel on the Modding Group Discord : [#finished-maps](https://discordapp.com/channels/441805394323439646/442342190060929055/)

## How do I load other plugins?

Essential mods are included in the mod manager by Umbranoxio!
Follow the instructions in the [beginners-guide](beginners-guide).

After you have run the mod manager, you can then add other plugins / mods as well.
Plugins / mods that aren't in the mod manager have to be placed manually in the following directories:

.dll plugins go in the following directory
Steam:
`steamapps\common\Beat Saber\Plugins`

Oculus:
`hyperbolic-magnetism-beat-saber\Plugins`

Asset replacement plugins go in the directory
Steam:
`steamapps\common\Beat Saber\Beat Saber_Data`

Oculus:
`hyperbolic-magnetism-beat-saber\Beat Saber_Data`

## Custom sabers?

### How do I use custom sabers?
Using custom sabers: Here is a video tutorial https://youtu.be/dUzyochSTt4
(Add link to #beginners-guide section here)

### How do I make custom sabers?
Making custom sabers:
Here is a written tutorial:
https://bs.assistant.moe/Sabers/
And here is a video tutorial:
https://www.youtube.com/watch?v=mhMeR9CEUjk

## Custom avatars?

### How do I use Custom Avatars?
Using custom avatars: Follow the instructions included with the plugin
https://github.com/xyonico/CustomAvatarsPlugin/releases/latest

Use Page Up / Page Down to switch avatars in game.
Use the Home key on your keyboard to toggle your avatar in first person view

### How do I make Custom Avatars?
Making custom avatars: Here is a full body avatar tutorial by Assistant https://bs.assistant.moe/Avatars/

## Multiplayer?

Here is a guide to setup the multiplayer plugin: https://bs.assistant.moe/Multiplayer/

## How do I make a Beatmap?

There are currently 3 editors. All export the same files, but offer different workflows.

### Edit Saber
A robust 3D track editor made in Unreal Engine by ikeiwa!
https://github.com/Ikeiwa/EditSaber/releases

### Unofficial 2D Track Editor
A 2D track editor made in Processing by Megalon!
**Note: This is depreciated! Please use the 3D editor (Edit Saber) instead!**
https://github.com/megalon/BeatSaber-UnofficialTrackEditor/releases

### Midi converter / web based editor
Converter by ciwolsey 
https://github.com/ciwolsey/midisaber 
and companion track editor
https://beatmapper.surge.sh/

## Do you have any tips for making a good map?

Here is an excel spreadsheet by M.Rappold that analyzises the in game tracks and offers suggestions for making your own tracks.
https://bit.ly/2lzzSxd

Awfulnaut's best practices guide.
https://bit.ly/2LjbURw

Full mapmaking guide by Freeek: 
https://www.youtube.com/playlist?list=PLYeZR6d3zDPgDgWogOwMteL-5SQWAE14b

## How do I use the editors?

Here is a tutorial playlist:
https://www.youtube.com/playlist?list=PLYeZR6d3zDPgDgWogOwMteL-5SQWAE14b

## Do I need Beat Saber installed to use the editors?

No. Edit Saber will ask for the Beat Saber directory, but it can be any folder.

## What if I want to make my own editor / converter?

Understanding the track JSON file: https://pastebin.com/cTPGrxWY

Understanding the events data: https://docs.google.com/spreadsheets/d/1vCTlDvx0ZW8NkkZBYW6ecvXaVRxDUKX7QIoah9PCp_c/htmlview

Example track file: https://pastebin.com/rkZVSmte

## My game updated and now none of my mods are working!
Each time the game updates it is possible that mods will stop working and need to be updated.
The devs realize this, so when the game updates and you run it for the first time, everything in the Plugins folder is moved into the `Incompatible Plugins` folder. **Leave those plugins in there!**

To get mods back, simply **run the mod manager again.**
The mod manager only includes mods that have been proven to be compatible with the latest version of the game!

Get the mod manager from the [beginners-guide](beginners-guide).

## Should I use wrist weights when I play?

***DO NOT USE WRIST WEIGHTS!***
You will only hurt yourself. Besides, a lightsaber wouldn't be heavy, it's made of *light.*
Please read this comment for more information https://www.reddit.com/r/Vive/comments/8g9jgs/beat_saber_has_now_released/dya1yl7/

## My game will not load!

You may have a popup on your desktop asking about your Beat Saver auth token to vote on songs at the end of the game.
If you don't care to vote on songs, simply click "Cancel" and the popup will not appear again.

## My game launches, then instantly closes!

Check your plugins folder for `BeepBoop.dll`. This was a troll plugin designed to do exactly that.
Simply delete the dll file to fix it.

## "Your audio file name is wrong" message in the Edit Saber

The 3D editor only supports .ogg files. You have to convert your file to ogg using a converter, such as audacity.
If you simply change the file extension to .ogg, it will not work.

## How do I delay a song so that it doesn't start right when the level loads?

Currently this isn't possible in Beat Saber. For now you have to edit the song in an audio editor (such as Audacity) to add silence at the beginning of the track.

## I tried to install mods via the Mod Installer but it gives me an error that it can't find the IPA.exe.

Try installing the song injector separately, then try running the mod installer again. https://github.com/xyonico/BeatSaberSongInjector/releases

