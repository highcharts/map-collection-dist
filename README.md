# Highmaps - Map Collection
[Website](https://www.highcharts.com) | [API](https://api.highcharts.com/highmaps) | [Demo](https://www.highcharts.com/maps/demo) | [Issues](https://github.com/highcharts/map-collection-dist/issues)

## License
The use of the maps in this collection requires that you follow our terms and conditions that are stated in [License.md](https://github.com/highcharts/map-collection-dist/blob/master/LICENSE.md).

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
