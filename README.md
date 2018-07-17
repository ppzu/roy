# Roy [![Build Status](https://travis-ci.org/puffnfresh/roy.png?branch=master)](https://travis-ci.org/puffnfresh/roy)
Roy is a small functional language that compiles to JavaScript. It has a few main features:

* Damas-Hindley-Milner type inference
* Whitespace significant syntax
* Simple tagged unions
* Pattern matching
* Structural typing
* Monad syntax
* Not-horrible JS output

## Usage
Install roy:

    make deps
    make

Enter a read-eval-print loop (REPL):

    ./roy

Compile and run a `.roy` file:

    ./roy -r examples/helloworld.roy

Compile a `.roy` file to `.js`:

    ./roy examples/helloworld.roy
    cat examples/helloworld.js

## Examples
Input (test.roy):

```roy
let addTwo n =
    n + 2

console.log (addTwo 40)
```

Output (test.js):

```roy
var addTwo = function(n) {
    return n + 2;
}
console.log(addTwo(40))
```

Calling `addTwo "test"` will result in a compile-time error (`addTwo` can only take a Number).

See the examples directory for more.

## License
MIT

## Editor Support
* [Vim](https://github.com/jb55/Vim-Roy)
* [Emacs](https://github.com/folone/roy-mode)
* [Chocolat, SublimeText2, TextMate](https://github.com/paulmillr/roy.tmbundle)
* [SublimeText](https://github.com/joneshf/sublime-roy)

## Resources
* Roy website: http://roy.brianmckenna.org/
* Roy Google Group: http://groups.google.com/group/roylang
* Roy docs: http://guide.roylang.org/
* Roy Twitter: http://twitter.com/roylangjs
* Bitbucket repo: https://bitbucket.org/puffnfresh/roy
* GitHub repo: https://github.com/puffnfresh/roy
* Brian's blog: http://brianmckenna.org/
* altJS channel: [irc://irc.freenode.net/altJS](irc://irc.freenode.net/#altJS)
* roy channel: [irc://irc.freenode.net/roy](irc://irc.freenode.net/#roy)
