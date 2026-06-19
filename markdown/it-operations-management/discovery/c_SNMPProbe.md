---
title: SNMP probes
description: The SNMP probes use the SNMP protocol to query a particular device for a list of OIDs, which are then traversed and the results passed back to the sensors. MID Servers support all SNMP protocol versions by default. You can set a MID Server to only support specific versions of SNMP.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/discovery/c\_SNMPProbe.html
release: zurich
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [List of Discovery probes, Discovery probes and sensors, Using Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# SNMP probes

The SNMP probes use the SNMP protocol to query a particular device for a list of OIDs, which are then traversed and the results passed back to the sensors. MID Servers support all SNMP protocol versions by default. You can set a MID Server to only support specific versions of SNMP.

Discovery supports SNMP versions 1, 2c, and 3. The default value is ALL. If you select one of the versions, but don’t have that version’s credentials, the Use SNMP Version reverts back to ALL.

**Note:** SNMP version credentials must be active=true. If a particular version is inactive, it will also revert back to ALL. A message will appear similar to: `--- No SNMP credentials of type 'snmpv3' are active in this instance. Setting Use SNMP version back to All`.

## SNMP patterns

The Network Router pattern replaces the several SNMP-related probes for the discovery of routers and switches. See [Available discovery patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery-and-service-mapping-patterns/available-patterns.md) for a list of patterns.

-   **[SNMP probe parameters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/r_SNMPProbeParameters.md)**  
This list of parameters may be passed to the SNMP probes.
-   **[Load a MIB module](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/t_LoadAMIBModule.md)**  
You can load an additional Management Information Base \(MIB\) module by creating a new ecc\_agent\_mib record and attaching the actual MIB file to the record.
-   **[SNMP probe MIB modules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/r_SNMPProbeMIBModules.md)**  
A management information base module \(MIB\) is a database that is used to manage elements in a network.

**Parent Topic:**[List of Discovery probes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/r_ListOfDiscoveryProbes.md)

