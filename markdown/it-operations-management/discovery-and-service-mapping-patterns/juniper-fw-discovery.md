---
title: Next-Generation Juniper Network Firewall discovery
description: The ServiceNow Discovery application uses the Next-Generation Juniper Network Firewall discovery pattern to find Juniper network firewalls. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/discovery-and-service-mapping-patterns/juniper-fw-discovery.html
release: zurich
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Available on-premise discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Next-Generation Juniper Network Firewall discovery

The ServiceNow Discovery application uses the Next-Generation Juniper Network Firewall discovery pattern to find Juniper network firewalls. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

The discovery pattern uses a set of SNMP calls to find the Juniper network firewalls. Discovery uses the pattern to run horizontal discovery.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Juniper Network Firewall data model

The Next-Generation Juniper Network Firewall pattern introduces the following CI classes that are part of the Juniper firewall data model.

|CI class|Extends from|
|--------|------------|
|Firewall Device \[cmdb\_ci\_firewall\_device\]|IP Firewall \[cmdb\_ci\_ip\_firewall\]|
|Juniper Firewall Device \[cmdb\_ci\_firewall\_device\_juniper\]|Firewall Device \[cmdb\_ci\_firewall\_device\]|
|Firewall Cluster \[cmdb\_ci\_firewall\_cluster\]|Cluster \[cmdb\_ci\_cluster\]|
|Juniper Firewall Cluster \[cmdb\_ci\_firewall\_cluster\_juniper\]|Firewall Cluster \[cmdb\_ci\_firewall\_cluster\]|
|Firewall Device Group \[cmdb\_ci\_firewall\_device\_group\]|Configuration Item \[cmdb\_ci\]|
|Firewall Manager \[cmdb\_ci\_firewall\_manager\]|Configuration Item \[cmdb\_ci\]|
|Firewall Security Policy \[cmdb\_ci\_firewall\_security\_policy\]|Configuration Item \[cmdb\_ci\]|

## Prerequisites

-   Ensure that your network firewall device has SNMP access.
-   On the ServiceNow instance, configure SNMP credentials.
-   Add the SNMP system OID record for the Juniper device to the ServiceNow instance. Update the following:
    -   Classifier: Juniper Firewall
    -   Class: Juniper Firewall Device

Deploy the pattern as follows:

1.  Download and install the CMDB CI Class Models: Release 1.10.0 from the ServiceNow Store. The app adds the new CMDB classes required for network firewall discovery. For more information, see [Firewall extension classes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/cmdb-ci-class-models/cmdb-ci-class-models-fw.md).
2.  Download and install the discovery pattern from the ServiceNow Store.
3.  Sync the pattern with the appropriate MID Server.

## Data collected by Discovery during horizontal discovery

The discovered data includes the following tables and fields.

|Field|Description|
|-----|-----------|
|Name \[name\]|Hostname.|
|Serial Number \[serial\_number\]|Device serial number.|
|Operational Status \[operational\_status\]|Indicates if the device is in active state.|
|IP address \[ip\_address\]|IP address.|
|Manufacturer \[manufacturer\]|Device manufacturer.|
|Description \[short\_description\]|Short description.|
|Model Number \[model\_number\]|Device model number.|
|Firmware \[firmware\_version\]|Firmware version.|
|Hardware Operating System \[hardware\_os\]|OS running on the hardware.|
|Hardware OS Version \[hardware\_os\_version\]|OS version running on the hardware.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Hostname.|
|Serial Number \[serial\_number\]|Serial number of the device.|
|Fully qualified domain name \[fqdn\]|Fully qualified domain name.|
|Operational Status \[operational\_status\]|Indicates if the device is in active state.|
|IP address \[ip\_address\]|IP address.|
|Manufacturer \[manufacturer\]|Device manufacturer.|
|Description \[short\_description\]|Short description.|
|Model Number \[model\_number\]|Device model number.|
|Firmware \[firmware\_version\]|Firmware version.|
|Hardware Operating System \[hardware\_os\]|OS running on the hardware.|
|Hardware OS Version \[hardware\_os\_version\]|OS version running on the hardware.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Hostname.|
|Serial Number \[serial\_number\]|Serial number of the device.|
|Fully qualified domain name \[fqdn\]|Fully qualified domain name.|
|Operational Status \[operational\_status\]|Indicates if the device is in active state.|
|IP address \[ip\_address\]|IP address.|
|Manufacturer \[manufacturer\]|Device manufacturer.|
|Description \[short\_description\]|Short description.|
|Model Number \[model\_number\]|Device model number.|
|Firmware \[firmware\_version\]|Firmware version.|
|Hardware Operating System \[hardware\_os\]|OS running on the hardware.|
|Hardware OS Version \[hardware\_os\_version\]|OS version running on the hardware.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Hostname.|
|Fully qualified domain name \[fqdn\]|Fully qualified domain name.|
|IP address \[ip\_address\]|IP address.|
|Manufacturer \[manufacturer\]|Device manufacturer.|
|Description \[short\_description\]|Short description.|
|Model Number \[model\_number\]|Device model number.|
|Hardware Operating System \[hardware\_os\]|OS running on the hardware.|
|Hardware OS Version \[hardware\_os\_version\]|OS version running on the hardware.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Hostname.|
|Fully qualified domain name \[fqdn\]|Fully qualified domain name.|
|IP address \[ip\_address\]|IP address.|
|Manufacturer \[manufacturer\]|Device manufacturer.|
|Description \[short\_description\]|Short description.|
|Model Number \[model\_number\]|Device model number.|
|Hardware Operating System \[hardware\_os\]|OS running on the hardware.|
|Hardware OS Version \[hardware\_os\_version\]|OS version running on the hardware.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the network adapter.|
|IP Address \[ip\_address\]|IP address of the network adapter.|
|MAC Address \[mac\_address\]|MAC address of the network adapter.|
|Configuration Item \[cmdb\_ci\]|References the Juniper Firewall Device \[cmdb\_ci\_firewall\_device\_juniper\] associated with this network adapter.|

The Dependency Views map on the Juniper Firewall Device CI shows the Juniper Firewall Cluster to which it belongs.

\[Omitted image "juniper-fw-dependency-views.png"\] Alt text: CIs and connections on a Dependency Views map

## CI relationships

The Next-Generation Juniper Network Firewall pattern creates the following relationships and references to support Juniper network firewall discovery. References link to records in other tables and don't appear in the CI Relationship \[cmdb\_rel\_ci\] table.

|CI|Relationship|CI|
|---|------------|---|
|Juniper Firewall Cluster \[cmdb\_ci\_firewall\_cluster\_juniper\]|Hosted on::Hosts|Juniper Firewall Device \[cmdb\_ci\_firewall\_device\_juniper\]|
|Juniper Firewall Device \[cmdb\_ci\_firewall\_device\_juniper\]|Owns::Owned by|Network Adapter \[cmdb\_ci\_network\_adapter\]|
|Juniper Firewall Device \[cmdb\_ci\_firewall\_device\_juniper\]|Owns::Owned by|IP Address \[cmdb\_ci\_ip\_address\]|
|Juniper Firewall Device \[cmdb\_ci\_firewall\_device\_juniper\]|Uses::Used by|Router Interface \[dscy\_router\_interface\]|
|Firewall Device \[cmdb\_ci\_firewall\_device\]|Contains::Contained by|Firewall Security Policy \[cmdb\_ci\_firewall\_security\_policy\]|
|Firewall Device Group \[cmdb\_ci\_firewall\_device\_group\]|Members::Member Of|Firewall Device \[cmdb\_ci\_firewall\_device\]|
|Firewall Device Group \[cmdb\_ci\_firewall\_device\_group\]|Contains::Contained by|Firewall Security Policy \[cmdb\_ci\_firewall\_security\_policy\]|
|Firewall Manager \[cmdb\_ci\_firewall\_manager\]|Manages::Managed by|Firewall Device \[cmdb\_ci\_firewall\_device\]|
|Firewall Manager \[cmdb\_ci\_firewall\_manager\]|Contains::Contained by|Firewall Security Policy \[cmdb\_ci\_firewall\_security\_policy\]|

|CI|Field|Referenced CI|
|---|-----|-------------|
|Serial Number \[cmdb\_serial\_number\]|Configuration item \[configuration\_item\]|Juniper Firewall Device \[cmdb\_ci\_firewall\_device\_juniper\]|
|Network Adapter \[cmdb\_ci\_network\_adapter\]|Configuration Item \[cmdb\_ci\]|Juniper Firewall Device \[cmdb\_ci\_firewall\_device\_juniper\]|
|Router Interface \[dscy\_router\_interface\]|Configuration Item \[cmdb\_ci\]|Juniper Firewall Device \[cmdb\_ci\_firewall\_device\_juniper\]|

**Parent Topic:**[Available on-premise discovery patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery-and-service-mapping-patterns/available-patterns.md)

