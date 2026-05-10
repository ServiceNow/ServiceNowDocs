---
title: Next-Generation Cisco Firewall discovery
description: The ServiceNow Discovery application uses the Next Generation Cisco Firewall pattern to find Cisco firewalls. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Available on-premise discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Next-Generation Cisco Firewall discovery

The ServiceNow Discovery application uses the Next Generation Cisco Firewall pattern to find Cisco firewalls. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

The discovery pattern uses a set of SNMP calls to find the Cisco firewalls. Discovery uses the pattern to run horizontal discovery.

You can use this pattern on the ServiceNow AI Platform® using the Madrid release or later.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

-   Ensure that your network firewall device has SNMP access.
-   On the ServiceNow instance, configure SNMP credentials. For more information, see [SNMP credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/c_SNMPCredentials.md).
-   Add the SNMP system OID record for the Cisco device to the ServiceNow instance. Update the following:
    -   Classifier: Cisco Firewall
    -   Class: Cisco Firewall Device
-   Deploy the pattern as follows:
    1.  Download and install [Firewall extension classes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/cmdb-ci-class-models/cmdb-ci-class-models-fw.md) from the ServiceNow Store. The app adds the new CMDB classes required for network firewall discovery.
    2.  Download and install the Discovery and Service Mapping Patterns application from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).
    3.  Sync the pattern with the appropriate MID Server.

## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Next Generation Cisco Firewall pattern.

|Field|Description|
|-----|-----------|
|Serial number \[serial\_number\]|Serial number of the device.|
|Name \[name\]|Administratively assigned name for this managed node. By convention, this is the node's fully qualified domain name \(FQDN\).|
|IP Address \[ip\_address\]|IP address of the device.|
|Firmware version \[firmware\_version\]|Firmware version.|
|Fully qualified domain name \[fqdn\]|FQDN of the device.|
|Manufacturer \[manufacturer\]|Device manufacturer.|
|Model ID \[model\_id\]|Device model name.|
|Harware OS \[hardware\_os\]|Operating system \(OS\) running on the hardware.|
|Hardware OS Version \[hardware\_os\_version\]|OS version running on the hardware.|
|Description \[short\_description\]|Short description of the Cisco device.|
|Operational status \[operational\_status\]|Indicates if the device is in active state.|
|Hardware Status \[hardware\_status\]|Detailed description of the current status of the resource.|

|Field|Description|
|-----|-----------|
|IP Address \[ip\_address\]|IP address of the Cisco firewall.|
|Netmask \[netmask\]|Netmask of the Cisco firewall.|
|Nic \[nic\]|References the Network Adapter \[cmdb\_ci\_network\_adapter\] table.|

|Field|Description|
|-----|-----------|
|IP Address \[ip\_address\]|IP address of the network adapter.|
|Alias \[alias\]|User-assigned name for the network adapter.|
|Netmask \[netmask\]|Netmask of the network adapter.|
|MAC Address \[mac\_address\]|MAC address of the network adapter.|
|Name \[name\]|Name of the network adapter.|
|Configuration Item \[cmdb\_ci\]|References the Cisco Firewall Device \[cmdb\_ci\_firewall\_device\_cisco\] table.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the Domain Name System \(DNS\).|
|IP Address \[ip\_address\]|IP address of the DNS.|

This Dependency Views map on the Cisco Firewall Device CI shows the Cisco Firewall Device.

![CIs and connections on a Dependency Views map](../image/cisco-fw-dependency-views.png)

## CI relationships

These relationships are created to support Cisco firewall discovery.

|CI|Relationship|CI|
|---|------------|---|
|Cisco Firewall Device \[cmdb\_ci\_firewall\_device\_cisco\]|Owns::Owned by|IP Address \[cmdb\_ci\_ip\_address\]|
|Cisco Firewall Device \[cmdb\_ci\_firewall\_device\_cisco\]|Owns::Owned by|Network Adapter \[cmdb\_ci\_network\_adapter\]|
|Cisco Firewall Device \[cmdb\_ci\_firewall\_device\_cisco\]|Uses::Used by|Router Interface \[dscy\_router\_interface\]|
|IP Address \[cmdb\_ci\_ip\_address\]|References|Network Adapter \[cmdb\_ci\_network\_adapter\]|
|Network Adapter \[cmdb\_ci\_network\_adapter\]|Owns::Owned by|IP Address \[cmdb\_ci\_ip\_address\]|
|Network Adapter \[cmdb\_ci\_network\_adapter\]|References|Cisco Firewall Device \[cmdb\_ci\_firewall\_device\_cisco\]|
|Router Interface \[dscy\_router\_interface\]|References|Cisco Firewall Device \[cmdb\_ci\_firewall\_device\_cisco\]|
|Serial Number \[cmdb\_serial\_number\]|References|Cisco Firewall Device \[cmdb\_ci\_firewall\_device\_cisco\]|

**Parent Topic:**[Available on-premise discovery patterns](../concept/available-patterns.md)

