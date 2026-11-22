# Desk series – OpenStreetMap data (Taskbar Railway)

This repository contains one file, `stations-odbl.json`: the real railway lines used in the desktop game **Taskbar Railway**. For each of 12 lines it lists the station names, their order, positions (latitude/longitude) and the straight-line distance from the first stop (`km`).

## Source and attribution

**© OpenStreetMap contributors.** The data was extracted once from [OpenStreetMap](https://www.openstreetmap.org/) on 2026-11-22 via the Overpass API (route relations and their stop members). The field `quelle` of each line names the OpenStreetMap relation, and `abgerufen` gives the date of the extract.

Lines: Amsterdam, Berlin, Hamburg, Köln, London, München, New York, Paris, Rhein-Main, Tokio, Wien, Zürich. Line numbers, network or operator names, colours and logos were deliberately left out; only place names are used.

Changes made: only stops with a stop role were kept, in route order. Distances were computed as straight lines between consecutive stops, and the result was converted to this JSON format.

## Licence

`stations-odbl.json` is a derived database of OpenStreetMap. It is made available under the [Open Database License (ODbL) 1.0](https://opendatacommons.org/licenses/odbl/1-0/); the full text is in `LICENSE`. More information: https://www.openstreetmap.org/copyright

The game Taskbar Railway itself (code, graphics, sound) is not part of this repository and is not covered by the ODbL. The same file also ships with the game (`data/flutter_assets/assets/osm/stations-odbl.json`).

## Updating

The file is generated in the game's repository with `dart run tool/odbl_datei.dart` and copied here unchanged.
