## Portfolio

### Beat Saber modding
I make mods for the hit VR rhythm game Beat Saber.
- [HitScoreVisualizer](https://github.com/artemiswkearney/HitScoreVisualizer)
	- Enhances the score popups that appear when a note is hit, to contain information on accuracy and how the game scored the hit.
	- Supports custom format specifiers in a configuration file, along with many other customizable features.
	- Used by most high-level Beat Saber players.
- [CustomMenuText](https://github.com/artemiswkearney/CustomMenuText)
	- Changes the logo/title in the game's main menu to user-provided text, randomly chosen from the configuration file.
	- Also supports loading arbitrary fonts into the game to display the text using.
- [CustomJSONData](https://github.com/artemiswkearney/CustomJSONData)
	- Allows beatmap creators to embed arbitrary data in beatmaps, and allows plugin developers to access that data with a convenient interface. Creates limitless possibilities for extending the game.
	- Uses C#'s `dynamic` feature to provide native-feeling syntax for accessing data loaded from JSON files.
- [CustomEvents](https://github.com/artemiswkearney/SimpleCustomEvents)
	- Implementing a specification from CustomJSONData, allows mappers to trigger arbitrary custom events handled by plugins. 
	- Uses an approach inspired by Beat Saber's own algorithms to broadcast events to other plugins in real-time as the player plays supported songs.
- More to come

### Other
- My [Discord bot](https://github.com/artemiswkearney/artibot)
	- A Discord bot for household task automation (e.g. grocery list management)
	- Modular design to make adding new features quick and easy
	- Includes a mini-library called Reactor that handles all the work of building UI based on message reactions
