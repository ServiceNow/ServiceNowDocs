---
title: SegmentHandle API - Scoped
description: Methods for handling a single instance of a segment, such as a header or item. This class is defined in the SegmentHandler script include.Adds a predefined field on the current segment instance to the payload.Adds a predefined nested child segment to the payload.Moves up one level in a schema.Gets the root SegmentHandler object, regardless of nesting depth.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# SegmentHandle API- Scoped

Methods for handling a single instance of a segment, such as a header or item. This class is defined in the SegmentHandler script include.

The [SegmentHandler](../../SegmentHandlerScoped/concept/SegmentHandlerAPIScoped.md#) script include requires the Zero Copy Connector for ERP \(com.sn\_erp\_integration\) store application and is provided within the sn\_erp\_integration namespace. For more information, refer to [Zero Copy Connector for ERP](https://www.servicenow.com/docs/access?context=erp-integration-overview&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US).

Role required: sn\_erp\_integration.erp\_user

Use the methods in this class for the following tasks:

-   Add fields to that specific segment instance.
-   Add nested/child segments under the instance.
-   Chain back to parent or root using the `endSegment()` or `root()` methods.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## SegmentHandle - addField\(String fieldName, String value\)

Adds a predefined field on the current segment instance to the payload.

|Name|Type|Description|
|----|----|-----------|
|fieldName|String|The name of the field to be added to the segment.|
|value|String|The value of the field to be added to the segment.|

|Type|Description|
|----|-----------|
|Object|Current SegmentHandle object for chaining.|

The following example shows how to create a segment payload. Use explicit variables when you want to keep references to specific segments.

-   Multiple obj.addSegment\("E1EDK01"\) calls generate multiple header segments.
-   Nested segments are created from the correct parent handle \(p01, p20, and so on\).
-   Handles like k01\_1, k01\_2, p01 can be reused later to add more fields or children.

```
var obj = new SegmentHandler('460d3ff2ff5de210d3a2fffffffffff8');

// Create first E1EDK01
let k01_1 = obj.addSegment("E1EDK01")
    .addField("BELNR", "1000")
    .addField("CURCY", "USD");

// Create another E1EDK01 
let k01_2 = obj.addSegment("E1EDK01")
    .addField("BELNR", "2000")
    .addField("CURCY", "EUR");

// Create E1EDP01 with nested segments
let p01 = obj.addSegment("E1EDP01")
    .addField("MENGE", "50")
    .addField("POSEX", "0010");

let p20 = p01.addSegment("E1EDP20")
    .addField("AMENG", "10")
    .addField("WMENG", "5");

p20.addSegment("E1EDP19")
    .addField("IDTNR", "MAT01");

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

## SegmentHandle - addSegment\(String segmentName, Object values\)

Adds a predefined nested child segment to the payload.

|Name|Type|Description|
|----|----|-----------|
|segmentName|String|Name of a segment nested within the current segment.|
|values|Object|Optional implementation in place of the addField\(\) method.|

|Type|Description|
|----|-----------|
|Object|Returns a new SegmentHandle for the child segment.|

The following example shows how to create a segment payload. Use explicit variables when you want to keep references to specific segments.

-   Multiple obj.addSegment\("E1EDK01"\) calls generate multiple header segments.
-   Nested segments are created from the correct parent handle \(p01, p20, and so on\).
-   Handles like k01\_1, k01\_2, p01 can be reused later to add more fields or children.

```
var obj = new SegmentHandler('460d3ff2ff5de210d3a2fffffffffff8');

// Create first E1EDK01
let k01_1 = obj.addSegment("E1EDK01")
    .addField("BELNR", "1000")
    .addField("CURCY", "USD");

// Create another E1EDK01 
let k01_2 = obj.addSegment("E1EDK01")
    .addField("BELNR", "2000")
    .addField("CURCY", "EUR");

// Create E1EDP01 with nested segments
let p01 = obj.addSegment("E1EDP01")
    .addField("MENGE", "50")
    .addField("POSEX", "0010");

let p20 = p01.addSegment("E1EDP20")
    .addField("AMENG", "10")
    .addField("WMENG", "5");

p20.addSegment("E1EDP19")
    .addField("IDTNR", "MAT01");

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

## SegmentHandle - endSegment\(\)

Moves up one level in a schema.

|Name|Type|Description|
|----|----|-----------|
|None| ||

<table id="table_rkt_53x_3hc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Parent handle or root handler.-   From a child segment, returns the parent SegmentHandle object.
-   From the top-level segment, returns the parent SegmentHandler object.

Use the root\(\) method to return the root SegmentHandler object.

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

## SegmentHandle - root\(\)

Gets the root SegmentHandler object, regardless of nesting depth.

|Name|Type|Description|
|----|----|-----------|
|None| ||

|Type|Description|
|----|-----------|
|Object|SegmentHandler at the root level.|

The following example shows how to move between levels in a schema.

```
let p19 = p20.addSegment("E1EDP19").addField("IDTNR", "MAT01");
p19.endSegment()     // back to E1EDP20
    .endSegment()    // back to E1EDP01
    .root()          // back to SegmentHandler
    .addSegment("E1EDK01").addField("BELNR", "3000");
```

