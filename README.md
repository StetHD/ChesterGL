# ChesterGL

## What is this?

It's a simple WebGL 2d library that I've been writing since early 2011 mainly to teach myself OpenGL-ES 2.0. Nothing more than that. If you can build a game with this, awesome :) (and let me know)

The API is somewhat inspired in [cocos2d-iphone](https://github.com/cocos2d/cocos2d-iphone), but just inspired. It's not intended to be a port of cocos2d for WebGL.

## How to have fun

Get the latest "stable" release from here:

[http://funkaster.github.com/ChesterGL/chesterGL-latest.zip](http://funkaster.github.com/ChesterGL/chester-latest.zip)

Unzip, create your html webpage, add chester.min.js to the scripts, have fun :)
If you need help on how to do everything, the best idea would be to check the [online tests](http://funkaster.github.com/ChesterGL/test/)

Or look at the (not always updated) [online documentation](http://funkaster.github.com/ChesterGL/)

Sorry, the docs are not yet complete, but they will at some point :)
Just look at the examples and figure your way out from there. It shouldn't be too hard

Or wait until I write my "how to make an HTML5 game using chesterGL" (should be soon)

## How to join the fun

	 # clone the repo
	 git clone git://github.com/funkaster/ChesterGL.git
	 cd ChesterGL
     make debug

## How to just check this working

Point your browser (even your mobile browser!) to: [http://funkaster.github.com/ChesterGL/test/](http://funkaster.github.com/ChesterGL/test/)

## How to compile

You will need to modify the Makefile and change the location of closure compiler, as well as add the following externs:

* jquery-1.5.js
* webkit_console.js

All of them are in the svn repo of google closure. You also will need closure-compiler and the closure builder (+ the closure library, of course). You can read about that here:

https://developers.google.com/closure/library/docs/calcdeps

Check the Makefile for where to place them or modify that to suit your needs.

## Known problems

<strike>There's a weird problem that makes textures not load the first time, so you might need to reload the page. On webgl I fixed this by reloading the asset if the texture2d binding failed, in canvas mode you will need to reload the page</strike>. This was fixed by the asset loader.

## Known problems in canvas mode

* You will not get a z-position, for really obvious reasons.
* Color tinting will not work (I haven't found a way to replace that part)
* Block groups (batched sprites) will not add any improvement, for obvious reasons

## Roadmap

### 0.1

* Initial version

### 0.2

You can always look at the issues on the [github project](https://github.com/funkaster/ChesterGL/issues) and look for the right milestone.

* <strike>Fix BlockGroup (batched blocks in a single gl call)</strike>
* <strike>Improve canvas fallback</strike>
* <strike>Improve support for tile maps</strike>
* Improve speed on iOS (see test_ios.html). Right now we can get:
 * ~26fps with 12 moving sprites on an iPhone 4, iOS 4.3.5
 * ~35fps with 42 moving sprites on iTouch 4gen, iOS 5.0
* Improve support for Texture Packer sprite sheets
* <strike>Add time-based animations (shouldn't be too hard)</strike>

### 1.0

* Finish the webgl binding for iOS (what!?)
* Make it a real game library:
 * Add new interesting effects (light?)
 * Add more actions
* Add your ideas here