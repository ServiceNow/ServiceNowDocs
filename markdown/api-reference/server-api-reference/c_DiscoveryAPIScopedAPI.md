---
title: DiscoveryAPI - Scoped
description: The DiscoveryAPI class provides methods that launch a quick discovery of a single IPv4 address and return summaries of previously launched discovery statuses for a single configuration item \(CI\) or for all scanned CIs.Discovers a specified IPv4 address.Used to return a summary of a configuration item's Discovery status given the specific status sys\_id and IPv4 address.Used to return a summary of a CI Discovery status given a specific Discovery Status sys\_id.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# DiscoveryAPI- Scoped

The DiscoveryAPI class provides methods that launch a quick discovery of a single IPv4 address and return summaries of previously launched discovery statuses for a single configuration item \(CI\) or for all scanned CIs.

This class runs is in the `sn_discovery` namespace.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## DiscoveryAPI - discoverIpAddress\(String ipAddress, String application, String source\)

Discovers a specified IPv4 address.

A MID Server is selected automatically, based on the IP address provided or the application specified.

<table id="table_c4m_wcd_qcb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

application

</td><td>

String

</td><td>

Optional. Application configured for the MID Server.To define a **source** parameter but not an **application** parameter, use "NULL" as the place holder.

 Default: Discovery

</td></tr><tr><td>

ipAddress

</td><td>

String

</td><td>

IP address to discover.

</td></tr><tr><td>

source

</td><td>

String

</td><td>

Optional. Source of the Discovery. This same value appears in the optional **Source** field in the Discovery Status record, which indicates how the Discovery was triggered. Default: Discovery\_API

</td></tr></tbody>
</table><table id="table_d4m_wcd_qcb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

Discovery status record sys\_id.The following exceptions can be thrown during MID Server selection:

-   **NoSuitableMidServerFoundException**: `No appropriate MID Server available for this Discovery`
-   **BadArgumentException**: `Invalid argument detected during MID Server selection`

</td></tr></tbody>
</table>```
var sysid = sn_discovery.DiscoveryAPI.discoverIpAddress("11.23.125.39");
```

## DiscoveryAPI - reportCiIpAddressStatus\(Object ipAddress, Object discoveryStatusSysId\)

Used to return a summary of a configuration item's Discovery status given the specific status sys\_id and IPv4 address.

The following exceptions can be thrown:

-   **DiscoveryStatusNotFoundException**: `Displays this message: Discovery Status with sys id '<invalid value>' does not exist`
-   **DiscoveryDeviceHistoryNotFoundException**: `Device History with Discovery Status sys id '<invalid value>' and ipAddress '<invalid value>' does not exist`
-   **IllegalArgumentException** \(invalid input arguments\): This argument exception prevents input values from being null.
    -   `Discovery Status sys id can not be null`
    -   `ipAddress can not be null`
-   **IllegalArgumentException** \(values stored in database\): This argument exception prevents erroneous data from being returned to the caller in the case of bad attribute values.
    -   `Discovery Status 'state' property can not be null`
    -   `Device history 'source' property can not be null`
    -   `Device history 'issues' property is not an integer: <invalid value>`
    -   `Device history 'issues' property can not be less than 0: <invalid value>`

|Name|Type|Description|
|----|----|-----------|
|ipAddress|string|The IPv4 address that was scanned.|
|discoveryStatusSysId|string|The sys\_id of the Discovery status record for the IP address that was scanned.|

|Type|Description|
|----|-----------|
|array|JavaScript array of immutable [ReportCiStatusOutputJS](../../ReportCiStatusOutputJSScoped/concept/c_ReportCiStatusOutputJSScopedAPI.md#) objects.|

```
var ipResultObj = sn_discovery.DiscoveryAPI.reportCiIpAddressStatus(ipAddress, discoveryStatus);

```

## DiscoveryAPI - reportCiStatus\(Object discoveryStatusSysId\)

Used to return a summary of a CI Discovery status given a specific Discovery Status sys\_id.

The following exceptions can be thrown:

-   **DiscoveryStatusNotFoundException**: `Discovery Status with sys id '<invalid value>' does not exist`
-   **DiscoveryDeviceHistoryNotFoundException**: `Device History with Discovery Status sys id '<invalid value>' and ipAddress '<invalid value>' does not exist`
-   **IllegalArgumentException** \(invalid input arguments\): This argument exception prevents input values from being null.
    -   `Discovery Status sys id can not be null`
    -   `ipAddress can not be null`
-   **IllegalArgumentException** \(values stored in database\): This argument exception imposes post conditions on database access values.
    -   `Discovery Status 'state' property can not be null`
    -   `Device history 'source' property can not be null`
    -   `Device history 'issues' property is not an integer: <invalid value>`
    -   `Device history 'issues' property can not be less than 0: <invalid value>`

|Name|Type|Description|
|----|----|-----------|
|sys\_id|string|The sys\_id of a Discovery status record.|

|Type|Description|
|----|-----------|
|array|JavaScript array of immutable [ReportCiStatusOutputJS](../../ReportCiStatusOutputJSScoped/concept/c_ReportCiStatusOutputJSScopedAPI.md#) objects.|

```
var ipResultObjArray = sn_discovery.DiscoveryAPI.reportCiStatus(discoveryStatus);
for(var idx=0; idx < ipResultObjArray.length; idx++) {    
var ipResultObj = ipResultObjArray[idx]; 
```

