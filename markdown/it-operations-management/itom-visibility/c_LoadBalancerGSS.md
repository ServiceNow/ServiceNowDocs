---
title: Cisco GSS load balancer discovery
description: Discovery of Cisco GSS load balancers is performed by both SNMP and SSH.
locale: en-US
release: australia
product: ITOM Visibility
classification: itom-visibility
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Load balancers, Network device discovery, Data collected by ITOM Visibility, ITOM Visibility reference, ITOM Visibility, IT Operations Management]
---

# Cisco GSS load balancer discovery

Discovery of Cisco GSS load balancers is performed by both SNMP and SSH.

**Note:** For information on Probe to Pattern migration see the knowledge article [KB0694477](https://support.servicenow.com/kb_view.do?sysparm_article=KB0694477).

## Classifiers

Discovery uses the Cisco GSS Load Balancer classifier, which contains the condition: `sysdescr contains Global Site Selector` to classify the device.

## Probes

Discovery uses several probes, including an SNMP probe to discover the specific GSS device and a **Serial Number** probe to identify the serial number of the device. See the table below for the list of related probes.

**Warning:** You must have SNMP and [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US) configured correctly for the GSS load balancers on your network.

The following probes are triggered after classification:

|Probe|Description|Type|
|-----|-----------|----|
|Cisco GSS - Identity|A multiprobe that identifies the GSS device and serial number.|MultiProbe|
|Cisco GSS - Network|This is included in the Cisco GSS - Identify probe.|Java- SNMP|
|Cisco GSS - Serial Number|This is included in the Cisco GSS - Identify probe.|JavaScript|
|Cisco GSS - Get Domains|A probe that discovers global domain names corresponding to the device.|JavaScript|

## Tables

Discovery creates a record for each GSS device in the Cisco GSS \[cmdb\_ci\_lb\_cisco\_gss\] table. Domains are populated in the DNS Names \[cmdb\_ci\_dns\_name\] table. Host names and IP addresses are stored in the IP Address to DNS Name \[cmdb\_ip\_address\_dns\_name\] table. [Service Mapping](../../service-mapping/reference/c_ServiceMappingOverview.md) uses this information. You can see the DNS name information on the **DNS Names for CIs** related list of the Load Balancer form.

**Note:** The Cisco GSS pattern is available by default to use with the [Pattern Designer](../../service-mapping/concept/c_MappingPatternsCustomization.md).

**Parent Topic:**[Load balancer discovery](c_LoadBalancers.md)

