## Group 2 - Game Package


Welcome to the Group 2 final project page!

Our final project is a game suite featuring profiles, score tracking, and easy to modify package to add and remove games dynamically.

### Table of Contents

- [Getting Started](#getting-started)
- [Setting Up](#setting-up)
  * [installgames.py](#installgamespy)
  * [__init__.py](#__init__py)
- [Future improvements](#future-improvements)


### Getting Started

1. Download game_package.zip and unzip to desired directory
2. Run game_bundle.py to start program
   - User may include profile name on command line to load or create profile
   - If profile name exists, the profile will load. Leaving the CLA blank will prompt user for username
3. After profile handling, the main menu will appear. Type the name of the game to begin playing.
4. After exiting the game, the main menu will appear again to play a new game.
   - Scores will be saved on game exit.
5. Type 'exit' at main menu to quit the program.


### Setting Up A New Game

A few steps are needed to add a new game to the package

#### installgames.py

1\. First we need to add the name of the game to populate the list of games in the main menu.

```markdown
#Provides list of games in package to populate main menu
def gamelist():

#Add name of game as it should appear in the menu
	return(['Game1', 'Game2', 'Game3'])
gamelist.__doc__ = """List of available games"""
```


2\. A function to execute the game will need to be created in installgames.py.
The naming convention is the name of the game followed by 'exec'.

```markdown
#Executes your game
def nameofgameexec():

	return nameofgame.main()
nameofgame.__doc__ = """Executes your game"""
```

The game's main function will be called in the game_bundle.py program to execute the game code.

3\. Add a test 

```markdown
if __name__ == '__main__':
    assert nameofgameexec == True
```

#### __init__.py

4\. In the \_\_init\_\_.py file, located in the \games folder, the name of the .py file for the new game will need to be added to the \_\_all\_\_ list. This allows for the games to be imported as modules all at once in the top-level programs.

```markdown

__all__ = ["game1", "game2", "game3"]

```

### Future improvements

- We would like to be able to allow users to just drop a new game into the games folder, and have everything update dynamically rather than requiring these steps.

- We would like to implement contexual scoring rather than requiring games to follow a certain structure.

- Some of the included games need bug fixes.

- We would like to handle multiple profiles for multiplayer games, such as pong.py.

- The scores are currently only being tracked as a history rather than updating inside the file.

- Create more interactive and detailed main menu.

- Implement a GUI.


Authored by Chris Davis
