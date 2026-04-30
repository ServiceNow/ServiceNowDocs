---
title: Configure the SNMP traps listener to receive OEM traps
description: Configure the SNMP trap listener to receive traps from Oracle Enterprise Manager \(OEM\).
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure event collection for SNMP traps, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM Health, IT Operations Management]
---

# Configure the SNMP traps listener to receive OEM traps

Configure the SNMP trap listener to receive traps from Oracle Enterprise Manager \(OEM\).

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

Event Management can process Oracle Enterprise Manager Cloud Control SNMP traps as events. For the SNMP trap listener to receive traps from OEM, you must designate the MID Server that runs the SNMP trap listener as a recipient of the trap. Upon receiving an OEM trap, the MID Server sends the trap to the ServiceNow instance for further processing as an event by Event Management.

The `OEM 12c Trap` event rule is provided with the default base instance, as well as these alert action rules:

-   `Oracle EM Launch Target Status`
-   `Oracle EM Launch View Event`

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Integrations** &gt; **MID SNMP Traps Listener**.

2.  Click **New**.

3.  Fill in the fields, as described in [Configure event collection for SNMP traps](t_EMSNMPTrapEvent.md).

    For the **SNMP version** field, select: `v1 and v2c`.

4.  Click **Submit**.

    **Note:**

    Ensure all required SNMP MIB files are uploaded on the instance. For more information, see [Load a MIB module](../../discovery/task/t_LoadAMIBModule.md).

    .


## What to do next

In Oracle Enterprise Manager Cloud Control, configure the MID Server as a trap listener target.

**Parent Topic:**[Configure event collection for SNMP traps](t_EMSNMPTrapEvent.md)

