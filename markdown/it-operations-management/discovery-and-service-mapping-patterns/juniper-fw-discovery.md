---
title: Next-Generation Juniper Network Firewall discovery
description: The ServiceNow Discovery application uses the Next-Generation Juniper Network Firewall discovery pattern to find Juniper network firewalls. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Available on-premise discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Next-Generation Juniper Network Firewall discovery

The ServiceNow Discovery application uses the Next-Generation Juniper Network Firewall discovery pattern to find Juniper network firewalls. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

The discovery pattern uses a set of SNMP calls to find the Juniper network firewalls. Discovery uses the pattern to run horizontal discovery.

You can use this pattern on the ServiceNow AI Platform® using the Madrid release or later.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

-   Ensure that your network firewall device has SNMP access.
-   On the ServiceNow instance, configure SNMP credentials.
-   Add the SNMP system OID record for the Juniper device to the ServiceNow instance. Update the following:
    -   Classifier: Juniper Firewall
    -   Class: Juniper Firewall Device

Deploy the pattern as follows:

1.  Download and install the CMDB CI Class Models: Release 1.10.0 from the ServiceNow Store. The app adds the new CMDB classes required for network firewall discovery. For more information, see Firewall extension classes.
2.  Download and install the discovery pattern from the ServiceNow Store.
3.  Sync the pattern with the appropriate MID Server.

## Data collected by Discovery during horizontal discovery

The discovered data includes the following tables and fields.

|Table and field|Description|
|---------------|-----------|
|IP Firewall \[cmdb\_ci\_ip\_firewall\] - Contains all network firewalls.|
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
|Firewall Device \[cmdb\_ci\_firewall\_device\] - Abstract class for vendor-specific firewalls.|
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
|Juniper Firewall Device \[cmdb\_ci\_firewall\_device\_juniper\] - Contains physical Juniper firewalls.|
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
|Firewall Cluster \[cmdb\_ci\_firewall\_cluster\] - Abstract class for a vendor-specific firewall cluster.|
|Name \[name\]|Hostname.|
|Fully qualified domain name \[fqdn\]|Fully qualified domain name.|
|IP address \[ip\_address\]|IP address.|
|Manufacturer \[manufacturer\]|Device manufacturer.|
|Description \[short\_description\]|Short description.|
|Model Number \[model\_number\]|Device model number.|
|Hardware Operating System \[hardware\_os\]|OS running on the hardware.|
|Hardware OS Version \[hardware\_os\_version\]|OS version running on the hardware.|
|Juniper Firewall Cluster \[cmdb\_ci\_firewall\_cluster\_juniper\] - Contains Juniper firewall cluster.|
|Name \[name\]|Hostname.|
|Fully qualified domain name \[fqdn\]|Fully qualified domain name.|
|IP address \[ip\_address\]|IP address.|
|Manufacturer \[manufacturer\]|Device manufacturer.|
|Description \[short\_description\]|Short description.|
|Model Number \[model\_number\]|Device model number.|
|Hardware Operating System \[hardware\_os\]|OS running on the hardware.|
|Hardware OS Version \[hardware\_os\_version\]|OS version running on the hardware.|

The Dependency Views map on the Juniper Firewall Device CI shows the Juniper Firewall Cluster to which it belongs.

![CIs and connections on a Dependency Views map](../image/juniper-fw-dependency-views.png)

## CI relationships

These relationships are created to support Juniper network firewall discovery:

|CI|Relationship|CI|
|---|------------|---|
|Firewall Cluster \[cmdb\_ci\_firewall\_cluster\]|Extends from|Cluster \[cmdb\_ci\_cluster\]|
|Juniper Firewall Cluster \[cmdb\_ci\_firewall\_cluster\_juniper\]|Extends from|Firewall Cluster \[cmdb\_ci\_firewall\_cluster\]|
|Hosted::Hosted on|Juniper Firewall Device \[cmdb\_ci\_firewall\_device\_juniper\]|
|Firewall Device \[cmdb\_ci\_firewall\_device\]|Extends from|IP Firewall \[cmdb\_ci\_ip\_firewall\]|
|Contains::Contained by|Firewall Security Policy \[cmdb\_ci\_firewall\_security\_policy\]|
|Juniper Firewall Device \[cmdb\_ci\_firewall\_device\_juniper\]|Extends from|Firewall Device \[cmdb\_ci\_firewall\_device\]|
|Firewall Device Group \[cmdb\_ci\_firewall\_device\_group\]|Extends from|CMDB CI \[cmdb\_ci\]|
|Members::Member Of|Firewall Device \[cmdb\_ci\_firewall\_device\]|
|Contains::Contained by|Firewall Security Policy \[cmdb\_ci\_firewall\_security\_policy\]|
|Firewall Manager \[cmdb\_ci\_firewall\_manager\]|Extends from|CMDB CI \[cmdb\_ci\]|
|Manages::Managed by|Firewall Device \[cmdb\_ci\_firewall\_device\]|
|Contains::Contained by|Firewall Security Policy \[cmdb\_ci\_firewall\_security\_policy\]|
|Firewall Security Policy \[cmdb\_ci\_firewall\_security\_policy\]|Extends from|CMDB CI \[cmdb\_ci\]|

**Parent Topic:**[Available on-premise discovery patterns](../concept/available-patterns.md)

