# saint L README

Laravel snippets for VS code (Visual Studio Code)

> Originaly the snippets initialized with the "[Laravel Blade Snippets](https://github.com/onecentlin/laravel-blade-snippets-vscode)" and then I modified them.

## Features

- Snippets (blade)

## Future features

- Format the code
- highlight code
- suggestion alternatives
- PHP to blade convertor 
  - `<?php ?>` to `@PHP @endphp`
  - `if() { }` to `@if() @endif`

For example if there is an image subfolder under your extension project workspace:

\!\[feature X\]\(images/feature-x.png\)

> Tip: Many popular extensions utilize animations. This is an excellent way to show off your extension! We recommend short, focused animations that are easy to follow.

## Requirements

If you have any requirements or dependencies, add a section describing those and how to install and configure them.

## Extension Settings

Include if your extension adds any VS Code settings through the `contributes.configuration` extension point.

For example:

This extension contributes the following settings:

* `myExtension.enable`: enable/disable this extension
* `myExtension.thing`: set to `blah` to do something

## Known Issues

Calling out known issues can help limit users opening duplicate issues against your extension.

## Release Notes

### 1.0.0
- Updates the snippet prefixes
One thing that was bothering me was, when I was in the middle of typing a directive (e.g.: `@ext...`) and the list of snippets shows up, and I pick one, I end up with two at-signs (`@@extends('name')`)! So the first change I've made was replace the `b:` with `@ `.
So, now we can have a nice `(@extends('name'))` withought needing to go back and remove the extra `@`

- There are `@` for non-atsign-directives as well for the sake of predictablity and staying united!

- Added 
  - 'else if line' snippet
To be added in the middle of other 'if' blocks
  - 'if is method': adds an 'if' block initialized with an 'isMethod()' 

- Renamed
  - "b:echo" => "b: mustache Esc"
  - "b:echo-html" => "b: mustache UnEsc"
  - "b:loop-first" & "b:loop-last" merged "@ if $loop"
  - 
- Replaced almost every dashes '-' in the prefixes with a single space, since it is easier to hit the spacebar.

- Removed:
  

-----------------------------------------------------------------------------------------------------------

## Working with Markdown

**Note:** You can author your README using Visual Studio Code.  Here are some useful editor keyboard shortcuts:

* Split the editor (`Cmd+\` on macOS or `Ctrl+\` on Windows and Linux)
* Toggle preview (`Shift+CMD+V` on macOS or `Shift+Ctrl+V` on Windows and Linux)
* Press `Ctrl+Space` (Windows, Linux) or `Cmd+Space` (macOS) to see a list of Markdown snippets

### For more information

* [Visual Studio Code's Markdown Support](http://code.visualstudio.com/docs/languages/markdown)
* [Markdown Syntax Reference](https://help.github.com/articles/markdown-basics/)

**Enjoy!**
