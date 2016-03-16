# [VS Code](https://code.visualstudio.com) Tips and Tricks

This is a collection of helpful tips and tricks for VS Code that I've collected while using the product. Most of these are contained in the documentation and I've provided a link when applicable. 

## Ignore files / folders

Edit `settings.json` by adding the following:

```json
"files.exclude": {
		"somefolder/": true, // Removes "somefolder" from VS Code's file explorer
		"somefile": true
}
```
