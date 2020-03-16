# bla_de (Blade/Laravel)

Laravel (Blade & Route) extension for VS code (Visual Studio Code)

<p align="center">
    <img src="images/L-big.png" width="400">
</p>

The most important thing I have in mind is not adding extra string/characters to the trigger string. The snippets should pop up when you are typing the code, but not some custome trigger.


> no: `b:bla-bla`

> no: `blade:bla-bla`

> yes: `@bla-bla`

Just start type the actuall code (`@section`, `Route::get`, ...) the snippets show up.
Easy, right?

### Blade snippets
Probably you noticed a space after the `@`. This make the snippet work if the developer types just `bla-bla` witought the `@`.
So, that means the snippet will show up if you just type:
`exten...`
`secti...`
`section sh...`

### Route snippets
The title of routes are too long to see it completely in the list of snippeted suggested when coding, so I had to add a short abbreviation of them! I know, that sucks but I couldn't find a better way that makes more sense :-(
```
Rt:Ctrl@actn
Rt:Rsrc
```
But the good thing is it still works if you type the start part of the route, just like the blade snippets.
```
Route::g...
Route::po...
Route::reso...
Route::apiRes...
```

## Use with caution: 
the trigger strings (prefixes) may change at any time until I found the best option!

## Features

- Blade snippets
- Route snippets
- Highlight and jump between blade blocks opening and closing

## Future features

- Format the code
- suggestion alternatives
- PHP to blade convertor 
  - `<?php ?>` to `@PHP @endphp`
  - `if() { }` to `@if() @endif`

## Extension Settings

nothing yet!

## Known Issues

The highlight/jump works for most of blocks in Blade (e.g: `@if @endif`) but it doesnt highlight/jump-to the middle directives (`@else`, `@else-if`, etc.). 
The reason is in VSCode it is not allowed to pare an block-open (e.g.: `@if`) to more than one block-close (e.g.: either `@endif` or `@else`).

In other word, in these (chained!) blocks, only the block-open and block-close can be highlighted and jump to.

- @if @else-if @else @endif
- @forelse(...) @empty @endforelse
- @env @elseenv @else @endenv


## Snippets

> Originaly the Blade snippets initialized with the "Laravel Blade Snippets" and then I modified them.

- The list of trigger-snippet code will be added soon

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
  
### 0.2.0
- Group routes by:
  - Middleware
  - Namespaces
  - Subdomain Routing
  - Route Prefixes
  - Route Name Prefixes

### 0.3.0
- Highlight "blade open/close pairs of blocks" and jump between matching pairs
  - @if @endif
  - @foreach @endforeach
  - @section @endsection
  - etc.
- Auto-closing-pairs works between single and double quotes nice and smoothly 
> before:  `<div class='{{'>`
> now:  `<div class='{{ }}'>`
- ### 0.3.1
  - Brings back the default braces and pairs
- ### 0.3.2
  - Auto Close braces when cursor is just before a '<'
    - before: `<a href="">{{</a>`
    - after: `<a href="">{{}}</a>`
- ### 0.3.3
  - Modify the final cursor position for some snippets