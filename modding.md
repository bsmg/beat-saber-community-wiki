<!-- TITLE: Modding -->
<!-- SUBTITLE: Instructions for getting started making mods for Beat Saber. -->

# Making Mods
Beat Saber does **not** have built in mod support.

Instead, most mods within the mod installer rely on [BSIPA (Beat Saber Illusion Plugin Architecture)](https://github.com/nike4613/BeatSaber-IPA-Reloaded/) to inject plugins into the game, as well as providing some useful tools for us modders.

Previously, we used [IPA (Illusion Plugin Architecture)](https://github.com/Eusth/IPA). Some plugins still use this, and is temporarily supported by BSIPA. We still use IPA for the mod tutorial, however it is recommended to use BSIPA for any future modding endeavors.

For those of you who prefer [BepInEx](https://github.com/BepInEx/BepInEx) over either of these options, Bepis is supposedly working on a BSIPA emulator for BepInEx, and already has one available for regular IPA plugins. As for developing Beat Saber plugins for BepInEx, well, you're kinda on your own.

### Need to setup a project?
If you are interested in creating a Beat Saber mod, but do not have a template or Visual Studio template set up, [follow the Intro guide to get your project all set up](modding/intro).

### Ready to go?
If you have a plugin template ready to go, and don't know how exactly to program a Beat Saber mod, [follow the example Modding Tutorial to get a basic grasp on Beat Saber modding](modding/example-mod).

### Want more?
If you've completed the modding tutorial, and still want more ways to improve your mod development experience, [check out the Extras page](modding/extras).

# Launch args
Helpful launch arguments that will make modding / debugging easier.

| Argument  | Description |
| ------------- | ------------- |
| `--verbose`  | Enables the output log window for IPA. This will show the debug console that mods use.  |
| `fpfc` | "First Person Flight Controller" This allows you to use WASD and the mouse to navigate around the menu in game. This makes testing much easier, because you don't have to put on your headset! |
| `-vrmode oculus` | If you are running Beat Saber through Steam, this allows you to play the game on an Oculus headset. |
<!-- # Mods Index
[Slaynash](https://www.twitch.tv/Slaynash) created an incredible spreadsheet of mods - you can [view it here.](https://docs.google.com/spreadsheets/d/1eVRbCUyaXjKUJRSNPZWERUO9tULK415buU0q-H7Z0dY)
We're working on getting the ModSaber archive organized, so hopefully we can have links to those mods in the future! -->

# Other Links
* [BeatMods](https://beatmods.com)
* [BeatMods Approval Guidelines](https://docs.google.com/document/d/15RBVesZdS-U94AvesJ2DJqcnAtgh9E2PZOcbjrQle5Y/edit?usp=sharing)
* [Unity Scripting API](https://docs.unity3d.com/ScriptReference/index.html)
* [dnSpy](https://github.com/0xd4d/dnSpy)
* [Harmony](https://github.com/pardeike/Harmony)
* [Beat Saber IPA](https://github.com/nike4613/BeatSaber-IPA-Reloaded)
* [Beat Saber Mods](https://stadivm.com/threads/how-to-install-beat-saber-mods.540/)
