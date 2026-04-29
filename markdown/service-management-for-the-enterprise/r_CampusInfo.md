---
title: Campus information
description: Sample code for campus and map set properties.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Community file, GeoJSON map files, Space management, Facilities Service Management overview, Facilities Service Management, Service Management]
---

# Campus information

Sample code for campus and map set properties.

```
"entity_version": 1,
    "id": 23641,
    "languages": [
        "en"
    ],
    "location": {
        "coordinates": [
            -117.20527,
            32.882205
        ],
        "type": "Point"
    },
    "map_version": 1,
    "obj_type": "CommunityMap",
    "properties": {
        "city": "San Diego",
        "com_type": "Business Campus",
        "country": "US",
        "default_lang": "en",
        "name": "ServiceNow - San Diego Campus",
        "postal code": "92121",
        "state": "CA",
        "street address": "4810 Eastgate Mall"
    }
```

-   The `id` is a unique id for this campus and is mapped to the database as the **external campus id** field in the campus table.

-   The `entity_version` and `map_version` are the versions of the map sets, helpful when a campus has multiple map sets.
-   The `location` contains WGS 84 coordinates providing the overall latitude and longitude of the campus.

    **Note:** Latitude and Longitude are set at the Campus level only.

-   Other data provides the name and address of the campus and is used to create a location in the location table for the campus.

**Parent Topic:**[Community file](r_CommunityFile.md)

