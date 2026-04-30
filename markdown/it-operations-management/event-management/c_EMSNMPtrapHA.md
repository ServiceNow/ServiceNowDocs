---
title: Configure SNMP Trap collection for high availability
description: For SNMP traps, the MID Server requires failover configuration for the trap listener.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure event collection for SNMP traps, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM Health, IT Operations Management]
---

# Configure SNMP Trap collection for high availability

For SNMP traps, the MID Server requires failover configuration for the trap listener.

You can configure two MID Servers for failover. Because the SNMP Trap listener on the MID Server receives inbound traffic on the IP address and port of the MID Server, you configure each MID Server to receive the same SNMP traps. Only one MID Server is active at any point in time, therefore Event Management does not receive duplicate traps.

**Parent Topic:**[Configure event collection for SNMP traps](../task/t_EMSNMPTrapEvent.md)

