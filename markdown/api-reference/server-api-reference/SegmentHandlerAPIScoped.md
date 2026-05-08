---
title: SegmentHandler API - Scoped
description: Script include providing a chainable API for building an IDoc payload for a specific operation.Instantiates a new SegmentHandler object bound to an IDoc operation.Adds a predefined top-level segment of the type segmentName to the payload.Gets the built segment payload.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# SegmentHandler API- Scoped

Script include providing a chainable API for building an IDoc payload for a specific operation.

This script include requires the Zero Copy Connector for ERP \(com.sn\_erp\_integration\) store application and is provided within the sn\_erp\_integration namespace. For more information, refer to Zero Copy Connector for ERP.

Role required: sn\_erp\_integration.erp\_user

The SegmentHandler class:

-   Owns the root data object and the IDoc segment schema.
-   Enables creating top-level segments. For example, `E1EDK01`, `E1EDP01`, and so on.

For handling lower-level instances of a segment, such as a header or item, refer to [SegmentHandle API - Scoped](../../SegmentHandleScoped/concept/SegmentHandleAPIScoped.md#).

See also [sn\_erp\_integration API - Scoped, Global](../../sn_erp_integrationBoth/concept/sn_erp_integrationBothAPI.md#).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## SegmentHandler - SegmentHandler\(String operationId\)

Instantiates a new SegmentHandler object bound to an IDoc operation.

<table id="table_qlv_2gw_3hc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

operationId

</td><td>

String

</td><td>

The sys\_id of a configured ERP model operation.Table: ERP model operation \[sn\_erp\_integration\_model\_operation\]

</td></tr></tbody>
</table>The following example shows how to build a header and item with nested segments in one fluent chain. The structure depends on the configured schema. The schema pattern is arrays of segments with nested arrays.

```
let obj = new sn_erp_integration.SegmentHandler('460d3ff2ff5de210d3a2fffffffffff8');

obj.addSegment("E1EDK01")
    .addField("BELNR", "1000")
    .addField("CURCY", "USD")
    .endSegment()
    .addSegment("E1EDP01")
    .addField("MENGE", "50")
    .addField("POSEX", "0010")
    .addSegment("E1EDP20")
    .addField("AMENG", "10")
    .addField("WMENG", "5")
    .addSegment("E1EDP19")
    .addField("IDTNR", "MAT01")
    .endSegment()
    .endSegment()
    .endSegment();

gs.info(JSON.stringify(obj.getData(), null, 2));
```

Output:

```
{
  "data": {
    "E1EDK01": [{
      "BELNR": "1000",
      "CURCY": "USD"
    }],
      "E1EDP01": [{
        "MENGE": "50",
        "POSEX": "0010",
        "E1EDP20": [{
          "AMENG": "10",
          "WMENG": "5",
          "E1EDP19": [{
            "IDTNR": "MAT01"
          }]
        }]
      }]
  }
}
```

## SegmentHandler - addSegment\(String segmentName, Object values\)

Adds a predefined top-level segment of the type segmentName to the payload.

**Note:** The segment must be defined in the operation.

|Name|Type|Description|
|----|----|-----------|
|segmentName|String|Name of the top-level segment.|
|values|Object|Optional implementation in place of the addField\(\) method.|

|Type|Description|
|----|-----------|
|Object|[SegmentHandle](../../SegmentHandleScoped/concept/SegmentHandleAPIScoped.md#) for the new segment instance.|

The following example shows how to build a header and item with nested segments in one fluent chain. The structure depends on the configured schema. The schema pattern is arrays of segments with nested arrays.

```
let obj = new sn_erp_integration.SegmentHandler('460d3ff2ff5de210d3a2fffffffffff8');

obj.addSegment("E1EDK01")
    .addField("BELNR", "1000")
    .addField("CURCY", "USD")
    .endSegment()
    .addSegment("E1EDP01")
    .addField("MENGE", "50")
    .addField("POSEX", "0010")
    .addSegment("E1EDP20")
    .addField("AMENG", "10")
    .addField("WMENG", "5")
    .addSegment("E1EDP19")
    .addField("IDTNR", "MAT01")
    .endSegment()
    .endSegment()
    .endSegment();

gs.info(JSON.stringify(obj.getData(), null, 2));
```

Output:

```
{
  "data": {
    "E1EDK01": [{
      "BELNR": "1000",
      "CURCY": "USD"
    }],
      "E1EDP01": [{
        "MENGE": "50",
        "POSEX": "0010",
        "E1EDP20": [{
          "AMENG": "10",
          "WMENG": "5",
          "E1EDP19": [{
            "IDTNR": "MAT01"
          }]
        }]
      }]
  }
}
```

## SegmentHandler - getData\(\)

Gets the built segment payload.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_rkt_53x_3hc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Object containing segment data.

</td></tr><tr><td>

data

</td><td>

Wrapper for the payload object containing all top-level and nested segments.`{ data: <payloadObject> }`

The exact structure depends on the configured schema, but the pattern \(arrays of segments with nested arrays\) is the same.

Data type: Object

</td></tr></tbody>
</table>The following example shows how to build a header and item with nested segments in one fluent chain. The structure depends on the configured schema. The schema pattern is arrays of segments with nested arrays.

```
let obj = new sn_erp_integration.SegmentHandler('460d3ff2ff5de210d3a2fffffffffff8');

obj.addSegment("E1EDK01")
    .addField("BELNR", "1000")
    .addField("CURCY", "USD")
    .endSegment()
    .addSegment("E1EDP01")
    .addField("MENGE", "50")
    .addField("POSEX", "0010")
    .addSegment("E1EDP20")
    .addField("AMENG", "10")
    .addField("WMENG", "5")
    .addSegment("E1EDP19")
    .addField("IDTNR", "MAT01")
    .endSegment()
    .endSegment()
    .endSegment();

gs.info(JSON.stringify(obj.getData(), null, 2));
```

Output:

```
{
  "data": {
    "E1EDK01": [{
      "BELNR": "1000",
      "CURCY": "USD"
    }],
      "E1EDP01": [{
        "MENGE": "50",
        "POSEX": "0010",
        "E1EDP20": [{
          "AMENG": "10",
          "WMENG": "5",
          "E1EDP19": [{
            "IDTNR": "MAT01"
          }]
        }]
      }]
  }
}
```

