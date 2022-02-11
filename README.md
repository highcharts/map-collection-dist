# Highcharts Map Collection
[Website](https://www.highcharts.com) | [API](https://api.highcharts.com/highmaps) | [Demo](https://www.highcharts.com/maps/demo) | [Issues](https://github.com/highcharts/map-collection-dist/issues)

## License
The use of the maps in this collection requires that you follow our terms and conditions that are stated in [License.md](https://github.com/highcharts/map-collection-dist/blob/master/LICENSE.md).

## Installation
### Install from our CDN
All our maps can be loaded from [code.highcharts.com/mapdata](https://code.highcharts.com/mapdata). The following example loads the map `custom/world.topo.json`:
```js
const topology = await fetch(
    'https://code.highcharts.com/mapdata/custom/world.topo.json'
).then(response => response.json());
```
After the map is loaded in the browser then you can use it in Highcharts Maps as following:
```js
Highcharts.mapChart('container', {
  chart: {
    map: topology
  },
  // ...
});
```

### Install from npm
```
npm i @highcharts/map-collection
```
To load a map in Node.js and use it in Highcharts Maps you can do the following:
```js
var Highcharts = require('highcharts/highmaps.js'),
    map = require('@highcharts/map-collection/custom/world.topo.json');

Highcharts.mapChart('container', {
  chart: {
    map: topojson
  },
  // ...
});
```
