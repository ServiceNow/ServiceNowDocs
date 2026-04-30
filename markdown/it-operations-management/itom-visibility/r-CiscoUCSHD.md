---
title: Cisco Unified Computing System \(UCS\)-HD device discovery
description: Discovery and Service Mapping Patterns application uses the to find Cisco UCS equipment, including chassis and blades. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: zurich
product: ITOM Visibility
classification: itom-visibility
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Network device discovery, Data collected by ITOM Visibility, ITOM Visibility reference, ITOM Visibility, IT Operations Management]
---

# Cisco Unified Computing System \(UCS\)-HD device discovery

Discovery and Service Mapping Patterns application uses the to find Cisco UCS equipment, including chassis and blades. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

**Note:** For information on Probe to Pattern migration see the knowledge article [KB0694477](https://support.servicenow.com/kb_view.do?sysparm_article=KB0694477).

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

-   **Create SNMP credentials**

    For more information, see [SNMP credentials](https://www.servicenow.com/docs/access?context=c_SNMPCredentials&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

-   **Create applicative credentials**

    Create applicative credentials for the **Cisco UCS Equipment \[cmdb\_ci\_ucs\_equipment\]** CI type. For more information, see [Applicative credentials](https://www.servicenow.com/docs/access?context=applicative-creds&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

-   **Classifier, pattern, and OIDs**

    The UCS classifier uses HorzontalDiscoveryProbe to launch the UCS - HD pattern. The classifier also uses these SNMP OIDs, which specify the Cisco UCS Equipment `[cmdb_ci_ucs_equipment]` table:

    |OID|Manufacturer|Model|Table|
    |---|------------|-----|-----|
    |1.3.6.1.4.1.9.12.3.1.3.847|Unified Computing Cisco UCS 6120XP 20-Port Fabric Interconnect|1.4\(3u\)\(NX-OS\) 5.0 Aggregation Switch|Cisco UCS Equipment|
    |1.3.6.1.4.1.9.12.3.1.3.899|Unified Computing Cisco UCS 6140XP 40-Port Fabric Interconnect|1.4\(3u\)\(NX-OS\) 5.0 Aggregation Switch|Cisco UCS Equipment|
    |1.3.6.1.4.1.9.12.3.1.3.1062|Unified Computing Cisco UCS 6248UP 48-Port Fabric Interconnect|2.0\(1t\)\(NX-OS\) 5.0.2 Aggregation Switch|Cisco UCS Equipment|
    |1.3.6.1.4.1.9.12.3.1.3.1063|Unified Computing Cisco UCS 6296UP 96-Port Fabric Interconnect|2.0\(1t\)\(NX-OS\) 5.0.2 Aggregation Switch|Cisco UCS Equipment|


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the UCS - HD pattern pattern. Only B-series devices are discovered. The UCS - HD pattern does not find C, S, or E series devices.

|Label|Field Name|
|-----|----------|
|Name|name|
|IP address|ip\_address|
|Model|model\_id|
|Distinguished name|dn|
|UCS Manager Version|version|

|Label|Field Name|
|-----|----------|
|Name|name|
|Model number|model\_number|
|Serial number|serial\_number|
|Chassis ID|chassis\_id|
|Operational status|operational\_status|
|Distinguished name|dn|

|Label|Field Name|
|-----|----------|
|Name|name|
|Model number|model\_number|
|Serial number|serial\_number|
|CPU count|cpu\_count|
|CPU core count|cpu\_core\_count|
|Ram|ram|
|Number of Adapters|number\_of\_adapters|
|Chassis ID|chassis\_id|
|Slot ID|slot\_id|
|Description|short\_description|
|Distinguished name|dn|
|Blade Serial Number|blade\_serial\_number|
|Operational status|operational\_status|

|Label|Field Name|
|-----|----------|
|Name|name|
|Vendor|vendor|
|Server ID|server\_id|
|Availability|availability|
|UUID|uuid|
|Rack serial|rack\_serial|
|Number of CPUs|num\_of\_cpus|
|Number of cores|num\_of\_cores|
|Model ID|model\_id|
|Total Memory|total\_memory|
|Distinguished name|dn|
|State|state|

## Relationships

These relationships are created to support UCS - HD discovery.

|CI|Relationship|CI|
|---|------------|---|
|cmdb\_ci\_ucs\_chassis|Contains::Contained by|cmdb\_ci\_ucs\_blade|
|cmdb\_ci\_ucs\_equipment|Contains::Contained by|cmdb\_ci\_ucs\_rack\_unit|
|cmdb\_ci\_ucs\_equipment|Contains::Contained by|cmdb\_ci\_ucs\_chassis|
|cmdb\_ci\_server|Runs on::Runs|cmdb\_ci\_ucs\_blade|

**Parent Topic:**[Network device discovery](../concept/c_NetworkDevices.md)

