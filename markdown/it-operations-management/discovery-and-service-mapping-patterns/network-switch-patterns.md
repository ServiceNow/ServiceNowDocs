---
title: Network switch discovery using patterns
description: The Discovery and Service Mapping Patterns application uses the Network Switch pattern to find network switches in your environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: xanadu
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Network switch discovery using patterns

The Discovery and Service Mapping Patterns application uses the Network Switch pattern to find network switches in your environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

To learn about network switches and their versions that you can discover, refer to [Detailed information on products discovered by ITOM Visibility](r_SupportedApplications.md).

For information on probe-based network switch and router discovery, see [Network switch and router discovery](../../discovery/reference/r_DataCollDiscoNWRouteAndSwitch.md).

## Prerequisites

-   **Verify that the applications are up to date**
    -   Discovery and Service Mapping Patterns
    -   Visibility Content
-   **Verify IP address information**

    The switch must contain IP address information for successful discovery.

-   **Verify that exit interface routing rules are configured and reachable**

    The switch that provides the IP address must have exit interface routing rules configured and be reachable for successful discovery.

-   **Create SNMP credentials**

    Create SNMP Community Credentials or SNMPv3 credentials. For more information, see [SNMP credentials](https://www.servicenow.com/docs/csh?topicname=c_SNMPCredentials&version=yokohama&pubname=yokohama-platform-security).

-   **Configure properties for switch discovery**

    Navigate to `sys_properties.list` and verify that the **glide.discovery.L3\_mapping** system property is set to **true**.

    You can configure these additional properties for network switch discovery.

<table id="table_c5g_sh1_1gc"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

glide.discovery.max\_concurrent\_invocations\_per\_schedule

</td><td>

Sets a maximum number of scheduled invocations for the same Discovery schedule. It prevents a backlog of scheduled runs if Discovery does not finish before the next one starts. The value is an integer that represents the max number of automated invocations that can run concurrently for the same schedule. If the limit is reached, subsequent scheduled invocations are canceled. A value of 0 or any negative number disables this property.

-   **Type:** integer
-   **Default value:** 3
-   **Location:** **Discovery Definition** &gt; **Properties**
**Note:** This property does not apply to schedules that have a 'Run after' configuration set to 'Even if canceled'.

</td></tr><tr><td>

glide.discovery.bgp\_router\_disable

</td><td>

Disables running the SNMP – Routing pattern when discovering a router running the BGP protocol. If you must populate the Device Neighbors \[discovery\_device\_neighbors\] table during horizontal layer 2 discovery of the BGP-enabled devices, set the **BGP router exploration disable** property to **No**. Notice that enabling this property can cause performance issues including out-of-memory issues on the MID Server.

-   **Type:** true \| false
-   **Default value:** true
-   **Location:** **Discovery Definition** &gt; **Properties**


</td></tr></tbody>
</table>
## Discovering stacked switches

Network switch discovery supports Cisco stacked switches. Multiple switches in the stack are identified by the primary IP address. Discovery identifies each member of the stack by elements such as the primary IP address, a name associated with the switch, and the stack mode. The relationship is created between a primary switch and the secondary switches.

The primary switch has all the fields listed in the IP Switch \[cmdb\_ci\_ip\_switch\] table. The secondary switch has name, serial\_number, model\_id, manufacturer, stack, and stack\_mode.

**Note:** If all ports on a switch are open for port 161, the switch has an IP per port, but the same serial number is used across all ports. The configuration item \(CI\) identification is based on the serial number, therefore, discovery updates the existing record every time instead of creating a new one.

## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Network Switch pattern.

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the switch.|
|Model ID \[model\_id\]|Hardware model ID of the switch.|
|Manufacturer \[manufacturer\]|Switch manufacturer.|
|Install Status \[install\_status\]|Install status of the device. Default value is Installed.|
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
|Stack \[stack\]|Indicates whether a network device is part of a stacked group of switches operating as one unit. Possible values are true or false.|
|Stack Mode \[stack\_mode\]|Stacking architecture or role of a network device within a stack. For example: standalone, stack\_master, or stack\_member.|
|Location \[location\]|Location where the switch is installed.|

|Field|Description|
|-----|-----------|
|IP Address \[ip\_address\]|IP address of the network switch.|
|Netmask \[netmask\]|Netmask of the network switch.|
|Nic \[nic\]|References the Network Adapter \[cmdb\_ci\_network\_adapter\] table.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the network adapter.|
|IP Address \[ip\_address\]|IP address of the network adapter.|
|Netmask \[netmask\]|Netmask of the network adapter.|
|MAC Address \[mac\_address\]|MAC address of the network adapter.|
|Alias \[alias\]|User-assigned name for the network adapter.|
|Configuration Item \[cmdb\_ci\]|References the IP Switch \[cmdb\_ci\_ip\_switch\] table.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the Domain Name System \(DNS\).|
|IP Address \[ip\_address\]|IP address of the DNS.|

## CI relationships

Discovery creates these relationships to support the network switch discovery.

|CI|Relationship|CI|
|---|------------|---|
|Exit Interface Routing Rule \[dscy\_route\_interface\]|References|IP Switch \[cmdb\_ci\_ip\_switch\]|
|IP Address \[cmdb\_ci\_ip\_address\]|References|Network Adapter \[cmdb\_ci\_network\_adapter\]|
|IP Switch \[cmdb\_ci\_ip\_switch\]|Contains::Contained by|Switch Forwarding Rule \[dscy\_swtch\_fwd\_rule\]|
|IP Switch \[cmdb\_ci\_ip\_switch\]|Contains::Contained by|Switch Partition \[dscy\_swtch\_partition\]|
|IP Switch \[cmdb\_ci\_ip\_switch\]|Contains::Contained by|Switchport \[dscy\_switchport\]|
|IP Switch \[cmdb\_ci\_ip\_switch\]|Owns::Owned by|IP Address \[cmdb\_ci\_ip\_address\]|
|IP Switch \[cmdb\_ci\_ip\_switch\]|Owns::Owned by|Network Adapter \[cmdb\_ci\_network\_adapter\]|
|IP Switch \[cmdb\_ci\_ip\_switch\]|Uses::Used by|Exit Interface Routing Rule \[dscy\_route\_interface\]|
|IP Switch \[cmdb\_ci\_ip\_switch\]|Uses::Used by|Next Hop Routing Rule \[dscy\_route\_next\_hop\]|
|IP Switch \[cmdb\_ci\_ip\_switch\]|Uses::Used by|Router Interface \[dscy\_router\_interface\]|
|Network Adapter \[cmdb\_ci\_network\_adapter\]|Owns::Owned by|IP Address \[cmdb\_ci\_ip\_address\]|
|Network Adapter \[cmdb\_ci\_network\_adapter\]|References|IP Switch \[cmdb\_ci\_ip\_switch\]|
|Network ARP Table \[discovery\_net\_arp\_table\]|References|IP Switch \[cmdb\_ci\_ip\_switch\]|
|Next Hop Routing Rule \[dscy\_route\_next\_hop\]|References|IP Switch \[cmdb\_ci\_ip\_switch\]|
|Router Interface \[dscy\_router\_interface\]|References|IP Switch \[cmdb\_ci\_ip\_switch\]|
|Serial Number \[cmdb\_serial\_number\]|References|IP Switch \[cmdb\_ci\_ip\_switch\]|
|Switch Bridge Port Table \[discovery\_switch\_bridge\_port\_table\]|References|IP Switch \[cmdb\_ci\_ip\_switch\]|
|Switch Forwarding Rule \[dscy\_swtch\_fwd\_rule\]|References|IP Switch \[cmdb\_ci\_ip\_switch\]|
|Switch Forwarding Table \[discovery\_switch\_fwd\_table\]|References|IP Switch \[cmdb\_ci\_ip\_switch\]|
|Switch Partition \[sdcy\_swtch\_partition\]|References|IP Switch \[cmdb\_ci\_ip\_switch\]|
|Switch Spanning Tree Table \[discovery\_switch\_spanning\_tree\_table\]|References|IP Switch \[cmdb\_ci\_ip\_switch\]|
|Switchport \[dscy\_switchport\]|References|IP Switch \[cmdb\_ci\_ip\_switch\]|

**Parent Topic:**[Available discovery patterns](../concept/available-patterns.md)

