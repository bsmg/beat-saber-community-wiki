<!-- TITLE: The Example Mod Tutorial -->
<!-- SUBTITLE: Learn how to make a Beat Saber Mod! -->


# Planning
This is just a checklist of things I need to cover *(Will be removed later*)

Plugin in question: Counter of the average accuracy of slices *(The extra 10 points you can get for the total of 110)* that appears at the end of a song.

* ~~Using dnSpy to find stuff I need~~
  * ~~*If required*, grab and use `ReflectionUtil`.~~
  * ~~From the looks of things, I can use `ScoreControllers` `ScoreWithoutMultiplier` void to grab the accuracy using the `cutDistanceScore` out integer.~~
* An easy Config class that utilizes `ModPrefs`
  * Recommend separating into a new file for multiple config options
* Simple on/off toggle for the mod using `CustomUI`.
* ~~Emphasize usage of `IEnumerator` when handling Unity objects~~
  * ~~Depending on the above, maybe show off `WaitUntil()` instead of using a loop and a half *(`while (true)` and repeat until something is found)*~~
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

This mod will also have the help of some of the commonly used Libraries that are available on [ModSaber.](https://www.modsaber.org/).

We will be using the following in our tutorial:

* **dnSpy** to look at Beat Saber's code for what we need.
* **Beat Saber Util** to store and retrieve some configuration options. *(You can also use **ModPrefs** if you wish)*
* **CustomUI** to create a simple Modifiers page that will change these options in-game.

# I. The Basics
## Config.cs
Before we do anything else, lets start the tutorial by creating a new `Config.cs` file. This will house our variables that we will, later in the tutorial, use to save and read from a file.

![Config](/uploads/modding-example-v-2/02-configcreate.png "Config")

We should now have an empty class. Let's create variables, and give them some temporary values for now. Later in the tutorial, we will replace these with `get` and `set` accessors that'll tie in to ModPrefs.

Just as a side note, each variable will have the `public static` keywords added on to them.

![Variables](/uploads/modding-example-v-2/03-variables.png "Variables")

| Variable | Description |
|-|-|
|**enabled**|Controls whether or not our plugin will be active at the end of the song.|
|**displayBoth**|Toggles the average bonus score for both sabers.|
|**displaySeparate**|Toggles the average bonus score for each left/right saber separately.|
|**decimalPrecision**|What decimal place our average will round to.|

With our new class in place, we can easily access different options in our plugin with the Config class, without having to create a new instance of it.

## AccuracyLists.cs
>If you are having trouble inheriting `MonoBehaviour`, add `using UnityEngine;` to the top of your file.
{.is-warning}

You thought you were done with creating files? Nope! We will create one more before we actually edit `Plugin.cs`. This new file, which I will call `AccuracyLists.cs`, will house the lists of bonus accuracy points for both the left and the right sabers.

Because we will be using this during a song, it'll inherit `MonoBehaviour`.

![04 Accuracylists](/uploads/modding-example-v-2/04-accuracylists.png "04 Accuracylists")

## What's Next?
So now we need to find a way to get the slice accuracy bonus from each note cut. We're going to have to find some sort of function or event that can help us not only by grabbing the score, but separating the points we obtain from the slice accuracy bonus.

Thankfully, there is a tool used heavily by Modders that will allow us to obtain just this.

## dnSpy To the Rescue!
>If you do not have dnSpy installed, please refer to our [brand spanking new Extras page to find out how to install dnSpy and decompile Beat Saber's code.](https://wiki.assistant.moe/modding/extras#dn-spy)
{.is-warning}

*dnSpy* is a useful program that allows us to view the decompiled code for Beat Saber! We can easily find what functions and variables to use when it's actually readable!

Let's select our opened `Assembly-CSharp` file and open the dropdowns until we reach an empty namespace (`{}`), then drop down that namespace.

![dnSpy Example](/uploads/modding/dnspy-example.png "dnSpy Example")

Hmm. That's a *lot* of classes. We're going to have to narrow down what we're looking for. Because what we are looking for is related to score, and plus it would have to be when a note is cut, my first guess will be to look in the `ScoreController` class. It'll be a little ways down, but it should have what we need.

![05 Dnspyscorecontroller](/uploads/modding-example-v-2/05-dnspyscorecontroller.png "05 Dnspyscorecontroller")

Here we are. We can see here we already have our way of grabbing note data whenever a note was cut; this will be useful for later. Let's scroll down a little bit into this large class.

![06 Scorewithoutmultiplier](/uploads/modding-example-v-2/06-scorewithoutmultiplier.png "06 Scorewithoutmultiplier")

*Ahhh*. Jackpot. This appears to be all of what we need to set up our `AccuracyLists` file. Let's head back to Visual Studio.

## Actually Writing Code
With our newfound knowledge from dnSpy, we can now actually start writing some code. Let's create two `List<int>`s that'll house the `cutDistanceScore`s from the `ScoreController`. Let's also create our `ScoreController` reference that will be used.

Unlike the previous mod example, we will not be creating a counter, so no `TextMeshPro`s will be used here.

Let's create an `Awake` void. We'll grab our ScoreController in the next section.

![07 Writingcode](/uploads/modding-example-v-2/07-writingcode.png "07 Writingcode")

## Grabbing the ScoreController
>If you are having issues with `IEnumerator`, append `using System.Collections` to the top of your file.
{.is-warning}

To obtain our ScoreController, let's create an `IEnumerator` called `GrabRequired()`. Unlike the previous mod tutorial, we will not use a `while(true)` loop and keep looping through until we find our ScoreController.

Let me introduce you all to `WaitUntil(predicate)`! It stops a Coroutine until the bool `predicate` is `true`. In our case, we'll see if Resources can load a ScoreController, and pass that as a lambda expression with no extra variables to pass into.

Since it will halt until our `ScoreController` is found, we do not need to worry about our variable being `null`. We can safely assign it via Resources, and move on to a brand new `Init()` void. We will then start our coroutine in the `Awake()` function.

![08 Grabbingscorecontroller](/uploads/modding-example-v-2/08-grabbingscorecontroller.png "08 Grabbingscorecontroller")

### Regarding Tasks and Threading
Through my own experience, and from the advice of other Modders, it is unwise to grab, assign, or modify Unity objects *(Hint: Almost all of them inherit `MonoBehaviour`)* inside a separate thread. Attempting to do so will, however not consistently, crash the game. It is much better to use `IEnumerators` and Coroutines for handling Unity objects, and use Tasks and separate threads for those which do not.