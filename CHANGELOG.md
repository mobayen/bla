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

### 0.4.0
- Adds the Unescaped-Data mustache syntax {!!|!!}
- ### 0.4.1
  - Improves the route 'trigger' text to stop trigger the snippets randomly
- ### 0.4.2
  - removes the extra tab between @php and @endphp

### 0.5.0
- Adds two more snippets
  - @dd()
  - the combo of @extend and @section

### 0.6.0
- trigger the snippet with the actual code

### 0.7.0
- Adds @slot @endslot as brackets
