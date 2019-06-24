<!-- TITLE: Modding -->
<!-- SUBTITLE: Instructions for modding Beat Saber -->

# Installing Mods
If you have no mods installed, visit the [Beginners Guide.](beginners-guide)

To install other mods that you have downloaded or made, place the plugin into your `Plugins` folder within the Beat Saber install directory.
Can't find where Beat Saber is installed? See: [Install Folder](/faq/install-folder).

### Linux?
If you happen to use Linux for gaming, and want to install mods on your Linux system, don't worry. [We've got a guide set up for you!](https://bsmg.wiki/modding/linux)

# Making Mods
Beat Saber does **not** have built in mod support.

Instead, most mods within the mod installer rely on [BSIPA (Beat Saber Illusion Plugin Architecture)](https://github.com/nike4613/BeatSaber-IPA-Reloaded/) to inject plugins into the game, as well as providing some useful tools for us modders.

Previously, we used [IPA (Illusion Plugin Architecture)](https://github.com/Eusth/IPA). Some plugins still use this, and is still temporarily supported by BSIPA. It is recommended to use BSIPA for any future modding endeavors, however.

* [If you want to get started making your own mod, this gets your project setup and ready to mod.](modding/intro)
* [Once you're ready to make a mod, here's a tutorial that'll teach you the basics of modding and using community built libraries.](modding/example-mod)
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
* [Unity Scripting API](https://docs.unity3d.com/ScriptReference/index.html)
* [dnSpy](https://github.com/0xd4d/dnSpy)
* [Harmony](https://github.com/pardeike/Harmony)
* [Beat Saber IPA](https://github.com/nike4613/BeatSaber-IPA-Reloaded)
