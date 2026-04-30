---
title: HPE BladeSystem Enclosure Discovery
description: ServiceNow Discovery uses the HPE BladeSystem Enclosure discovery pattern to discover BladeSystem, which is a line of Hewlett Packard Enterprise blade server machines. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: zurich
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Available on-premise discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# HPE BladeSystem Enclosure Discovery

ServiceNow Discovery uses the HPE BladeSystem Enclosure discovery pattern to discover BladeSystem, which is a line of Hewlett Packard Enterprise blade server machines. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

-   Ensure you are using the latest version of Discovery and Service Mapping Patterns.
-   Set SNMP credentials for the enclosure \(to be used by the Classifier\). For more information, see [SNMP credentials](https://www.servicenow.com/docs/access?context=c_SNMPCredentials&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).
-   Set the SSH credentials for the enclosure’s Onboard Administrator \(to be used by the Discovery pattern\). The account used for accessing the Onboard Administrator must have permissions to view all of the enclosure’s bays, so it can gather the blade servers' information. For more information, see [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).
-   Verify the Onboard Administrator’s IP address, which Discovery runs against.
-   Ensure that the host machine is reachable from the MID Server.

## Highlights and supported versions

The pattern has been tested against:

-   HPE BladeSystem c7000 Enclosure G2 and G3
-   HPE BladeSystem blades: HPE ProLiant BL460c
    -   Generations 8, 9 and 10
    -   ROM Versions: I31, I36, I41 \(2014-2021\)
    -   Blades being managed by a Virtual Connect Manager/Virtual Connect Enterprise Manager \(VCM/VCEM\) have a logical serial number. In this case, the serial number, which is exposed by WMI, for example, is the logical one, rather than the physical one, as is usually the case. When creating the relation between the blade and the OS server, based on the serial number, the system attempts to match both the physical and logical serial numbers with the ones owned by the OS Server.
    -   When discovering blade servers with the logical serial numbers, their logical serial numbers are inserted to **cmdb\_serial\_number** with the **logical** type. This is a new serial number type that was created to support these new serial numbers introduced by HP.

        **Note:** The WMI provides the logical serial number as the bios serial number. ESXi servers are discovered by probes. The ESXiserver CI gets the logical serial number as **chassis**.


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the HPE BladeSystem Enclosure Discovery pattern.

|Field|Description|
|-----|-----------|
|Name \[name\]|The name of the enclosure.|
|UUID \[uuid\]|The unique identifier of the enclosure \(HPE’s proprietary identifier\).|
|IP Address \[ip\_address\]|The management IP of the enclosure \(Onboard Administrator address\).|
|Model ID \[model\_id\]|The enclosure’s type \(model\).|
|Manufacturer \[manufacturer\]|The enclosure’s manufacturer name \(“HP” or “HPE”, depending upon the model\).|
|Serial number \[serial\_number\]|A generated serial number according to this convention: **&lt;enclosure’s original serial&gt; ::&lt;enclosure’s UUID&gt;**|
|Asset tag \[asset\_tag\]|The asset tag as extracted from the enclosure’s data.|
|Model number \[model\_number\]|The enclosure’s part number \(HPE proprietary\).|
|Midplane Spare Part Number \[midplane\_spare\_part\_number\]|The spare part number \(HPE proprietary\) of the mid-plane.|
|PDU Type \[pdu\_type\]|The type of Power Distribution Unit.|
|PDU Spare Part Number \[pdu\_spare\_part\_number\]|The Power Distribution Unit spare part number \(HPE proprietary\).|
|Onboard Administrator Tray Type \[onboard\_admin\_tray\_type\]|The type of the Onboard Administrator tray.|
|Onboard Administrator Tray Spare Part Number \[onboard\_admin\_tray\_spare\_part\_number\]|The Onboard Administrator tray’s spare part number \(HPE proprietary\).|
|Onboard Administrator Tray Serial Number \[onboard\_admin\_tray\_serial\_number\]|The Onboard administrator tray’s serial number.|

|Field|Description|
|-----|-----------|
|Name \[name\]|The generated value, according to this convention: **&lt;enclosure’s name&gt;/bay-&lt;bay number&gt;**|
|UUID \[uuid\]|The unique identifier of the blade server \(HPE’s proprietary identifier\).|
|Logical UUID \[uuid\_logical\]|The logical unique identifier of the HPE server blade \(HPE’s proprietary identifier\).|
|Model ID \[model\_id\]|The blade server’s product name \(model\).|
|Manufacturer \[manufacturer\]|The blade server’s manufacturer name \(“HP” or “HPE” depending on the model\).|
|Serial number \[serial\_number\]|A generated serial number according to this convention: **&lt;blade’s original serial&gt; :: &lt;blade’s UUID&gt;**.|
|Logical serial number \[serial\_number\_logical\]|The logical serial number of the HPE server blade \(HPE’s proprietary identifier\).|
|Asset tag \[asset\_tag\]|The asset tag as extracted from the blade’s data.|
|Model number \[model\_number\]|The blade’s part number \(HPE proprietary\).|
|RAM \(MB\) \[ram\]|The blade’s RAM size.|
|ROM Version \[rom\_version\]|The version of the blade’s ROM.|
|System Board Spare Part Number \[system\_board\_spare\_part\_number\]|The blade’s system board spare part number \(HPE proprietary\).|
|Boot Mode \[boot\_mode\]|The blade’s boot mode.|
|Secure Boot Status \[secure\_boot\_status\]|The blade’s secure board status.|
|Management Processor Type \[management\_processor\_type\]|The blade’s management processor type \(iLOversion\).|
|Management Processor Name \[management\_processor\_name\]|The blade’s management processor hostname.|
|Management Processor Firmware Version \[management\_processor\_firmware\_version\]|The blade’s management processor firmware version.|
|Management Processor IP Address \[amanagement\_processor\_ip\_address\]|The blade’s management processor IP address.|
|Management Processor MAC Address \[management\_processor\_mac\_address\]|The blade’s management processor MAC address.|
|Power Management Controller Version \[power\_management\_controller\_version\]|The blade’s power management controller’s version.|
|iLO Federation Capable \[ilo\_federation\_capable\]|The iLofederation capability enabled/disabled.|
|Bay Number \[bay\_number\]|The enclosure’s bay number in which the blade is installed.|

|Field|Description|
|-----|-----------|
|MAC Address \[mac\_address\]|The blade’s management processor’s ethernet address \(= iLOnetwork interface MAC address\).|
|Name \[name\]|The blade’s management processor’s hostname.|
|IP Address \[ip\_address\]|The blade’s management processor’s IP address.|
|Configuration Item \[cmdb\_ci\]|References the HPE BladeSystem Blade \[cmdb\_ci\_hpe\_bladesystem\_blade\] table.|

|Field|Description|
|-----|-----------|
|Name \[name\]|The blade’s management processor \(iLO\) IPv4 IP address.|
|IP Address \[ip\_address\]|The blade’s management processor’s IP address.|
|Nic \[nic\]|References the Network Adapter \[cmdb\_ci\_network\_adapter\] table.|

The implementation of HPE BladeSystem Enclosure CMDB model includes three new CI Classes:

|Field|Description|
|-----|-----------|
|Enclosure \[cmdb\_ci\_enclosure\]|A general class to represent any enclosure entity. Extends Hardware CI class.|
|HPE BladeSystem Enclosure \[cmdb\_ci\_hpe\_bladesystem\_enclosure\]|A CI class for representing the enclosure entity.|
|HPE BladeSystem Blade \[cmdb\_ci\_hpe\_bladesystem\_blade\]|A CI class for representing the blade server entity.|

## CI relationships

Discovery creates these relationships to support HPE BladeSystem Enclosure discovery.

|CI|Relationship|CI|
|---|------------|---|
|HPE BladeSystem Enclosure \[cmdb\_ci\_hpe\_bladesystem\_enclosure\]|Contains::Contained by|HPE BladeSystem Blade \[cmdb\_ci\_hpe\_bladesystem\_blade\]|
|HPE BladeSystem Blade \[cmdb\_ci\_hpe\_bladesystem\_blade\]|Owns::Owned by|Network Adapter \[cmdb\_ci\_network\_adapter\]|
|HPE BladeSystem Blade \[cmdb\_ci\_hpe\_bladesystem\_blade\]|Owns::Owned by|IP Address \[cmdb\_ci\_ip\_address\]|
|IP Address \[cmdb\_ci\_ip\_address\]|references|Network Adapter \[cmdb\_ci\_network\_adapter\]|
|Network Adapter \[cmdb\_ci\_network\_adapter\]|references|HPE BladeSystem Blade \[cmdb\_ci\_hpe\_bladesystem\_blade\]|
|Serial Number \[cmdb\_serial\_number\]|references|HPE BladeSystem Enclosure \[cmdb\_ci\_hpe\_bladesystem\_enclosure\]|
|Serial Number \[cmdb\_serial\_number\]|references|HPE BladeSystem Blade \[cmdb\_ci\_hpe\_bladesystem\_blade\]|

**Parent Topic:**[Available on-premise discovery patterns](../concept/available-patterns.md)

**Related topics**  


[SNMP-based queries](snmp-based-queries.md)

