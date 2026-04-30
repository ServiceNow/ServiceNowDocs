---
title: Fortinet firewall and FortiGate VDOM REST-based discovery
description: The Discovery and Service Mapping Patterns application uses the Next Generation Fortinet Network Firewall - REST pattern to find Fortinet firewalls through REST API calls. Additionally, the pattern extension VDOM Discovery finds FortiGate Virtual Domains \(VDOMs\). Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: zurich
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Available on-premise discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Fortinet firewall and FortiGate VDOM REST-based discovery

The Discovery and Service Mapping Patterns application uses the Next Generation Fortinet Network Firewall - REST pattern to find Fortinet firewalls through REST API calls. Additionally, the pattern extension VDOM Discovery finds FortiGate Virtual Domains \(VDOMs\). Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

The Next Generation Fortinet Network Firewall - REST pattern uses a set of REST API calls to find the Fortinet firewalls. For FortiGate VDOM discovery, only multi-VDOM mode is supported.

**Note:** Only the REST-based Fortinet firewall discovery method finds FortiGate VDOMs. The SNMP-based Fortinet firewall discovery method doesn't discover them. For information about the default SNMP-based Fortinet firewall discovery, see [Next-Generation Fortinet Network Firewall SNMP-based discovery](fortinet-fw-discovery.md).

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

To learn about Fortinet Firewalls and their versions that you can discover, refer to [Detailed information on products discovered by ITOM Visibility](r_SupportedApplications.md).

## Prerequisites

-   **Verify that the applications are up to date**
    -   Discovery and Service Mapping Patterns
    -   CMDB CI Class Models
-   **Create API Token**

    Create an API Token in Fortinet. For instructions on creating an API Token, go to the [Fortinet Document Library](https://docs.fortinet.com/) and search for the "Connect FortiGate device via API Token - Online Help" article under the FortiConverter Tool product family.

-   **Verify API access and permissions**

    -   Verify that the MID Server can access the Fortinet APIs.
    -   Verify that the API Token has sufficient permissions to retrieve the required information from the Fortinet devices.
    Required Fortinet APIs:

    -   `v2/cmdb/system/global`
    -   `api/v2/monitor/system/status`
    -   `api/v2/cmdb/system/ha`
    -   `api/v2/cmdb/router/static`
    -   `/api/v2/cmdb/firewall/policy`
    -   `api/v2/cmdb/system/vdom-property`
    -   `api/v2/cmdb/system/interface`
    -   `/api/v2/monitor/system/interface/select`
-   **Disable SNMP-based Fortinet firewall discovery**

    For more information, see [Disable SNMP-based Fortinet firewall discovery](../task/disable-snmp-fortinet-fw-discovery.md).

-   **Create an alias for the API Key Credentials**

    For more information, see [Create an alias for the API key credential for Fortinet firewall REST-based discovery](../task/create-alias-api-key-cred-fortinet.md).

-   **Create a serverless discovery schedule**

    For more information, see [Create a serverless schedule for Fortinet firewall REST-based discovery](../task/create-serverless-schedule-fortinet.md).


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Next Generation Fortinet Network Firewall - REST pattern.

|Field|Description|
|-----|-----------|
|Name \[name\]|**Hostname** field of the Fortinet device.|
|Serial number \[serial\_number\]|Serial number of the Fortinet device.|
|Fully qualified domain name \[fqdn\]|Fully qualified domain name of the Fortinet device.|
|Operational status \[operational\_status\]|Indicates whether the Fortinet device is in active state.|
|IP Address \[ip\_address\]|IP address of the Fortinet device.|
|Manufacturer \[manufacturer\]|Fortinet device manufacturer.|
|Description \[short\_description\]|Short description of the Fortinet device.|
|Model Number \[model\_number\]|Fortinet device model number.|
|Firmware version \[firmware\_version\]|Fortinet device firmware version.|
|Hardware OS \[hardware\_os\]|OS running on the hardware.|
|Hardware OS Version \[hardware\_os\_version\]|OS version running on the hardware.|

|Field|Description|
|-----|-----------|
|Name \[name\]|**Hostname** field of the Fortinet firewall cluster.|
|Fully qualified domain name \[fqdn\]|Fully qualified domain name of the firewall cluster.|
|IP address \[ip\_address\]|IP address of the firewall cluster.|
|Manufacturer \[manufacturer\]|Device manufacturer.|
|Description \[short\_description\]|Short description of the firewall cluster.|
|Model Number \[model\_number\]|Device model number.|
|Hardware OS \[hardware\_os\]|OS running on the hardware.|
|Hardware OS Version \[hardware\_os\_version\]|OS version running on the hardware.|

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
|IP Address \[ip\_address\]|IP address of the Fortinet firewall.|
|Netmask \[netmask\]|Netmask of the Fortinet firewall.|

Discovery populates the data in the CMDB when running the Next Generation Fortinet Network Firewall - REST pattern extension VDOM Discovery.

|Field|Description|
|-----|-----------|
|Vdom Index \[vdom\_index\]|Index of the VDOM in the list.|
|Name \[name\]|Name of the VDOM.|
|Description \[short\_description\]|Description of the VDOM property that provides additional context or information about the purpose of the property.|

|Field|Description|
|-----|-----------|
|ID \[id\]|Unique identifier for the interface. For example: port1.|
|Name \[name\]|Name of the interface. For example: LAN.|
|IP Address \[ip\_address\]|IP address assigned to the interface.|
|Description \[short\_description\]|Description of the interface, often used for documentation or identification purposes. For example: Main LAN interface.|
|MAC Address \[mac\_address\]|MAC address of the interface.|
|Access Type \[access\_type\]|Type of interface. For example: physical, VLAN, or aggregate.|

<table id="table_u1l_b4r_5cc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

Virtual LAN \(VLAN\) ID associated with the interface, if applicable.

 The format is: `VLAN-{Vlan ID}`. For example: VLAN-310.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Policy ID \[policy\_id\]|Unique ID assigned to the policy in VDOM or device level.|
|UUID \[uuid\]|Global unique identifier \(GUID\) for the firewall policy.|
|Name \[name\]|Name of the policy.|
|source\_interface|Network interface from which the traffic originates.|
|destination\_interface|Network interface to which the traffic is directed.|
|Source address \[source\_address\]|Source address or address group from which traffic originates.|
|Destination address \[destination\_address\]|Destination address or address group to which traffic is directed.|
|Internet Service \[internet\_service\]|Service or application being managed by the policy, often represented by a service group or name.|

## CI relationships

Discovery creates these relationships to support the Fortinet firewall discovery.

|CI|Relationship|CI|
|---|------------|---|
|Fortinet Firewall Cluster \[cmdb\_ci\_firewall\_cluster\_fortinet\]|Hosted on::Hosts|Fortinet Firewall Device \[cmdb\_ci\_firewall\_device\_fortinet\]|
|Fortinet Firewall Device \[cmdb\_ci\_firewall\_device\_fortinet\]|Owns::Owned by|IP Address \[cmdb\_ci\_ip\_address\]|
|Fortinet Firewall Device \[cmdb\_ci\_firewall\_device\_fortinet\]|Owns::Owned by|Network Adapter \[cmdb\_ci\_network\_adapter\]|
|Fortinet Firewall Device \[cmdb\_ci\_firewall\_device\_fortinet\]|Uses::Used by|Router Interface \[dscy\_router\_interface\]|
|Network Adapter \[cmdb\_ci\_network\_adapter\]|Owns::Owned by|IP Address \[cmdb\_ci\_ip\_address\]|
|Network Adapter \[cmdb\_ci\_network\_adapter\]|References|Fortinet Firewall Device \[cmdb\_ci\_firewall\_device\_fortinet\]|
|Router Interface \[dscy\_router\_interface\]|References|Fortinet Firewall Device \[cmdb\_ci\_firewall\_device\_fortinet\]|
|Serial Number \[cmdb\_serial\_number\]|References|Fortinet Firewall Device \[cmdb\_ci\_firewall\_device\_fortinet\]|

Discovery creates these relationships to support the FortiGate VDOM discovery.

|CI|Relationship|CI|
|---|------------|---|
|Fortinet Firewall Interface \[cmdb\_ci\_fortinet\_firewall\_interface\]|Extends from|Network Interface \[cmdb\_ci\_ni\_interface\]|
|Fortinet Firewall Policy \[cmdb\_ci\_fortinet\_firewall\_policy\]|Extends from|Firewall Security Policy \[cmdb\_ci\_firewall\_sec\_policy\]|
|Fortinet Virtual Domain \[cmdb\_ci\_fortinet\_vdom\]|Contains::Contained By|Fortinet Firewall Interface \[cmdb\_ci\_fortinet\_firewall\_interface\]|
|Fortinet Virtual Domain \[cmdb\_ci\_fortinet\_vdom\]|Contains::Contained By|Fortinet Firewall Policy \[cmdb\_ci\_fortinet\_firewall\_policy\]|
|Fortinet Virtual Domain \[cmdb\_ci\_fortinet\_vdom\]|Extends from|IP Firewall \[cmdb\_ci\_ip\_firewall\]|
|Fortinet Virtual Domain \[cmdb\_ci\_fortinet\_vdom\]|Hosted on::Hosts|Fortinet Firewall Device \[cmdb\_ci\_firewall\_device\_fortinet\]|
|Network Topology \[cmdb\_ci\_network\_topology\]|Members::Member of|Fortinet Firewall Interface \[cmdb\_ci\_fortinet\_firewall\_interface\]|

