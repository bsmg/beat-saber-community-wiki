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

We will be using Kyle1413's template for thise tutorial, [which you can grab here.](https://github.com/Kylemc1413/BS-Plugin-Template/releases/download/0.0.1/BS.Plugin.Template.zip)

![00 Kyletemplate](/uploads/modding-example-v-2/00-kyletemplate.png "00 Kyletemplate")

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
## Variables
Let's start the tutorial by creating two `List<int>` variables, marking them as `public static`. These will store our Accuracy bonus points and then read off of them.

![01 Pluginvariables](/uploads/modding-example-v-2/01-pluginvariables.png "01 Pluginvariables")

## Config.cs
Before we do anything else, lets create a new `Config.cs` file. This will house our variables that we will, later in the tutorial, use to save and read from a file.

![Config](/uploads/modding-example-v-2/02-configcreate.png "Config")

We should now have an empty class. Let's create variables, and give them some temporary values for now. Later in the tutorial, we will replace these with `get` and `set` accessors that'll tie in to ModPrefs.

Just as a side note, each variable will have the `public static` keywords added on to them.

![03 Replacement](/uploads/modding-example-v-2/03-replacement.png "03 Replacement")

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
With our newfound knowledge from dnSpy, we can now actually start writing some code. Let's create our `ScoreController` reference that will be used to plug a method into `OnNoteCut`.

Unlike the previous mod example, we will not be creating a counter, so no `TextMeshPro`s will be used here.

Let's create an `Awake` void. We'll clear the lists we created in `Plugin.cs` here, so they don't conflict with anything we've did in a previous level.

We'll grab our ScoreController in the next section.

![07 Replacementlol](/uploads/modding-example-v-2/07-replacementlol.png "07 Replacementlol")

## Grabbing the ScoreController
>If you are having issues with `IEnumerator`, append `using System.Collections` to the top of your file.
{.is-warning}

To obtain our ScoreController, let's create an `IEnumerator` called `GrabRequired()`. Unlike the previous mod tutorial, we will not use a `while(true)` loop and keep looping through until we find our ScoreController.

Let me introduce you all to `WaitUntil(predicate)`! It stops a Coroutine until the bool `predicate` is `true`. In our case, we'll see if Resources can load a ScoreController, and pass that as a lambda expression with no extra variables to pass into.

Since it will halt until our `ScoreController` is found, we do not need to worry about our variable being `null`. We can safely assign it via Resources, and move on to a brand new `Init()` void. We will then start our coroutine in the `Awake()` function.

![08 Replacement](/uploads/modding-example-v-2/08-replacement.png "08 Replacement")

### Regarding Tasks and Threading
Through my own experience, and from the advice of other Modders, it is unwise to grab, assign, or modify Unity objects *(Hint: Almost all of them inherit `MonoBehaviour`)* inside a separate thread. Attempting to do so will, however not consistently, crash the game. It is much better to use `IEnumerators` and Coroutines for handling Unity objects, and use Tasks and separate threads for those which do not.

## Note Cut Events
With our ScoreController variable in hand, we can add to the `noteWasCutEvent` and pass in a new void function that has the three required parameters. Here, we can use the static `ScoreController.ScoreWithoutMultiplier()` variable to grab our cut distance score. Because it outputs two unneeded variables, we can assign them to two filler variables. Because we are not using an after cut swing rating, we can simply plug in `null` for that.

Now we need to filter out bombs and bad cuts, and then add to the according `List<int>` we created in `Plugin.cs` based on the note type.

![09 Replacement](/uploads/modding-example-v-2/09-replacement.png "09 Replacement")

## Transitions To Menu
To access the Results screen *(Or in some cases, the Failed screen)*, we need to find when the game changes scenes from `Menu` to `GameCore`. Thankfully, the plugin template we are using already has detection for entering the `Menu` scene. Let's add on to that by checking to see if the game transitioned from `GameCore`.

We can also implement our `Config.cs` class here, by checking to see if its `enabled` variable is false, and then return the function.

While we're here, we can also create the GameObject that will hold our `AccuracyLists` class, since thankfully the plugin template also checks to see if we're entering `GameCore`.

![12 Replacement](/uploads/modding-example-v-2/12-replacement.png "12 Replacement")

## ResultsViewer.cs
Let's create a new class called `ResultsViewer` and have it extend from `MonoBehaviour`. This class will display the results of our accuracy points when we exit from a level. We will be using a maximum of 3 TextMeshPros to help us display our data.

Let's also createa  `List<GameObject>` variable that will hold each `GameObject` we create for viewing results, so we can mass delete them later.

We should create a helper class that creates these TextMeshPros for us, so we don't have to use repeated code. It will take in a `Vector3` for positioning, a  `List<int>` for our list data, and a `string` for a label.

![13 Replacement](/uploads/modding-example-v-2/13-replacement.png "13 Replacement")

## Creating a TextMeshPro
>If you are having trouble using `TextMeshPro`, add `using TMPro;` at the top of your file, or add it as a reference if that doesn't work.
{.is-warning}

In this function, let's create a new `GameObject` variable and a new `TextMeshPro` variable, and attach the TextMeshPro to our GameObject. We can set the `text` value using a sneaky trick. Using a `List<int>`s built in function, we can grab the average from the list, and pass it to `ToString()`. We can also pass in a formatter into `ToString()` and format it to 2 decimal places. Let's set the `fontSize` to3 and the alignment to `TextAlignmentOptions.Center`. Finally, let's set the position of the TextMeshPro via its `rectTransform`, and set it to our `position` parameter.

![14 Replacement](/uploads/modding-example-v-2/14-replacement.png "14 Replacement")

But wait! Let's add a label using our `label` parameter. We will mainly be copy and pasting our previous code, but there will be some differences.

Let's create a new GameObject that will hold our label. The `text` will be the `label` parameter, and the `fontSize` will be 2. Let's parent this TextMeshPro to the `viewer` TextMeshPro. We will finally set its `localPosition` a little bit above the actual `viewer`.

Let's finally add the two GameObjects we created to the `List<GameObject>` we created a little while back.

![15 Replacement](/uploads/modding-example-v-2/15-replacement.png "15 Replacement")

## Grabbing ResultsViewController
>If you are having trouble using `IEnumerator`, add `using System.Collections;` to the top of your file.
{.is-warning}

We want our results to appear when the user fails or succeeds in a level, and not when they exit to the main menu. This would mean some sort of results screen will have to be present. Just like that, a `ResultsViewController` exists in Beat Saber that displays information on whether or not you have succeeded and failed, along with the map information. We can easily spawn in our own results when this `ResultsViewController` is spawned, and then delete our results when the user presses `OK` or `Restart`.

Let's grab this `ResultsViewController` using the same way we grabbed our `ScoreController` from earlier. We'll make an `IEnumerator` and include a `WaitUntil` statement which will halt our function until it finds a `ResultsViewController`. It's OK if the User exits to the main menu, however, since our code will stop forever at this line since it can never find a `ResultsViewController`. Once we've found it, we can simply assign it to a private `ResultsViewController` variable. We will have one more `WaitUntil` statement, which will halt until our `ResultsViewController` variable is active. We can then move on to an `Init` void.

![16 Replacement](/uploads/modding-example-v-2/16-replacement.png "16 Replacement")

Our `Init` function is where we will finally create our results. Let's first check to see if our `ResultsViewController` is active. In case our `IEnumerator` from before found one while it wasn't supposed to, we can easily check if it's actually enabled.

Remember the `Config.cs` class we made way back towards the beginning of the tutorial? We'll be using it here. We'll create two seperate conditions: One where `Config.displaySeparate` is on, and one where `Config.displayBoth` is on.

If `Config.displaySeparate` is on, we'll call our `CreateViewer` helper function twice: One for `Plugin.lSaberCut`, and one for `Plugin.rSaberCut`.

If `Config.displayBoth` is on, we'll create a new `List<int>` based off of any one of our lists, and then use the `AddRange` function to add in the other list, and then pass that in to one singular `CreateViewer` function.

Instead of having you figure out where to put these things, I've went ahead and done the work for you.

![17 Resultsinit](/uploads/modding-example-v-2/17-resultsinit.png "17 Resultsinit")
## One Final Thing

Let's attach `ResultsViewController`'s two events into one void. The `continueButtonPressedEvent` and `restartButtonPressedEvent` will be fired when the respective buttons have been pressed. Let's add one `Continue` void to each of these. In our `Continue` void, we can simply loop through each GameObject in our `List<GameObject>` and call `Destroy()` on them.

![18 Resultsevents](/uploads/modding-example-v-2/18-resultsevents.png "18 Resultsevents")
