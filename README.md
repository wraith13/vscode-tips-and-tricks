# [VS Code](https://code.visualstudio.com) ヒントとテクニック

> 👻 このドキュメントは [VS Code Tips and Tricks](https://github.com/Microsoft/vscode-tips-and-tricks) の日本語訳です

# 目次

1. <a href="#基本">基本</a>
1. <a href="#カスタマイズ">カスタマイズ</a>
1. <a href="#拡張機能">拡張機能</a>
1. <a href="#ファイルとフォルダの管理">ファイルとフォルダの管理</a>
1. <a href="#便利な編集機能">便利な編集機能</a>
1. <a href="#インテリセンス">インテリセンス</a>
1. <a href="#スニペット">スニペット</a>
1. <a href="#fit統合">Git統合</a>
1. <a href="#デバッギング">デバッギング</a>
1. <a href="#タスク-ランナー">タスク ランナー</a>
1. <a href="#その他のリソース">その他のリソース</a>

> 以下のキーボードショートカットは最新ビルドと正確かもしれませんし、そうでないかもしれません。[こちら](https://code.visualstudio.com/docs/customization/keybindings)の最新のキーボードショートカットリファレンスを参照してください。

# 基本

## VS Code のインサイダーバージョン

VS Code チームは最新の機能とバグ修正を確認する為にインサイダーバージョンを使っています。 あたなも[ここからダウンロード](https://code.visualstudio.com/insiders)して同じバージョンを使う事ができます。

* アーリーアダプターの為に - インサイダーは最も直近のコード変更と時々壊れたビルドを手にすることになるでしょう。
* 頻繁なビルド - 最新のバグ修正と機能を含む毎日の新しいビルド。
* Side-by-side インストール - インサイダー版と安定版は互いに依存せずに利用可能です。

![side by side インストール](/media/side-by-side-install.png)

## はじめよう

ようこそページを開いて VS Code の基本に入門しよう。 <kbd>ヘルプ</kbd> → <kbd>ようこそ</kbd>.

![ようこそページ](/media/welcome_page.png)

対話型プレイグラウンドを含みます。

![対話型プレイグラウンド](/media/interactive_playground.png)

## コマンド パレット

あなたの現在のコンテキストで利用可能な全てのコマンドにアクセスできます。

> Mac: <kbd>cmd</kbd>+<kbd>shift</kbd>+<kbd>p</kbd> あるいは <kbd>f1</kbd>

> Windows / Linux: <kbd>ctrl</kbd>+<kbd>shift</kbd>+<kbd>p</kbd> あるいは <kbd>f1</kbd>

![コマンド パレット](/media/OpenCommandPalatte.gif)

## キーボードショートカットの参照

全てのコマンドは割り当てられたキーボードショートカットが存在する場合、ともにコマンドパレット上に表示されます。もしもあなたがキーボードショートカットを忘れてしまった場合、コマンドパレットがあなたの助けになるでしょう。

![キーボードショートカットの参照](/media/keyboard-references.png)

## クイック オープン

素早くファイルを開きます。

> Mac: <kbd>cmd+p</kbd>

> Windows / Linux: <kbd>ctrl+p</kbd>

![クイック オープン](/media/QuickOpen.gif)

> **Tip:** <kbd>?<kbd> とタイプするとヘルプが提示されます。

## CLI ツール

> Linux: [ここ](http://code.visualstudio.com/docs/editor/setup#_linux)の指示に従ってください。

> Windows: [ここ](http://code.visualstudio.com/docs/editor/setup#_windows)の指示に従ってください。

> Mac: 下記を参照してください。

コマンド パレットを開いて(<kbd>F1</kbd>) `shell command` とタイプし <kbd>enter</kbd> を叩いて `Shell Command: Install 'code' command in PATH` を実行します。

![shell command](/media/setup_shell-command.png)

```bash
# カレントディレクトリで code を開く
code .

# 新しいウィンドウの作成
code -n

# 言語の変更
code --locale=es

# diff エディタを開く
code --diff <file1> <file2>

# オプションヘルプの表示
code --help

# 全ての拡張の無効化
code --disable-extensions .
```

![全ての CLI コマンド](/media/vscode-cli-commands.png)

## .vscode フォルダ

Workspace specific files are in `.vscode`. For example, `tasks.json` for the Task Runner and `launch.json` for the debugger.

## ステータス バー の装飾

### エラーと警告

> Mac: <kbd>shift</kbd>+<kbd>cmd</kbd>+<kbd>m</kbd>

> Windows / Linux: <kbd>ctrl</kbd>+<kbd>shift</kbd>+<kbd>m</kbd>

Quickly jump to errors and warnings in the project. 

Cycle through errors with <kbd>f8</kbd> あるいは <kbd>shift</kbd>+<kbd>f8</kbd>

![エラーと警告](/media/Errors_Warnings.gif)

### 言語モードの変更

> Mac: <kbd>cmd</kbd>+<kbd>k</kbd> <kbd>m</kbd>

> Windows / Linux: <kbd>ctrl</kbd>+<kbd>k</kbd> <kbd>m</kbd>

![構文強調の変更](/media/change_syntax.gif)

# カスタマイズ

There are many things you can do to customize VS Code.

* テーマの変更
* キーボードショートカットの変更
* Tune your settings
* Add JSON validation
* スニペットの作成 
* 拡張機能のインストール

完全な[ドキュメント](http://code.visualstudio.com/docs/customization/overview)に目を通そう。

## テーマの変更

Open the command palatte and type "themes". You can install more themes from the extension Marketplace.

![Preview themes](/media/PreviewThemes.gif)

Additionally, you can install and change your file icon themes.

![File icon themes](/media/PreviewFileIconThemes.gif)

## キーボードショートカットの変更

### キーボードショートカット一覧

あなたの環境([macOS](https://go.microsoft.com/fwlink/?linkid=832143), [Windows](https://go.microsoft.com/fwlink/?linkid=832145), [Linux](https://go.microsoft.com/fwlink/?linkid=832144))の為のキーボードショートカット一覧をダウンロードしよう。

![Keyboard Reference Sheet](/media/KeyboardReferenceSheet.png)

### キーマップ

Are you used to keyboard shortcuts from another editor? You can install a Keymap extension that brings the keyboard shortcuts from your favorite editor to VS Code. Go to Preferences -> Keymap Extensions to see the current list on the [Marketplace](https://marketplace.visualstudio.com/search?target=VSCode&category=Keymaps&sortBy=Downloads). Some of the more popular ones:

- [Vim](https://marketplace.visualstudio.com/items?itemName=vscodevim.vim)
- [Sublime Text Keymap](https://marketplace.visualstudio.com/items?itemName=ms-vscode.sublime-keybindings)
- [Emacs Keymap](https://marketplace.visualstudio.com/items?itemName=hiro-sun.vscode-emacs)
- [Atom Keymap](https://marketplace.visualstudio.com/items?itemName=ms-vscode.atom-keybindings)

### キーボードショートカットのカスタマイズ

Open the command palatte and type "Keyboard Shortcuts." You can now add your own keybindings in the file on the right.

![キーボードショートカットのカスタマイズ](/media/KeyboardShortcuts.gif)

See more in the [Official Documentation](https://code.visualstudio.com/docs/customization/keybindings).

## Tune your settings

`settings.json` を開きます。

> Mac: <kbd>cmd</kbd>+<kbd>,</kbd>

> Windows / Linux: <kbd>ファイル</kbd> -> <kbd>基本設定</kbd> -> <kbd>設定</kbd>

### Format on paste

```json
"editor.formatOnPaste": true
```

### フォントサイズの変更

```json
"editor.fontSize": 18
```

### ズームレベルの変更

```json
"window.zoomLevel": 5
```

### フォント合字

```json
"editor.fontLigatures": true
```

> **Tip:** You will need to have a font installed that supports font ligatures. [FiraCode](https://github.com/tonsky/FiraCode) is a popular font on the VS Code team.

![フォント合字](/media/font-ligatures-annotated.png)

### 自動保存

```json
"files.autoSave": true
```

### Format on save

```json
"editor.formatOnSave": true,
```

### Change the size of tab characters

```json
"editor.tabSize": 4
```

### 空白文字およびタブ文字

```json
"editor.insertSpaces": true
```

### ホワイトスペースの表示

```json
"editor.renderWhitespace": true
```

### Ignore files / folders

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

And many, many [others](http://code.visualstudio.com/docs/customization/userandworkspace).

## Language specific settings

For those settings you only want for specific languages.

```json
"[languageid]": {
    
}
```

> **Tip:** You can find the language ID by typing in the command palatte "Configure language specific settings"

![language based settings](/media/lang-based-settings.png)

## Add JSON Validation

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

あるいは for a schema defined in your workspace

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

もしくは a custom schema

```json
"json.schemas": [
    {
        "fileMatch": [
            "/.myconfig"
        ],
        "schema": {
            "type": "object",
            "properties": {
                "name" : {
                    "type": "string",
                    "description": "The name of the entry"
                }
            }
        }
    },
```

See more in the [documentation](http://code.visualstudio.com/docs/languages/json).

# 拡張機能

## 拡張機能を見つける

1. VS Code の [marketplace](https://marketplace.visualstudio.com/vscode) で
1. VS Code 内で検索
1. お勧めの拡張機能を表示
1. Community curated extension lists, such as [awesome-vscode](https://github.com/viatsko/awesome-vscode).

## 拡張機能のインストール

アクティビティバーの拡張機能ボタンをクリックし、検索バーからあるいはその他ボタンをクリックしてフィルターしたりインストール数順で並べ替えたりして検索機能を探すことができます。

![拡張機能のインストール](/media/InstallExtensions.gif)

## オススメの拡張機能

Click the extension activity bar button. Then click "Show Recommended Extensions" in the more button menu. 

![オススメの拡張機能を表示](/media/ShowRecommendedExtensions.gif)

## Creating my own extension

Are you interested in creating your own extension? You can learn how to do this in the documentation, specifically check out the [documentation on contribution points](http://code.visualstudio.com/docs/extensionAPI/extension-points).

* configuration
* commands
* keybindings
* languages
* debuggers
* grammars
* themes
* snippets
* jsonValidation

# ファイルとフォルダの管理

## 統合ターミナル

> Windows / Linux / Mac: <kbd>ctrl</kbd>+<kbd>`</kbd>

![統合ターミナル](/media/integrated_terminal.png)

## 自動保存

<kbd>cmd</kbd>+<kbd>,</kbd> で `settings.json` を開きます。

> 👻  Windows および Linux の場合は <kbd>ファイル</kbd> -> <kbd>基本設定</kbd> -> <kbd>設定</kbd>

```json
"files.autoSave": "afterDelay"
```

## サイドバーの切り替え

> Mac: <kbd>cmd</kbd>+<kbd>b</kbd>

> Windows / Linux: <kbd>ctrl</kbd>+<kbd>b</kbd>

![サイドバーの切り替え](/media/toggle_side_bar.gif)

## Zen Mode

> Mac: <kbd>cmd</kbd>+<kbd>k</kbd> <kbd>z</kbd>

> Windows / Linux: <kbd>ctrl</kbd>+<kbd>k</kbd> <kbd>z</kbd>

![zen mode](/media/zen_mode.gif)

Enter distraction free mode.

## Side by side editing

> Mac: <kbd>cmd</kbd>+<kbd>\\</kbd> あるいは <kbd>cmd</kbd> then click a file from the file browser.

> Windows / Linux: <kbd>ctrl</kbd>+<kbd>\\</kbd>

> Linux: <kbd>ctrl</kbd>+<kbd>2</kbd>

![split editors](/media/split_editor.gif)

## エディタ間の切り替え

> Mac: <kbd>cmd</kbd>+<kbd>1</kbd>, <kbd>cmd</kbd>+<kbd>2</kbd>, <kbd>cmd</kbd>+<kbd>3</kbd>

> Windows / Linux: <kbd>ctrl</kbd>+<kbd>1</kbd>, <kbd>ctrl</kbd>+<kbd>2</kbd>, <kbd>ctrl</kbd>+<kbd>3</kbd>

![navigate editors](/media/navigate_editors.gif)

## エクスプローラー ウィンドウへの移動

> Mac: <kbd>cmd</kbd>+<kbd>shift</kbd>+<kbd>e</kbd>

> Windows / Linux: <kbd>ctrl</kbd>+<kbd>shift</kbd>+<kbd>e</kbd>

## ファイルのオープンと作成

> Mac: <kbd>cmd</kbd>+<kbd>click</kbd>

> Windows / Linux: <kbd>ctrl</kbd>+<kbd>click</kbd>

![ファイルのオープンと作成](/media/create_open_file.gif)

## カレントの開いているフォルダーを閉じる

> Mac: <kbd>cmd</kbd>+<kbd>w</kbd>

> Linux: <kbd>ctrl</kbd>+<kbd>k</kbd> <kbd>f</kbd>

## 履歴

Navigate entire history with <kbd>ctrl</kbd>+<kbd>tab</kbd>

Navigate back.

> Mac: <kbd>ctrl</kbd>+<kbd>-</kdbd>

> Windows / Linux: <kbd>alt</kbd>+<kbd>left</kbd>

Navigate Forward.

> Mac: <kbd>ctrl</kbd>+<kbd>shift</kbd>+<kbd>-</kbd>

> Windows / Linux: <kbd>alt</kbd>+<kbd>right</kbd>

![navigate history](/media/navigate_history.gif)

## Navigate to a file

> Mac: <kbd>cmd</kbd>+<kbd>e</kbd> あるいは <kbd>cmd</kbd>+<kbd>p</kbd>

> Windows / Linux: <kbd>ctrl</kbd>+<kbd>e</kbd> あるいは <kbd>ctrl</kbd>+<kbd>p</kbd>

![navigate to file](/media/navigate_to_file.gif)

## File associations

Setup language associations for files that aren't detected accurately (i.e. many config files).

```json
"file.associations": {
    ".database": "json"
}
```

# 便利な編集機能

Here are a selection of common features for editing code. If the keyboard shortcuts aren't comfortable for you, consider installing a [Keymap extension](https://marketplace.visualstudio.com/search?target=VSCode&category=Keymaps&sortBy=Downloads) for your old editor.

## Multi cursor selection

> Mac: <kbd>opt</kbd>+<kbd>cmd</kbd>+<kbd>up</kbd> あるいは <kbd>opt</kbd>+<kbd>cmd</kbd>+<kbd>down</kbd>

> Windows: <kbd>ctrl</kbd>+<kbd>alt</kbd>+<kbd>up</kbd> あるいは <kbd>ctrl</kbd>+<kbd>alt</kbd>+<kbd>down</kbd>

> Linux: <kbd>alt</kbd>+<kbd>shift</kbd>+<kbd>up</kbd> あるいは <kbd>alt</kbd>+<kbd>shift</kbd>+<kbd>down</kbd>

![multi cursor](/media/multi_cursor.gif)

![multi cursor second example](/media/editingevolved_multicursor.gif)

Add more cursors to current selection.

![add cursor to all occurrences of current selection](/media/add_cursor_current_selection.gif)

## 行の結合

> Mac: <kbd>ctrl</kbd>+<kbd>j</kbd>

> Windows / Linux: デフォルトでは割り当てられていません。<kbd>ファイル</kbd>→<kbd>基本設定</kbd>→<kbd>キーボード ショートカット</kbd> を開いて `editor.action.joinLines` にあなたの好みでショートカットを割り当ててください。

![行の結合](/media/JoinLines.gif)

## 行コピー ( 上 / 下 )

> Mac: <kbd>opt</kbd>+<kbd>shift</kbd>+<kbd>up</kbd> あるいは <kbd>opt</kbd>+<kbd>shift</kbd>+<kbd>down</kbd>

> Windows / Linux([Issue #5363](https://github.com/Microsoft/vscode/issues/5363)): <kbd>shift</kbd>+<kbd>alt</kbd>+<kbd>down</kbd> あるいは <kbd>shift</kbd>+<kbd>alt</kbd>+<kbd>up</kbd>

![行コピー ( 下 )](/media/copy_line_down.gif)

## 選択範囲の縮小と拡大

More in [documentation](http://code.visualstudio.com/docs/editor/editingevolved#_selection-multicursor)

> Mac: <kbd>ctrl</kbd>+<kbd>shift</kbd>+<kbd>cmd</kbd>+<kbd>left</kbd> あるいは <kbd>ctrl</kbd>+<kbd>shift</kbd>+<kbd>cmd</kbd>+<kbd>right</kbd>

> Windows / Linux: <kbd>shift</kbd>+<kbd>alt</kbd>+<kbd>left</kbd> あるいは <kbd>shift</kbd>+<kbd>alt</kbd>+<kbd>right</kbd>

![選択範囲の縮小と拡大](/media/shrink_expand_selection.gif)

## シンボル検索

> Mac: <kbd>cmd</kbd>+<kbd>shift</kbd>+<kbd>o</kbd>

> Windows / Linux: <kbd>ctrl</kbd>+<kbd>shift</kbd>+<kbd>o</kbd>

![シンボル検索](/media/find_by_symbol.gif)

## Navigate to a specific line

> Mac: <kbd>ctrl</kbd>+<kbd>g</kbd> あるいは <kbd>cmd</kbd>+<kbd>p</kbd> <kbd>:</kbd>

> Windows / Linux: <kbd>ctrl</kbd>+<kbd>g</kbd>

![navigate to line](/media/navigate_to_line.gif)

## カーソル位置をひとつ前に戻す

> Mac: <kbd>cmd</kbd>+<kbd>u</kbd>

> Windows / Linux: <kbd>ctrl</kbd>+<kbd>u</kbd>

![カーソル位置をひとつ前に戻す](/media/undo_cursor_position.gif)

## Move line up and down

> Mac: <kbd>opt</kbd>+<kbd>up</kbd> あるいは <kbd>opt</kbd>+<kbd>down</kbd>

> Windows / Linux: <kbd>alt</kbd>+<kbd>up</kbd> あるいは <kbd>alt</kbd>+<kbd>down</kbd>

![move line up and down](/media/move_line.gif)

## Trim trailing whitespace

> Mac: <kbd>cmd</kbd>+<kbd>shift</kbd>+<kbd>x</kbd>

> Windows / Linux: <kbd>ctrl</kbd>+<kbd>k</kbd> <kbd>ctrl</kbd>+<kbd>x</kbd>

![trailing whitespace](/media/trim_whitespace.gif)

## Code formatting

### Currently selected source code

> Mac: <kbd>cmd</kbd>+<kbd>k</kbd> <kbd>cmd</kbd>+<kbd>f</kbd>

> Windows / Linux: <kbd>ctrl</kbd>+<kbd>k</kbd> <kbd>ctrl</kbd>+<kbd>f</kbd>

### Whole document format

> Windows / Linux: <kbd>shift</kbd>+<kbd>alt</kbd>+<kbd>f</kbd>

![code formatting](/media/code_formatting.gif)

## コードの折りたたみ

> Mac: <kbd>shift</kbd>+<kbd>cmd</kbd>+<kbd>\[</kbd> and <kbd>shift</kbd>+<kbd>cmd</kbd>+<kbd>\]</kbd>

> Windows / Linux: <kbd>ctrl</kbd>+<kbd>shift</kbd>+<kbd>\[</kbd> and <kbd>ctrl</kbd>+<kbd>shift</kbd>+<kbd>\]</kbd>

![コードの折りたたみ](/media/code_folding.gif)

## 現在行を選択

> Mac: <kbd>cmd</kbd>+<kbd>i</kbd>

> Windows / Linux: <kbd>ctrl</kbd>+<kbd>i</kbd>

![現在行を選択](/media/select_current_line.gif)

## Navigate to beginning and end of file

> Mac: <kbd>cmd</kbd>+<kbd>up</kbd> and <kbd>cmd</kbd>+<kbd>down</kbd>

> Windows: <kbd>ctrl</kbd>+<kbd>up</kbd> and <kbd>ctrl</kbd>+<kbd>down</kbd>

> Linux: <kbd>ctrl</kbd>+<kbd>home</kbd> and <kbd>ctrl</kbd>+<kbd>end</kbd>

![navigate to beginning and end of file](/media/beginning_end_file.gif)

## README プレビューの切り替え

In a markdown file use

> Mac: <kbd>shift</kbd>+<kbd>cmd</kbd>+<kbd>v</kbd>

> Windows / Linux: <kbd>ctrl</kbd>+<kbd>shift</kbd>+<kbd>v</kbd>

![README プレビューの切り替え](/media/toggle_preview.gif)

## Side by Side Markdown Edit and Preview

In a markdown file use

> Linux: <kbd>ctrl</kbd>+<kbd>k</kbd> <kbd>v</kbd>

Special bonus: The preview will now sync.

![markdown sync](/media/markdown-preview-sync.gif)

# インテリセンス

いつでも、 <kbd>ctrl</kbd>+<kbd>space</kbd> でサジェストウィジェットの起動を試みることができます。

![インテリセンス](/media/intellisense.gif)

You can view available methods, parameter hints, short documentation, etc.

## 定義をここに表示

シンボルを選択肢して <kbd>alt</kbd>+<kbd>f12</kbd> を押します。あるいは、コンテキストメニューを使用します。

![定義をここに表示](/media/peek.gif)

## 定義へ移動

シンボルを選択肢して <kbd>f12</kbd> を押します。あるいは、コンテキストメニューを使用します。

![定義へ移動](/media/goto_definition.gif)

## Find all references

Select a symbol then type <kbd>shift</kbd>+<kbd>f12</kbd>. Alternatively, you can use the context menu.

![find all references](/media/find_all_references.gif)

## Rename symbol

Select a symbol then type <kbd>f2</kbd>. Alternatively, you can use the context menu.

![rename symbol](/media/rename_symbol.gif)

## .eslintrc.json

Install [eslint extension](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint). Configure 
your linter however you'd like. Specification is [here](http://eslint.org/docs/user-guide/configuring).

Here is configuration to use es6.

```json
{
    "env": {
        "browser": true,
        "commonjs": true,
        "es6": true,
        "node": true
    },
    "parserOptions": {
        "ecmaVersion": 6,
        "sourceType": "module",
        "ecmaFeatures": {
            "jsx": true,
            "classes": true,
            "defaultParams": true
        }
    },
    "rules": {
        "no-const-assign": 1,
        "no-extra-semi": 0,
        "semi": 0,
        "no-fallthrough": 0,
        "no-empty": 0,
        "no-mixed-spaces-and-tabs": 0,
        "no-redeclare": 0,
        "no-this-before-super": 1,
        "no-undef": 1,
        "no-unreachable": 1,
        "no-use-before-define": 0,
        "constructor-super": 1,
        "curly": 0,
        "eqeqeq": 0,
        "func-names": 0,
        "valid-typeof": 1
    }
}
```

## package.json

See intellisense for your package.json file.

![package json intellisense](/media/package_json_intellisense.gif)

## Emmet 構文

[Emmet 構文のサポート](http://code.visualstudio.com/docs/languages/html#_emmet-snippets).

![Emmet 構文](/media/emmet_syntax.gif)

# スニペット

## 独自スニペットの作成

<kbd>ファイル</kbd> → <kbd>基本設定</kbd> → <kbd>ユーザー スニペット</kbd>, select the language, and create a snippet. 
> 👻 Mac では <kbd>Code</kbd> → <kbd>基本設定</kbd> → <kbd>ユーザー スニペット</kbd> となっている

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

# Git統合

## Diffs

Click Git icon then select the file to diff.

![Git アイコン](/media/git_icon.png)

## Side by side

Default is side by side diff.

![git diff side by side](/media/git_side_by_side.png)

## インライン表示

Toggle inline view by clicking more button in the top right.

![more git button](/media/more_button.png)

![git inline](/media/git_inline.png)

## ブランチ

Easily switch between branches via the status bar.

![ブランチの切り替え](/media/switch_branches.gif)

## ステージング

### Stage all

Hover over the number of files and click the plus button.

![git stage all](/media/git_stage_all.gif)

### Stage selected

Stage a portion of a file by selecting that file (using the arrows) and then staging "selected lines" via the more button.

![git stage selected](/media/git_stage_selected.gif)

## 前回のコミットを元に戻す

![前回のコミットを元に戻す](/media/undo_last_commit.gif)

## Git 出力の表示

Sometimes I want to see what my tool is doing. Visual Studio Code makes it easy to see 
what git commands are running. This is helpful when learning git or debugging a difficult 
source control issue.

> Mac: <kbd>shift</kbd>+<kbd>cmd</kbd>+<kbd>u</kbd>

> Windows / Linux: <kbd>ctrl</kbd>+<kbd>shift</kbd>+<kbd>u</kbd>

to run `toggleOutput`. Select Git in the dropdown.

## Gutter indicators

View diff decorations in editor. See [documentation](http://code.visualstudio.com/docs/editor/versioncontrol#_gutter-indicators) for more details.

![git gutter indicators](/media/editingevolved_gutter.png)

## Resolve merge conflicts

During a merge click the git icon and make changes in the diff view.

![Git アイコン](/media/git_icon.png)

## Setup VS Code as default merge tool

```bash
git config --global merge.tool code
```

# デバッギング

## Configure debugger

<kdb>f1</kdb> and select "Debug: Open Launch.json", select the environment. 
This will generate a `launch.json` file. Works out of the box as expected for
Node and other environments. May need some additional configuration for other languages.
See [documentation](http://code.visualstudio.com/docs/editor/debugging) for more details.

![configure debugging](/media/configure_debug.gif)

## Breakpoints and stepping through

Place breakpoints next to the line number. Navigate forward with the debug widget.

![debug](/media/node_debug.gif)

## Data inspection

Inspect variables in the debug panels and in the console.

![data inspection](/media/debug_data_inspection.gif)

# タスク ランナー

## Auto detect tasks

<kbd>f1</kbd>, type "Configure Task", then select "Configure Task Runner". 
This will generate a task.json file with content like the following. See 
[documentation](http://go.microsoft.com/fwlink/?LinkId=733558) for more details.

```javascript
{
	// See http://go.microsoft.com/fwlink/?LinkId=733558
	// for the documentation about the tasks.json format
	"version": "0.1.0",
	"command": "npm",
	"isShellCommand": true,
	"showOutput": "always",
	"suppressTaskName": true,
	"tasks": [
		{
			"taskName": "install",
			"args": ["install"]
		},
		{
			"taskName": "build",
			"args": ["run", "build"]
		}
	]
}
```

There are occasionally issues with auto generation. Check out the documentation
for getting things to work properly.

> 👻 json の中ではコメントは使えないです。

## コマンドパレットからのタスク実行

<kbd>f1</kbd>, run the command "Run Task", and select the task you want to run. Terminate the running
task by running the command "Terminate Running Task"

![タスク ランナー](/media/task_runner.gif)


## その他のリソース

* [vscode official docs](https://code.visualstudio.com/docs)
* [react sample app](https://github.com/Microsoft/vscode-react-sample)
* [awesome vscode](https://github.com/viatsko/awesome-vscode)
