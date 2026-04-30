---
title: GlideappCalculationHelper - Global
description: The GlideappCalculationHelper API is a scriptable object that provides methods that add items to an existing request or request the recalculation of the price of a request.Adds a specific catalog item to an existing request. This API should be used only before a request \(REQ\) is approved. After the REQ is approved, the RITM process is not initiated.Recalculates the price of all of the items in a specified request.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideappCalculationHelper- Global

The GlideappCalculationHelper API is a scriptable object that provides methods that add items to an existing request or request the recalculation of the price of a request.

The methods for this API are used in global server-side scripts \(script includes, business rules, etc.\). There is currently no support for scoped applications.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideappCalculationHelper - addItemToExistingRequest\(String requestID, String catalogID, String quantity\)

Adds a specific catalog item to an existing request. This API should be used only before a request \(REQ\) is approved. After the REQ is approved, the RITM process is not initiated.

|Name|Type|Description|
|----|----|-----------|
|requestID|String|Sys\_id of the request to which to add the catalog item\(s\)|
|catalogID|String|Sys\_id of the catalog item to add to the request|
|quantity|String|Number \(quantity\) of the specified catalog item to be add to the request.|

|Type|Description|
|----|-----------|
|void| |

```
var catItemId = "04b7e94b4f7b4200086eeed18110c7fd";
var requestId = "6eed229047801200e0ef563dbb9a71c2";
var helper = new GlideappCalculationHelper();
helper.addItemToExistingRequest(requestId, catItemId, "1");
```

## GlideappCalculationHelper - rebalanceRequest\(String requestID\)

Recalculates the price of all of the items in a specified request.

|Name|Type|Description|
|----|----|-----------|
|requestID|String|Sys\_id of the request for which to recalculate the price|

|Type|Description|
|----|-----------|
|void| |

```
var catItemId = "04b7e94b4f7b4200086eeed18110c7fd";
var requestId = "6eed229047801200e0ef563dbb9a71c2";
var helper = new GlideappCalculationHelper();
//Add an item to the request
helper.addItemToExistingRequest(requestId, catItemId, "1");
//Re-calculate the price of the request after adding the item
helper.rebalanceRequest(requestId);
```

