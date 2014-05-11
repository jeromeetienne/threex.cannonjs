threex.cannonjs
===============

threex.cannonjs  is a [threex game extension for three.js](http://jeromeetienne.github.io/threex/). It provides realistic physics easy to include in your own games. So you can take object in your game and make them fall as if it was the real world! You can code a [pool game](http://en.wikipedia.org/wiki/Pool_\(cue_sports\)) in a day! You make rocks falls from the sky in a realistic fasion! Sky is the limit! 
It is a warper over the excelent library [cannon.js](http://cannonjs.org/) physics library. It has been written by [Stefan Hedman](http://steffe.se/) or [@schteppe](https://twitter.com/schteppe) on twitter.

Show Don't Tell
===============
* [examples/basic.html](http://jeromeetienne.github.io/threex.cannonjs/examples/basic.html)
\[[view source](https://github.com/jeromeetienne/threex.cannonjs/blob/master/examples/basic.html)\] :
It shows this feature, and that one which is coded like that.
* [examples/domino.html](http://jeromeetienne.github.io/threex.cannonjs/examples/domino.html)
\[[view source](https://github.com/jeromeetienne/threex.cannonjs/blob/master/examples/domino.html)\] :
It show dominos falling on each others like on tv :)

A Screenshot
============
[![screenshot](https://raw.githubusercontent.com/jeromeetienne/threex.cannonjs/master/examples/images/screenshot-threex-cannonjs-512x512.jpg)](http://jeromeetienne.github.io/threex.cannonjs/examples/domino.html)

How To Install It
=================

You can install it manually. Just do 

```html
<script src='threex.cannonjs.js'></script>
```

You can install with [bower](http://bower.io/).

```bash
bower install threex.cannonjs
```

then you add that in your html

```html
<script src="bower_components/threex.cannonjs/threex.cannonjs.js"></script>
```


How To Install it ?
===================
Init the physics world

```javascript
var worldx	= new THREEx.CannonWorld().start();
```

create a physics body from a ```THREE.Mesh```

```javascript
var bodyx	= new THREEx.CannonBody(mesh)
```

add this physics body to our physics world and keep updating it

```javascript
worldx.add(bodyx)
updateFcts.push(function(delta, now){
	bodyx.update(delta, now);		
});
```
	
one may wish to setup an initial velocity

```javacript
bodyx.body.angularVelocity.set(0,2,0);
```
