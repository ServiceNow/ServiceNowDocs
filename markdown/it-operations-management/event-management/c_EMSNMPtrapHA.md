---
title: Configure SNMP Trap collection for high availability
description: For SNMP traps, the MID Server requires failover configuration for the trap listener.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/event-management/c\_EMSNMPtrapHA.html
release: australia
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configure event collection for SNMP traps, Configure Event Management connectors, Event Management Integrations, Configure, Event Management, ITOM AIOps, IT Operations Management]
---

# Configure SNMP Trap collection for high availability

For SNMP traps, the MID Server requires failover configuration for the trap listener.

You can configure two MID Servers for failover. Because each MID Server receives inbound traffic on its own IP address and port, configure each one to receive the same SNMP traps. Only one MID Server is active at any point in time, therefore Event Management does not receive duplicate traps.

**Parent Topic:**[Configure event collection for SNMP traps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/event-management/t_EMSNMPTrapEvent.md)

