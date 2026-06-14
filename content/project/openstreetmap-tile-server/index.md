---
title: "openstreetmap-tile-server"
summary: "A self-hosted OpenStreetMap tile server configuration optimized for offline/air-gapped environments."
tags:
  - OpenStreetMap
  - Tile server
  - Offline maps
  - Docker
  - GIS
  - Systems administration
date: 2024-05-23
featured: true
image:
  filename: featured.png
  focal_point: Smart
links:
  - icon: github
    icon_pack: fab
    name: Code
    url: https://github.com/Harvester57/openstreetmap-tile-server
---

**openstreetmap-tile-server** is a deployment configuration and guide for hosting a local, offline OpenStreetMap (OSM) tile server. Designed specifically for high-security, air-gapped, or isolated network environments, it enables applications to render mapping data without requesting external web resources.

This stack leverages Docker to simplify deployment, package ingestion, and render pipeline orchestration.

### Stack Components

*   **Database:** PostgreSQL with PostGIS extensions to manage geographical data.
*   **Ingestion:** Osm2pgsql for importing and styling `.osm.pbf` map files.
*   **Renderer:** Mapnik and renderd for rendering vector map data into raster tiles.
*   **Tile Server:** Apache with mod_tile to serve pre-rendered or on-the-fly map tiles.
*   **Front-End Integration:** Simple Leaflet-based templates for verifying local tile rendering.

### Usage Outline

Pre-render tiles or import specific geographical datasets (e.g., country extracts from Geofabrik) to serve them locally within your network. Useful for command-and-control centers, localized flight-tracking platforms, and telemetry dashboards operating in secure perimeters.
