<!-- TITLE: Mediocre Mapper User Guide -->
<!-- SUBTITLE: Essential information to get up and running using Mediocre Mapper Mk5 -->

> Mediocre Mapper (MM) is no longer in development or supported by its creator. Mk5 (released on 9/24/19) is the final public release.
{.is-warning}
# Editor Setup
## Installation
1. Download MediocreMapper.zip from [GitHub](https://github.com/squeaksies/MediocreMapper/releases/latest) 
> Do not download Mediocre Mapper Server (mediocremapperserver.zip). This is a separate tool for mapping collaboration that is not covered on this page.
{.is-warning}
2. Unzip the file and place the extracted folder wherever you like on your hard drive.
3. Double click `mediocremapper.exe` to run.
## First Time Setup
The first time you run MM you will need to direct it to the location of two folders: `CustomLevels` and `CustomWIPLevels`. You have several options available to you:

**If you have VR and Beat Saber:**
* Give MM the path to the two appropriate folders
* Steam Example: `C:\Program Files (x86)\Steam\steamapps\common\Beat Saber\Beat Saber_Data\CustomLevels`
* Oculus Example: `C:\Program Files\Oculus\Software\Software\hyperbolic-magnetism-beat-saber\Beat Saber_Data\CustomWIPLevels`

**If you do not have VR or Beat Saber OR have VR but don’t have Beat Saber:**
* Make two folders called `CustomLevels` and `CustomWIPLevels`
* Example: `C:\Users\Helen\Documents\CustomWIPLevels`

All of your working map files will go into a song name folder within this CustomWIPLevels folder.

## Editor Settings
These core settings are all available from the MM home page when you first open the program. 
### Map Selection
The map selection pane has four tabs, each with songs listed alphabetically.
* **WIP Songs:** This tab contains all of the map folders saved in your `CustomWIPLevels` folder. New maps are created here and are accessible in-game under "Custom WIP Levels."
* **Custom Songs:** This tab contains all the downloaded custom songs saved in your `CustomLevels` folder. Maps are accessible in-game under "Custom Levels."
* **Multi-Mapper:** This tab contains any maps being collboratively worked on via the *Mediocre Mapper Server.*
* **Temp Loader:** This tab allows you to temporarily "quick preview" zip files online (i.e., from #testplays, BeatSaver, or BeastSaber) without downloading and extracting them.

There are several functions available to you on this screen:
* The <kbd>Refresh Song List</kbd> button refreshes the songs listed.
* The <kbd>Edit</kbd> button next to a map opens it in MM. 
* The <kbd>Delete</kbd> button next to a map perma-deletes it. **Note:** Once deleted this way maps are gone forever and unrecoverable.
* The <kbd>Star</kbd> button next to a map favorites it, bumping it to the top of the list.
### Map Creation
Below the map selection pane you can create a new empty song folder in `CustomWIPLevels` by entering the desired name of your folder (typically Song Name or Artist - Song Name) then clicking <kbd>Create Level</kbd>.
### Settings
The settings pane includes global settings for autosaving, zip packaging, folder paths, and more.
* **Autosave Settings:** Autosave is enabled by default at an interval of 300 seconds (5 minutes). This is generally fine for most users unless you are doing a light-heavy map. Autosave while playing the song in the editor is also enabled by default.
* **Mapping & Lighting Settings:** 
   - No lighting is off by default, meaning that any lighting events placed on the lighting track will play. Check to prevent lights from playing while mapping.
   - You have the option to provide MM with an alternate folder to save your packaged songs. By default the packaged song will be found in the same folder where the uncompressed map lives.
* **Beta Settings:** If you have the Mapping Extensions mod installed you will have additional checkboxes enabled for "extended" mapping features like precision placement, precision rotation, and six-lane. New mappers are encouraged to skip this until they're more comfortable with the basics.
* **Legacy Settings:** If you have the ChromaToggle mod installed you can check this box to enable the game modes but it has been unsupported for some time.
* **Other Settings:** Click the <kbd>Clear Settings</kbd> button to revert to default settings. You may also enter new paths for either of your song folders. If for some reason nothing works you can click the <kbd>Everything Inexplicably Broken?</kbd> button to delete your MM config file.
# Song Setup
> This is a stub section in progress. DM helencarnate#2079 if you'd like to contribute.
{.is-info}
Once you've finished one-time editor setup you're ready to create your first map.
## Song Creation
There are four files (minimum) you need to create a map:
**Mapper-Provided**
* Your song file in .ogg format (review setup instructions).
* Your cover file in .jpg or .png. 
**Editor-Created**
* Info.dat file which contains all of the core data for your map as a whole. Created the first time you open the map.
* [difficulty].dat file which contains all of the data specific to each difficulty.

You have two options to create your song folder:
1. Enter your desired folder name in the 'Create New Level' pane and click <kbd>Create Level</kbd>. Your new folder will automatically appear in your map list.
2. Navigate to your `CustomWIPLevels` folder and make a folder with your desired folder name. You will need to click <kbd>Refresh Song List</kbd> to see your folder.

Click <kbd>Edit</kbd> to enter your song information and metadata.
## Song Info Settings
The `Song Info` page is the first screen you see every time you edit a map.
### Whole Map Settings
On the left side of the `Song Info` page is information that applies to your whole map. See [Beat Saber Metadata Criteria](https://docs.google.com/document/d/1ehotupIYMVlc8x41JldO-24m7Am-oTVYnciF9KCRdNM/edit) for standards on presenting complex song names and multiple artists.
* **Song Name:** The primary name of the song
* **Song SubName:** Any following tags like (Short Ver.), (SDVX Mix), etc.
* **Song Artist:** The person or group who authored the song
* **Mapper:** This is YOU! It's recommended you list your name the same as your BeatSaver user name
* **BPM:** The tempo of the song. It's *critical* to get this right before you start. See [Basic Audio Setup](#) for guidance
* **Audio File Name:** The name of the song file you have placed in `CustomWIPLevels > [Song Folder]` Recommended to just name it *song.ogg* to avoid the pitfalls of special characters
* **Preview Start Time:** Position in the song file, in seconds, of the start of the in-game menu song preview. Defaults to 12s
* **Preview Duration:** Duration, in seconds, of the in-game menu song preview. Defaults to 10s
* **Cover Image Name:** The name of the image file you have placed in `CustomWIPLevels > [Song Folder]`. Must be perfectly square and at least 256 px but no more than 512 px
* **Environment Name:** A dropdown menu of the default environments or platforms available. See [Basic Lighting Practices](#) for an overview of these environments
* **Custom Platform:** The copy/pasted name of a custom platform from [ModelSaber](https://modelsaber.com/Platforms/). This feature is glitchy and it's recommended that you JSON edit any custom platform information
* **Contributors Tab:** This side tab is an optional spot to give credit to mappers, lighters, playtesters or other contributors to your map. Enter the contributor role, their name, and the file name of a square "profile image" which you place in your song folder

The <kbd>Open Sond Folder</kbd> button will open your song folder in Windows Explorer. This will help you confirm that you have your files in the right spot.
The <kbd>Package Song to Zip</kbd> button will remove your autosaves folder and zip the files for BeatSaver.
The <kbd>Save Song Info</kbd> button commits all of your metadata to the info.dat file
### Difficulty Settings

## Mapping Settings
# Basic Controls
> This is a stub section in progress. DM helencarnate#2079 if you'd like to contribute.
{.is-info}
# Error Checker
> This is a stub section in progress. DM helencarnate#2079 if you'd like to contribute.
{.is-info}
# Song Packaging
> This is a stub section in progress. DM helencarnate#2079 if you'd like to contribute.
{.is-info}
