---
title: JSON file format
description: The JSON file should contain an array of monitor objects, either directly or wrapped in a checks or monitors property.
locale: en-US
release: yokohama
product: Synthetic Monitoring
classification: synthetic-monitoring
topic_type: reference
last_updated: "2026-02-24"
reading_time_minutes: 1
breadcrumb: [Synthetic monitoring reference, Synthetic monitoring, ITOM AIOps, IT Operations Management]
---

# JSON file format

The JSON file should contain an array of monitor objects, either directly or wrapped in a `checks` or `monitors` property.

## Direct array

```json
[
  {
    "name": "API Health Check",
    "method": "GET",
    "cmdb_ci": "sys_id_of_http_endpoint",
    "interval": 5,
    "locations": ["location_sys_id_1"],
    "enabled": true,
    "parent_service_sys_id": "service_sys_id",
    "support_group_sys_id": "group_sys_id"
  }
]
```

## Wrapped in object

```json
{
  "checks": [
    {
      "name": "API Health Check",
      "method": "GET",
      "cmdb_ci": "sys_id_of_http_endpoint",
      ...
    }
  ]
}
```

**Parent Topic:**[Synthetic monitoring reference](synthetic-monitoring-reference.md)

