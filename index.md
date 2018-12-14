## Group 2 - Game Package


Welcome to the Group 2 final project page!

Our final project is a game suite featuring profiles, score tracking, and easy to modify package to add and remove games dynamically.

### Table of Contents

- [Getting Started](#getting-started)
- [Setting Up](#setting-up)
  * [installgames.py](#installgamespy)
  * [__init__.py](#__init__py)
  * [Future improvements](#future-improvements)
- [Launching the Program](#launching-the-program)

### Getting Started

Here we will talk about the package components



### Setting Up

Here we will talk about adding and removing games

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

#### Future improvements

We would like to be able to allow users to just drop a new game into the games folder, and have everything update dynamically rather than requiring these steps.




### Launching the Program

Here we will talk about how to load/create profiles and use the menu
