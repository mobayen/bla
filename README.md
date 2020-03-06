# bla_de (Blade/Laravel)

Laravel (Blade & Route) snippets for VS code (Visual Studio Code)

the most thing I have in mind is not adding custom string to the trigger string.

> no: `b:bla-bla`
> no: `blade:bla-bla`
> yes: `@ bla-bla`

the space after the `@` make the snippet work if the developer typs just `bla-bla` witought the `@`

> Originaly the snippets initialized with the "[Laravel Blade Snippets](https://github.com/onecentlin/laravel-blade-snippets-vscode)" and then I modified them.

caution: the trigger strings (prefixes) could change until I found the best option!

## Features

- Blade snippets
- Route snippets
- More comming...

## Future features

- Format the code
- highlight code
- suggestion alternatives
- PHP to blade convertor 
  - `<?php ?>` to `@PHP @endphp`
  - `if() { }` to `@if() @endif`

<p align="center">
<img src="images/L-big.png" width="400">
</p>

## Extension Settings

nothing yet!

## Known Issues

nothing yet!

## Release Notes

### 0.0.0
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

- Route snippets have been added.

- Route snippets have been added.
  - Routes accepts `Controller@action` pattern
  - Routes accepts a closure

- Removed:
  - ...
