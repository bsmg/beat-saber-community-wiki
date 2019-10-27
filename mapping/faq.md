<!-- TITLE: Mapping FAQ -->
<!-- SUBTITLE: Frequently asked questions about all things mapping, grouped by topic -->
**Many thanks to contributors from across the mapping community who have made this expanded wiki possible!**
* [Mapping Term Glossary](/mapping/glossary)

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
Small offsets within a second (1000ms) can be made in some editors (e.g. MediocreMapper), but recommended practice is to insert the correct amount of silence to the audio file. For instructions using Audacity to accomplish this read [Basic Audio Setup](/mapping/basic-audio).
## My song's volume is too soft/too loud. Can I change this?
Yes, it is possible to both make it louder (to a certain degree) or make it softer. For instructions see [Basic Audio Setup](/mapping/basic-audio). While there are mods that can change the music or note slash volume not many players use this, which is why it's better to set the right volume for you song in the audio file.
# Mediocre Mapper FAQ
## "Your audio file name is wrong" message in the editor
The 3D Editor only supports `.ogg` files. You have to convert your file to Ogg Vorbis using a converter, such as [Audacity](https://www.audacityteam.org/).
If you simply change the file extension to `.ogg` it will not work.

# BeatSaver & Publishing FAQ
## Invalid Beatmap: Error in Info.dat
![Error in info.dat error](https://cdn.discordapp.com/attachments/443569023951568906/638148374092316685/unknown.png)
This error is caused by having a map that doesn't follow the latest BeatSaver data schema (a known issue of the Mk5 of Mediocre Mapper). You will need to edit your info.dat and difficulty files to address. See the [BeatSaver section](/mapping#beat-saver-data-schema-change-october-27-2019) of the main mapping wiki page.
## I'm having issues uploading the map to BeatSaver, it says the format is invalid but everything looks right.
If you have Windows file extensions turned off then you might have unknowingly saved your files with names as `cover.jpg.jpg`.  To turn on file extensions in Windows do the following:
![File Extensions](https://i.imgur.com/xYTTkVN.png "File Extensions")