---
title: GlideSysListControl - Scoped
description: The GlideSysListControl API provides methods that enable you to determine if the New or Edit buttons are displayed.Instantiates a GlideSysListControl object.Returns the sys\_id for the control.Returns true if the edit button is not displayed.Returns true when the New button is not displayed.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideSysListControl- Scoped

The GlideSysListControl API provides methods that enable you to determine if the **New** or **Edit** buttons are displayed.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideSysListControl - GlideSysListControl\(String tableName\)

Instantiates a GlideSysListControl object.

|Name|Type|Description|
|----|----|-----------|
|tableName|String|Name of the table|

## GlideSysListControl - getControlID\(\)

Returns the sys\_id for the control.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|sys\_id of the control|

```
var sysListCtrl = new GlideSysListControl("incident");
var controlID = sysListCtrl.getControlID();
gs.info(controlID);
```

Output:

```
91a807a60a0a3c74012113e28b47ca2e
```

## GlideSysListControl - isOmitEditButton\(\)

Returns true if the edit button is not displayed.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|True when the edit button is not displayed.|

```
var sysListCtrl = new GlideSysListControl("incident");
var isOmitted = sysListCtrl.isOmitEditButton();
gs.info(isOmitted);
```

Output:

```
false
```

## GlideSysListControl - isOmitNewButton\(\)

Returns true when the New button is not displayed.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|True when the new button is not displayed.|

```
var sysListCtrl = new GlideSysListControl("incident");
var isOmitted = sysListCtrl.isOmitNewButton();
gs.info(isOmitted);
```

Output:

```
false
```

