---
title: Network router discovery using patterns
description: The Discovery and Service Mapping Patterns application uses the Network Router pattern to find network routers in your environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/discovery-and-service-mapping-patterns/network-router-patterns.html
release: zurich
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Available on-premise discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Network router discovery using patterns

The Discovery and Service Mapping Patterns application uses the Network Router pattern to find network routers in your environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

To learn about network routers and their versions that you can discover, refer to [Detailed information on products discovered by ITOM Visibility](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/itom-visibility/r_SupportedApplications.md).

For information on probe-based network switch and router discovery, see [Network switch and router discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/itom-visibility/r_DataCollDiscoNWRouteAndSwitch.md).

## Cisco Nexus Virtual Routing and Forwarding \(VRF\) data model

The pattern introduces the following CI class starting with Discovery and Service Mapping Patterns version 1.35.0.

|CI class|Extends from|
|--------|------------|
|Virtual Routing and Forwarding \(VRF\) \[cmdb\_ci\_virtual\_routing\_forwarding\]|Configuration Item \[cmdb\_ci\]|

## Prerequisites

-   **Verify that the applications are up to date**
    -   Discovery and Service Mapping Patterns
    -   Visibility Content
-   **Verify IP address information**

    The router must contain IP address information for successful discovery.

-   **Verify that exit interface routing rules are configured and reachable**

    The router that provides the IP address must have exit interface routing rules configured and be reachable for successful discovery.

-   **Create SNMP credentials**

    Create SNMP Community Credentials or SNMPv3 credentials. For more information, see [SNMP credentials](https://www.servicenow.com/docs/access?context=c_SNMPCredentials&version=yokohama).

-   **Configure properties for router discovery**

    Navigate to `sys_properties.list` and verify that the **glide.discovery.L3\_mapping** system property is set to **true**.

    You can configure these additional properties for network router discovery.

<table id="table_ljq_hnr_hkc"><thead><tr><th>

System property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

glide.discovery.max\_concurrent\_invocations\_per\_schedule

</td><td>

Sets a maximum number of scheduled invocations for the same Discovery schedule. It prevents a backlog of scheduled runs if Discovery does not finish before the next one starts. The value is an integer that represents the max number of automated invocations that can run concurrently for the same schedule. If the limit is reached, subsequent scheduled invocations are canceled. A value of 0 or any negative number disables this property.

-   **Type:** integer
-   **Default value:** 3
**Note:** This property does not apply to schedules that have a 'Run after' configuration set to 'Even if canceled'.

</td></tr><tr><td>

glide.discovery.bgp\_router\_disable

</td><td>

Disables running the SNMP – Routing pattern when discovering a router running the BGP protocol. If you must populate the Device Neighbors \[discovery\_device\_neighbors\] table during horizontal layer 2 discovery of the BGP-enabled devices, set the **glide.discovery.bgp\_router\_disable** property to **false**. Notice that enabling this property can cause performance issues including out-of-memory issues on the MID Server.

-   **Type:** Boolean
-   **Default value:** true


</td></tr><tr><td>

glide.discovery.disable\_next\_hop\_data

</td><td>

Skips populating the Next Hop Routing Rule table for BGP-enabled routers during horizontal discovery. The device, its physical interfaces, and its neighbors are still discovered.This property takes effect only when the**glide.discovery.bgp\_router\_disable** property is set to false.

-   **Type:** Boolean
-   **Default value:** false
For more information, see [Turn off next-hop route data collection for BGP routers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery-and-service-mapping-patterns/turn-off-bgp-next-hop-collection.md).

</td></tr></tbody>
</table>-   **For Cisco Nexus VRF discovery**

    Verify the following requirements:

    -   Discovery and Service Mapping Patterns starting from version 1.35.0.
    -   Read permissions for the following commands on the Cisco Nexus device:
        -   `sh vrf`
        -   `sh hsrp br`
        -   `sh ip interface vrf all`
        -   `sh ipv6 interface vrf all`
    -   Create SSH credentials for the Cisco Nexus user. For more information, see [SSH credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/r_SSHCredentialsForm.md).

## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Network Router pattern.

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the router.|
|Model ID \[model\_id\]|Hardware model ID of the router.|
|Manufacturer \[manufacturer\]|Router manufacturer.|
|Serial number \[serial\_number\]|Unique hardware serial number of the router.|
|IP Address \[ip\_address\]|IP addresses assigned to interfaces.|
|Description \[short\_description\]|Device description.|
|Can route IP \[can\_route\]|Indicates whether the IP pockets can be routed between networks. Possible values are true or false.|
|Can partition VLANs \[can\_partitionvlans\]|Indicates whether the local area network \(LAN\) can be partitioned. Possible values are true or false.|
|Can switch IP \[can\_switch\]|Indicates whether a network device has Layer 2 switching capabilities. Possible values are true or false.|
|Physical interface count \[physical\_interface\_count\]|Number of physical interfaces.|
|Ports \[ports\]|Individual network interface \(physical or logical\) used to connect devices such as computers, servers, access points, or uplinks to switches or routers.|
|Discovery Protocol ID \[discovery\_proto\_id\]|Unique identifier of the device participating in the Cisco Discovery Protocol \(CDP\) or Link Layer Discovery Protocol \(LLDP\) protocol.|
|Discovery Protocol Type \[discovery\_proto\_type\]|Protocol type. Possible values are CDP or LLDP.|

|Field|Description|
|-----|-----------|
|IP Address \[ip\_address\]|IP address of the router.|
|Netmask \[netmask\]|Netmask of the router.|
|Nic \[nic\]|References the Network Adapter \[cmdb\_ci\_network\_adapter\] table.|
|Owned By Configuration Item \[owned\_by\_cmdb\_ci\]\*|References the Virtual Routing and Forwarding \(VRF\) \[cmdb\_ci\_virtual\_routing\_forwarding\] table|

\* Populated for Cisco Nexus VRF discovery only.

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the network adapter.|
|IP Address \[ip\_address\]|IP address of the network adapter.|
|Netmask \[netmask\]|Netmask of the network adapter.|
|MAC Address \[mac\_address\]|MAC address of the network adapter.|
|Alias \[alias\]|User-assigned name for the network adapter.|
|Configuration Item \[cmdb\_ci\]|References the IP Router \[cmdb\_ci\_ip\_router\] table.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the Domain Name System \(DNS\).|
|IP Address \[ip\_address\]|IP address of the DNS.|

|Field|Description|
|-----|-----------|
|Name \[name\]|VRF name as configured on the network device.|
|VRF ID \[vrf\_id\]|VRF identifier assigned by the network device operating system \(OS\).|
|Display Name \[display\_name\]|Display name composed of the VRF name and the associated network device name.|
|Configuration Item \[configuration\_item\]|References the IP Router \[cmdb\_ci\_ip\_router\] table.|

\* Populated for Cisco Nexus VRF discovery only.

## CI relationships

Discovery creates these relationships and references to support the network router discovery. References link to records in other tables and don't appear in the CI Relationship \[cmdb\_rel\_ci\] table.

|CI|Relationship|CI|
|---|------------|---|
|IP Router \[cmdb\_ci\_ip\_router\]|Contains::Contained by|Switch Forwarding Rule \[dscy\_swtch\_fwd\_rule\]|
|IP Router \[cmdb\_ci\_ip\_router\]|Contains::Contained by|Switch Partition \[dscy\_swtch\_partition\]|
|IP Router \[cmdb\_ci\_ip\_router\]|Contains::Contained by|Switchport \[dscy\_switchport\]|
|IP Router \[cmdb\_ci\_ip\_router\]|Owns::Owned by|IP Address \[cmdb\_ci\_ip\_address\]|
|IP Router \[cmdb\_ci\_ip\_router\]|Owns::Owned by|Network Adapter \[cmdb\_ci\_network\_adapter\]|
|IP Router \[cmdb\_ci\_ip\_router\]|Uses::Used by|Exit Interface Routing Rule \[dscy\_route\_interface\]|
|IP Router \[cmdb\_ci\_ip\_router\]|Uses::Used by|Next Hop Routing Rule \[dscy\_route\_next\_hop\]|
|IP Router \[cmdb\_ci\_ip\_router\]|Uses::Used by|Router Interface \[dscy\_router\_interface\]|
|Network Adapter \[cmdb\_ci\_network\_adapter\]|Owns::Owned by|IP Address \[cmdb\_ci\_ip\_address\]|
|IP Router \[cmdb\_ci\_ip\_router\]|Owns::Owned by|Virtual Routing and Forwarding \(VRF\) \[cmdb\_ci\_virtual\_routing\_forwarding\]\*|
|Virtual Routing and Forwarding \(VRF\) \[cmdb\_ci\_virtual\_routing\_forwarding\]|Contains::Contained by|IP Address \[cmdb\_ci\_ip\_address\]\*|

\* Created for Cisco Nexus VRF discovery only.

|CI/Table|Field|Referenced CI|
|--------|-----|-------------|
|Network Adapter \[cmdb\_ci\_network\_adapter\]|Configuration Item \[cmdb\_ci\]|IP Router \[cmdb\_ci\_ip\_router\]|
|Network ARP Table \[discovery\_net\_arp\_table\]|Configuration Item \[cmdb\_ci\]|IP Router \[cmdb\_ci\_ip\_router\]|
|Next Hop Routing Rule \[dscy\_route\_next\_hop\]|Configuration Item \[cmdb\_ci\]|IP Router \[cmdb\_ci\_ip\_router\]|
|Router Interface \[dscy\_router\_interface\]|Configuration Item \[cmdb\_ci\]|IP Router \[cmdb\_ci\_ip\_router\]|
|Serial Number \[cmdb\_serial\_number\]|Configuration Item \[cmdb\_ci\]|IP Router \[cmdb\_ci\_ip\_router\]|
|Switch Bridge Port Table \[discovery\_switch\_bridge\_port\_table\]|Configuration Item \[cmdb\_ci\]|IP Router \[cmdb\_ci\_ip\_router\]|
|Switch Forwarding Rule \[dscy\_swtch\_fwd\_rule\]|Configuration Item \[cmdb\_ci\]|IP Router \[cmdb\_ci\_ip\_router\]|
|Switch Forwarding Table \[discovery\_switch\_fwd\_table\]|Configuration Item \[cmdb\_ci\]|IP Router \[cmdb\_ci\_ip\_router\]|
|Switch Partition \[sdcy\_swtch\_partition\]|Configuration Item \[cmdb\_ci\]|IP Router \[cmdb\_ci\_ip\_router\]|
|Switch Spanning Tree Table \[discovery\_switch\_spanning\_tree\_table\]|Configuration Item \[cmdb\_ci\]|IP Router \[cmdb\_ci\_ip\_router\]|
|Switchport \[dscy\_switchport\]|Configuration Item \[cmdb\_ci\]|IP Router \[cmdb\_ci\_ip\_router\]|
|Exit Interface Routing Rule \[dscy\_route\_interface\]|Configuration Item \[cmdb\_ci\]|IP Router \[cmdb\_ci\_ip\_router\]|
|IP Address \[cmdb\_ci\_ip\_address\]|Nic \[nic\]|Network Adapter \[cmdb\_ci\_network\_adapter\]|
|IP Address \[cmdb\_ci\_ip\_address\]|Owned By Configuration Item \[owned\_by\_cmdb\_ci\]|Virtual Routing and Forwarding \(VRF\) \[cmdb\_ci\_virtual\_routing\_forwarding\]\*|
|Virtual Routing and Forwarding \(VRF\) \[cmdb\_ci\_virtual\_routing\_forwarding\]|Configuration Item \[configuration\_item\]|IP Router \[cmdb\_ci\_ip\_router\]\*|

\* Populated for Cisco Nexus VRF discovery only.

-   **[Turn off next-hop route data collection for BGP routers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery-and-service-mapping-patterns/turn-off-bgp-next-hop-collection.md)**  
You can turn off Next Hop Routing Rule \[dscy\_route\_next\_hop\] table collection for BGP-enabled routers to reduce MID Server memory load during router discovery.

**Parent Topic:**[Available on-premise discovery patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery-and-service-mapping-patterns/available-patterns.md)

