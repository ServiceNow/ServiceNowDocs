---
title: Level geometry file
description: The level geometry file contains all the geometry for a given level. Each file is one map that can be rendered in the ServiceNow platform.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [GeoJSON map files, Space management, Facilities Service Management overview, Facilities Service Management, Service Management]
---

# Level geometry file

The level geometry file contains all the geometry for a given level. Each file is one map that can be rendered in the ServiceNow platform.

The file naming standard is:

-   Name with the `id` of the level found in the community map file
-   Must contain `-geojson-geojson-level-geom-`

For example, level 46475 is found in a file named `map-23641-mv-1-ev-1-geojson-geojson-level-geom-46475-fv-2.json`

The main component of the level file is an array of features, and looks like:

```
{
            "geometry": {
                "coordinates": [
                    [
                        [
                            -117.2057125,
                            32.8818922
                        ],
                        [
                            -117.2057223,
                            32.8819201
                        ],
                        [
                            -117.2057559,
                            32.8819117
                        ],
                        [
                            -117.205746,
                            32.8818838
                        ],
                        [
                            -117.2057125,
                            32.8818922
                        ]
                    ]
                ],
                "type": "Polygon"
            },
            "id": 13960404,
            "label_area": [
                -117.20573465198783,
                32.88190207162559,
                2.9198852018440062,
                2.9198852018440062,
                1.2818771600723267
            ],
            "location": {
                "coordinates": [
                    -117.2057347,
                    32.8819021
                ],
                "type": "Point"
            },
            "obj_type": "Geometry",
            "properties": {
                "display_name": "Reef Shark",
                "entities": [
                    1473100
                ],
                "facility": "room",
                "int_address": "Room B1-132"
            },
            "type": "Feature"
        },
```

-   The `geometry` object is the geoJSON representation of points that make up the object. For more information about the GeoJSON standard, see [http://geojson.org](http://geojson.org).
-   `Geometries` can be turned into fm\_space records.
-   The `id` is mapped to the external space id on the fm\_space record.
-   The `display_name` is the name of the space.
-   The `type` is the most important property. In the example, the class is a `facility` and the type for that class is a `room`. When parsing, these values determine:
    -   If an fm\_space record is created for the geometry
    -   If the fm\_space has a subtype
    -   If any default icons are assigned to a space
    -   If any default colors are assigned to the map

-   **[Valid classes](r_ValidClasses.md)**  
There are certain classes and class types that are valid for the level geometry file.

**Parent Topic:**[GeoJSON map files](r_GeoJSONMapFiles.md)

