GeoJSON-GolfCourses
===================
[GeoJSON](http://geojson.org) of all named golf course boundaries in [OpenStreetMap](http://www.openstreetmap.org).

Inspired by cageyjames and his [GeoJSON](https://github.com/cageyjames/GeoJSON-Ballparks) of baseball stadiums and by jssisskind and his [GeoJSON](https://github.com/sisskind/GeoJSON-Football) of NFL stadiums, I've created a GeoJSON of golf course boundaries.

###Currently Included:
  1. Named golf course boundaries from North America

###Initial Process:
  1. Download [geofabrik](http://download.geofabrik.de/north-america.html) export of North America.
  2. Filter the extract using [Osmosis](http://wiki.openstreetmap.org/wiki/Osmfilter)
`osmosis --read-xml north-america-latest.osm.pbf --tag-filter accept-ways leisure=golf_course --used-node --write-xml namerica.osm`
  3. Load into QGIS and filter `name IS NOT null`
  4. Save as GeoJSON including BBox

###Coming Soon:
  1. European golf courses
