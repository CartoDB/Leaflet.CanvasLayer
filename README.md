
# Intro

Leaflet.CanvasLayer is a full map canvas layer that allows you to render stuff on top of a map with HTML5 canvas element.
Leaflet provides a [tiled canvas layer](http://leafletjs.com/reference.html#tilelayer-canvas) which provides one canvas per tile to render. Some things require a single canvas to render them properly.

see a running example: http://cartodb.github.io/Leaflet.CanvasLayer/example.html

# how to use

just subclass it and override render method

```
var MyLayer = L.CanvasLayer.extend({
    render: function() {
        var canvas = this.getCanvas();
        var ctx = canvas.getContext('2d');
        // render
    }
});


// create and add to the map
var layer = new MyLayer();
layer.addTo(map);

```

if you are creating an animation just use ``redraw`` method to schedule a canvas refresh

# example

 - used for map animation in http://mwcimpact.com/

# license

MIT



