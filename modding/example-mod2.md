<!-- TITLE: The Example Mod Tutorial -->
<!-- SUBTITLE: Learn how to make a Beat Saber Mod! -->


# Planning
This is just a checklist of things I need to cover *(Will be removed later*)

Plugin in question: Counter of the average accuracy of slices *(The extra 10 points you can get for the total of 110)* that appears at the end of a song.

* Using dnSpy to find stuff I need
  * *If required*, grab and use `ReflectionUtil`.
  * From the looks of things, I can use `ScoreControllers` `ScoreWithoutMultiplier` void to grab the accuracy using the `cutDistanceScore` out integer.
* An easy Config class that utilizes `ModPrefs`
  * Recommend separating into a new file for multiple config options
* Simple on/off toggle for the mod using `CustomUI`.
* Emphasize usage of `IEnumerator` when handling Unity objects
  * Depending on the above, maybe show off `WaitUntil()` instead of using a loop and a half *(`while (true)` and repeat until something is found)*
* A lot more images for code
* Don't code badly :mad:
# Prelude
>If at any point you feel overwhelmed, it probably means you do not have enough experience. In that case, consider watching some Unity and C# tutorials to get familar with Unity and how it works.
{.is-danger}

Before we begin, we'll assume you've followed the [template setup guide](https://wiki.assistant.moe/modding/intro) to create the project and add the necessary references.

![Beginnings](/uploads/modding-example-v-2/00-beginnings.png "Beginnings")

## Our Plugin

The plugin we will be making will keep track of the average bonus accuracy points you can get in a swing.

To help explain that, here's a screenshot from the game, with the help of the [First Person Flying Camera](https://wiki.assistant.moe/modding#launch-args).

![Accuracy Explanation](/uploads/modding-example-v-2/01-accuracyexplanation.png "Accuracy Explanation")

We will be keeping track of the last 10 points you can get for the maximum of 110.

This mod will also have the help of some of the commonly used Libraries that are available on Mod Saber.

We will be using the following in our tutorial:

* **dnSpy** to look at Beat Saber's code for what we need.
* **ModPrefs** to store and retrieve some configuration options.
* **CustomUI** to create a simple Modifiers page that will change these options in-game.

# I. The Basics
## Config.cs
Before we do anything else, lets start the tutorial by creating a new file. This will house our variables that we will, later in the tutorial, use ModPrefs to save and read from a file.

![Config](/uploads/modding-example-v-2/02-configcreate.png "Config")

We should now have an empty class. Let's create variables, and give them some temporary values for now.

Just as a side note, each variable will have the `public static` keywords added on to them.

| Variable | Description |
|-|-|
|**enabled**|Controls whether or not our plugin will be active at the end of the song.|
|**displayBoth**|Toggles the average bonus score for both sabers.|
|**displaySeparate**|Toggles the average bonus score for each left/right saber separately.|
|**decimalPrecision**|What decimal place our average will round to.|


