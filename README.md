# Kataster

A QGIS plugin for searching and viewing Estonian cadastre data.

## Features

- **Smart search box** — Search by:
  - **Cadastre unit tunnus** (e.g., `78401:101:4011`) → view version history
  - **Address** (e.g., `Kolde pst 8, Tallinn`) → auto-resolve to cadastre unit(s)
  - **Border point number** (e.g., `100000311380`) → view measurement details on the map

- **Version history** — Load one or multiple versions of a cadastre unit:
  - Double-click a version row to load it instantly
  - Check multiple rows and click "Laadi valitud versioonid" to load several at once
  - Versions are styled with transparent fills and colored outlines, grouped by tunnus
  - Map automatically zooms and flashes the unit when you search

- **Border points (piiripunktid)** — Look up survey points:
  - View coordinates, measurement method, surveyor, and other attributes
  - Point is displayed on the map and grouped under "Piiripunktid"

- **Tidy layer tree** — Loaded layers are organized into groups:
  - Versions grouped by cadastre unit tunnus
  - Border points in a shared group

## Installation

Copy the `katastri_plugin` folder to your QGIS plugins directory:
- **Windows**: `C:\Users\<username>\AppData\Roaming\QGIS\QGIS3\profiles\default\python\plugins`
- **Linux**: `~/.local/share/QGIS/QGIS3/profiles/default/python/plugins`
- **macOS**: `~/Library/Application Support/QGIS/QGIS3/profiles/default/python/plugins`

Then enable it in QGIS: **Plugins → Manage and Install Plugins → search "Kataster"**.

## Usage

1. **Open the panel** — Click the Kataster toolbar icon (or go to **Web → Kataster**)
2. **Search** — Type a tunnus, address, or border-point number and press Enter
3. **Load versions** — Double-click a row to load one, or check boxes and click the button to load several
4. **View on map** — Loaded versions appear as grouped layers; the map zooms automatically

## Data sources

- **Cadastre versions**: Estonian Land Board (Maa- ja Ruumiamet) WFS service
- **Address search (gazetteer)**: In-ADS address lookup service
- **Border points**: Estonian Land Board cadastre point layer

## License

Released under the [MIT License](LICENSE) — free to use, modify, and distribute.


