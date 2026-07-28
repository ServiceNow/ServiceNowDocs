---
title: Examples of Retrieving Data from Nokia Altiplano via REST API
description: Examples of Retrieving Data from Nokia Altiplano via REST API.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-service-ops/telecommunications-service-operations-management/retrieving-data-nokia-altiplano-API.html
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: reference
last_updated: "2026-07-28"
reading_time_minutes: 1
breadcrumb: [Reference, Telecommunications Service Operations Management]
---

# Examples of Retrieving Data from Nokia Altiplano via REST API

Examples of Retrieving Data from Nokia Altiplano via REST API.

## URL format

Versioned URL: POST: `altiplano-indexsearch/latestcompleted-inv/_search`

## For OLT

```

{
    "_source": [
        "deviceAVmetadata",
        "inventorymetadata",
        "inventorydata.ietf-hardware:hardware",
        "inventorydata.ietf-hardware:hardware-state",
        "inventorydata.nokia-state:state"
    ],
    "sort": [{"_id": {"order": "asc"}}],    
    "from": 0,  
    "size":300
}

```

## For ONU

```

{
      "query": {
            "bool": {
                "should": [
                    {
                        "exists": {
                            "field": "inventorydata.ietf-interfaces:interfaces-state.interface.bbf-xponvani:v-ani.onu-present-on-this-olt.detected-serial-number"
                        }
                    }
                ]
            }
    },
    "_source": [
         "inventorydata.ietf-interfaces:interfaces-state.interface.bbf-xponvani:v-ani.onu-present-on-this-olt.detected-serial-number",
        "inventorydata.bbf-fiber-onu-emulated-mount:onus.onu.root.ietf-hardware-mounted:hardware-state",
        "inventorydata.bbf-fiber-onu-emulated-mount:onus.onu.name"
     ],
    "sort": [{"_id": {"order": "asc"}}],    
    "from": 0,  
    "size": 3
}
```

**Parent Topic:**[Telecommunications Service Operations Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/components-installed-with-tsom.md)

