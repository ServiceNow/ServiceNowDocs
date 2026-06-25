---
title: Next-Generation Fortinet Network Firewall SNMP-based discovery
description: The Discovery and Service Mapping Patterns application uses the Next Generation Fortinet Network Firewall pattern to find Fortinet firewalls through a series of SNMP calls. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery-and-service-mapping-patterns/fortinet-fw-discovery.html
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Available on-premise discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Next-Generation Fortinet Network Firewall SNMP-based discovery

The Discovery and Service Mapping Patterns application uses the Next Generation Fortinet Network Firewall pattern to find Fortinet firewalls through a series of SNMP calls. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

The Next Generation Fortinet Network Firewall pattern uses a set of SNMP calls to find the Fortinet firewalls. Discovery uses the pattern to run horizontal discovery.

**Note:** Only the REST-based Fortinet firewall discovery method finds FortiGate VDOMs. The SNMP-based Fortinet firewall discovery method doesn't discover them. For information on REST-based Fortinet firewall and FortiGate Virtual Domains \(VDOMs\) discovery, see [Fortinet firewall and FortiGate VDOM REST-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/fortinet-fw-vdoms-rest-discovery.md).

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

To learn about Fortinet firewalls and their versions that you can discover, refer to [Detailed information on products discovered by ITOM Visibility](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/r_SupportedApplications.md).

## Fortinet Firewall data model

The Next Generation Fortinet Network Firewall pattern introduces the following CI classes that extend an existing CMDB class.

|CI class|Extends from|
|--------|------------|
|Fortinet Firewall Cluster \[cmdb\_ci\_firewall\_cluster\_fortinet\]|Firewall Cluster \[cmdb\_ci\_firewall\_cluster\]|
|Fortinet Firewall Device \[cmdb\_ci\_firewall\_device\_fortinet\]|Firewall Device \[cmdb\_ci\_firewall\_device\]|

## Prerequisites

-   **Verify the applications are up to date**
    -   Discovery and Service Mapping Patterns
    -   CMDB CI Class Models
-   **Ensure SNMP access**

    Ensure that your Fortinet firewall device has SNMP access.

-   **Configure SNMP credentials**

    On the ServiceNow instance, configure SNMP credentials. For more information, see [SNMP credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/c_SNMPCredentials.md).

-   **Add SNMP system OID record to ServiceNow instance**

    Add the SNMP system OID record for the Fortinet device to the ServiceNow instance. Update the following:

    -   Classifier: Fortinet Firewall
    -   Class: Fortinet Firewall Device
-   **Run a horizontal discovery**

    For more information, see [Running discoveries in your network](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/running-discoveries.md).


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Next Generation Fortinet Network Firewall Pattern.

|Field|Description|
|-----|-----------|
|Name \[name\]|Hostname.|
|Fully qualified domain name \[fqdn\]|Fully qualified domain name.|
|IP address \[ip\_address\]|IP address.|
|Manufacturer \[manufacturer\]|Device manufacturer.|
|Description \[short\_description\]|Short description of the Fortinet firewall cluster.|
|Model Number \[model\_number\]|Device model number.|
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
|Description \[short\_description\]|Short description of the device.|
|Model Number \[model\_number\]|Device model number.|
|Firmware \[firmware\_version\]|Firmware version.|
|Hardware Operating System \[hardware\_os\]|OS running on the hardware.|
|Hardware OS Version \[hardware\_os\_version\]|OS version running on the hardware.|

|Field|Description|
|-----|-----------|
|IP Address \[ip\_address\]|IP address of the Fortinet firewall.|
|Netmask \[netmask\]|Netmask of the Fortinet firewall.|
|Nic \[nic\]|References the Network Adapter \[cmdb\_ci\_network\_adapter\] table.|

|Field|Description|
|-----|-----------|
|IP Address \[ip\_address\]|IP address of the network adapter.|
|Netmask \[netmask\]|Netmask of the network adapter.|
|Alias \[alias\]|User-assigned name for the network adapter.|
|MAC Address \[mac\_address\]|MAC address of the network adapter.|
|Name \[name\]|Name of the network adapter.|
|Configuration Item \[cmdb\_ci\]|References the Fortinet Firewall Device \[cmdb\_ci\_firewall\_device\_fortinet\] table.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the Domain Name System \(DNS\).|
|IP Address \[ip\_address\]|IP address of the DNS.|

This Dependency Views map on the Fortinet Firewall Device CI shows the Fortinet Firewall Cluster to which it belongs.

\[Omitted image "fortinet-fw-dependency-views.png"\] Alt text: CIs and connections on a Dependency Views map

## CI relationships

The Next Generation Fortinet Network Firewall pattern creates the following relationships and references to support Fortinet firewall discovery. References link to records in other tables and don't appear in the CI Relationship \[cmdb\_rel\_ci\] table.

|CI|Relationship|CI|
|---|------------|---|
|Fortinet Firewall Cluster \[cmdb\_ci\_firewall\_cluster\_fortinet\]|Hosted on::Hosts|Fortinet Firewall Device \[cmdb\_ci\_firewall\_device\_fortinet\]|
|Fortinet Firewall Device \[cmdb\_ci\_firewall\_device\_fortinet\]|Owns::Owned by|IP Address \[cmdb\_ci\_ip\_address\]|
|Fortinet Firewall Device \[cmdb\_ci\_firewall\_device\_fortinet\]|Owns::Owned by|Network Adapter \[cmdb\_ci\_network\_adapter\]|
|Fortinet Firewall Device \[cmdb\_ci\_firewall\_device\_fortinet\]|Uses::Used by|Router Interface \[dscy\_router\_interface\]|
|Network Adapter \[cmdb\_ci\_network\_adapter\]|Owns::Owned by|IP Address \[cmdb\_ci\_ip\_address\]|

|CI|Field|Referenced CI|
|---|-----|-------------|
|Serial Number \[cmdb\_serial\_number\]|Configuration item \[configuration\_item\]|Fortinet Firewall Device \[cmdb\_ci\_firewall\_device\_fortinet\]|
|Network Adapter \[cmdb\_ci\_network\_adapter\]|Configuration Item \[cmdb\_ci\]|Fortinet Firewall Device \[cmdb\_ci\_firewall\_device\_fortinet\]|
|Router Interface \[dscy\_router\_interface\]|Configuration Item \[cmdb\_ci\]|Fortinet Firewall Device \[cmdb\_ci\_firewall\_device\_fortinet\]|
|IP Address \[cmdb\_ci\_ip\_address\]|Nic \[nic\]|Network Adapter \[cmdb\_ci\_network\_adapter\]|

**Parent Topic:**[Available on-premise discovery patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/available-patterns.md)

