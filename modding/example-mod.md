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
> **This section is a work in progress. Until this message disappears, this page is most likely not finished.**
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

## Setting Variables
> If at any point you feel overwhelmed, it probably means you do not have enough experience. In that case, consider watching some Unity and C# tutorials to get familiar with Unity.
{.is-danger}

Before we begin with our plugin, it is important to create some variables that will help us later in development:

![Plugin Variables](/uploads/modding-example/plugin-variables-setup.png "Plugin Variables")
*(Courtesy of [Beat Saber Progress Counter](https://github.com/Strackeror/BeatSaberProgressCounter/))*

`env` | The `0.11.2` patch of Beat Saber brought with it a different way the game loads scenes. Instead of one "master" scene, it is split up into different scenes depending on the environment. We will detect if the game is played a game based off the name of the scene.
`enabled` | Toggles our plugin on or off with the flip of a variable. If you want to add a configuration file later on, this will be one option you don't want to miss.
`counterPosition` | Where our counter will be located in the scene.

> If you receive an error relating to the Vector3 variable, you may need to add `using UnityEngine;` to the top of your file.
{.is-danger}

## --verbose
Let's add a quick line of code to the beginning of our `OnApplicationStart()` void function:

`Console.WriteLine("Hello World!");`

It is useful to modify the starting parameters of Beat Saber (through Steam or a shortcut) and add `--verbose` to the end. This will start Beat Saber with a console window open, displaying logs from every mod you have installed. If you compile then launch Beat Saber, and scroll from the top of the console window, you should see our Hello World message. Any errors that would cause our plugin to not work properly will be shown here, although because our plugin is in a compiled state, it will not tell us the exact line number. Be careful!
## Creating a GameObject
We will write little code inside of `Plugin.cs`. We will create a MonoBehavior script which will handle the heavy lifting for us. In fact, we will only be writing three more lines of code before we move on to another file.

![Plugin Scenechanged](/uploads/modding-example/plugin-scenechanged.png "Plugin Scenechanged")

> If you receive an error relating to `env.Contains()`, you may need to add `using System.Linq;` to the top of your file.
{.is-danger}

### What's going on here?
Instead of having an if statement inside an if statement, we've compressed the code into just 3 lines.

* The first line deals with the `enabled` variable we set earlier. If it is `false`, C# will take the inverse, which will be `true`. It'll activate the if statement, causing the function to return, and stop execution.

* The second line deals with the `env` string array we also created earlier. If the name of the scene is included in that array, it continues to our last line. If it does not, it'll activate the if statement, causing the function to return. This prevents our plugin from activating in the main menu, the tutorial, or in the very beggining "Health Warning and Information" screen.

### What's with the error?
Our plugin does not have a `MissedCounter` file to plug into our last line. Here we are creating an Empty GameObject at the very center of the scene, and adding a missing script into it. This is what we're going to be creating right now!

## MissedCounter.cs
Let's create a new `MissedCounter.cs` file that extends from `MonoBehavior`. For those who don't know, go to `Project` >> `Add Class...` and type in the name. In the class name, add ` : MonoBehavior` to the end.
> If you receive an error extending from `MonoBehaviour`, you will need to add `using UnityEngine;` to the top of your file.
{.is-danger}

![Plugin Missedcounter](/uploads/modding-example/plugin-missedcounter.png "Plugin Missedcounter")

For those who are familiar with Unity, you will recognize what we've just made. Here we can import Unity's default `Init()`, `Start()`, and `Update()` functions, and you can pretty much go nuts from here.

# TextMeshes, Events, and Counting
In the previous section we covered the basics of any plugin. We created basic variables and have created an empty GameObject that will be called once a song is loaded. In this section, we will finish our component we added into the empty GameObject.

## References and TextMeshPro

If you [followed the plugin setup guide](/modding/intro), you learned how to add References when you set up the project. In this example, we will be adding `TextMeshPro` as a Reference to gain access to custom text in Beat Saber.

If you have forgot:
1. Under `Project`, click `Add Reference...`
2. Under `Browse`, click the `Browse` button. You should be where you left off when adding References. Search for and then add `TextMeshPro`.
3. In `MissedCounter.cs`, add `using TMPro;` to the top of the file.

![Plugin Addreferences](/uploads/modding-example/plugin-addreferences.png "Plugin Addreferences")

## Adding Variables

Before we can make a working counter, we need to make some variables that will help us in this task. Let's create these variables:

![Plugin Variables 2](/uploads/modding-example/plugin-variables-2.png "Plugin Variables 2")

### What are these variables?

`counter` will be our simple counter that will increment every time we hit a note incorrectly, or miss a note entirely.
`score` will be our reference to a Beat Saber component which has two events we will use, `onNoteHit` and `onNoteMiss`.
`counterGO` will be a second GameObject we will create which will act as the counter itself. The `MissedCounter.cs` will be a label which will tell uses that the counter they are seeing is for Misses.
`counterText` will be the TextMeshPro mesh we will add to `counterGO`.

## Initializing

Before anything can work, we need to gain access to the `ScoreController` Beat Saber uses, and sometimes that will take time. There are many different ways to get access, but here are two commonly used and very similar methods.

In both cases, we will be the `Awake()` function built-in to Unity components which will start a function utilizing an infinite `while(true)` loop that will attempt to get the first `ScoreController`. If we find it, the loop will break and continue execution into an `Init()` function. If we don't, we'll wait for a bit before trying again.

### Coroutines and IEnumerators
> If you receive an error relating to `IEnumator`, add `using System.Collections;` to the top of your file.
{.is-danger}

This has been used since the beginning of Beat Saber modding, where the version of .NET was 3.6. With no `System.Threading.Tasks` and no asynchronous tasks, we had to rely on built-in MonoBehaviour scripts. We will be creating an `IEnumerator` which will hold our code.



Also, be sure to visit the [#mod-development](https://discordapp.com/channels/441805394323439646/443146108420620318/) channel on the [modding discord](https://discord.gg/beatsabermods), to share what you're working on!