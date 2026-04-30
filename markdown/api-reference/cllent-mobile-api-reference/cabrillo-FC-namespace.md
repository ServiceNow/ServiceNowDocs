---
title: cabrillo.flowControl - Client
description: Cabrillo JS functions for managing the flow of a web view.Indicates to the client that the web flow is complete.Indicates to the client that the web flow is complete and the client should update the native screens.
locale: en-US
release: xanadu
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Client mobile API reference, API reference, API implementation and reference]
---

# cabrillo.flowControl - Client

Cabrillo JS functions for managing the flow of a web view.

**Parent Topic:**[Client mobile API reference](../../../../../build/applications/concept/api-client-mobile.md)

## cabrillo.flowControl - flowEnded\(String flowName\)

Indicates to the client that the web flow is complete.

The mobile client can then take appropriate action, which typically is to close the web view.

|Name|Type|Description|
|----|----|-----------|
|flowName|String|Optional. The name of the web flow to close.|

|Type|Description|
|----|-----------|
|None| |

```
var flowName = 'Open Incident Flow';
cabrillo.flowControl.flowEnded(flowName);
```

## cabrillo.flowControl - flowEndedWithUpdate\(String flowName, boolean clientRefreshNeeded\)

Indicates to the client that the web flow is complete and the client should update the native screens.

The mobile client can then take appropriate action, which typically is to close the web view.

<table id="table_oyf_tnn_wbb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

flowName

</td><td>

String

</td><td>

Optional. The name of the web flow to close.

</td></tr><tr><td>

clientRefreshNeeded

</td><td>

Boolean

</td><td>

Optional. Flag that indicates whether the client needs to refresh the displayed data.Valid values:

-   true: The client needs to refresh the displayed data.
-   false: The client doesn't need to refresh the displayed data.

Default: false

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

```
var flowName = 'Open Incident Flow';
var clientRefreshNeeded = true;
cabrillo.flowControl.flowEnded(flowName, clientRefreshNeeded);
```

