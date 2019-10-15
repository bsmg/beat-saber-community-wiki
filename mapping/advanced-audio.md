<!-- TITLE: Advanced Audio Editing -->
<!-- SUBTITLE: Diving deeper into audio editing -->

**Content in this section is derived from original guides by n3tman and LittleAsi, edited by Kolezan. Many thanks to contributors from across the mapping community who made this expanded wiki possible!**
* [Frequently Asked Questions](/mapping/faq)
* [Glossary of Terms](/mapping/glossary)

On this page you will find additional guides and resources for better understanding audio or more advanced techniques of editing audio.
# Checking Audio Quality
Generally, as a rule, always use **WAV(E) or FLAC (lossless uncompressed or compressed)** files as sources for your songs. This is because **lossy formats like MP3, AAC or OGG always lose information when converted to their formats** and cannot be restored by 'un-converting'. This is why you should never use your exported OGG-file to make new edits to your audio. Therefore, always use a lossless source file, if possible. However, some FLAC sources could be 'up-converted' from lossy formats, so using a spectral analyser tool to check your audio file(s) before using them is a recommended practice. For more information on audio formats [this article is recommended](https://opentrackers.org/whatinterviewprep.com/prepare-for-the-interview/audio-formats/index.html).
> Tip: Save your own lossless WAV(E) files when doing edits, at each step, so you always have a lossless source to continue editing from without having to redo everything from the start.

The best way to check for source quality and quality loss is using [Spek](http://spek.cc/), a free acoustic spectrum analyser tool:

![Spectrum example](https://i.imgur.com/fdOZR2K.png "Spectrum example")

This tool shows the time of the song from left to right, the frequencies from lowest at the bottom to highest at the top and the loudness of the frequencies in color (legend to the right). This screenshot shows the same song with the top graph being a WAVE file and the bottom graph being an OGG file export of the same WAVE file.

The biggest difference you will notice is the frequency cut off at the top. This is a common technique for lossy formats to save on data as these high frequencies aren’t as important for the overall sound reproduction.
However, if you look more closely at the frequencies in the audible spectrum (20hz to 20khz) you can see that the top graph looks a lot smoother with good gradients compared to the bottom graph which is more jagged and doesn’t include much of the finer gradients. Look for this when analysing sound files. For more info on spectrum analysis [this article is recommended](https://opentrackers.org/whatinterviewprep.com/prepare-for-the-interview/spectral-analysis/index.html).

To use this tool simply open Spek.exe then drag and drop the audio file into the window.
## Choosing Appropriate OGG Export Quality
You should aim at preserving most of the source audio data while still having the smallest file size. Keep OGG file size under 14MB (for BeatSaver) or 7MB (for Discord without Nitro).
To know what level is ideal for your song you can export your track with different qualities and compare the spectrals. However, as a general recommendation follow these settings:

* High quality source (WAVE, FLAC or MP3/AAC@+200kbps): choose an OGG quality level between 9 to 6.
* Low quality source (MP3 / AAC / OGG): choose an OGG quality level between 5 to 3.

You can’t increase audio quality by saving a lossy track with a higher bitrate (e.g. saving a YouTube-sourced track with level 10 quality), you will only bloat the file size. As explained in the previous chapter, information is lost when transcoding to any lossy format and thus can’t be restored. Transcoding one lossless format to another lossless format is fine though, e.g. FLAC to WAV(E).
# Song Editing using Cross-fades
When editing a shorter version of a song and a simple hard immediate cut between two similar sections of a song isn’t enough to convince your ears (usually the sections aren’t perfectly the same, usually in non-electronic music) then applying a cross-fade between the sections usually helps. Any type of restructuring editing is easier in a DAW software that uses beat grid editing, but it is possible to do the same in the free software of Audacity as well, which we will show here.

For those who don’t know, a cross-fade is when one audio track fades out while another simultaneously fades in. For best result find identical or near-identical sections on each end of the region you want to cut. Instrumental regions in electronic music better suited than regions with vocals. **Using the smallest segment possible, particularly a small section between two peaks/beats, is better to convince a listener.**

There is also a video of this process [available here](https://www.youtube.com/watch?v=oSua4ITfPy8).

**To crossfade two sections of a song do the following:**
1. Open the song in Audacity.
2. Duplicate the song track (Select menu -> All + Edit menu -> Duplicate, or simply press Ctrl+A then Ctrl+D.)
3. Roughly fill the unwanted end of the first track and unwanted start of the second track with silence (Select, then Generate menu -> Silence...).
![Cut song section](https://i.imgur.com/IRiNCz0.png "Cut song section")
4. Align the tracks by using the Time Shift Tool (![Time Shift Tool](/uploads/wiki/timeshift.png)) to move the second track to a place roughly in place so the similar sections are close to each other. Then zoom in and adjust again, then repeat till the waveform changes to dots when you zoom. Align the dots on the bottom track with the similar peaks and lows with the top track, if possible. (Tip: Utilize a Click Track to make sure the tracks are in time with each other. See * [Audio Preparation: Adding Click Track](https://bsmg.wiki/mapping/basic-audio#add-a-click-track).)
![Zoomed syncing](https://i.imgur.com/9jyrzzv.png "Zoomed syncing")
5. The last section of the top track should now be identical or similar to the first section of the bottom track but from different times in the song. Listen to the overlapping area to confirm a match, making sure there is no echo/offset from misaligned tracks.
>Tip: To avoid overdrive/clipping from two -0db peaking tracks you can set the faders for both tracks to -6db ![Fader](https://i.imgur.com/kvsHvMT.png) then later back to +0db after the crossfade has been applied. Double click the fader to type in the number.
7. Select the overlapping region across both tracks.
8. Go to `Effect menu -> Crossfade Tracks`. Set Fade direction to `Alternating Out / In`. Click OK to apply crossfade.
![Crossfade](https://i.imgur.com/amqrj1I.png "Crossfade")
9. Listen to the overlapping sections again. If all went well, you should now have a perfectly blended transition between the two tracks.
10. Combine the tracks by selecting all (`Select menu -> All` or `Ctrl+A`) then going to `Tracks menu -> Mix` then `Mix and Render`.
11. Done. You could now proceed with other [Audio Editing](/mapping/basic-audio#editing-with-audacity) or finish with [Exporting](/mapping/basic-audio#exporting).
# Variable BPM
If the song you’re trying to map has a tempo that doesn’t sync up with a fixed BPM (as in, even with BPM values with decimals), such as (older) acoustic pop, rock or metal songs, they were most likely not recorded to a metronome and will thus not easily sync up to a fixed BPM in Audacity or the map editor. No matter what the solution is it always involves brute forcing it by manually adjusting the BPM (tempo track) at intervals, sometimes every beat, to fit the song. This takes a lot of time and patience, so make sure it's worth the extra effort.

The benefit of having a synced BPM/tempo track is easier and consistent note placement and editing, as well as easier and consistent lighting editing, especially with more than one difficulty in a map.

There are several methods to go about handling variable BPM:
* Manually time the BPM changes in MedicoreMapper. [Video tutorial by BennyDaBeast here](https://www.youtube.com/watch?v=6AwR4SeaiHU).
* Use a DAW software and find all the tempo changes using a tempo track editor. Use Jumps instead of Ramps as that’s how MediocreMapper changes tempo. When you’ve found all the tempo changes input those into MediocreMapper. (Remember, DAW softwares usually display measures and beats, but MediocreMapper only displays beats.)
* Use a DAW software and time warp the sound into a fixed BPM. This, however, could introduce artifacts or warp the sound and could be more easily noticeable by listeners/players.
