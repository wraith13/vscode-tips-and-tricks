# [VS Code](https://code.visualstudio.com) Tips and Tricks

This is a collection of helpful tips and tricks for VS Code. 

# Table of Contents

1. <a href="#basics">Basics</a>
2. <a href="#customization">Customization</a>
3. <a href="#file-and-folder-management">File and folder management</a>
4. <a href="#editing-hacks">Editing hacks</a>
5. <a href="#intellisense">Intellisense</a>
6. <a href="#git-integration">Git integration</a>
7. <a href="#readme-tips">Readme tips</a>
8. <a href="#debugging">Debugging</a>
9. <a href="#task-runner">Task runner</a>
10. <a href="#snippets">Snippets</a>

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

<kbd>shift+cmd+m</kbd> quickly jump to errors and warnings in the project. Cycle through errors with <kbd>f8</kbd> or <kbd>shift+f8</kbd>

![status errors and warnings](/media/status_errors_warnings.png)

**Update extensions**

Badges will appear in the bottom left of the status bar. 

![extension actions](/media/extension_actions.png)

**Change syntax**

<kbd>cmd+k m</kbd>

![change syntax](/media/change_syntax.gif)

# Customization

Lots of things you can do here. Check out the full [documentation](http://code.visualstudio.com/docs/customization/overview). 

## Ignore files / folders

[See documentation for more details](http://code.visualstudio.com/docs/customization/userandworkspace#_default-settings). Edit `settings.json` by adding the following:

Removes these files / folders from your editor window. 

```json
"files.exclude": {
		"somefolder/": true, 
		"somefile": true
}
```

Remove these files / folders from search results. 

```json
"search.exclude": {
    "someFolder/": true,
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


# File and folder management

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

# Editing hacks

## Bracket matching

More in [documentation](http://code.visualstudio.com/docs/editor/editingevolved#_bracket-matching).

<kbd>up+cmd+\<kbd>

![bracket matching](/media/bracket_matching.gif)

## Multi cursor selection

More in [documentation](http://code.visualstudio.com/docs/editor/editingevolved#_selection-multicursor)

![multi cursor](/media/multi_cursor.gif)

![multi cursor second example](/media/editingevolved_multicursor.gif)

Add more cursors to current selection.

![add cursor to all occurrences of current selection](/media/add_cursor_current_selection.gif)

## Shrink / expand selection

More in [documentation](http://code.visualstudio.com/docs/editor/editingevolved#_selection-multicursor)

<kbd>ctrl+shift+cmd+left</kbd> or <kbd>ctrl+shift+cmd+right</kbd>

![shrink expand selection](/media/shrink_expand_selection.gif)

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

## Trim trailing whitespace

<kbd>shift+up+x</kbd>

![trailing whitespace](/media/trim_whitespace.gif)

## Code formatting

<kbd>shift+alt+f</kbd>

![code formatting](/media/code_formatting.gif)

## Code folding

<kbd>shift+cmd+[</kbd> and <kbd>shift+cmd+]</kbd>

![code folding](/media/code_folding.gif)

## Select current line

<kbd>cmd+i</kbd>

![select current line](/media/select_current_line.gif)

## Navigate to beginning and end of file

<kbd>cmd+up</kbd> and <kbd>cmd+down</kbd>

![navigate to beginning and end of file](/media/beginning_end_file.gif)

# Intellisense

Anytime, try <kbd>ctrl+space</kbd> to trigger the suggest widget. This might be the most important tip of them all. 

![intellisense](/media/intellisense.gif)

You can view available methods, parameter hints, short documentation, etc. 

## Peek

// TODO 

## Go to definition

// TODO 

## jsconfig.json

Use ES6 by configuring jsconfig.json in the root of your javascript source files. 

```json
{
    "compilerOptions": {
        "target": "ES6",
        "module": "commonjs"
    }, "exclude": [
        "npm_modules"
    ]
}
```

## .eslintrc

Install [eslint extension](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint). Configure 
your linter however you'd like. Specification is [here](http://eslint.org/docs/user-guide/configuring). 

Here is configuration to use babel-eslint and es6. 

```json
{
    "parserOptions": {
        "ecmaVersion": 6,
        "sourceType": "module",
        "ecmaFeatures": {
            "jsx": true,
            "classes": true,
            "defaultParams": true
        }
    },
    "parser": "babel-eslint"
}
```

## Install typings

Install [typings](https://github.com/typings/typings) to bring in the `.d.ts` files which power javascript intellisense. 

```bash
npm install typings --global

# Search for definitions.
typings search tape

# Find an available definition (by name).
typings search --name react

# Install typings (DT is "ambient", make sure to enable the flag and persist the selection in `typings.json`).
typings install react --ambient --save
```

`install` will create a typings folder. VS Code will reference the `.d.ts` files for intellisense. 

## json validation

Enabled by default for many files. Create your own schema and validation in `settings.json`

```json
"json.schemas": [
    {
        "fileMatch": [
            "/bower.json"
        ],
        "url": "http://json.schemastore.org/bower"
    }
]
``` 

or for a schema defined in your workspace

```json
"json.schemas": [
    {
        "fileMatch": [
            "/foo.json"
        ],
        "url": "./myschema.json"
    }
]
``` 

See more in the [documentation](http://code.visualstudio.com/docs/languages/json).

## Emmet syntax

[Support for Emmet syntax](http://code.visualstudio.com/docs/languages/html#_emmet-snippets).  

![emmet syntax](emmet_syntax.gif)

# Git Integration

Excellent integration for entire Git workflow. 

## Diffs

Click Git icon then select the file to diff. 

![git icon](/media/git_icon.png)

**Side by side**

Default is side by side diff. 

![git diff side by side](/media/git_side_by_side.png)

**Inline view**

Toggle inline view by clicking more button in the top right. 

![more git button](/media/more_button.png)

![git inline](/media/git_inline.png)

## Branches

Easily switch between branches via the status bar. 

![switch branches](/media/switch_branches.gif)

## Staging

**Stage all**

Hover over the number of files and click the plus button. 

![git stage all](/media/git_stage_all.gif)

**Stage selected**

Stage a portion of a file by selecting that file (using the arrows) and then staging 
"selected lines" via the more button. 

![git stage selected](/media/git_stage_selected.gif)

## Undo last commit

![undo last commit](/media/undo_last_commit.gif)

## See Git output

Sometimes I want to see what my tool is doing. Visual Studio Code makes it easy to see 
what git commands are running. This is helpful when learning git or debugging a difficult 
source control issue. 

<kbd>shift+cmd+u</kbd> to run `toggleOutput`. Select Git in the dropdown.

## Gutter indicators

View diff decorations in editor. See [documentation](http://code.visualstudio.com/docs/editor/editingevolved#_gutter-indicators) for more details. 

![git gutter indicators](/media/editingevolved_gutter.png)

## Resolve merge conflicts

// TODO

## Setup VS Code as default merge tool

// TODO

## Git output window

// TODO
 
# README tips

## Toggle preview

<kbd>shift+cmd+v</kbd> to `Toggle Preview`

![toggle readme preview](/media/toggle_preview.gif)

## Styling README pages

# Debugging

## Configure debugger

// TODO

## Data inspection in the console

// TODO

# Task Runner

## Auto detect tasks

// TODO

## Gulp tasks

// TODO

## NPM tasks

// TODO

# Snippets

## Create custom snippets

`File -> Preferences -> User Snippets`, select the language, and create a shippet. 

```json
"create component": {
    "prefix": "component",
    "body": [
        "class $1 extends React.Component {",
        "",
        "	render() {",
        "		return ($2);",
        " 	}",
        "",
        "}"
    ]
},
```

See more details in [documentation](http://code.visualstudio.com/docs/customization/userdefinedsnippets#_creating-your-own-snippets). 