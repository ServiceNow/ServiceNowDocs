---
title: Building information
description: Each drawing in the campus map file represents a building or campus overview. The campus overview is a map that shows the entire campus, and is included for multi-building campuses only.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Community file, GeoJSON map files, Space management, Facilities Service Management overview, Facilities Service Management, Service Management]
---

# Building information

Each drawing in the campus map file represents a building or campus overview. The campus overview is a map that shows the entire campus, and is included for multi-building campuses only.

```
{
            "id": 28500,
            "levels": [
 
           . . . . . . . . . . . <See level section>>
 
            ],
            "obj_type": "Drawing",
            "properties": {
                "display_name": "SD Campus Building 1",
                "map_type": "Shopping Mall",
                "name": "San Diego Campus Building 1"
            },
            "ref_frame": {
                "angle_deg": -16.554,
                "height": 782.891,
                "local2m": 0.05893868944676606,
                "transform": [
                    6.043292819573627e-07,
                    1.508500607965198e-07,
                    1.7962840831123188e-07,
                    -5.075094178111973e-07,
                    -117.206364,
                    32.882096
                ],
                "width": 1505.19
            }
        },
```

-   This information is used to create a building in alm\_building.
-   The `id` is mapped to the external building id in alm\_building.
-   The `display_name` is used to name the building.
-   The `ref frame` is used to align the building horizontally and vertically. The GeoJSON data, contains WGS 84 information used to rotate the image so it displays at a natural horizontal orientation.

**Parent Topic:**[Community file](r_CommunityFile.md)

