## CustomEvents
[*GitHub*](https://github.com/artemiswkearney/SimpleCustomEvents)

A library for Beat Saber that lets other mods define and register for new beatmap event types, and lets beatmap creators use those events in songs. This could be used to create anything from new types of notes to changes to the environment to entirely new gameplay mechanics, as new mods are developed that take advantage of this library's features.

CustomEvents implements a specification defined by the [CustomJSONData](/customjsondata.html) library. The current version (referred to as "SimpleCustomEvents" on GitHub) exists to make custom events useable now; future plans exist to develop more advanced features to give modders more control over events and how they receive them, while maintaining backwards compatibility with the current interface.

Features:
- The design of the `CustomEventCallbackController` class draws heavy inspiration from Beat Saber's internal `BeatmapObjectCallbackController`, so the interface should be familiar to plugin developers who have worked with the game's existing beatmap events.
	- Using this interface, event callbacks can be registered with callahead times, meaning your code can run some amount of time before the point where the event occurs in the song. This is useful for things like spawning notes ahead of time, and for anything else that needs preparation before the moment where it intuitively "occurs" in the song.
	- The plugin also provides two native C# events: one that fires when the `BeatmapObjectCallbackController` is ready, and one that fires whenever a custom event occurs. These exist to improve usability and reduce the need for costly Unity engine methods such as `GameObject.FindObjectOfType`.
