<!-- TITLE: Modding -->
<!-- SUBTITLE: Instructions for modding Beat Saber -->

# Installing Mods
If you have no mods installed, visit the [Beginners Guide.](beginners-guide)

To install other mods that you have downloaded or made, place the plugin into your `Plugins` folder within the Beat Saber install directory.
Can't find where Beat Saber is installed? See: [Install Folder](/faq/install-folder).
# Making Mods
Beat Saber does **not** have built in mod support.
Instead, all mods within the mod installer rely on [IPA (Illusion Plugin Architecture)](https://github.com/Eusth/IPA) to inject plugins into the game.
* [Beat Saber modding intro / template](modding/intro)
* [Making a basic mod](modding/example-mod)

# Launch args
Helpful launch arguments that will make modding / debugging easier.

| Argument  | Description |
| ------------- | ------------- |
| `--verbose`  | Enables the output log window for IPA. This will show the debug console that mods use.  |
| `fpfc` | "First Person Flight Controller" This allows you to use WASD and the mouse to navigate around the menu in game. This makes testing much easier, because you don't have to put on your headset! |
| `-vrmode oculus` | If you are running Beat Saber through Steam, this allows you to play the game on an Ouclus headset. |
# Mods Index
See: [All Mods.](modding/all-mods)

# Other Links
* [ModSaber](https://www.modsaber.org/)
* [Unity Scripting API](https://docs.unity3d.com/ScriptReference/index.html)
* [dnSpy](https://github.com/0xd4d/dnSpy)
* [Harmony](https://github.com/pardeike/Harmony)
* [Beat Saber IPA](https://github.com/nike4613/BeatSaber-IPA-Reloaded)
