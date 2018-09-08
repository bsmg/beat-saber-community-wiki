<!-- TITLE: Mapping -->
<!-- SUBTITLE: Too many anime maps? Not enough anime maps? Ready to take matters into your own hands? You've come to the right place. -->


# Tutorials and References
* [BennyDaBeast's Mapping Tutorials](https://bsaber.com/benny-custom-mapping/)
* [Freeek's Mapping and Editor Tutorials](https://www.youtube.com/playlist?list=PLYeZR6d3zDPgDgWogOwMteL-5SQWAE14b)
* [Awfulnaut's Best Practices Guide](https://bit.ly/2LjbURw)
* [M.Rappold's OST analysis](https://bit.ly/2lzzSxd)
# Editors and Tools

**The official editor has not been released.**
All custom maps are being made using the community built map editors.
There are currently 3 editors. All export the same files, but offer different workflows.
## Edit Saber
A robust 3D track editor made in Unreal Engine by ikeiwa!
*Most people use this editor.*
https://github.com/Ikeiwa/EditSaber/releases

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

# Frequently Asked Questions
## Do I need Beat Saber installed to use the editors?
No. Edit Saber will ask for the Beat Saber directory, but it can be any folder.

## What if I want to make my own editor / converter?
Understanding the track JSON file: https://pastebin.com/cTPGrxWY
Understanding the events data: https://docs.google.com/spreadsheets/d/1vCTlDvx0ZW8NkkZBYW6ecvXaVRxDUKX7QIoah9PCp_c/htmlview
Example track file: https://pastebin.com/rkZVSmte

## Where are custom maps saved?
Custom maps are saved to the `CustomSongs` folder in your Beat Saber install folder.
**Where is Beat Saber installed?** See [install folder.](faq/install-folder)

## "Your audio file name is wrong" message in the Edit Saber
The 3D Editor only supports `.ogg` files. You have to convert your file to Ogg Vorbis using a converter, such as Audacity.
If you simply change the file extension to `.ogg`, it will not work.

## How do I delay a song so that it doesn't start right when the level loads?
Currently this isn't possible in Beat Saber or the editors. For now you have to edit the song in an audio editor *(such as Audacity)* to add silence at the beginning of the track.

## I'm having issues uploading the map to BeatSaver, it says the format is invalid but everything looks right.
If you have Windows file extensions turned off, then you might have unknowingly saved your files with names like `cover.jpg.jpg`.  To turn off file extensions in Windows, see the following image:

![File Extensions](/uploads/images/file-extensions.png "File Extensions")