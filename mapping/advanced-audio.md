<!-- TITLE: Advanced Audio Editing -->
<!-- SUBTITLE: Advanced Audio Editing -->

**Content in this section is derived from original guides by n3tman and LittleAsi, edited by Kolezan. Many thanks to contributors from across the mapping community who made this expanded wiki possible!**
* [Frequently Asked Questions](/mapping/faq)
* [Glossary of Terms](/mapping/glossary)

On this page you will find additional guides and resources for better understanding audio or more advanced techniques of editing audio.
# Checking Audio Quality
Generally, as a rule, always use **WAV(E) or FLAC (lossless uncompressed or compressed)** files as sources for your songs. This is because **lossy formats like MP3, AAC or OGG always lose information when converted to their formats** and cannot be restored by 'un-converting'. This is why you should never use your exported OGG-file to make new edits to your audio. Therefore, always use a lossless source file, if possible. However, some FLAC sources could be “up-converted” from lossy formats, so using a spectral analyser tool to check your audio file(s) before using them is a recommended practice.
Tip: Save your own lossless WAV(E) files when doing edits, at each step, so you always have a lossless source to continue editing from when you need to do edits.
For more info on audio formats * [this article is recommended](https://opentrackers.org/whatinterviewprep.com/prepare-for-the-interview/audio-formats/index.html).

The best way to check this quality loss is using * [Spek](http://spek.cc/), a free acoustic spectrum analyser tool:

![Spectrum example](https://i.imgur.com/fdOZR2K.png "Spectrum example")

This tool shows the time of the song from left to right, the frequencies from lowest at the bottom to highest at the top and the loudness of the frequencies in color (legend to the right). This screenshot shows the same song with the top graph being a WAVE file and the bottom graph being an OGG file export of the same WAVE file.

The biggest difference you will notice is the frequency cut off at the top. This is a common technique for lossy formats to save on data as these high frequencies aren’t as important for the overall sound reproduction.
However, if you look more closely at the frequencies in the audible spectrum (20hz to 20khz) you can see that the top graph looks a lot smoother with good gradients compared to the bottom graph which is more jagged and doesn’t include much of the finer gradients. Look for this when analysing sound files. For more info on spectrum analysis * [this article is recommended](https://opentrackers.org/whatinterviewprep.com/prepare-for-the-interview/spectral-analysis/index.html).

To use this tool simply open Spek.exe then drag and drop the audio file into the window.
## Choosing Appropriate OGG Export Quality
You should aim at preserving most of the source audio data while still having the smallest file size. Keep OGG file size under 14MB (for BeatSaver) or 7MB (for Discord without Nitro).
To know what level is ideal for your song you can export your track with different qualities and compare the spectrals. However, as a general recommendation follow these settings:

* High quality source (WAVE, FLAC or MP3/AAC@+200kbps): choose an OGG quality level between 9 to 6.
* Low quality source (MP3 / AAC / OGG): choose an OGG quality level between 5 to 3.

You can’t increase audio quality by saving a lossy track with a higher bitrate (e.g. saving a YouTube-sourced track with level 10 quality), you will only bloat the file size. As explained in the previous chapter, information is lost when transcoding to any lossy format and thus can’t be restored. Transcoding one lossless format to another lossless format is fine though, e.g. FLAC to WAV(E).

# Song Editing using Cross-fades
When editing a shorter version of a song and a simple hard immediate cut between two similar sections of a song isn’t enough to convince your ears (usually the sections aren’t perfectly the same, usually in non-electronic music) then applying a cross-fade between the sections usually helps. Any type of restructuring editing is easier in a DAW software that uses beat grid editing, but it is possible to do the same in the free software of Audacity as well, which we will show here.

For those who don’t know, a cross-fade is when one audio track fades out while another simultaneously fades in. For best result find identical or near-identical sections on each end of the region you want to cut. Instrumental regions in electronic music better suited than regions with vocals. **Using the smallest segment possible, particularly a small section between two peaks/beats, is better to convince a listener's ears.**

There is also a video of this process * [available here](https://www.youtube.com/watch?v=oSua4ITfPy8).

**To crossfade two sections of a song do the following:**
1. Open the song in Audacity.
2. Duplicate the song track (Select menu -> All + Edit menu -> Duplicate, or simply press Ctrl+A then Ctrl+D.)
3. Roughly fill the unwanted end of the first track and unwanted start of the second track with silence (Select, then Generate menu -> Silence...).


