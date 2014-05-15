Portland-park-data
==================

park data in JSON for PDX

## Data Structure

an array of objects that look like this;

``` JSON
{
    "Address":"SE 17th Ave & Taylor St",
    "OwnedAcres":"5.8799999999999999",
    "Property":"Colonel Summers Park",
    "PropertyID":"12","SubArea":"SE",
    "UnownedAcres":"0",
    "YearAcquired":"1921",
    "Zip":"97214",
    "amenities":[
        "basketball court",
        "disabled access picnic area",
        "paths : paved",
        "picnic site : reservable",
        "picnic tables",
        "playground",
        "softball field",
        "statue or public art",
        "tennis court",
        "volleyball court",
        "picnic shelter"
    ],
    "loc":{
        "lon":-122.64692,
        "lat":45.515669
    }
}
```

## Installing

You can install from npm by adding to your package.json

``` JSON
  "author": "meandave",
  "license": "MIT",
  "dependencies": {
    "level-geospatial": "0.0.5",
    "level": "^0.18.0",
    "pdx-park-data": "meandavejustice/Portland-park-data"
  }
```

then running `npm install` then you can include it in your project with
as you would any other node_module.

``` javascript
var parks = require('Portland-park-data');
var db = require('level')('./parkData');
var geo = require('level-geospatial')(db);

console.log(parks);
```

If you don't have node/npm installed you can get it with cURL:
`curl -O https://raw.githubusercontent.com/meandavejustice/Portland-park-data/master/parks.json`

Or you can of course just clone the repo:
`git clone git@github.com:meandavejustice/Portland-park-data.git`
