<!-- TITLE: FAQ -->
<!-- SUBTITLE: Frequently Asked Questions! -->
# FAQ
## How do I load custom songs?
Use the [Mod Manager](https://github.com/Umbranoxio/BeatSaberModInstaller/releases) by Umbranox! 
Follow the instructions in the [Beginners Guide](beginners-guide).

## Where do I find custom songs?
[Beat Saver](https://beatsaver.com/)
[Beast Saber](https://bsaber.com/)

We also have a designated channel on the Modding Group Discord: `[#finished-maps](https://discordapp.com/channels/441805394323439646/442342190060929055/)`

## How do I load other plugins?
Essential mods are included in the mod manager by Umbranoxio!
Follow the instructions in the [Beginners Guide](beginners-guide).

After you have run the Mod Manager, you can then add other plugins / mods as well.
Plugins / mods that aren't in the mod manager have to be placed manually in the following directories:

`.dll` plugins go in the following directory:
|  |  |
| --- | --- |
| Steam | `steamapps\common\Beat Saber\Plugins` |
| Oculus | `hyperbolic-magnetism-beat-saber\Plugins` |

Asset replacement plugins go in the directory:
|  |  |
| --- | --- |
| Steam | `steamapps\common\Beat Saber\Beat Saber_Data` |
| Oculus | `hyperbolic-magnetism-beat-saber\Beat Saber_Data` |

## Custom sabers?
### How do I use custom sabers?
Here is a video tutorial https://youtu.be/dUzyochSTt4
<!-- (Add link to #beginners-guide section here) -->

### How do I make custom sabers?
Making custom sabers:
* [Written Tutorial](https://bs.assistant.moe/Sabers/)
* [Video Tutorial](https://www.youtube.com/watch?v=mhMeR9CEUjk)

## Custom avatars?
### How do I use Custom Avatars?
Follow the instructions included with the plugin:
https://github.com/xyonico/CustomAvatarsPlugin/releases/latest

Use <kbd>PageUp</kbd> / <kbd>PageDown</kbd> to switch avatars in game.
Use the <kbd>Home</kbd> key on your keyboard to toggle your avatar in first person view.

### How do I make Custom Avatars?
Here is a full body avatar tutorial written by Assistant: https://bs.assistant.moe/Avatars/

## Multiplayer?
Here is a guide to setup the multiplayer plugin: https://bs.assistant.moe/Multiplayer/

## My game updated and now none of my mods are working!
Each time the game updates it is possible *(and very likely)* that mods will stop working and need to be updated.
The devs realized this, so when the game updates and you run it for the first time, everything in the `Plugins` folder is moved into the `Incompatible Plugins` folder. **Leave those plugins in there!**

To get mods back, simply **run the mod manager again.**
The mod manager only includes mods that have been proven to be compatible with the latest version of the game!

Get the mod manager from the [Beginners Guide](beginners-guide).

## Should I use wrist weights when I play?
> **DO NOT USE WRIST WEIGHTS!**
{.is-danger}

You will only hurt yourself. Besides, a lightsaber wouldn't be heavy, *it's made of light.*
Please read [this comment](https://www.reddit.com/r/Vive/comments/8g9jgs/beat_saber_has_now_released/dya1yl7/) for more information.

## My game will not load!
You may have a popup on your desktop asking about your Beat Saver auth token to vote on songs at the end of the game.
If you don't care to vote on songs, simply click **"Cancel"** and the popup will not appear again.

## My game launches, then instantly closes!
Check your plugins folder for `BeepBoop.dll`. This was a troll plugin designed to do exactly that.
Simply delete the `.dll` to fix it.

## "Your audio file name is wrong" message in the Edit Saber
The 3D Editor only supports `.ogg` files. You have to convert your file to Ogg Vorbis using a converter, such as Audacity.
If you simply change the file extension to `.ogg`, it will not work.

## How do I delay a song so that it doesn't start right when the level loads?
Currently this isn't possible in Beat Saber. For now you have to edit the song in an audio editor *(such as Audacity)* to add silence at the beginning of the track.

## I tried to install mods via the Mod Installer but it gives me an error that it can't find the IPA.exe.
Try installing the [Song Injector](https://github.com/xyonico/BeatSaberSongInjector/releases) separately, then try running the Mod Manager again.

## I want to double the BPM of my song, is there an easy way to do that?
Here is a [Python3 Script](https://cdn.discordapp.com/attachments/442372806705938434/447910905972523008/beat-saber-time-multiplier.zip) that will multiply the BPM and `_time` values in your JSON file by any given factor.