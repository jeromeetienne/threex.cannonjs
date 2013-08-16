threex.cannonjs
===============

```threex.cannonjs``` is a wrapper to ease access between
[cannon.js](http://cannonjs.org/)
and
[three.js](http://threejs.org/).

There is a [domino demo live](http://jeromeetienne.github.io/threex/src/threex.cannonjs/examples/domino.html)
 and its 
[source](https://github.com/jeromeetienne/threex/blob/master/src/threex.cannonjs/examples/domino.html).
Here is the basic example 
[live](http://jeromeetienne.github.io/threex/src/threex.cannonjs/examples/basic.html)
 and its 
[source](https://github.com/jeromeetienne/threex/blob/master/src/threex.cannonjs/examples/basic.html).

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


## how to use it

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
