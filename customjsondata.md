## CustomJSONData
[*GitHub*](https://github.com/artemiswkearney/CustomJSONData)

A library for Beat Saber mods that lets other mods access arbitrary data from beatmap files. This allows modders to make entirely new features available to beatmap creators.

Previous mods that extended the feature set available to beatmap creators, such as [Chroma](https://github.com/BinaryElement/Chroma/wiki) and [MappingExtensions](https://github.com/Kylemc1413/MappingExtensions), relied on magic numbers with special meanings in existing beatmap syntax. While this approach was functional, it imposed severe limitations on plugin developers and made the process of using these features for beatmap creators somewhat opaque.    
CustomJSONData seeks to improve upon this paradigm by allowing beatmaps to contain arbitrary JSON objects, and thus effectively arbitrary data.

Features:
- Custom data can be specified on any and all objects in a beatmap file; notes, obstacles, bombs, and lighting events can all hold custom data, and custom data can also be specified for a difficulty of a beatmap or for a song as a whole.

- For plugin developers, accessing the data couldn't be easier; CustomJSONData provides custom data as a new property on existing game classes representing beatmap objects, and members of the custom data JSON object can be accessed identically to members of a C# object via use of the `dynamic` language feature.

- The static utility class `CustomJSONData.Trees` provides even more convenience for working with custom data objects.
	- `at`, `get`, and `get`'s specialized form `getNullable` can be used for defensive programming against ill-formed data
	- Inspired by monadic programming concepts, `tryNull` can be used to write code that may fail without the effort of explicit error handling
	- `mergeTrees` and `map` turn the "Tree" type of custom data objects into a proper data structure, with conceptual similarities both to the JSON format the data was originally specified in and to Lisp-style s-expressions

- Also supports loading data for entirely custom beatmap events, which could be used to implement anything from new note types to new environment/lighting events to entirely new gameplay mechanics.
	- Subscription to/emitting of these events is handled by [another plugin](/customevents.html), but the file format is specified by CustomJSONData, and CustomJSONData loads the events from the beatmap file.

- All these features and more are described in further technical detail on the project's [GitHub wiki](https://github.com/artemiswkearney/CustomJSONData/wiki).
