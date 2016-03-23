# [VS Code](https://code.visualstudio.com) Tips and Tricks

This is a collection of helpful tips and tricks for VS Code. 

# Basics

## Open command palette

Easy access to all commands available in VS Code. 

<kbd>cmd+shift+p</kbd>

![command palette](/media/command_p.png)

## Quick open

Quickly open files and run commands (see below). 

<kbd>cmd+p</kbd>

## Copy and paste commands into quick open

<kbd>cmd+p</kbd> then paste the command you want to run. This is especially
useful with the extension marketplace. 

![marketplace copy and paste](/media/mp_copy_paste.png)

## Status bar decorations

**Errors and Warnings**

Quickly jump to errors and warnings in the project. 

![status errors and warnings](/media/status_errors_warnings.png)

# Customizing

## Ignore files / folders

[See documentation for more details](http://code.visualstudio.com/docs/customization/userandworkspace#_default-settings). Edit `settings.json` by adding the following:

```json
"files.exclude": {
		"somefolder/": true, 
		"somefile": true
}
```

## Preview themes

![Preview themes](/media/preview_themes.gif)

## Customize editor

Open `settings.json` with <kbd>cmd+,</kbd>

*Change the font size*

```json
"editor.fontSize": 18
```

*Change the size of tab characters*

```json
"editor.tabSize": 4
```

*Spaces or tabs*

```json
"editor.insertSpaces": true
```

And many, many [others](http://code.visualstudio.com/docs/customization/userandworkspace).


# File / folder management

## OS X layout

Using mission control, put a terminal window on the same screen as VS Code. Wala! You know have an integrated terminal. 

![OS X layout](/media/osx_layout.png)

## Autosave

Open `settings.json` with <kbd>cmd+,</kbd>

```json
"files.autoSave": "on"
```

## Toggle sidebar

<kbd>cmd+B</kbd>

![toggle side bar](/media/toggle_side_bar.gif)

## Side by side editing

<kbd>cmd+\</kbd> or <kbd>cmd</kbd> then click a file from the file browser. 

![split editors](/media/split_editor.gif)

## Switch between editors

<kbd>cmd+1</kbd>, <kbd>cmd+2</kbd>, <kbd>cmd+3</kbd>

![navigate editors](/media/navigate_editors.gif)

## History

Navigate entire history with <kbd>ctrl+tab</kbd>
Navigate back with <kbd>ctrl+-</kdbd>.
Navigate forward with <kbd>ctrl+shift+up</kbd>

![navigate history](/media/navigate_history.gif)

## Navigate to a file

<kbd>cmd+e</kbd> or <kbd>cmd+p</kbd>

![navigate to file](/media/navigate_to_file.gif)

## File associations

Setup language associations for files that aren't detected accurately (i.e. many config files). 

```json
"file.associations": {
    ".eslintrc": "json"
}
```

# Editor hacks

## Find by symbol

<kbd>cmd+up+o</kbd>

![Find by symbol](/media/find_by_symbol.gif)

## Navigate to a specific line

<kbd>ctrl+g</kbd> or <kbd>cmd+p, :</kbd>

![navigate to line](/media/navigate_to_line.gif)

## Undo cursor position

<kbd>cmd+u</kbd>

![undo cursor position](/media/undo_cursor_position.gif)

## Move line up and down

<kbd>opt+up</kbd> or <kbd>opt+down</kbd>

![move line up and down](/media/move_line.gif)

# Intellisense

Anytime, try <kbd>ctrl+space</kbd> to trigger the suggest widget. 

## jsconfig.json

## .eslintrc

## Install typings

# Debugging

# Task Runner

## Auto detect tasks

## Gulp tasks

## Mocha

# Git Integration

Excellent integration for entire Git workflow. 

## Diffs

## Branches

## Staging

## Committing

## See Git output

Sometimes I want to see what my tool is doing. Visual Studio Code makes it easy to see 
what git commands are running. This is helpful when learning git or debugging a difficult 
source control issue. 



## Styling README pages
