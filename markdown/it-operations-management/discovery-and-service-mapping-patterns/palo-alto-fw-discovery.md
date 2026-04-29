---
title: Palo Alto Networks firewall discovery
description: The ServiceNow Discovery application uses the Next-Generation Palo Alto Firewall pattern to find Palo Alto Networks firewalls. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Available on-premise discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Palo Alto Networks firewall discovery

The ServiceNow Discovery application uses the Next-Generation Palo Alto Firewall pattern to find Palo Alto Networks firewalls. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

The discovery pattern uses a set of SNMP calls to find the Palo Alto Networks firewalls. Discovery uses the pattern to run horizontal discovery.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

-   Ensure that your network firewall device has SNMP access.
-   On the ServiceNow instance, configure SNMP credentials. For more information, see [SNMP credentials](https://www.servicenow.com/docs/access?context=c_SNMPCredentials&version=australia&pubname=australia-platform-security&ft:locale=en-US).
-   Add the SNMP system OID record for the Palo Alto Networks device to the ServiceNow instance. Update the following:
    -   Classifier: Palo Alto Firewall
    -   Class: Palo Alto Firewall Device
-   Deploy the pattern as follows:
    1.  Download and install [Firewall extension classes](https://www.servicenow.com/docs/access?context=cmdb-ci-class-models-fw&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US) from the ServiceNow Store. The app adds the new CMDB classes required for network firewall discovery.
    2.  Download and install the discovery pattern from the ServiceNow Store.
    3.  Sync the pattern with the appropriate MID Server.

## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Next-Generation Palo Alto Firewall Pattern.

|Field|Description|
|-----|-----------|
|IP Address \[ip\_address\]|IP address of the Palo Alto device.|
|Serial number \[serial\_number\]|Serial number of the Palo Alto device.|
|Fully qualified domain name \[fqdn\]|Fully qualified domain name \(FQDN\) of the Palo Alto device.|
|Manufacturer \[manufacturer\]|Palo Alto device manufacturer.|
|Model ID \[model\_id\]|Model ID of the Palo Alto device.|
|Operational status \[operational\_status\]|Indicates whether the Palo Alto device is in active state.|
|Hardware OS \[hardware\_os\]|OS running on the hardware.|
|Hardware OS Version \[hardware\_os\_version\]|OS version running on the hardware.|
|Description \[short\_description\]|Short description of the Palo Alto device.|
|Firmware version \[firmware\_version\]|Palo Alto device firmware version.|

|Field|Description|
|-----|-----------|
|IP Address \[ip\_address\]|IP address of the network adapter.|
|Alias \[alias\]|The user-assigned name for the network adapter.|
|Netmask \[netmask\]|Netmask of the network adapter.|
|MAC address \[mac\_address\]|MAC address of the network adapter.|
|Name \[name\]|Name of the network adapter.|
|Configuration Item \[cmdb\_ci\]|References the Palo Alto Firewall Device \[cmdb\_ci\_firewall\_device\_palo\_alto\] table.|

|Field|Description|
|-----|-----------|
|IP Address \[ip\_address\]|IP address of the Palo Alto firewall.|
|Netmask \[netmask\]|Netmask of the Palo Alto firewall.|
|Nic \[nic\]|References the Network Adapter \[cmdb\_ci\_network\_adapter\] table.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Domain Name System \(DNS\) name of the Palo Alto firewall device.|
|IP Address \[ip\_address\]|Host IP address.|

## CI relationships

These relationships are created to support Palo Alto Networks firewall discovery:

|CI|Relationship|CI|
|---|------------|---|
|IP Address \[cmdb\_ci\_ip\_address\]|References|Netwrk Adapter \[cmdb\_ci\_network\_adapter\]|
|Network Adapter \[cmdb\_ci\_network\_adapter\]|Owns::Owned by|IP Address \[cmdb\_ci\_ip\_address\]|
|Netwrk Adapter \[cmdb\_ci\_network\_adapter\]|References|Palo Alto Firewall Device \[cmdb\_ci\_firewall\_device\_palo\_alto\]|
|Palo Alto Firewall Device \[cmdb\_ci\_firewall\_device\_palo\_alto\]|Extends from|Firewall Device \[cmdb\_ci\_firewall\_device\]|
|Palo Alto Firewall Device \[cmdb\_ci\_firewall\_device\_palo\_alto\]|Owns::Owned by|Netwrk Adapter \[cmdb\_ci\_network\_adapter\]|
|Palo Alto Firewall Device \[cmdb\_ci\_firewall\_device\_palo\_alto\]|Owns::Owned by|IP Address \[cmdb\_ci\_ip\_address\]|
|Palo Alto Firewall Device \[cmdb\_ci\_firewall\_device\_palo\_alto\]|Uses::Used by|Router Interface \[dscy\_router\_interface\]|
|Router Interface \[dscy\_router\_interface\]|References|Palo Alto Firewall Device \[cmdb\_ci\_firewall\_device\_palo\_alto\]|
|Serial Number \[cmdb\_serial\_number\]|References|Palo Alto Firewall Device \[cmdb\_ci\_firewall\_device\_palo\_alto\]|

**Parent Topic:**[Available on-premise discovery patterns](../concept/available-patterns.md)

