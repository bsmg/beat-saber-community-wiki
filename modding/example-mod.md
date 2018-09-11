<!-- TITLE: Example Mod -->
<!-- SUBTITLE: Learn how to make a basic mod for Beat Saber! -->
# Using dnSpy
dnSpy is a .NET debugger and assembly editor that allows you to import compiled `.dll`s and view them decompiled into C#.
In the case of modding, we can use dnSpy to view the source code of Beat Saber and find methods and variables that would be handy to have for some plugins.
Read more about it [here](https://github.com/0xd4d/dnSpy).

Download the [latest release of dnSpy.zip](https://github.com/0xd4d/dnSpy/releases/latest).
Extract the zip, and run `dnSpy.exe`.
Then drop in the file `\<Beat Saber Directory>\Beat Saber_Data\Managed\Assembly-CSharp.dll`
`Assembly-CSharp.dll` contains nearly all of the games' code.

You can also use dnSpy to view the code of plugins, even those that have not yet published to GitHub. Be wary, though!

![Dnspy Example](/uploads/modding/dnspy-example.png "Dnspy Example")
# Plugin Beginnings
> This section is a work in progress. Until this message disappears, this page is most likely not finished.
{.is-danger}

If you followed the [template setup guide](/modding/intro), you should end up with something similar to the following below:

![Plugin Example](/uploads/modding-example/plugin-example-2.png "Where We Left Off")

Before we continue on with the example, we will assume that you have:
* A basic to intermediate understanding of C#
* A basic to intermediate understanding of the ins and outs of Unity (GameObjects, Components, etc.)

## A Quick Summary
In this example, we will work on a basic plugin that counts how many notes we miss or hit incorrectly while playing a song. This example plugin will utilize:
* An empty GameObject which will hold a Component class file.
* TextMeshPro meshes.
* A basic overview of events and actions.

# Setting Variables
> If at any point you feel overwhelmed, it probably means you do not have enough experience. In that case, consider watching some Unity and C# tutorials to get familiar with Unity.
{.is-danger}
Before we begin with our plugin, it is important to create some variables that will help us later in development:

![Plugin Variables](/uploads/modding-example/plugin-variables.png "Plugin Variables")
*(Courtesy of [Beat Saber Progress Counter](https://github.com/Strackeror/BeatSaberProgressCounter/))*

`env` | The `0.11.2` patch of Beat Saber brought with it a different way the game loads scenes. Instead of one "master" scene, it is split up into different scenes depending on the environment. We will detect if the game is played a game based off the name of the scene.
`enabled` | Toggles our plugin on or off with the flip of a variable. If you want to add a configuration file later on, this will be one option you don't want to miss.
`counterPosition` | Where our counter will be located in the scene.

> If you receive an error relating to the Vector3 variable, you may need to add `using UnityEngine;` to the top of your file.
{.is-danger}

# Creating a GameObject
We will write little code inside of `Plugin.cs`. We will create a MonoBehavior script which will handle the heavy lifting for us. In fact, we will only be writing three more lines of code before we move on to another file.



> If you receive an error relating to `env.Contains()`, you may need to add `using System.Linq;` to the top of your file.
{.is-danger}

Also, be sure to visit the [#mod-development](https://discordapp.com/channels/441805394323439646/443146108420620318/) channel on the [modding discord](https://discord.gg/beatsabermods), to share what you're working on!