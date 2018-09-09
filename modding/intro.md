<!-- TITLE: Modding Intro -->
<!-- SUBTITLE: Learn how to setup the plugin template -->

# Intro
Beat Saber is made in Unity 2018 using C# with .NET framework 4.6.
For convenience, RQ has created a plugin template that for Visual studio. This guide will show you how to setup that template.

Download the latest version of [Visual Studio Community.](https://visualstudio.microsoft.com/)
Download the [Beat Saber Plugin Template](/uploads/modding/beat-saber-plugin-template.zip "Beat Saber Plugin Template") by RQ.
Download [dnSpy](https://github.com/0xd4d/dnSpy)
# Template setup
Install Instructions:
1. Open C:\Users\\<Username\>\Documents\Visual Studio 2017\Templates\ProjectTemplates.
2. Drop in `beat-saber-plugin-template.zip`

After you have place the zip file in the correct directory, open Visual Studio 2017 and create a new project.
You should see the Beat Saber Plugin Template in the Visual C# section.
Create a new project using the template.
![Modding Plugin Template](/uploads/modding/modding-plugin-template.png "Modding Plugin Template")

The default assembly name is `UnnamedAssembly`
To rename the assembly:
1. In the Solution Explorer panel, double click on Properties.
2. Change the text in the textbox Assembly name.


![Modding Plugin Properties](/uploads/modding/modding-plugin-properties.png "Modding Plugin Properties")

# Fixing references
TODO

# Compiling the plugin
If you have fixed all of the references in the project, on the top menu bar press `Build -> Build Solution`
Or <kbd>CTLR + SHIFT + B</kbd>

Your compiled DLL should appear in the `BIN -> Debug` folder of your project.

You can then copy this DLL into the `Plugins` folder within your Beat Saber directory.
# Moving forward
Check out the [example mod](example-mod) tutorial.