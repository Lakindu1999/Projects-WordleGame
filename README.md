# Wordle Game

## Introduction
The provided code introduces a Python/SQL implementation of the Wordle game. Wordle is a word-guessing game where the player attempts to guess a hidden five-letter word. The game provides a user-friendly interface, allowing players to interact with the program.

### Key Components:
1.Wordle data:
• Initializes necessary attributes such as the list of words, the target word, user information, daily mode status, and database connection.
• Manages the game's logic, including starting and stopping the game, checking if the player is still playing and choosing a word.
• Utilizes SQLite3 to store user and game information.

2.Loop ( function):
• The game involves a loop where the player attempts to guess the hidden word within a limited number of attempts (6 in this case).
• After each guess, the player receives feedback on the correctness of their guessed word.
• The game ends when the player either successfully guesses the word or exhausts the allowed attempts.

3.User Interaction:
• The player interacts with the game by entering their guesses during each iteration of the loop.
• If the player successfully guesses the word, a congratulatory message is displayed. • If the player fails to guess within the allowed attempts, a corresponding message is shown.

4.Database Interaction:
• The game logs user activity depending on the daily mode status.
• Information stored includes the user's name, game status (success or fail),word and the date of play.

Python offers an interactive implementation of the Wordle game, blending user engagement, game logic, and data storage. Players can enjoy the challenge of guessing the hidden word while the program maintains a record of user and game data for future reference


## Data
The data in this context refers to the user and game information managed by the Wordle game. This includes details such as usernames, game statuses (success or fail), Correct word and the dates of play. The data source is primarily the interactions between the user and the game during each play session. The workflow involves initializing the game, user inputs for guessing the word, and storing relevant information in a SQLite3 database.

### Workflow of the program
![Screenshot 2024-02-27 100008](https://github.com/Lakindu1999/Projects-WordleGame/assets/86758637/b0df9b2c-80ac-4561-bb1c-02987949d800)


# Database
The database used in this implementation is SQLite3, a lightweight relational database management system. Two tables, namely 'users' and 'games,' are employed to store different types of information. The 'users' table is used when daily_mode is True which includes columns for usernames, statuses, the last played date & word. The 'games' table is used when daily_mode is False which includes columns for usernames, game statuses, word and played dates.
![Screenshot 2024-02-27 100130](https://github.com/Lakindu1999/Projects-WordleGame/assets/86758637/8872d2cf-af53-4d5d-9302-ed59ef60a1d8)

### Users Database:
![image](https://github.com/Lakindu1999/Projects-WordleGame/assets/86758637/4b731430-6fab-411d-a8c3-97c7958078be)

### Games Database:
![image](https://github.com/Lakindu1999/Projects-WordleGame/assets/86758637/81fe1e45-0821-4727-bcf0-4c8b56c4a8ae)


# Implementation
The implementation involves several key features:
• Data Storage: SQLite3 is utilized to create and manage the database. Tables are defined with relevant columns to store user and game information.
• User and Game Logic: The Wordle game logic is implemented to handle user inputs, track game progress, and determine outcomes (success or fail).
• Database Interaction: The program interacts with the SQLite3 database to store and retrieve user and game information.

### When daily_mode = True :
2nd attempt =Output
![image](https://github.com/Lakindu1999/Projects-WordleGame/assets/86758637/71a33afd-cb5e-4d50-bcee-af8080de0910)

### When Correct word is Successfully guessed :
![image](https://github.com/Lakindu1999/Projects-WordleGame/assets/86758637/2ebe41a5-ba61-4fa9-9bd2-d6bd96426be1)

### When Correct word is failed to guessed :
![image](https://github.com/Lakindu1999/Projects-WordleGame/assets/86758637/982bce62-6ef2-4a8d-819c-b8021c8f1a0d)


# Decisions Made
• Table Structure: The decision to use two tables, 'users' and 'games,' facilitates a clear separation of daily_mode data is True or False, improving data organization.
• Database Choice: SQLite3 is chosen for its simplicity and suitability for this lightweight application.

# Software
• Code Components/Interface: The code includes managing game-related functionalities. The SQLite3 library is used for database interactions.
• Usability: The code provides a user-friendly interface for playing the Wordle game, prompting users for input and providing feedback on game outcomes
• Information Flow: Data flows between the game logic and the SQLite3 database, ensuring a seamless exchange of user and game information.

# Conclusion
The Wordle game implementation is effective in managing user interactions and tracking game statistics. However, a notable limitation is the restriction to capital letters for target words. This may impact user engagement by limiting word diversity. Despite this, the game showcases a robust structure with database functionality. Future improvements could focus on expanding the word pool to include various letter casings, enhancing the gaming experience. The limitation serves as an opportunity for growth, and future iterations could address this to cater to a broader audience.
