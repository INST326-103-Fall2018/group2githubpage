## Group 2 - Game Package


Welcome to the Group 2 final project page!

Our final project is a game suite featuring profiles, score tracking, and easy to modify package to add and remove games dynamically.


### Getting Started

Here we will talk about the package components



### Setting Up

Here we will talk about adding and removing games

#### installgames.py

1. First we need to add the name of the game to populate the list of games in the main menu.

```markdown
#Provides list of games in package to populate main menu
def gamelist():

#Add name of game as it should appear in the menu
	return(['Game1', 'Game2', 'Game3'])
gamelist.__doc__ = """List of available games"""
```


2. A function to execute the game will need to be created in installgames.py.
The naming convention is the name of the game followed by 'exec'.

```markdown
#Executes your game
def nameofgameexec():

	return nameofgame.main()
nameofgame.__doc__ = """Executes your game"""
```

The game's main function will be called in the game_bundle.py function to execute the game code.

3. Add a test 

```markdown
if __name__ == '__main__':
    assert nameofgameexec == True
```





























You can use the [editor on GitHub](https://github.com/INST326-103-Fall2018/inst326group2.github.io/edit/master/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/INST326-103-Fall2018/inst326group2.github.io/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
