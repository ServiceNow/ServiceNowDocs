---
title: Disable SNMP-based Fortinet firewall discovery
description: Disable the default SNMP-based Fortinet firewall discovery and use REST-based discovery instead to discover FortiGate Virtual Domains \(VDOMs\).
locale: en-US
release: xanadu
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: task
last_updated: "2024-09-26"
reading_time_minutes: 1
breadcrumb: [Fortinet firewall and FortiGate VDOM REST-based, Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Disable SNMP-based Fortinet firewall discovery

Disable the default SNMP-based Fortinet firewall discovery and use REST-based discovery instead to discover FortiGate Virtual Domains \(VDOMs\).

## Before you begin

Role required: discovery\_admin

## Procedure

1.  Navigate to **All** &gt; **Discovery Definition** &gt; **CI Classification** &gt; **SNMP**.

2.  In the **Name** field, search for `Fortinet Firewall`.

3.  Select the Fortinet Firewall record.

4.  Clear the **Active** check box.

5.  Select **Update**.


## What to do next

Create an alias and add it to an API key credential. For more information, see [Create an alias for the API key credential for Fortinet firewall REST-based discovery](create-alias-api-key-cred-fortinet.md).

**Related topics**  


[Fortinet firewall and FortiGate VDOM REST-based discovery](../reference/fortinet-fw-vdoms-rest-discovery.md)

