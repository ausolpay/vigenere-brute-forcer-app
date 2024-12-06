# vigenere-brute-forcer-app
Built for 9 o'clock Felcycle 'Find Ratts' Challenge - Add more words to the extra-words js file and ill commit changes
README: Vigenère Cipher Brute Forcer v1.0
________________________________________
Overview
The Vigenère Cipher Brute Forcer is a web-based application that assists with solving encrypted messages using the Vigenère cipher. This tool provides options to brute force potential decryption keys, manually solve ciphers, and analyze decrypted outputs for common patterns, valid words, or multi-word results.
This is version 1, a work-in-progress app developed over three days, aimed at assisting with the Felcycle Puzzle and other decryption tasks.
________________________________________
Features
1.	Brute Force Decryption:
o	Attempts to decrypt the cipher using all possible keys based on user-defined parameters like key length and filtering options.
o	Includes optional features to:
	Add a "Zeroth" row in the Vigenère table.
	Remove specific letters (D and R) from the alphabet.
	Filter results based on repeated letters, common words, or an extended word list.
2.	Manual Solve:
o	Allows users to input a cipher and a manual key to directly decrypt a message.
3.	Word List Integration:
o	Fetches and combines two lists:
	Common words from an external API.
	Extra words from a customizable local word list (e.g., Felcycle-related terms).
o	Enables filtering results using the combined word list.
4.	Anagram Generator:
o	Processes decrypted results to find valid anagrams based on the combined word list.
o	Supports both single and multi-word anagram generation.
5.	Progress Tracking:
o	Displays a real-time progress bar and estimated time remaining during brute force and anagram generation.
o	Provides interactive feedback such as "Just getting started," "Over halfway there," and "Almost done!"
6.	Output Sections:
o	Displays:
	Decrypted results.
	Filtered keys.
	Filtered decrypted results.
	Results containing 4+ words or keys.
	Multi-word results.
	Full word results (8-character keys).
	Generated anagrams.
7.	Dynamic Reset and Pause/Resume:
o	Includes a reset button to clear all inputs and outputs.
o	Brute force can be paused and resumed as needed.
________________________________________
How to Use
1.	Launch the App:
o	Open index.html in any modern browser.
2.	Input Parameters:
o	Enter the encrypted message (cipher word) in the Cipher Word field.
o	Optionally, provide a partial key to narrow down brute force attempts.
3.	Select Key Length:
o	Choose a key length (2-8 characters) for the brute force process.
4.	Apply Filters (optional):
o	Enable one or more filters to refine results:
	Add Zeroth: Includes an extra row in the Vigenère table starting with the full alphabet.
	Remove D and R: Excludes letters D and R from the alphabet.
	Only Keys with Repeated Letters: Filters keys that have repeated characters.
	Only Keys with Common Words: Filters keys that contain common dictionary words.
	Use Word List Keys Only: Uses the preloaded word list for potential keys.
	Only Results with Letters Repeated Twice: Filters decrypted results that repeat any letter exactly twice.
5.	Decrypt:
o	Manual Solve: Enter a key to decrypt directly.
o	Brute Force: Click the "Brute Force" button to initiate the decryption process.
6.	Track Progress:
o	Monitor the progress bar and estimated time remaining.
o	View decrypted results in real time as they are processed.
7.	Generate Anagrams:
o	After decryption, click Generate Anagrams to analyze decrypted results for valid anagrams.
8.	Reset:
o	Clear all inputs and outputs using the Reset button.
________________________________________
Word List Management
•	Custom Word List:
o	The extra-words.js file contains additional terms specific to your needs, such as Felcycle-related keywords.
o	Modify this file to add/remove words as needed.
o	The app combines these extra words with a common word list fetched from the Datamuse API.
________________________________________
Technical Notes
•	Vigenère Table:
o	The app dynamically creates the Vigenère table based on the selected filters (e.g., removing specific letters).
•	Performance Considerations:
o	Brute force and anagram generation can be resource-intensive for longer key lengths or large input data. Use filters to optimize performance.
o	Progress updates are throttled to prevent browser freezing.
________________________________________
Known Limitations (v1.0)
•	Performance:
o	Brute force decryption may slow down for key lengths >6 without filters.
•	API Dependency:
o	Requires an internet connection to fetch the common word list from the Datamuse API.
•	Interface:
o	Currently designed for desktop browsers. Mobile compatibility may require adjustments.
________________________________________
Planned Improvements
•	Enhance performance for long keys by parallelizing computations.
•	Add a mobile-friendly layout.
•	Improve anagram generation for large datasets.
•	Introduce save/load functionality for decrypted results.
________________________________________
File Structure
•	HTML: index.html - Main user interface.
•	JavaScript:
o	app.js - Core logic for brute force decryption, word list management, and anagram generation.
o	extra-words.js - Additional word list customization.
•	CSS: styles.css - Application styling.
________________________________________
This app is intended for personal use and is actively being improved. Contributions and feedback are welcome as we progress toward future versions.

