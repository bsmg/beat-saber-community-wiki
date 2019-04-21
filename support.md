<!-- TITLE: Support -->
<!-- SUBTITLE: Common modding-related issues! -->

### Table of Contents
1. [Installer Issues](#1-installer-problems)
2. [In-Game Issues](#2-game-has-issues-after-installing-mods)
3. [Common Questions](#3-common-questions)
4. [Troubleshooting](#4-troubleshooting)
5. [Still Having Issues](#5-still-having-issues)

# 1. Installer problems
### 1.1 Is the mod manager a virus?
BitDefender and other AV software seem to have added the Mod Manager into their database of suspicious programs. See this [GitHub issue](https://github.com/beat-saber-modding-group/BeatSaberModInstaller/issues/20) for more info, and use your best judgement.

### 1.2 I can't download the mod manager, or it closes as soon as I start it up
Make sure you're using the one from the [BSMG GitHub](https://github.com/beat-saber-modding-group/BeatSaberModInstaller/releases/latest). There are 3 releases being distributed due to concerns about how different AV software blocks the application:
* BeatSaberModManager-Unbundled.zip
* BeatSaberModManager.exe
* BeatSaberModManagerClassic.exe
Take your pick, they all work the same way. Alternatively, consider using [BeatDrop](https://bsaber.com/beatdrop/) instead.

### 1.3 Permission errors
Run the mod manager in admin mode if your PC's security settings have insufficient permissions to patch files by default.
Your anti-virus program can also be the cause for permission errors make sure you add the entire beatsaber folder to your exceptions, 
>You could also add the `beatsaber.exe` and `ipa.exe` to your list of exceptions

### 1.4 No mods in game
So you just installed some mods but they don't seem to appear in game. Make sure that the following are correct:
* As stated multiple times in the [beginner's guide](/beginners-guide), **you ran the game once before installing mods**
* You're **scrolling right **to actually see the CustomMaps songpack.
* There actually is a Plugins folder in your install directory.
* Steam/Oculus is launching Beat Saber from the **same installation** that mods are in. *e.g. mods are on the D drive but steam is launching from the C drive*
* If you installed mods manually,make sure you included all the files from the download and put them in the correct folders, as well as their dependencies.
* Redownload the dependencies, `BSUtils`, `Harmony`, `IniParser` and `BSIPA` and extract them to the correct folders, and run the IPA.exe again.

![Custommaps](/uploads/custommaps.png "Custommaps")
# 2. Game has issues after installing mods
### 2.1 GetThreadContext Failed Error
If a window pops up saying `GetThreadContext Failed` and/or you hear a Windows error sound, you may have software on your PC that's breaking Beat Saber mods. Many third-party anti-cheat software like ESEA and FaceIt disrupt BSIPA from applying mods to Beat Saber, even when not running. Some Anti-Virus software also exhibit similar behavior. 

We're working on a more permanent solution, but at the moment you need to do the following steps:
1. Uninstall the anti-cheat software.
2. Reboot your PC.
3. Verify files in Steam, or reinstall the game on Oculus Home.

This should fix the problem.

### 2.2 Black screen/Evironment, Unity Crash Window
This one is simple: verify files if you have the game on Steam, or reinstall the game on Oculus Home, if you're reinstalling refer to [Backing Up Custom Content](#4-1-backing-up-custom-content)
This seems to happen when upgrading Beat Saber to 0.13 from 0.12 and having mods installed previously, but not to users with clean installs of the game.
> We're trying to get to the bottom of this problem but we have insufficient data. If you got the Unity crash window and you'd like to help us, please navigate to `%AppData%\..\LocalLow\Hyperbolic Magnetism\` (copy-paste it into your address bar) and see if there's anything in the `Crashes` folder. If there is, zip it up and ping `@williums#0001` in the BSMG #support channel. Thank you!

### 2.3 The game is extremely laggy after installing mods
If the game lags so badly that you can barely click the `Continue` button on the Health & Saftey screen, then verify files if you have the game on Steam, or reinstall the game on Oculus Home.

If that didn't solve the issue, the problem could be GeForce Experience setting your Render Scale way too high, or see the section on [Improving framerate](#3-2-framerate-is-low)
# 3. Common Questions
### 3.1 My menus are completely blank in game
If your main window in game is blank, your save file likely got corrupted. To fix it: 
1. Navigate to: `%AppData%\..\LocalLow\Hyperbolic Magnetism` *(copy and paste it to your address bar)*
2. Delete or rename the Beat Saber folder to something else. 
 
When you re-enter the game, it'll recreate the save file and should load the main menu properly.

### 3.2 Framerate is low
If [2.3](#2-3-the-game-is-extremely-laggy-after-installing-mods) didn't improve your framerate, then your PC might be struggling to keep up with the stress caused by mods. Here are some things you can do to improve framerate, in no particular order:
* Use a less complex avatar.
* The custom sabers `Plasma Katanas` have tons of custom events and are known to introduce lag if you miss.
* CameraPlus can be very taxing, especially if you have multiple cameras and increase the FOV.
* Turn down Render Scale, Anti-Aliasing, mirror, fog, etc in the base game settings.
* For Oculus players: consider using 2 sensors instead of 3+.
* Reduce your total mod and song count. 
* Low framerate can also be caused by something going wrong at: `%AppData%\..\LocalLow\Hyperbolic Magnetism` You can fix this by either renaming or deleting the folder. (Deleting the folder will cause you to lose your local scores)

VR is very CPU intensive, especially if you add mods. If you're struggling to run the game with the mods you want, consider upgrading your hardware. Note that Beat Saber doesn't utilize the GPU very much as it's a fairly simple game visually. 

### 3.3 How do I use `x` mod?
If you're using the Beat Saber Mod Manager, click the mod and hit the "View Selected Mod Info" button. http://beatmods.com has a "More Info" button on each mod as well.

## Custom Avatars Issues
### A.1 Custom avatars show up in my headset, how do I get rid of that?
Click the `Home` button on your keyboard with the game in focus to toggle visibility in the headset.

### A.2

## Songloader Issues
### S.1 My Songs Are Missing
>Make sure you read [No Mods In Game](#1-4-no-mods-in-game)
Make sure your songs are in your CustomSongs folder, this will be located in your main beat saber folder/directory, this contains all of the custom songs you have downloaded so far.
If its there then your plugins are probably the problem 

### S.2 Songs Are Broken/Invisible Blocks
If your songs are broken make sure you have the lastest version of the song loader plugin, as songs mapped for newer versions don't work well with previous versions of the game.
If that didn't fix it then you might have a corrupted song, you can try finding it by refering to [Finding Broken Content](#4-2-finding-broken-content)

## Camera Plus Issues
### 3.8 Camera Plus Isn't Working
Make sure the setting for "Smooth Camera" is turned off in your ingame settings, also if that doesn't work make sure you have the mod intalled properly
try reinstalling it, and all of its dependencies.

### 3.9 My desktop view only takes up a small section of the screen
Your CameraPlus display isn't filling up your canvas. Either drag the corner to fit the screen, or right click the window and click "Fit to Canvas".

# 4. Troubleshooting
### 4.1 Backing Up Custom Content
Backing up your custom content is ideal so you wont lose your custom content
mainly songs, but sabers and avatars too, although I highly recommend you install your custom content after verifying that the mods work
as songs and avatars and platforms and sabers can break your game if they become outdated or corrupted somehow, refer to [Finding Broken Content](#4-2-finding-broken-content)

To back up your custom content simply move them out of the `Beat Saber Directory`
Either to your desktop or the folder before that, your directory will usually be at

>Steam: 	`\steamapps\common\Beat Saber\`

>Oculus: 	`\hyperbolic-magnetism-beat-saber\`

### 4.2 Finding Broken Content
If you're on Steam you can go to Beat Saber > Properties > Set Launch Options > Add "--verbose" to the text filed that appears

If you're on Oculus then you will have to 
Right click on Beat Saber.exe and create a shortcut. Right click the shortcut and edit the Target to add "--verbose" to the end of it. Should be something like "C:\Program Files\Oculus\Software\Software\hyperbolic-magnetism-beat-saber\Beat Saber.exe" --verbose

After adding verbose to your game hopefully it will display any errors regarding your avatars, sabers, and songs although it may not show 100% of the time
for avatars and sabers, you may have to remove all your avatars/sabers and try them one by one to see which one breaks the game.
//add wahtever fuckin else u want in here, and please add more to this as this can get confusing.

# 5. Still having issues
If this page doesn't cover the bases, then feel free to ask a question in the discord! To increase the chance that you'll have your questions answered, consider the following:
* Use the right channel please. `#support` for mod troubleshooting, `#model-discussion` for questions about **making** your own avatars, and `#mapping-discussion` for questions about **making** maps.
* Be polite and respectful
* Describe your problem in detail. "It didn't work" is about as descriptive as telling your doctor you don't feel well. What's not working, and what did you try? Are there any messages that come up on screen? Did your entire screen turn bright purple? 

> Note: those with the `Support` role are volunteers that might choose to help out in their free time. It's recognition for the efforts and knowledge, but it doesn't necessarily mean that they'll be around to help just because they're online.
{.is-warning}
