# Highcharts Map Collection
[Website](https://www.highcharts.com) | [API](https://api.highcharts.com/highmaps) | [Demo](https://www.highcharts.com/demo/maps/all-maps) | [Issues](https://github.com/highcharts/map-collection-dist/issues)

## License
The use of the maps in this collection requires that you follow our terms and conditions that are stated in [License.md](https://github.com/highcharts/map-collection-dist/blob/master/LICENSE.md).

## Installation
### Install from npm

The Map Collection is available on npm as [@highcharts/map-collection](https://www.npmjs.com/package/@highcharts/map-collection) and can be installed as following:
```sh
npm i @highcharts/map-collection
```

1. Load a map in Node.js and use it in Highcharts Maps. Apply it in [`chart.map`](https://api.highcharts.com/highmaps/chart.map) to make it the default map for all series.

```js
const Highcharts = require('highcharts/highmaps.js'),
    map = require('@highcharts/map-collection/custom/world.topo.json');

Highcharts.mapChart('container', {
    chart: {
        map
    },
    // ...
});
```

Alternatively, you can apply different maps for different series ([view demo](https://jsfiddle.net/gh/get/library/pure/highcharts/highcharts/tree/master/samples/maps/series/affectsmapview/)):
```js
series: [{
    mapData: map,
    // ...
```


2. Join your data with the map. By default Highcharts Maps is set up to map your data against the `hc-key` property of the Map Collection, allowing you to define your data like this:
```js
data: [['us-ny', 0], ['us-mi', 5], ['us-tx', 3], ['us-ak', 5]]
```
For other data joining options, see the [`series.joinBy`](https://api.highcharts.com/highmaps/plotOptions.series.joinBy) and [`series.keys`](https://api.highcharts.com/highcharts/plotOptions.series.keys) options.

### Download the source code

The source code for the Map Collection is available on [GitHub](https://github.com/highcharts/map-collection-dist). Each release is tagged with the version number and linked assets: https://github.com/highcharts/map-collection-dist/releases

### Install from our CDN

By using the Highcharts CDN, you agree to abide by [this fair usage policy](https://www.highcharts.com/blog/fair-usage-policy-pdf) and the associated licensing terms.

In the [Map Collection reference](https://code.highcharts.com/mapdata/), each map name is followed by links to demos and data. Click the TopoJSON link and copy the URL.

Load the map and parse the JSON:

```js
const map = await fetch(
    'https://code.highcharts.com/mapdata/custom/world.topo.json'
).then(response => response.json());

Highcharts.mapChart('container', {
    chart: {
        map
    },
    // ...
});
```

Specific map versions are available via versioned URLs.
For example: <code>https://code.highcharts.com/mapdata/<strong>2.3</strong>/custom/world.topo.json</code>
corresponds to version **^2.3**.
