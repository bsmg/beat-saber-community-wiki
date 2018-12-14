<!-- TITLE: Mapping -->
<!-- SUBTITLE: Too many anime maps? Not enough anime maps? Ready to take matters into your own hands? You've come to the right place. -->

# Tutorials and References
* [BennyDaBeast's Mapping Tutorials](https://bsaber.com/benny-custom-mapping/)
* [Freeek's Mapping and Editor Tutorials](https://www.youtube.com/playlist?list=PLYeZR6d3zDPgDgWogOwMteL-5SQWAE14b)
* [Awfulnaut's Best Practices Guide](https://bit.ly/2LjbURw)
* [M.Rappold's OST Analysis Spreadsheet](https://bit.ly/2lzzSxd)
* [Kolezan's Song/Audio Editing Guide](https://bsaber.com/custom-mapping-song-audio-editing/)
* [Publishing Songs](https://beatsaver.com)

> Please do not upload WIPs to beatsaver! It's hard to tell which maps aren't finished in game, and anyone who plays your WIP without practice mode enabled will create a new leaderboard for that map. Uploading to beatsaver should be akin to putting it on store shelves - that is, it's your final product. To share for playtesting, we encourage you to use google drive, dropbox, uploading to discord, etc. 
{.is-warning}

# Editors

**The official editor has not been released.**
All custom maps are being made using the community built map editors.
There are currently 3 editors. All export the same files, but offer different workflows.

## Edit Saber
A robust 3D track editor made in Unreal Engine by Ikeiwa!
*Most people use a version of this editor.*

There are several forks of Edit Saber, listed below.

### Mediocre Mapper
A fork of Edit Saber Enhanced made by squeaksies.
This version adds even more features to Edit Saber Enhanced. 
https://github.com/squeaksies/MediocreMapper/releases/latest

### Edit Saber Enhanced
A fork of Ikeiwa's Edit Saber 6v2 with a ton of additional features.
A collaboration between permissionBRICK and squeaksies.
https://github.com/permissionBRICK/EditSaberEnhanced/releases/latest

### Original
The original Edit Saber
https://github.com/Ikeiwa/EditSaber/releases/latest

## Midi converter / web based editor
Midi converter made by ciwolsey!
This editor relies on midi data to outline a beatmap, then that track can be edited in the companion web editor.
https://github.com/ciwolsey/midisaber 
and companion track editor!
https://beatmapper.surge.sh/

## Unofficial 2D Track Editor
A 2D track editor made in Processing by Megalon!
**Note: This is depreciated and there is very little support for this program, if any!**
https://github.com/megalon/BeatSaber-UnofficialTrackEditor/releases

# Other Resources
## Lightmap
A tool to automatically generate lighting events for a custom song by Freeek and Recrudesce!
Get it here: https://github.com/recrudesce/lightmap/releases
Explanation video and examples: https://www.youtube.com/watch?v=ImO9cFW5vyQ&t

## THE OSU! EDITOR
You can use the osu! editor to help you with timing when creating your map. Here is a video tutorial by Fayhe 
https://www.youtube.com/watch?v=nIX0koHzW8c&t

## BPM Saber
Elliotttate's tool for finding the BPM of a song
https://bsaber.com/bpmsaber/

## BPM Changer
A [tool](https://github.com/zevdg/bpm-saber) for changing the BPM of a beatsaber track without changing the position of the boxes and walls relative to the music.

# Legacy Tools
These tools have been deprecated by MediocreMapper, but you might find these helpful if you are using older tools.

## VARIABLE BPM
Currently variable BPM isn't supported by the game, but you can fake it by offsetting notes to fit the grid. TehSuperToilet made a guide on how to do this. [It is included in this zip file.](https://cdn.discordapp.com/attachments/443569023951568906/459771392054001664/bpm_changer.zip)

## Copy-Paste Lighting Guide
Normally, lighting events cannot be copy pasted but this [tutorial](https://bsaber.com/copy-and-paste-lighting-events-in-editsaber/) should make things easier.

# "Mappers" role on the Beat Saber Modding Group Discord
If you'd like to apply for the Mappers role on the Beat Saber Modding Group Discord, use the following google form.
https://goo.gl/forms/KM71UKjQpbCesWNg2

# Frequently Asked Questions
## Do I need Beat Saber installed to use the editors?
No. The editor will ask for the Beat Saber directory, but it can be any folder.

## What if I want to make my own editor / converter?
Understanding the track JSON file: https://pastebin.com/cTPGrxWY
Understanding the events data: https://docs.google.com/spreadsheets/d/1vCTlDvx0ZW8NkkZBYW6ecvXaVRxDUKX7QIoah9PCp_c/htmlview
Example track file: https://pastebin.com/rkZVSmte

## Where are custom maps saved?
Custom maps are saved to the `CustomSongs` folder in your Beat Saber install folder.
**Where is Beat Saber installed?** See [install folder.](faq/install-folder)

## "Your audio file name is wrong" message in the Edit Saber
The 3D Editor only supports `.ogg` files. You have to convert your file to Ogg Vorbis using a converter, such as [Audacity](https://www.audacityteam.org/).
If you simply change the file extension to `.ogg`, it will not work.

## How do I delay a song so that it doesn't start right when the level loads?
Currently this isn't possible in Beat Saber or the editors. For now you have to edit the song in an audio editor *(such as Audacity)* to add silence at the beginning of the track.
Check out [Kolezan's Song/Audio Editing Guide](https://bsaber.com/custom-mapping-song-audio-editing/) for instructions.

## I'm having issues uploading the map to BeatSaver, it says the format is invalid but everything looks right.
If you have Windows file extensions turned off, then you might have unknowingly saved your files with names like `cover.jpg.jpg`.  To turn off file extensions in Windows, see the following image:
![File Extensions](/uploads/images/file-extensions.png "File Extensions")

## I want to double the BPM of my song, is there an easy way to do that?
Here is a [Python3 Script](https://cdn.discordapp.com/attachments/442372806705938434/447910905972523008/beat-saber-time-multiplier.zip) that will multiply the BPM and `_time` values in your JSON file by any given factor.