# MapOverlay

Overlays maps of two different places at the same ground scale, so you can
see how they compare.

Pan and zoom the top map. The other map follows its zoom, corrected for
latitude, since Web Mercator stretches the map further from the equator.
Swap which map is on top to pan the other one. The URL holds the current
comparison, so you can bookmark or share it.

Uses [Leaflet](https://leafletjs.com/),
[OpenStreetMap](https://www.openstreetmap.org/copyright) tiles and
[Nominatim](https://nominatim.org/) search. None of them needs an API key.

## Running

Serve it over HTTP, e.g. GitHub Pages, or locally:

    python3 -m http.server 8000

then open http://localhost:8000/. Opening `index.html` as a `file:` URL
doesn't work, because the OSM tile servers refuse requests with no Referer.
