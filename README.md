# Highmaps - Map Collection
[Website](https://www.highcharts.com) | [API](https://api.highcharts.com/highmaps) | [Demo](https://www.highcharts.com/maps/demo) | [Issues](https://github.com/highcharts/map-collection-dist/issues)

## Copyright
Some maps require that the original source of the map data is credited when used.
The copyright information is added to the chart credits by default, but please be aware that you will have to display this information somewhere else if you choose to disable chart credits.
Copyright information for each map can be found as properties in the GeoJSON and Javascript files.

See [code.highcharts.com/mapdata](https://code.highcharts.com/mapdata/) for overview of which maps requires creditation.

## Installation
### Install from our CDN
All our maps can be loaded from [code.highcharts.com/mapdata](https://code.highcharts.com/mapdata). The following example loads the map `custom/world.js`:
```html
<script src="https://code.highcharts.com/mapdata/custom/world.js"></script>
```
After the map is loaded in the browser then you can use it in Highmaps as following:
```javascript
Highcharts.mapChart('container', {
  chart: {
    map: 'custom/world'
  },
  // ...
});
```

### Install from npm
```
npm i @highcharts/map-collection
```
To load a map in Node.js and use it in Highmaps you can do the following:
```javascript
var Highcharts = require('highcharts/highmaps.js'),
    map = require('@highcharts/map-collection/custom/world.geo.json');

Highcharts.mapChart('container', {
  chart: {
    map: geojson
  },
  // ...
});
```