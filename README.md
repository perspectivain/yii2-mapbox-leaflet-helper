Yii2 Mapbox with Leaflet helper
=======
Helper to use Mapbox with Leaflet

Usage
=======

Register in view file..

```
<?php
use perspectivain\mapbox\MapboxAPIHelper;

MapBoxAPIHelper::registerScript($this, ['drawing', 'fullScreen', 'minimap', 'omnivore']);
```

And use it...

```
L.mapbox.accessToken = 'XXXX';
    var map = L.mapbox
        .map('map', 'XXX.kjkb4j0a')
        .setView([LAT, LON], 13)
        .on('ready', function() {
            new L.Control.MiniMap(L.mapbox.tileLayer('XXX.kjkb4j0a')) //minimpa plugin use
                .addTo(map);
        });

    L.control.fullscreen().addTo(map); //fullscreen plugin use

    ...

```

Installing
======
The preferred way to install this extension is through composer.

```
{
  "require": {
    "perspectivain/yii2-mapbox-leaflet-helper": "*"
  }
}
```
