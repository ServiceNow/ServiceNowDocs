---
title: Level information
description: Each building \(drawing\) has a list of levels. Each level is a map and represents one floor, though that is not a rule.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/service-management-for-the-enterprise/service-management-legacy/r\_LevelInfo.html
release: australia
product: Service Management \(Legacy\)
classification: service-management-legacy
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Community file, GeoJSON map files, Space management, Facilities Service Management overview, Facilities Service Management, Service Management]
---

# Level information

Each building \(drawing\) has a list of levels. Each level is a map and represents one floor, though that is not a rule.

```
{
                    "id": 46475,
                    "obj_type": "Level",
                    "properties": {
                        "main": true,
                        "name": "1",
                        "parent_level": 46465,
                        "root_geom": 13958749,
                        "zlevel": 0
                    }
                },
                {
                    "id": 46477,
                    "obj_type": "Level",
                    "properties": {
                        "name": "2",
                        "type": "indoor",
                        "zlevel": 1
                    }
                },
                {
                    "id": 46478,
                    "obj_type": "Level",
                    "properties": {
                        "name": "3",
                        "type": "indoor",
                        "zlevel": 2
                    }
                }
```

-   Each level creates an fm\_level record.
-   The `id` is mapped to the external level id in fm\_level.
-   The `name` is mapped to the name field in fm\_level.
-   The `zlevel` orders the levels \(0 is ground level\).
-   The `main` property assigns the main level of the building and is used as the default map when a building is selected.
-   The `id` is used to find the correct level geometry file.

**Parent Topic:**[Community file](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/service-management-for-the-enterprise/service-management-legacy/r_CommunityFile.md)

