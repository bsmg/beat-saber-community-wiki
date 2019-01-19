<!-- TITLE: Extras -->
<!-- SUBTITLE: The basics weren't good enough? Here's some more tools that you can use! -->

Here is some extra content and information that will help you on your way to creating a plugin. Inspecting the source code, accessing private settings, and using external libraries are all things Beat Saber plugins do, so why leave you off with *just* the basics?

Here are programs and libraries that allow you to go more advanced with your plugins an dwill help you greatly if you decide to explore new territory in Beat Saber modding. Remember, the [Beat Saber Modding group](https://discord.gg/beatsabermods) is always here for your programming help!


>This is heavily unfinished! If you wish to cover a library, or an aspect of modding, please DM me on Discord `Caeden117#0117` and let me know what to add.
{.is-danger}
# dnSpy
dnSpy is a .NET debugger and assembly editor that allows you to import compiled `.dll`s and view them decompiled into C#.
In the case of modding, we can use dnSpy to view the source code of Beat Saber and find methods and variables that would be handy to have for some plugins.
Read more about it [here](https://github.com/0xd4d/dnSpy).

Download the [latest release of dnSpy.zip](https://github.com/0xd4d/dnSpy/releases/latest).

Then extract the zip, and run `dnSpy.exe`.

If all has been done correctly, things should look something like this, without the large list of files on the left side.

![Dnspy Start](/uploads/modding/dnspy-start.png "Starting Page")

Then go to `File >> Open`, then locate and open the compiled Beat Saber code located in `\<Beat Saber Directory>\Beat Saber_Data\Managed\Assembly-CSharp.dll`

![Dnspy Start](/uploads/modding/dnspy-assembly.png "Code Location")

You can also use dnSpy to view and even edit the code of plugins, even those that have not yet published to GitHub. Be wary, though! Snooping around in other's code without permission is a bad idea.

![dnSpy Example](/uploads/modding/dnspy-example.png "dnSpy Example")

# Harmony
Harmony is a library for patching compiled .NET and Mono methods during runtime.
This allows editing of core Beat Saber functions and allows plugins to achieve things way beyond what basic Illusion Plugin Architecture can achieve.
Read more about it [here.](https://github.com/pardeike/Harmony)

Download the [latest release of Harmony](https://github.com/pardeike/Harmony/releases)
Extract `0Harmony.dll` to `/<Beat Saber Directory>\Beat Saber_Data\Managed`.
Add Harmony as a reference ([Click here if you forget how to add a reference to your project](/modding/example-mod#references-and-text-mesh-pro)).

> Plugins that utilize Harmony ***require*** the `0Harmony.dll` file inside of `/<Beat Saber Directory>\Beat Saber_Data\Managed`. Add a try-catch statement when you patch the game so the plugin doesn't crash when starting without Harmony.
{.is-warning}

# Reflection Util
ReflectionUtil is a simple file that allows grabbing and setting private variables inside of files.
This is used in conjuction with [dnSpy](/modding/extras#dnspy) to search for and set private variables in code.
Reflection Util is available in many mods, so [here is one from Beat Saber Utils](https://github.com/Kylemc1413/Beat-Saber-Utils/blob/master/Beat%20Saber%20Utils/Utilities/ReflectionUtil.cs)

## From Beat Saber Utils
If you haven't already, add Beat Saber Utils as a reference to your project. *(Link real soon guys)*

From there, add `using BS_Utils.Utilities;` to the top of your file.

Access it using `ReflectionUtil`.

## Creating Your Own
Create a new file called `ReflectionUtil.cs`
Copy and paste the above code to the newly created file, making sure to replace `namespace BS_Utils.Utilities` with the name of your project.

In other files, objects will now include a `GetPrivateField<T>(name)` and a `SetPrivateField(name)` function. You can pass in the name of any private variable (Usually marked with the `private` protection keyword, and/or an underscore `_` before the name) into either, and either:
* A compatible file type for `T` (Use `Saber` when trying to get a Saber set as a private field) when using `GetPrivateField<T>()`
Or...
* A compatible object to set `value` to when using `SetPrivateField(name, value)`.

You can also manually pass objects in by using `ReflectionUtil.GetPrivateField<T>(obj, name)` or `ReflectionUtil.SetPrivateField(obj, name, value)`.