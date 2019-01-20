<!-- TITLE: Modding Intro -->
<!-- SUBTITLE: Learn how to setup the plugin template -->

# Intro
Beat Saber is made in Unity 2018 using C# with .NET framework 4.6.
For convenience, RQ has created a plugin template for Visual Studio. This guide will show you how to setup that template.

Download the latest version of [Visual Studio Community.](https://visualstudio.microsoft.com/)

There are multiple templates that you can choose to install.

The new [BS Plugin Template](https://github.com/Kylemc1413/BS-Plugin-Template/releases/download/0.0.1/BS.Plugin.Template.zip) by Kyle1413 includes more options to guide you, as well as a basic use case of CustomUI. We will be using this for the Mod Tutorial.

However, if you wish to go more barebones, here is the older [Beat Saber Plugin Template](/uploads/modding/beat-saber-plugin-template.zip "Beat Saber Plugin Template") by RQ.

# Template setup
Install Instructions:
1. Open C:\Users\\<Username\>\Documents\Visual Studio 2017\Templates\ProjectTemplates.
2. Drop in `beat-saber-plugin-template.zip`.  You do not need to extract the contents here, dropping the zipped file will work.

After you have place the zip file in the correct directory, open Visual Studio 2017 and create a new project.
You should see the Beat Saber Plugin Template in the Visual C# section.
Create a new project using the template.
![Modding Plugin Template](/uploads/modding/modding-plugin-template.png "Modding Plugin Template")

The default assembly name is `UnnamedAssembly` (Or `NewPlugin` depending on the template you downloaded).
To rename the assembly:
1. In the Solution Explorer panel, double click on Properties.

![Modding Plugin Prop Selected](/uploads/modding/modding-plugin-prop-selected.png "Modding Plugin Prop Selected")

2. Change the text in the textbox Assembly name.

![Modding Plugin Properties](/uploads/modding/modding-plugin-properties.png "Modding Plugin Properties")

# Check out the code

In the solution explorer, double click on `Plugin.cs` to open it up.
You should see something like this.

![Plugin Cs Example](/uploads/modding/plugin-cs-example.png "Plugin Cs Example")

Note the red squiggly underlines. This is means Visual Studio can't find our references.

# Fixing references

To do this, right click on `References` in the Solution Explorer, and select `Add Reference...`

![Add Reference](/uploads/modding/add-a-ref.png "Add Reference")

This will open the Reference Manager window, and you can browse to find the DLL files that are missing.
Most of these files will be located within `\<Beat Saber directory>\Beat Saber_Data\Managed`

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

Your compiled DLL should appear in the `\Bin\Debug` folder of your project.

You can then copy this DLL into the `Plugins` folder within your Beat Saber directory.

# Moving forward
Check out the [example mod](example-mod) tutorial.