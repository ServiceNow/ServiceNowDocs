---
title: Cisco Switch Wireless Access Point \(WAP\) discovery
description: The ServiceNow Discovery application uses the Cisco WAPs extension to find Wireless Access Points \(WAPs\) that are controlled by a Cisco network switch. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Available on-premise discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Cisco Switch Wireless Access Point \(WAP\) discovery

The ServiceNow Discovery application uses the Cisco WAPs extension to find Wireless Access Points \(WAPs\) that are controlled by a Cisco network switch. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

This extension extends the Network Switch discovery pattern. For more information, see [Network switch and router discovery](../../discovery/reference/r_DataCollDiscoNWRouteAndSwitch.md).

Discovery uses the Cisco WAPs extension to run horizontal discovery.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

For prerequisites related to network switch discovery, see [Network switch and router discovery](../../discovery/reference/r_DataCollDiscoNWRouteAndSwitch.md).

In addition, these prerequisites must be in place for the Cisco WAPs extension:

-   Permission to query the OID: 1.3.6.1.4.1.14179.2.2.1.1.
-   The client must be able to run discovery patterns.
-   The client must use a Cisco network switch.
-   The client must have SNMP access to the Cisco network switch that controls the WAP devices.

## Data collected by Discovery during horizontal discovery

The data discovered by the Cisco WAP extension includes the following tables and fields.

|Tables and fields|Description|
|-----------------|-----------|
|Main CI Class \[cmdb\_ci\_wap\_network\]|
|Name \[name\]|Name assigned to the WAP. Collected from bsnAPName.|
|MAC Address \[mac\_address\]|The MAC address of the WAP. Collected from bsnAPDot3MacAddress.|
|IP address \[ip\_address\]|IP address of the WAP. Collected from bsnApIpAddress.|
|Firmware version \[firmware\_version\]|IOS version of the IOS Cisco WAP. Collected from bsnAPIOSVersion.|
|Serial Number \[serial\_number\]|WAP serial number. Collected from bsnAPSerialNumber.|
|Model number \[model\_number\]|WAP model. Collected from bsnAPModel.|
|snmp\_sys\_location|User-specified location of the WAP. Collected from bsnAPLocation.|
|Manufacturer \[manufacturer\]|Manufacturer of the WAP \(Cisco\).|

The Dependency Views map shows all discovered Cisco WAP CIs and the relationships between them.

![CIs and connections on a Dependency Views map](../image/cisco-waps-dependency-view.png)

## CI relationships

These relationships are created to support Cisco WAPs discovery:

|CI|Relationship|CI|
|---|------------|---|
|cmdb\_ci\_ip\_switch|Controller for :: Controlled by|cmdb\_ci\_wap\_network|

**Parent Topic:**[Available on-premise discovery patterns](../concept/available-patterns.md)

