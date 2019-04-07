<!-- TITLE: Modding Intro -->
<!-- SUBTITLE: Learn how to setup the plugin template -->

# Intro
Beat Saber is made in Unity 2018 using C# with .NET framework 4.6.
For convenience, RQ has created a plugin template for Visual Studio. This guide will show you how to setup that template.

Download the latest version of [Visual Studio Community.](https://visualstudio.microsoft.com/)

There are multiple templates that you can choose to install.

## BSIPA
DaNike includes a [modding template](https://github.com/nike4613/BeatSaber-IPA-Reloaded/releases/latest) if you intend to make your plugin using BSIPA. Simply grab the template `.zip` from the latest release!

## IPA
If you wish to use the older IPA, the [BS Plugin Template](https://github.com/Kylemc1413/BS-Plugin-Template/releases/download/0.0.1/BS.Plugin.Template.zip) by Kyle1413 includes more options to guide you, as well as a basic use case of CustomUI. We will be using this for the Mod Tutorial, however intend to upgrade to BSIPA in the near future.

However, if you wish to go more barebones, here is the older [Beat Saber Plugin Template](/uploads/modding/beat-saber-plugin-template.zip "Beat Saber Plugin Template") by RQ.

# Template setup
Install Instructions:
1. Open C:\Users\You\Documents\Visual Studio 2017\Templates\ProjectTemplates.
2. Drop in `beat-saber-plugin-template.zip`.  You do not need to extract the contents here, dropping the zipped file will work.

After you have place the zip file in the correct directory, open Visual Studio 2017 and create a new project.
You should see the Beat Saber Plugin Template in the Visual C# section.
Create a new project using the template.

![Modding Plugin Template](/uploads/modding/modding-plugin-template.png "Modding Plugin Template")

If you intend on making a mod to be published to BeatMods, you will have to rename the assembly to your mod. Using the default assembly name won't cut it!

To rename the assembly:
1. In the Solution Explorer panel, double click on Properties.

![Modding Plugin Prop Selected](/uploads/modding/modding-plugin-prop-selected.png "Modding Plugin Prop Selected")

2. Change the text in the textbox Assembly name.

![Modding Plugin Properties](/uploads/modding/modding-plugin-properties.png "Modding Plugin Properties")

# Changing copy directory

If you are using Kyle1413's BS Template, it comes with a built in post-build event that attempts to copy your built file to:

`C:\Program Files (x86)\Steam\steamapps\common\Beat Saber\Plugins`

If your Beat Saber install is located here, no worries. If not, we need to change this.

1. Under `Project`, click on `<Project Name> Properties...` at the very bottom of the dropdown.
2. In the menu that pops up, click `Build Events`
3. Replace the last directory in the Post-build event command line *(The directory should look like the one above)* with the directory to your Plugins folder.
4. Save and exit that menu.

# Check out the code

In the solution explorer, double click on `Plugin.cs` to open it up.
You should see something like this. It'll look different depending on the template, but should look similar.

![Plugin Cs Example](/uploads/modding/plugin-cs-example.png "Plugin Cs Example")

Note the red squiggly underlines. This is means Visual Studio can't find our references.

# Fixing references

To do this, right click on `References` in the Solution Explorer, and select `Add Reference...`

![Add Reference](/uploads/modding/add-a-ref.png "Add Reference")

This will open the Reference Manager window, and you can browse to find the DLL files that are missing.
Most of these files will be located within `\<Beat Saber directory>\Beat Saber_Data\Managed`

(For IPA, use `IllusionInjector` and `IllusionPlugin`. For BSIPA, `IPA.Loader` is all that you need)

![Finding References](/uploads/modding/dnspy-assembly.png "Finding References")

![References Windows](/uploads/modding-example/plugin-addreferences.png "References Windows")

Some Libraries are located in the Plugins folder as well. Check there for any libraries you forgot to add.

The most popular libraries located in the Plugins folder include:
* Async Twitch
* Beat Saber Utils
* CustomUI

**Can't find your Beat Saber directory?** See [install folder](/faq/install-folder).

# Compiling the plugin
If you have fixed all of the references in the project, on the top menu bar press `Build -> Build Solution` or <kbd>CTRL + SHIFT + B</kbd>

Your compiled DLL should appear in the `\Bin\Debug` folder of your project, or copied over to your Plugins folder, depending on what template you use.

You can then copy this DLL into the `Plugins` folder within your Beat Saber directory.

# Moving forward
Check out the [example mod](example-mod) tutorial.