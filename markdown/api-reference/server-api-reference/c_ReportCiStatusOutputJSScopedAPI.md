---
title: ReportCiStatusOutputJS - Scoped
description: The ReportCiStatusOutputJS API provides methods that return specific object properties for the DiscoveryAPI reportCiIpAddressStatus method and then converts the information into a JSON string.Returns the state of the scanned CI.Returns the value in the cmdb\_ci field from the discovery\_device\_history table for the CI being scanned.Returns the value from the State field in the Discovery Status \[discovery\_status\] table.Returns the value from the source field in the discovery\_device\_history table for the CI being scanned.Returns the value from the issues field in the discovery\_device\_history table for the CI being scanned.Returns the value from the issues\_link field in the discovery\_device\_history table for the CI being scanned.Serializes the ReportCiStatusOutputJS object.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# ReportCiStatusOutputJS- Scoped

The ReportCiStatusOutputJS API provides methods that return specific object properties for the DiscoveryAPI reportCiIpAddressStatus method and then converts the information into a JSON string.

This class runs is in the `sn_discovery` namespace.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## ReportCiStatusOutputJS - getCiOperationStatus\(\)

Returns the state of the scanned CI.

This is a calculated field based on the last\_state field in discovery\_device\_history table and the state field in the discovery\_status table.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_t4x_hfb_scb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

string

</td><td>

The three possible states returned by this method are:-   Processing: Discovery is still processing the request.
-   Successful: A CI was created or updated.
-   NotSuccessful: A CI was not created or updated, and the Discovery status was Completed or Cancelled.

</td></tr></tbody>
</table>```
var ipResultObj = sn_discovery.DiscoveryAPI.reportCiIpAddressStatus(ipAddress, discoveryStatus);
gs.info("ipResultObj(CiOperationStatus): " + ipResultObj.getCiOperationStatus());

```

## ReportCiStatusOutputJS - getCmdbCI\(\)

Returns the value in the cmdb\_ci field from the discovery\_device\_history table for the CI being scanned.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|string|Sys\_id of the CI created or updated. This value can be null in the case of intermediate results before a CI is created.|

```
var ipResultObj = sn_discovery.DiscoveryAPI.reportCiIpAddressStatus(ipAddress, discoveryStatus);
gs.info("ipResultObj(cmdb): " + ipResultObj.getCmdbCI());

```

## ReportCiStatusOutputJS - getDiscoveryState\(\)

Returns the value from the **State** field in the Discovery Status \[discovery\_status\] table.

The values returned by this method are used to calculate the value returned by the [getCiOperationStatus\(\)](c_ReportCiStatusOutputJSScopedAPI.md#) method

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_otv_blb_scb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

string

</td><td>

The possible states returned by this method are:-   Starting
-   Active
-   Complete
-   Cancelled

</td></tr></tbody>
</table>```
var ipResultObj = sn_discovery.DiscoveryAPI.reportCiIpAddressStatus(ipAddress, discoveryStatus);
gs.info("ipResultObj(discoveryState): " + ipResultObj.getDiscoveryState());

```

## ReportCiStatusOutputJS - getIpAddress\(\)

Returns the value from the source field in the discovery\_device\_history table for the CI being scanned.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|string|The IP address of the CI being scanned.|

```
var ipResultObj = sn_discovery.DiscoveryAPI.reportCiIpAddressStatus(ipAddress, discoveryStatus);
gs.info("ipResultObj(IpAddress): " + ipResultObj.getIpAddress());
```

## ReportCiStatusOutputJS - getIssues\(\)

Returns the value from the issues field in the discovery\_device\_history table for the CI being scanned.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|integer|Number of issues in this Discovery for this CI.|

```
var ipResultObj = sn_discovery.DiscoveryAPI.reportCiIpAddressStatus(ipAddress, discoveryStatus);
gs.info("ipResultObj(issues): " + ipResultObj.getIssues());
```

## ReportCiStatusOutputJS - getIssuesLink\(\)

Returns the value from the issues\_link field in the discovery\_device\_history table for the CI being scanned.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_flk_m5b_scb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

string

</td><td>

The issues\_link field from the discovery\_device\_history table.This value may be null or an anchor tag defining a hyperlink to a page that provides the list of issues associated with the Discovery Status and CI \(IP address\).

</td></tr></tbody>
</table>```
var ipResultObj = sn_discovery.DiscoveryAPI.reportCiIpAddressStatus(ipAddress, discoveryStatus);
gs.info("ipResultObj(issues_link): " + ipResultObj.getIssuesLink());
```

## ReportCiStatusOutputJS - toJson\(\)

Serializes the **ReportCiStatusOutputJS** object.

This method throws the **IllegalArgumentException** exception, `Cannot serialize object, e` when the method is unable to serialize the object. The **e** is the exception object, which provides the exception message and trace.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|string|Serialized instance of the **ReportCiStatusOutputJS** object into a JSON string.|

```
var ipResultObj = sn_discovery.DiscoveryAPI.reportCiIpAddressStatus(ipAddress, discoveryStatus);
gs.info("ipResultObj(json): " + ipResultObj.toJson());
```

