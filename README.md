# [VS Code](https://code.visualstudio.com) Tips and Tricks

This is a collection of helpful tips and tricks for VS Code that I've collected while using the product. Most of these are contained in the documentation and I've provided a link when applicable. 

## Ignore files / folders

[See documentation for more details](http://code.visualstudio.com/docs/customization/userandworkspace#_default-settings). Edit `settings.json` by adding the following:

```json
"files.exclude": {
		"somefolder/": true, 
		"somefile": true
}
```

## Auto preview themes
