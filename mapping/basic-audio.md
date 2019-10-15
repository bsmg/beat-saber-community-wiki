<!-- TITLE: Basic Audio Setup-->
<!-- SUBTITLE: Get your audio file tune up, set up, and ready for mapping -->

**Content in this section is derived from original guides by Kolezan & Nik.** Many thanks to contributors from across the mapping community who made this expanded wiki possible!
* [Frequently Asked Questions](/mapping/faq)
* [Glossary of Terms](/mapping/glossary)

This page provides both new and experienced mappers with general recommendations for setting up a new song file before starting to map. Not all sections may apply for your song, so review the table of contents to the left and skip any sections you deem them unnecessary.
# Song Selection for New Mappers
These recommendations are **not** requirements but will help to ease you into mapping. If you want to map “In A Gadda Da Vida” for your first map then have at it but know that you’ll face a **lot** of additional challenges.

* Choose a song that has a clear beat to map to. Some genres work better than others.
* Choose a song with a consistent tempo (for example songs with electronic drums). Songs that have tempo/BPM changes over time can be very complicated to map.
* Choose a song on the shorter side (less than 3 minutes is better). Mapping a 10-minute epic to start with may lead to frustration and/or burn out.
* Finally, choose a song that you don’t mind listening to over and over and over and over again. But avoid mapping your favorite song as your first few maps, save that for when you’re more experienced.
# Audio Quality
Before you begin mapping, ensure you have a high quality source file for your song. Many maps have terrible audio files, often from YouTube rips or low bitrate files. Follow these general guidelines as you work on your maps:

* Use the highest quality source you can find such as WAV(E) or FLAC files (lossless format). A close second are high bitrate (+200kbps) MP3 or AAC files (lossy formats). Often an artist’s [Bandcamp](https://bandcamp.com/), [SoundCloud](https://soundcloud.com) (if they offer downloads) or other sites where you can buy the tracks/album will have the highest quality source.
* Use a YouTube rip **only** as a last resort. The bitrate is low and the volume is seldom right. In this case some audio editing might be required (see [Editing with Audacity](#)).

See the [Advanced Audio Editing](/mapping/advanced-audio) page for more in-depth techniques and tools for analysing the high quality audio.
# Finding the BPM
There are three ways to find the BPM for the song which you want to map. Try them in order (easiest to hardest) if the you don't get any results:
## Online Search
You can search online using a search engine site (e.g. [Google](http://google.com) in your web browser for `[song name] + [artist] + “bpm”` and often find a number of sites (e.g. [SongBPM.com](https://songbpm.com/) with this information.
## Tool-Assisted BPM Calculation
**Arrow Vortex** is a free tool to analyze a song’s BPM automatically. It will also find the offset needed to line the audio up to the beat in Audacity or your map editor. Ryger’s [Arrow Vortex BPM Analysis Tutorial](https://youtu.be/Z49UKFefu5c) includes both BPM detection and confirmation.
## Manual BPM Calculation
If both methods above fail you will have to manually find the BPM, but this is easier than you might think.
1. Use an online BPM tapping calculator (like the [Tap for BPM Tool](https://www.all8.com/tools/bpm.htm), open the page in your web browser).
2. Play the song in your favorite music player.
3. With the webpage in focus, tap any key to the beat (every quarter note) for about 30 seconds and the tool will display the BPM of the song.
4. Take note of the nearest whole value.
# Audio Preparation
To make it easier to map and make sure that the song is synced perfectly you need to set up your audio file correctly. This page will assume you are using [Audacity](https://www.audacityteam.org/)
## Add a Click Track
1. Open the song you want to map into Audacity.
2. Add a new mono track from `Tracks menu > Add New > Mono Track`
3. Place the cursor at the start of the new track (Click on the track and press your Home key) and then click `Generate menu > Rhythm Track…`
4. Input the nearest whole BPM you got earlier into the Tempo field and enter the duration of the song in the optional rhythm track duration field (the duration is displayed at the top right of the timeline).
5. Copy the other recommended settings below:
![Audacity Rhythm Track Menu](https://i.imgur.com/jC6OU0i.png)
If everything was correctly input you will have something like this:
![Audacity main screen showing song track and rhythm track](https://i.imgur.com/R55YOXZ.png)
This click track is completely in sync with the beats in the map editor later when you input the same BPM in the map editor.
## Plan Your First Note
Think about the intro of your song. Depending on where in the song you want to place your first block, you'll need to avoid both a *hot start* (not enough time before the first block) and a too-long intro. Your song will fit into one of three categories:
1. **Songs with no intro:** It is critical to leave at **minimum two seconds** of preparation time for the player before the first playable note(s) in your map, otherwise this is known as a “Hot Start.”
2. **Songs with a short intro:** If your song has a short intro that is **less than eight seconds** it is OK for the music to start playing immediately.
3. **Songs with a long intro:** If the song has a very long and uneventful/fade-in intro for **more than ten seconds** it is strongly recommended to place the first notes within eight seconds from map start.

In all cases above you will need to time shift the song to an appropriate time based on your needs:
1. **No intro:** Move the song back in time, placing the first mapped note(s) after two seconds. Then sync the song to the beat (See Sync the Song to the Beat). Later fill the gap with silence (See Adding Silence).
2. **Short Intro:** Sync the song to the beat (See Sync the Song to the Beat) and then fill the gap with silence (See Adding Silence) or trim the audio before 0 seconds depending on which case applies (See Trimming the Intro).
3. **Long intro:** Move the song forward in time, placing the first note(s) within 8 seconds (See Sync the Song to the Beat), then trim the audio before 0 seconds (See Trimming the Intro).

## Sync the Song to the Beat
1. Select the Time Shift Tool (![Time Shift Tool](/uploads/wiki/timeshift.png)).
2. Left click on the song track and hold, then drag the audio so that the first planned mapped note(s) in your song ends up within the appropriate seconds (see timeline above the track) to avoid a “Hot Start” or too long intro (See Planning the First Notes if you haven’t already).
3. Release to place the audio in the new position.
4. Play back the audio in this position. The song will be out of sync, so find the closest beat in the click track and align your song to the beat (click track) by moving it backward or forwards in time by small increments. Zoom in for better accuracy. Repeat until it sounds spot on.
5. When you think you’ve found the beats of the song to match the Click Track review the whole song to ensure that the BPM you have is the correct one and that the song is in the same fixed BPM throughout the whole song. If not, you might have gotten the wrong BPM, in which case try to tap out the BPM again manually, see “Manual BPM Calculation”. 
> If BPM is correct for parts of the song but suddenly change then you most likely have a song with Variable BPM, see [Advanced Audio Editing Variable BPM](/mapping/advanced-audio#variable-bpm) for more info.
{.is-warning}

Below shows how it looks like when the first planned mapped note(s) (cursor position) are placed after 2 seconds and the beats of the song is synced to the BPM/Click Track.
![Audacity song lined up with rhythm track](https://i.imgur.com/Znpy0PZ.png)
After time shifting the song you will need to add silence, see below on how to do that.
# Editing with Audacity
After syncing the song to the beat manually or by using Vortex Arrow you will have to add silence to the intro of the song. You may also need to do other edits if they’re necessary. More on that below.

## Add Silence
If the waveform/audio clip has a gap to the timeline start (0,0 seconds) you will need to add silence, or else Audacity will export from the start of the audio clip. Do the following to add silence:
1. Switch to the Selection Tool (![Selection Tool](/uploads/wiki/selection.png)) and select the empty space between the audio clip and the start of the track (Yellow vertical lines will indicate the start and end edges when you make a selection).
2. Click Generate menu – > Silence…
3. The right amount of silence should already be input automagically so just hit OK. (After generating the silence you can click the dark line in the song track to get rid of the cut.)
4. Done.
![Adding silence with Audacity](https://i.imgur.com/6lZv03x.png)

## Trim the Intro
If your track has arrows pointing to the left at the start it means you’ve time shifted the audio forward in time outside the timeline. If you’ve done this to shorten the intro, although not necessary, it is beneficial to trim the sound clip and add a fade in. To trim and add a fade in to the song (optional) do the following:
1. Drag a selection from 0.0 seconds to the end of the audio track (yellow vertical lines).
2. Click Trim audio outside selection (![Trim audio to selection](https://i.imgur.com/0qOEXjQ.png)). The arrows should now disappear. 
3. (Optional) Make a selection from track start (vertical yellow line) to about 1-2 seconds (depending on into).
4. (Optional) Go to `Effect menu -> Fade In`.
5. Done.

Before (left) and after (right):
![Trimming the song intro](https://i.imgur.com/AbKyyl4.png)

## Check Song Volume
To ensure that your song isn’t too soft, or even too loud for that matter, we can measure it using RMS (Root Mean Squared) in Audacity. To have a good balance between note slice sounds and your song the RMS value should be **louder than -11db** (in the verses and/or choruses) or **softer than -8.5db** (at the loudest parts).

To check the RMS value in your song do the following:
1. Open Contrast Analyzer in `Analyze menu -> Contrast…`
2. With the Contrast Analysis window still open, select a part of the chorus section (about 15-20 seconds) of your song
3. Click any of the Measure selection buttons. (We only need to use one.)
4. In the Volume output field you will now find a value. Compare this value to the recommended values above.
5. If this value is smaller (more negative) than the recommended values, see “Volume Modification, Making it Louder”.
6. If this value is bigger than (less negative) than the recommended values see “Volume Modification, Making it Softer”.
![Analyzing song volume with Audacity](https://i.imgur.com/EmfULcw.png)
## Volume Modification
Before you continue with the next steps with the song editing it highly recommended to save your current progress as a WAVE file as a backup. This is to ensure that you if you need to go back and redo some of the editing you will have a high quality source to use. (Don’t load the OGG you exported as it will have lost a lot of the source quality.) Remove the Click Track if you haven’t already done so, then go to `File menu -> Export -> Export as WAV`, then save the file to a location of your choice.
> Doing any kind of audio editing on a song will inevitably change its sound, however, it's an imporant step to give your players the best map and song experience.
{.is-info}

### Making Your Song Louder
If your song’s chorus has a lower RMS value than the recommended **-11db** then you will need to do Compression and/or Limiting to bring the volume up. (Note: Amplify/Gain is not used for this, as anything above 0db will create an unpleasant distortion.)

To check if you need to apply Compressor before Limiter visually analyse the waveform. If there are a lot of sharp peaks with a pretty constant body throughout the song, as shown in the example below, then you will not need to apply compressor. Only a Limiter will suffice (skip to Limiter).
![Viewing a song that is too quiet](https://i.imgur.com/mcuODfJ.png)
However, if the waveform varies a lot between soft and loud parts then compression will most likely be needed first.
### Compression
1. Select the whole song track (Double click on the track)
2. Go to Effects menu -> Compressor
3. As a starting point, copy the settings below and click OK. Make sure that Compress based on Peaks is checked.
![Understanding compression](https://i.imgur.com/avQlouA.png)
Here’s a before (top) and after (bottom) Compressor comparison:
![Before and after compression](https://i.imgur.com/M6A60eV.png)

#### Limiter
The compressor reduces many of the unnecessary peaks and makes the more important sounds louder. However, we still haven’t reached the right RMS volume for the song. To achieve this we will remove more of the headroom using the Limiter effect:
1. Select the whole song (Double click the song track)
2. Go to `Effects menu -> Limiter…`
3. As a starting point, copy the settings below:
![Limiter in Audacity](https://i.imgur.com/6fAwHCv.png)
4. Click OK to apply Limiter.

To know if you’ve reached the right volume after compressing and limiting check again with the RMS volume tool:
1. Open Contrast Analyzer in `Analyze menu -> Contrast…`
2. With the Contrast Analysis window still open, select a part of the chorus section (about 15-20 seconds) of your song.
3. Click any of the Measure selection buttons. (We only need to use one.)
4. In the Volume output field you will now find a value. This value should be between -8.5db and -9.5db for optimal level. If not, undo the limiter process and increment the Input Gain by +/-0.5db and try again.

After limiting you will have something like this:
![Song after limiting](https://i.imgur.com/TRkvzTc.png)
You can now skip to “Outro/Trimming the End”.
### Making Your Song Softer
Some modern electronic music producers have a tendency to make their songs really loud (killing any dynamic range in the process) just to have a louder track. In the rare cases you have this kind of song (**RMS value above -8.5db**) it is **strongly recommended** to lower the volume of the song to make all Beat Saber songs normalized. This helps with hearing the note slice sounds better and to give the players a much more pleasant experience switching between songs.

Before you lower the volume you want to know approximately how much you need to lower the volume with. Do this by checking with the RMS volume tool:
1. Open Contrast Analyzer in `Analyze menu -> Contrast…`
2. With the Contrast Analysis window still open, select a part of the chorus section (about 15-20 seconds) of your song.
3. Click any of the Measure selection buttons. (We only need to use one.)
4. In the Volume output field you will now find a value. Calculate the difference between your value and -8.5db and remember this value.
5. Close the Contrast Analysis window.

Now let’s use the Amplify effect to lower the volume:
1. Select the whole song (Double click the song track)
2. Go to `Effects menu -> Amplify...`
3. Enter the difference value you calculated earlier (it should be negative) into the Amplification field:
![Amplification menu](https://i.imgur.com/OoyhGek.png)
New Peak Amplification field will repeat what the first input field says, this is normal for a song that is already peaking at 0db.
4. Click OK to apply a negative Amplify effect.
5. Done.

To know if you’ve reached the right volume check again with the RMS volume tool:
1. Open Contrast Analyzer in `Analyze menu -> Contrast…`
2. With the Contrast Analysis window still open, select a part of the chorus section (about 15-20 seconds) of your song.
3. Click any of the Measure selection buttons. (We only need to use one.)
4. In the Volume output field you will now find a value. This value should be between -8.5db and -9.5db for optimal level. If not, undo the Amplify process and increment the Input value by +/- 0.5db and try again.

After the negative value Amplify effect your song will look something like this:
![Amplification effect](https://i.imgur.com/EIu7AFi.png)
### Trimming the Outro
In Beat Saber the map will continue for as long as the audio file lasts. E.g. this means that having silence for five seconds after the song has ended the map will still play for five seconds before terminating and bringing the player to the score view. This is why it’s important to mind the time from the last note to when the audio track ends.

Go to the end of your song and play the last part and outro. From the point where you intend to have the last note(s) count to 3 or 4 seconds and pause the playback. Where your playback cursor is now located is where you should generally cut off your song. (Naturally all songs will differ, so do what makes most sense for your song.)

To trim the ending at this point do the following:
1. From the paused playback position drag a selection from here to the end of the track (yellow vertical line) and press the Delete key to remove this part.
2. Make a new selection from the end of the song track (yellow vertical line) and backwards about 2 to 3 seconds.
3. Go to `Effects menu -> Studio Fade Out`
4. Done.

The song will now fade out just before it gets to the end of the map and the player will be presented with the scoring results much faster.
# Exporting
We now have our finished audio that you will use and hear in the editor and the game. It is recommended to make another WAVE file backup just in case you need to export to OGG again in a lower quality. (`File menu -> Export as WAV`).

To generate a compatible sound file to use we need to do the following:
1. Delete the Click Track (if you haven’t already done so).
2. Click the `File menu -> Export -> Export as OGG.`
3. Name your file `song.ogg`.
4. Choose an appropriate OGG quality ([more info here](/advanced-audio#choosing-appropriate-ogg-export-quality)):
* a. High quality source (WAVE / FLAC / MP3 / AAC) use 6-9 (unless there is a file size issue.)
* b. Low quality source (YouTube or such): use 3-5; 
5. Click Save.

The song/audio file is now ready to be used in any map editor. Input the BPM you got earlier in your map editor of choice and make sure to use 0ms offset for all difficulties (since the song is already synced to the beat).
>Audio file should not be larger than ~14 MB due to the BeatSaver 15 MB ZIP file limit. If this is the case export at a lower quality until the file meets the file size limit. ZIP files over 8 MB cannot be shared directly on Discord (without Nitro) for playtesting.{.is-info}