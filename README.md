
# Intro

Leaflet.Canvas is a full map canvas layer that allows you to render stuff on top of a map with HTML5 canvas element.
Leaflet provides a canvas layer which provides one canvas per tile to render. Some things require a single canvas to render them

# how to use

just subclass it and override render method

```
L.TorqueLayer = L.CanvasLayer.extend({
    render: function() {
        var canvas = this.getCanvas();
        var ctx = canvas.getContext('2d');
        // render
    }
});

```

if you are creating an animation just use ``redraw`` method to schedule a canvas refresh


# license

MIT



