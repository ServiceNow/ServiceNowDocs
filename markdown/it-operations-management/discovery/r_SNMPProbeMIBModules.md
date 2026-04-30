---
title: SNMP probe MIB modules
description: A management information base module \(MIB\) is a database that is used to manage elements in a network.
locale: en-US
release: yokohama
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [SNMP probes, List of Discovery probes, Discovery probes and sensors, Discovery, ITOM Visibility, IT Operations Management]
---

# SNMP probe MIB modules

A management information base module \(MIB\) is a database that is used to manage elements in a network.

Your instance includes object definitions from the most common management information base \(MIB\) files. Before adding a new object definition, consult the list of MIB modules to ensure that the object definitions are not already available. The instance includes object definitions from the most common management information base \(MIB\) files. The MID Server MIB File \[ecc\_agent\_mib\] table is domain separated. You can create versions of these policies that only a MID Server from the same domain can use. For instructions, see [Set up domain separation for MID servers](https://www.servicenow.com/docs/access?context=c_MIDServerDomainSeparation&version=yokohama&pubname=yokohama-servicenow-platform&section=t_SetUpDomainSeparationForDiscovery&ft:locale=en-US).

The following table contains the MIBs that load automatically. The MIBs that are bundled with the MID Server are not visible in the instance. The MIBs that are in the ecc\_agent\_mib table are included in the instance by default and can be viewed in the **MID Server** &gt; **SNMP MIBs** module.

**Important:** MIB files in a ServiceNow instance do not use a file extension. If the **glide.attachment.extensions** system property in your instance contains a list of file extensions permitted for import, MIB files do not load. To ensure that MIB files can load, add a temporary extension to the files prior to loading, such as **.mib**, and then list that extension in the **glide.attachment.extensions** property. When you load the file, a business rule called **MIB filename compliance** strips this extension from the file before it inserts the record into the ecc\_agent\_mib table.

|Bundled with the MID Server|Included in the instance|
|---------------------------|------------------------|
|ATM-MIB|A10 AX MIB|
|BRIDGE-MIB|A10 COMMONS MIB|
|DISMAN-EVENT-MIB|CISCO-SMI|
|ENTITY-MIB|CISCO-STACK-MIB|
|EtherLike-MIB|CISCO-TC|
|FRAME-RELAY-DTE-MIB|CISCO-VTP-MIB|
|HOST-RESOURCES-MIB|F5-BIGIP-COMMON-MIB|
|HOST-RESOURCES-TYPES|F5-BIGIP-LOCAL-MIB|
|IANA-ADDRESS-FAMILY-NUMBERS-MIB|F5-BIGIP-SYSTEM-MIB|
|IANAifType-MIB|FOUNDRY-SN-AGENT-MIB|
|IP-MIB|FOUNDRY-SN-ROOT-MIB|
|IP-FORWARD-MIB|LanMgr-Mib-II-MIB|
|IPMROUTE-STD-MIB|MSFT-MIB|
|IPV6-MIB|NetWare-Host-Ext-MIB|
|ISDN-MIB|NetWare-Server-MIB|
|RFC-1212|PowerNet-MIB|
|RFC-1215|QMS-MIB|
|RFC1155-SMI| |
|RFC1213-MIB| |
|RFC1398-MIB| |
|RFC1406-MIB| |
|RMON2-MIB| |
|RSVP-MIB| |
|SNMPv2-SMI| |
|SNMPv2-TC| |
|UPS-MIB| |

**Parent Topic:**[SNMP probes](../concept/c_SNMPProbe.md)

