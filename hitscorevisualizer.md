## HitScoreVisualizer    
[*GitHub*](https://github.com/artemiswkearney/HitScoreVisualizer)

A mod for Beat Saber that adds more detailed information to the score popups that appear when the player hits a note. HitScoreVisualizer is used by many top-level Beat Saber players to get real-time feedback on their play and how they can improve, and has become so popular that further development has been commissioned by the userbase.

Features:
- The base game displays only a single number showing the total score earned from hitting a note. HitScoreVisualizer allows you to display a **judgment** in addition to or in place of this number, classifying the hit by how many points it earned.

- Judgments are fully user-customizable. In the plugin's configuration file, users can specify any number of judgments, the score thresholds required to earn them, the colors to display them in, and the text to display when each judgment is earned.

- Users can configure whether to display only the judgment message, only the score (colored based on judgment), or both. If displaying both, users can choose whether to display the message or the score on top.

- To provide further customization and flexibility, the `format` display mode can be enabled, which allows judgments to include format specifiers (similar in concept to those used by `printf` in C-family programming languages). Format specifiers allow the insertion of information such as the score earned for the hit; the score as a percentage of the total possible score; and the score earned in each subcategory of the game's scoring algorithm.

- In addition, format specifiers are provided that allow *segment judgments* to be inserted into the main judgment message. As with judgments, any number of segment judgments may be specified in the configuration file.
	- Beat Saber determines scoring for each note by summing values earned in three categories: the angle covered by the swing before the saber makes contact with the block, the angle covered by the swing's follow-through after the saber makes contact with the block; and how close the plane of the cut comes to passing through the block's center.
	- Segment judgments are earned based on score in one of these subcategories, rather than total score.
	- Segment judgments can be used to provide, in a form that's easier to quickly read than a number, an indication of where you're doing well with your swings and what can be changed to improve your scoring.

- The plugin's default configuration is periodically updated to optimize the experience and to demonstrate new features. These updates will overwrite the automatically generated default configuration file. However, if the user has modified their configuration, it will be left unchanged in functionality. When updates change plugin functionality or configuration format, effort is put in to ensure behavior remains the same for existing users with customized configurations.

- A configuration option is available that positions judgment text in a fixed location rather than having judgments appear as popups floating below the note track. When this option is enabled, only the most recent judgment earned will be visible. (This feature was commissioned by the community.)
