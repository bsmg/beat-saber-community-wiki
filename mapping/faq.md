<!-- TITLE: Mapping FAQ -->
<!-- SUBTITLE: Frequently asked questions about all things mapping, grouped by topic -->

>The Mapping FAQ is getting a big upgrade soon and has moved to a child page within mapping. Thanks for your patience while we improve this space!
{.is-info}
# General Mapping FAQ
## Do I need Beat Saber installed to use the editors?
Offical editor, yes. Community editors, no. The method for setting up your editor to use an alternate folder varies by which editor you choose.

## What if I want to make my own editor / converter?
Take a look at the SongCore documentation on [Kyle 1413's GitHub](https://github.com/Kylemc1413/SongCore)

## Where are custom maps saved?
Custom maps are read from the `Beat Saber/Beat Saber_Data/CustomLevels` folder in your Beat Saber install folder. If your song isn't complete, place it in `CustomWIPLevels` to prevent custom leaderboards from being made for it.
**Where is Beat Saber installed?** See [install folder](faq/install-folder)

## I want to double the BPM of my song, is there an easy way to do that?
Here is a [Python3 Script](https://cdn.discordapp.com/attachments/442372806705938434/447910905972523008/beat-saber-time-multiplier.zip) that will multiply the BPM and `_time` values in your JSON file by any given factor.

# Audio FAQ
## How do I delay a song so that it doesn't start right when the level loads?
Currently this isn't possible in Beat Saber or the editors. For now you have to edit the song in an audio editor *(such as Audacity)* to add silence at the beginning of the track.
Check out [Kolezan's Song/Audio Editing Guide](https://bsaber.com/custom-mapping-song-audio-editing/) for instructions.
# Mediocre Mapper FAQ
## "Your audio file name is wrong" message in the editor
The 3D Editor only supports `.ogg` files. You have to convert your file to Ogg Vorbis using a converter, such as [Audacity](https://www.audacityteam.org/).
If you simply change the file extension to `.ogg`, it will not work.

# BeatSaver & Publishing FAQ
## I'm having issues uploading the map to BeatSaver, it says the format is invalid but everything looks right.
If you have Windows file extensions turned off, then you might have unknowingly saved your files with names like `cover.jpg.jpg`.  To turn off file extensions in Windows, see the following image:
![File Extensions](/uploads/images/file-extensions.png "File Extensions")