# BigBlueButton Adopter's Map

This is the repository for the [map of BigBlueButton](https://map.bigbluebutton.org) adopters.
The map shows the locations of participating BigBlueButton installations.

## Get Your Installation on the Map!

If you have a BigBlueButton installation and would like it to appear on the map, just create a [pull request](https://github.com/bigbluebutton/bigbluebutton-map/pulls) where you add your data to the file [adopters.geojson](adopters.geojson).
To do so, add this object with your data as a new line `features`-list in said file:

```json
{"type": "Feature", "properties": {"institution": "YOUR_INSTITUTION"}, "geometry": {"type": "Point", "coordinates": [0.0, 0.0]}}
```

Replace `YOUR_INSTITUION` and `[0.0, 0.0]` with your `lon` and `lat` coordinates and your good to go.

__⚠ Important:__

- Make sure the order is correct. Longitude first, then latitude.
- To avoid merge conflicts, insert yout institution as a single line somewhere in the middle (followed by a comma).


### How to get your Coordinates

You can use the tool [nominatim](https://nominatim.openstreetmap.org) to look up an address and get its coordinates.
Alternatively, you can right click on a location in google maps and you will be shown the coordinates in the menu.

Note that in both of these ways, you will have to **invert the order of the coordinates** (which you will get in `lat/lon`) for this map (where it is `lon/lat`).

## Idea & Origin

The idea for this map came up in the [regular meeting](https://hackmd.io/@lkiesow/bigbluebutton-adopters-meeting) of german speaking BigBlueButton adopters.
The inspiration and the [leaflet.js](https://leafletjs.com/) code comes from the [Opencast](https://opencast.org/) project and its similar [map.opencast.org](https://map.opencast.org/).
