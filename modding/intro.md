<!-- TITLE: Modding Intro -->
<!-- SUBTITLE: Learn how to setup the plugin template -->

# Intro
Download the latest version of [Visual Studio Community.](https://visualstudio.microsoft.com/)
Download the [Beat Saber Plugin Template](/uploads/modding/beat-saber-plugin-template.zip "Beat Saber Plugin Template") by RQ.
Download [dnSpy](https://github.com/0xd4d/dnSpy)
# Template setup
Install Instructions:
1. Open C:\Users\\<Username\>\Documents\Visual Studio 2017\Templates\ProjectTemplates.
2. Drop in `beat-saber-plugin-template.zip`

The default assembly name is `Unnamed Assembly`
To rename the assembly:
1. In the Solution Explorer panel, double click on Properties.
2. Change the text in the textbox Assembly name.

# Fixing references
TODO
# Compiling the plugin
If you have fixed all of the references in the project, on the top menu bar press `Build -> Build Solution`
Or <kbd>CTLR + SHIFT + B</kbd>

Your compiled DLL should appear in the `BIN -> Debug` folder of your project.

You can then copy this DLL into the `Plugins` folder within your Beat Saber directory.
# Moving forward
Check out the [example mod](example-mod) tutorial.