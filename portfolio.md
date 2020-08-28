## Portfolio

## Freelance work
Currently ✅ accepting new contracts. Check my [GitHub profile](https://github.com/artemiswkearney) for my email address.  
My skills include:
- Web
	- Modern JS / Typescript
		- Advanced Typescript features (such as mapped types and conditional types)
	- React (including React Native)
	- Meteor
- Game Dev / Modding
	- Unity
	- C#
	- Decompilation / Reverse Engineering
- Other
	- Unit testing
	- A knack for UX design
	- Abstraction/library/domain-specific language creation
	- Functional programming (especially in Racket)

Past freelance projects:
- [YouTube Playlist Randomizer](https://artemiswkearney.github.io/youtube-playlist-randomizer/)
	- YouTube's built-in shuffle feature only shuffles the first 200 videos of long playlists.
	- This site shuffles any number of videos, and can shuffle together multiple playlists.

### Beat Saber modding
I make mods for the hit VR rhythm game Beat Saber.
- [HitScoreVisualizer](/hitscorevisualizer.html)
	- Enhances the score popups that appear when a note is hit, to contain information on accuracy and how the game scored the hit.
	- Supports custom format specifiers in a configuration file, along with many other customizable features.
	- Used by most high-level Beat Saber players.
- [CustomMenuText](/custommenutext.html)
	- Changes the logo/title in the game's main menu to user-provided text, randomly chosen from the configuration file.
	- Also supports loading arbitrary fonts into the game to display the text using.
- [CustomJSONData](/customjsondata.html)
	- Allows beatmap creators to embed arbitrary data in beatmaps, and allows plugin developers to access that data with a convenient interface. Creates limitless possibilities for extending the game.
	- Uses C#'s `dynamic` feature to provide native-feeling syntax for accessing data loaded from JSON files.
- [CustomEvents](/customevents.html)
	- Implementing a specification from CustomJSONData, allows mappers to trigger arbitrary custom events handled by plugins. 
	- Uses an approach inspired by Beat Saber's own algorithms to broadcast events to other plugins in real-time as the player plays supported songs.
- More to come

### Other
- My [Discord bot](https://github.com/artemiswkearney/artibot)
	- A Discord bot for household task automation (e.g. grocery list management)
	- Modular design to make adding new features quick and easy
	- Includes a mini-library called Reactor that handles all the work of building UI based on message reactions
