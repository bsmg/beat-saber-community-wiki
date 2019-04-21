<!-- TITLE: Support -->
<!-- SUBTITLE: Before you go yell in the #support channel, check these common issues! -->

### Table of Contents
1. [Installer Issues](#1-installer-problems)
2. [In-Game Issues](#2-game-has-issues-after-installing-mods)
3. [Other Issues](#3-other-issues)
4. [Common Mod Questions](#4-common-mod-questions)


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

# 2. Game has issues after installing mods
### 2.1 GetThreadContext Failed Error
If a window pops up saying `GetThreadContext Failed` and/or you hear a Windows error sound, you may have software on your PC that's breaking Beat Saber mods. Many third-party anti-cheat software like ESEA and FaceIt Anti-Cheat disrupt BSIPA from applying mods to Beat Saber, even when not running. Some Anti-Virus software exhibit similar behavior. 

We're working on a more permanent solution, but at the moment you need to do the following steps:
1. Uninstall the anti-cheat software
2. Reboot your PC
3. Verify files in Steam, or reinstall the game on Oculus Home

This should fix the problem.

### 2.2 The desktop window and headset view are completely black upon running the game, or a Unity crash window pops up on screen.
This one is simple: verify files if you have the game on Steam, or reinstall the game on Oculus Home. This seems to happen when upgrading Beat Saber to 0.13 from 0.12 and having mods installed previously, but not to users with clean installs of the game.
> We're trying to get to the bottom of this problem but we have insufficient data. If you got the Unity crash window and you'd like to help us, please navigate to `%AppData%\..\LocalLow\Hyperbolic Magnetism\` (copy-paste it into your address bar) and see if there's anything in the `Crashes` folder. If there is, zip it up and ping `@williums#0001` in the BSMG #support channel. Thank you!

### 2.3 The game is extremely laggy after installing mods
If the game lags so badly that you can barely click the `Continue` button on the Health & Saftey screen, then verify files if you have the game on Steam, or reinstall the game on Oculus Home.

If that didn't solve the issue, the problem could be GeForce Experience setting your Render Scale way too high, or see the section on [improving framerate](#framerate-is-low)
# 3. Common Issues
### 3.1 My menus are completely blank in game
If your main window in game is blank, your save file likely got corrupted. To fix it: 
1. Navigate to: `%AppData%\..\LocalLow\Hyperbolic Magnetism` *(copy and paste it to your address bar)*
2. Delete or rename the Beat Saber folder to something else. 
 
When you re-enter the game, it'll recreate the save file and should load the main menu properly.

### 3.2 Framerate is low
If 

