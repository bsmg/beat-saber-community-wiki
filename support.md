<!-- TITLE: Support -->
<!-- SUBTITLE: Common modding-related issues! -->

### Table of Contents
0. [Important Notes](#0-important-notes)
1. [Installer Issues](#1-installer-issues)
2. [In-Game Issues](#2-game-issues-post-modding)
3. [Common Questions](#3-common-questions)
4. [Troubleshooting](#4-troubleshooting)
5. [If All Else Fails](#5-if-all-else-fails)
6. [Still Having Issues](#6-still-having-issues)

# 0. Recent FAQs
### New Update, Mods are not showing up in Game!
This is caused because modAssistant doesn´t run your `IPA.exe` after mod installation.

To fix that, just go into your game installation folder, and drag your `BeatSaber.exe` onto the `IPA.exe` inside your game folder.
A command window should show up and patch your game again. When that is finished you should be good to go!

### Installers only show mods for 1.0.0
Anything for 1.0.0 works for 1.0.1. If anyone has spare time and wants to reupload all the 1.0.0 mods for 1.0.1 on BeatMods let us know, I'm only half joking.

### Steam Vr Loading Issue
The new SteamVR update causes the game to hang upon loading into a map, sometimes so long that you've missed blocks by the time the game loads.
1.**Under Developer Settings**
2.**Turn On**
3.**Do Not Fade To Grid When App Hangs**
>Refer To This Gif.
https://media.discordapp.net/attachments/442696229508612096/580271306461806640/fix_game_not_responding.gif

### If You're Updating From A Previously Modded Copy
Delete your Plugins folder and **run the game once** on the new update. Then, reinstall your mods using an installer linked on the [beginner's guide](/beginners-guide). 

If the game boots with no mods installed, check the Plugins folder for mods. If none exist, simply rerun the manager - you likely didn't run the game once before reinstalling mods.
If the game seems unplayable, check [section 2](#2-game-issues-post-modding)

## The installers aren't installing any plugins
The installers download mods to `Beat Saber/IPA/Pending`, and these files are moved to your plugins folder when you launch the game. If your game Plugins folder still is empty afterwards, run `ipa.exe` again and make sure that nothing is preventing it from running, e.g. `Anti-viruses, Admin permissions, etc.`

# 1. Installer Issues
### 1.1 Is the mod manager a virus?
BitDefender and other AV software seem to have added the Mod Manager into their database of suspicious programs. See this [GitHub issue](https://github.com/beat-saber-modding-group/BeatSaberModInstaller/issues/20) for more info, and use your best judgement.

### 1.2 I can't download the mod manager, or it closes as soon as I start it up|
You're probably trying to run the old mod managers, just use mod assistant instead. [ModAssistant Github](https://github.com/Assistant/ModAssistant/releases/latest).
You can also refer to [Videos On Installer Usage, And Manual Installation](#watch-videos-on-installing)

### 1.3 Permission Errors
Run the mod manager in admin mode if your PC's security settings have insufficient permissions to patch files by default.
Your anti-virus program can also be the cause for permission errors. Add the entire beatsaber folder to your exceptions. 
>You could also add the `beatsaber.exe` and `ipa.exe` to your list of exceptions

### 1.4 No mods in game
So you just installed some mods but they don't seem to appear in game. Make sure that the following are correct:
* **Make sure that you ran the game once before installing mods**. If you didn't, there likely isn't a Plugins folder in your install directory as BSIPA removes all mods on the first run of a fresh update. Reinstall mods again if this is the case.
* Steam/Oculus is launching Beat Saber from the **same installation** that mods are in. *e.g. mods are on the D drive but steam is launching from the C drive.* Set the correct install location in your choice of installer.
* If you installed mods manually, make sure you included all the files from the download and put them in the correct folders, as well as their dependencies.
* Redownload the dependencies, `BSUtils`, `Harmony`, `IniParser` , `CustomUI`, `BSIPA` and extract them to the correct folders, and run the IPA.exe again.

# 2. Game Issues Post-Modding
## Crashing/Game Not Starting Issues

### 2.1 GetThreadContext Failed Error
If a window pops up saying `GetThreadContext Failed` and/or you hear a Windows error sound, you may have software on your PC that breaks Beat Saber mods. Many third-party anti-cheat software like ESEA and FaceIt disrupt BSIPA from applying mods to Beat Saber, even when not running. Some Anti-Virus software also exhibit similar behavior. 

To solve this problem:
1. Uninstall the anti-cheat software.
2. Reboot your PC.
3. Check if any remnants of the software still exist in your `AppData` folders.
4. Run the game.
If problems persist then try the following:
`Additional Note:The problem can continue to persist due to lacking permissions or exceptions, any program that can block bsipa, or programs marked suspicious can make this problem persist`
Steam: [Verify Steam Game Files](#verify-game-files-for-steam)
Oculus: Perform a [Clean Installation](#clean-installation)

This should fix the problem.

### 2.2 Black screen/Environment, Unity crash window, Avatar standing in Black environment
This one is simple: verify files if you have the game on Steam, or reinstall the game on Oculus Home, 
if you're reinstalling refer to these:
[Backing Up Custom Content](#4-1-backing-up-custom-content)
[Clean Installation](#clean-installation)
This seems to happen when updating Beat Saber and having mods installed previously, but not to users with clean installs of the game.

## Framerate Issues
### 2.3 The game is unbearably laggy after installing mods
If the game lags so badly that you can barely click the `Continue` button on the Health & Saftey screen, then verify files if you have the game on Steam, or reinstall the game on Oculus Home. 
Do the same if it won't start up at all, and shows no error messages when trying to launch the game.

If that didn't solve the issue, then check section [2.4 Improving framerate](#framerate-issues)

### 2.4 Improving Framerate
If [2.3](#2-3-the-game-is-extremely-laggy-after-installing-mods-or-it-wont-start-up-at-all) didn't improve your fps, then your PC might simply be struggling to keep up with the stress caused by mods. Here are some things you can do to improve framerate, in no particular order:

**NVDIA GEFORCE EXPERIENCE NOW OPTIMIZES BEATSABER, IT USUALLY SETS YOUR GAMES RENDERING SCALE PAST 1.0, USUALLY 1.4 or 1.8 THIS IS THE COMMON REASON FOR LAG RECENTLY**

* Use a less complex custom avatar.
* The custom saber **Plasma Katanas** have tons of custom events and are known to introduce lag if you miss.
* CameraPlus can be very taxing, especially if you have multiple cameras and increase the FOV.
* Turn down Render Scale, Anti-Aliasing, mirror, fog, etc in the base game settings.
* For Oculus players: consider using 2 sensors instead of 3+.
* Reduce your total mod and song count. 
* Perform a clean reinstall of the game files. [Clean Installation](#clean-installation)
* Low framerate can also be caused by something going wrong within your application data folder, to fix this refer to [Deleting The Beatsaber Folder Within Your App Data](#deleting-your-beat-saber-saves-in-app-data)
* CountersPlus counters like scorecounter and swing speed can be expensive. [See this github wiki page on performance with Counters+](https://github.com/Caeden117/CountersPlus/wiki/Performance-and-Optimization)

VR is very CPU intensive, especially if you add mods. If you're struggling to run the game with the mods you want, consider upgrading your hardware. Note that Beat Saber doesn't utilize the GPU very much as it's a fairly simple game visually.

# 3. Common Questions
### 3.1 Blank Menu No Buttons
If your main window in game is blank, your save file likely got corrupted.
To fix this refer to [Delete Beatsaber Folder Within Your App Data](#deleting-your-beat-saber-saves-in-app-data)
>Note: This will delete your local scores and statistics.
{.is-warning}

### 3.2 How do I use `x` mod?
If you're using Mod Assistant or Beat Saber Mod Manager, click the mod and hit the "View Selected Mod Info" button. http://beatmods.com has a "More Info" button on each mod as well.

### 3.3 Crashing (Multiplayer Mod + Rumble Enchancer)
There's a issue between certain versions of the multiplayer mod and the rumble enchancer mod, if both are installed the game will crash and such, uninstall either. 

## Custom Avatars Issues
### 3.4 Custom Avatars (Not) Showing Ingame
Click the **Home** button on your keyboard with the game in focus to toggle visibility in the headset.

### 3.22 My Avatars Are Broken
Make sure your custom avatars plugin is installed properly and updated, also make sure your dependencies are too.
You might have a corrupted/broken avatar, having one avatar break can break all of your avatars likewise with songs and sabers.
Refer to [Finding Broken Content](#4-2-finding-broken-content) if you think you have corrupted avatars or if you've made sure your mods and dependencies are updated but avatars still are broken.

## Songloader Issues

### 3.5 My Songs Are Missing
>Make sure you read [No Mods In Game](#1-4-no-mods-in-game) first.

Make sure your songs are in your CustomLevels folder, this will be located in *Beat Saber/Beat Saber_Data/*, this contains all of the custom songs you have downloaded so far.
If its there then your plugins are probably the problem 

### 3.6 Songs Are Broken/Invisible Blocks/Red Play Button
If your songs are broken make sure you have the lastest version of the song loader plugin, as songs mapped for newer versions don't work well with previous versions of the game.
If that didn't fix it then you might have a corrupted song, you can try finding it by refering to [Finding Broken Content](#4-2-finding-broken-content)

Also try re-installing the plugin again, if that doesn't work reinstall your game, [Clean Install](#clean-installation)

## Camera Plus Issues
### 3.7 Camera Plus Isn't Working/Past Health Screen
Make sure the setting for "Smooth Camera" is turned off in your ingame settings,
If that doesn't work make sure you have the mod installed properly try reinstalling it, and all of its dependencies.

### 3.8 My desktop view only takes up a small section of the screen
Your CameraPlus display isn't filling up your canvas. Either drag the corner to fit the screen, or right click the window and click "Fit to Canvas".

> Note that CameraPlus' context menu has been disabled as of 1.0.0 due to compatibility issues. Edit the config file manually or use the hotkeys to edit settings, you can find a full list of options on the [GitHub](https://github.com/Kylemc1413/CameraPlus)

## Beatsaver Downloader Issues
### 3.9 Beatsaver Downloader More Songs Button
The **More Songs button is located in the Mods button in the main menu**, if the button for More Songs is greyed out then make sure all your songs loaded first, as seen in the bar on the main menu
if your mods button isnt there then kindly make sure your plugins and dependencies are working and installed properly, refer to [No Mods In Game](#1-4-no-mods-in-game).

### 3.10 Nothing Showing Up In The More Songs Menu
The probable causes for beatsaver downloader not working are:
1. Make sure all of your songs have loaded in before, or else the More Songs button will be greyed out.
2. Your anti-virus or firewall blocking access to beatsaver.

# 4. Troubleshooting
### 4.1 Backing Up Custom Content
Backing up your custom content is ideal so you wont lose your custom content
mainly songs, but sabers and avatars too, although I highly recommend you install your custom content after verifying that the mods work
as songs and avatars and platforms and sabers can break your game if they become outdated or corrupted somehow, refer to [Finding Broken Content](#4-2-finding-broken-content)

To back up your custom content simply move them out of the `Beat Saber Directory`
Either to your desktop or the folder before that, your directory will usually be at
*The fastest way I found was to just copy it and paste it into the directory just before beatsaber, a.k.a a nearby/previous directory it takes only a few seconds to copy and paste.*

>Steam: 	`\steamapps\common\Beat Saber\`

>Oculus: 	`\hyperbolic-magnetism-beat-saber\`

### 4.2 Understanding Logs
If you're on Steam you can go to 
>Beat Saber > Properties > Set Launch Options > Add `--verbose` to the text field that appears

If you're on Oculus then you will have to Right click on Beat Saber.exe and create a shortcut. 
>Right click the shortcut and edit the Target to add "--verbose" to the end of it. Should be something like `C:\Program Files\Oculus\Software\Software\hyperbolic-magnetism-beat-saber\Beat Saber.exe" --verbose`

After adding verbose to your game hopefully it will display any errors regarding your avatars, sabers, and songs 
* This may not show 100% of the time for avatars and sabers, and you may have to remove all your avatars/sabers and try them one by one to see which one breaks the game.

These messages are also written to `Beat Saber/Logs`.

A list of common exceptions can be found [here](https://bsmg.wiki/support/exceptions).

## Deleting Your Beat Saber saves in AppData
This will delete your scores and local data but not your online scores or anything like that.
You can find the folder here 
>`%appdata%/../locallow/hyperbolic magnetism/beat saber`

Copy and paste everything from inside the bar above and paste it to your address bar in file explorer
To "delete" this folder `(the beatsaber folder in locallow)` you can rename it or actually delete it. 

You can also get to this folder by showing hidden items and navigating to your
>Users > "USER" > AppData > Local Low > Hyperbolic-magnetism

[video](https://youtu.be/ONxJcD3Ir3Q){.youtube}


 >Note: Deleting the Appdata folder will also delete your local scores and statistics.
{.is-warning}

## Verify Game Files For Steam
Steam Verify Game Files
To verify your game files on steam follow these steps:
1.)Make sure steamvr is closed as it wont let you verify your games otherwise. 
2.)Go to your steam library and find Beat Saber
3.)Right click Beat Saber and click on Properties
4.)Go to the "Local Files" tab in properties
5.)Select the last option "Verify Integrity Of Game Files"
6.)Let it finish verifying and downloading any missing files and you should be good to go.

[video](https://www.youtube.com/watch?v=EBFfT4-ZiIc){.youtube}

## Clean Installation
Basically:
1.[Backing Up Custom Content](#4-1-backing-up-custom-content) 
2. Uninstall Beat Saber
3. Delete your "Beat Saber" folder
4. Reinstall the game
5. Before Modding Launch The Game Once `Vanilla Or Without Mods **FIRST**`

To perform a clean installation you're going to have to make sure that all of the files related to beatsaber have been deleted "Application Data being a separate thing"
**First make sure you've backed up all of your custom content!** `Refer To :`[Backing Up Custom Content](#4-1-backing-up-custom-content) 
Then you'll have to go to whichever directory you had beatsaber installed and **Delete the ENTIRE Beat Saber Folder** to make sure you have no files left over which
may break your game or mods, Oculus just deletes the folder as is, but this may but highly unlikely break or not work, but better safe than sorry!
`This Next Part Is Optional`
**Now if you really want to have a CLEAN** Installation `Refer To:`[Deleting The Beatsaber Folder Within Your App Data](#deleting-your-beat-saber-saves-in-app-data)

## Watch Videos On Installing
**QUICK NOTE THE PLUGINS WILL SHOW UP IN YOUR PLUGINS FOLDER AFTER LAUNCHING THE GAME IF YOU USE THE INSTALLER**
Here are videos I made showing the two methods for the entire modding process. I did both methods, using the installer, and doing it manually.
Also I apologize for the small end bit in the manual install, I've never used playlists before and I'm still not sure on how to use them.
[video](https://youtu.be/nbWNwwWFGKg){.youtube} [video](https://youtu.be/4OH7CniNsUg){.youtube}

# 5. If All Else Fails
If none of these solutions worked for you then I'd recommend a complete purge of your beatsaber files, this would include your game and the data it saves inside your appdata folder
Refer to [Clean Install](#clean-installation) basically, uninstalling your game, then deleting all the remaining files if any files remain after uninstalling, after doing a complete game uninstall,
it would be best to [Delete The Beatsaber Folder Within Your App Data](#deleting-your-beat-saber-saves-in-app-data) and with this all the files related to beatsaber would be deleted by now,
from here please verify the following.
* Make sure your current user **is an administrator**
* Your anti-virus is **Off** (for the meantime at least)
* You have permission to create folders and edit files within the disk drive/your pc, (from what I heard a windows update recently caused problems for people)
* Your drivers are up to date
* That the problem doesn't lie within your headset, or operating system, or your hardware/software
* Your internet connection is completely fine, not blocking nor lacking access to anything related to beatsaber modding and steam etc.
### Desperate Measures
* Reinstalling all things related to VR.
* Reinstalling all the programs and such Unity uses. *DirectX, etc.*
### REALLY DESPERATE MEASURES
* Reinstall your os and format your drive.
This is an absolute last ditch effort that would make sure that everything software related is eliminated as a variable, and could help determine if it is a hardware issue,
I personally dont recommend this unless you have no other choice. Don't forget to back up your important files elsewhere either to an external drive or cloud storage. 
# 6. Still having issues
If this page doesn't cover the bases, then feel free to ask a question in the discord! To increase the chance that you'll have your questions answered, consider the following:
* Use the right channel please. `#support` for mod troubleshooting, `#model-discussion` for questions about **making your own avatars or sabers**, and `#mapping-discussion` for questions about **making maps.**
* Be polite and respectful
* Describe your problem in detail. "It didn't work" is about as descriptive as telling your doctor you don't feel well. What's not working, and what did you try? Are there any messages that come up on screen? Did your entire screen turn bright purple? 

> Note: those with the `Support` role are volunteers that might choose to help out in their free time. The support role is in recognition of the knowledge and effort they have put forth, but it doesn't necessarily mean that they'll be around to help just because they're online.
{.is-warning}

Thank you!

> Thank you to Saber-Chan for their hard work on this page.
