---
title: Network printer discovery
description: Discovery identifies and classifies information about network printers.
locale: en-US
release: australia
product: ITOM Visibility
classification: itom-visibility
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Network device discovery, Data collected by ITOM Visibility, ITOM Visibility reference, ITOM Visibility, IT Operations Management]
---

# Network printer discovery

Discovery identifies and classifies information about network printers.

Discovery can identify and classify Network Printers. For more information, see [Network discovery](../concept/c_NetworkDiscovery.md#).

|Label|Table name|Field name|Source|
|-----|----------|----------|------|
|Serial number|cmdb\_ci|serial\_number|SNMP, various MIBs|
|Start date|cmdb\_ci|start\_date|SNMP, RFC1213 MIB|
|Manufacturer|cmdb\_ci|manufacturer|SNMP, RFC1213 MIB|
|Model ID|cmdb\_ci|model\_id|SNMP, RFC1213 MIB|
|IP address|cmdb\_ci\_network\_adapter|ip\_address|SNMP, IP MIB|
|MAC address|cmdb\_ci\_network\_adapter|mac\_address|SNMP, IF MIB|
|Printer type|cmdb\_ci\_printer|print\_type|SNMP, PRINT MIB|
|Use count|cmdb\_ci\_printer|use\_count|SNMP, PRINT MIB|
|Use count units|cmdb\_ci\_printer|use\_units|SNMP, PRINT MIB|
|Colors|cmdb\_ci\_printer|colors|SNMP, PRINT MIB|
|Horizontal resolution|cmdb\_ci\_printer|horizontal\_resolution|SNMP, PRINT MIB|
|Vertical resolution|cmdb\_ci\_printer|vertical\_resolution|SNMP, PRINT MIB|
|Resolution units|cmdb\_ci\_printer|resolution\_units|SNMP, PRINT MIB|
|Description|discovery\_printer\_supplies|description|SNMP, PRINT MIB|
|Supply type|discovery\_printer\_supplies|supply\_type|SNMP, PRINT MIB|
|Supply class|discovery\_printer\_supplies|supply\_class|SNMP, PRINT MIB|
|Current level|discovery\_printer\_supplies|current\_level|SNMP, PRINT MIB|
|Max capacity|discovery\_printer\_supplies|max\_capacity|SNMP, PRINT MIB|
|Name|cmdb\_ci|name|Shazzam, SNMP, various MIBs|

**Parent Topic:**[Network device discovery](../concept/c_NetworkDevices.md)

