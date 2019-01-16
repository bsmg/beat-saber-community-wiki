<!-- TITLE: The Example Mod Tutorial -->
<!-- SUBTITLE: Learn how to make a Beat Saber Mod! -->


# Planning
This is just a checklist of things I need to cover *(Will be removed later*)

Plugin in question: Counter of the average accuracy of slices *(The extra 10 points you can get for the total of 110)* that appears at the end of a song.

* Using dnSpy to find stuff I need
  * *If required*, grab and use `ReflectionUtil`.
  * From the looks of things, I can use `ScoreControllers` `ScoreWithoutMultiplier` void to grab the accuracy using the `cutDistanceScore` out integer.
* An easy Config class that utilizes `ModPrefs`
* Simple on/off toggle for the mod using `CustomUI`.
* Emphasize usage of `IEnumerator` when handling Unity objects
  * Depending on the above, maybe show off `WaitUntil()` instead of using a loop and a half *(`while (true)` and repeat until something is found)*
# Before We Begin