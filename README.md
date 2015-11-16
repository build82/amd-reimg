# reimg (amd)
reimg - A JavaScript library for converting image formats (AMD module)

This lightweight image transformation module preforms common image conversions. 
Also, the module facilitates client retrieval of image elements.
All operations were coded upstream (& formatted as an AMD module in this fork f
or use in supporting JavaScript frameworks.

supported conversions : 
* svg -> base64
* svg -> canvas
* svg -> html `<img/>` element
* svg -> png
* canvas -> base64
* canvas -> html `<img/>` element
* canvas -> png

<br/>

include the module :
```html
<script>
	require(['build82/reimg'], function(reimg) {
		...
	});
</script>
```

<br/>

example :
```html
<script>
	require(['build82/reimg', 'dojo/dom', 'dojo/domReady!'], function(dom, reimg) {
		// convert svg element to png
		var svg_png = reimg.fromSvg(dom.byId('svg_element_id')).toPng();

		// convert canvas to png
		var canvas_png = reimg.fromCanvas(dom.byId('canvas_id')).toPng();

		// client download of canvas as png image
		reimg.fromCanvas(dom.byId('canvas_id')).downloadPng();
	});
</script>
```

