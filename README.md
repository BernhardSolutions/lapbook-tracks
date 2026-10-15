# Lapbook race track layouts (OpenStreetMap-derived)

This dataset contains the race track outlines used in the Lapbook app that were derived from
OpenStreetMap data. It is published under the Open Database License (ODbL) 1.0, as required for
derivative databases of OpenStreetMap.

© OpenStreetMap contributors. Data available under the Open Database License:
https://opendatacommons.org/licenses/odbl/1-0/

## Contents

`lapbook-tracks-osm.json`: 54 tracks, 55 layouts. Per layout: name,
lap length in metres (measured from the geometry) and the outline as SVG path data in the viewBox
`0 0 100 60`. `osmRef` names one OpenStreetMap way of the track.

## How it was made

Ways tagged `highway=raceway` around each track were loaded from OpenStreetMap (Overpass API),
pit lanes removed, and the ways joined into closed loops. For each layout the loop closest to the
published lap length was chosen, projected, simplified (Douglas-Peucker) and fitted into the viewBox.

You may use, share and adapt this data under the terms of the ODbL. If you publicly use an adapted
version of this database, you must also offer it under the ODbL.
