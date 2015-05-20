folding-tile
=============

See the [component page](https://namannehra.github.io/folding-tile/) for more information.

## Installing

Install using bower.
```
bower install --save namannehra/folding-tile#latest
```

Import webcomponents.js for browsers which lack native support for web components. Import folding-tile.
```
<script src="bower_components/webcomponentsjs/webcomponents.min.js"></script>
<link rel="import" href="bower_components/folding-tile/folding-tile.html">
```

## Getting Started

Element providing folding tile.
```
<folding-tile></folding-tile>
```

#### Play and Pause
Animation can be paused and played usign pause() and play() methods
```
var tile = document.querySelector('folding-tile');
tile.pause();
```

#### Customize
The default tile cycles between four colors; by default they are blue, red, yellow and green. These colors and duration on animation can be customized using attributes. Don't use rgba colors.
```
<folding-tile duration="4000" color1="grey" color2="purple" color3="grey" color4="purple"></folding-tile>
```

#### Customize on run-time
play() method needs to be called for changed to take effect if properties are changed using javascript after element is created.
```
var tile = document.querySelector('folding-tile');
tile.duration = 40000;
tile.color1 = 'black';
tile.play; //changes won't take effect if play() in not called
```

#### CSS
Can be styled using CSS.
```
<style shim-shadowdom>
	folding-tile {
		border-radius: 32px;
		/* It is recommended to keep height and width equal */
		height: 128px;
		width: 128px;
		opacity: 0.7;
		/* It is recommended to set perspective equal to double of height */
		-webkit-perspective: 256px;
		perspective: 256px;
	}
	folding-tile::shadow .shadow {
		backgroung-color: rgba(255,255,255,0.3);
	}
</style>
```

## Help and Support

Send an email for support or feature request.
```
naman.nehra98@gmail.com
```