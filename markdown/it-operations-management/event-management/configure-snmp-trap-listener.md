---
title: Configure the SNMP traps listener to receive OEM traps
description: Configure the SNMP trap listener to receive traps from Oracle Enterprise Manager \(OEM\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/event-management/configure-snmp-trap-listener.html
release: zurich
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Configure event collection for SNMP traps, Configure Event Management connectors, Event Management Integrations, Configure, Event Management, ITOM AIOps, IT Operations Management]
---

# Configure the SNMP traps listener to receive OEM traps

Configure the SNMP trap listener to receive traps from Oracle Enterprise Manager \(OEM\).

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

Event Management can process Oracle Enterprise Manager Cloud Control SNMP traps as events. For the SNMP trap listener to receive traps from OEM, you must designate the MID Server that runs the SNMP trap listener as a recipient of the trap. Upon receiving an OEM trap, the MID Server sends the trap to the ServiceNow instance for further processing as an event by Event Management.

The OEM 12c Trap event rule, Oracle EM MIB, and associated alert action rules are provided out-of-the-box, as well as these alert action rules:

-   `Oracle EM Launch Target Status`
-   `Oracle EM Launch View Event`

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Integrations** &gt; **MID SNMP Traps Listener**.

2.  Click **New**.

3.  Fill in the fields, as described in [Configure event collection for SNMP traps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/t_EMSNMPTrapEvent.md).

    For the **SNMP version** field, select: `v1 and v2c`.

    The SNMP version field on the trap listener form has two options: v1 and v2c \(default\) and v3.The OEM 12c Trap event rule specifically processes SNMPv1-style traps \(it relies on v1 fields like enterprise, generic\_trap, and specific\_trap\). So selecting v1 and v2c is correct for OEM.

4.  Verify the setup.

    -   Check the listener is running: After submitting the trap listener record, look at the MID Server log for a message like "TrapListenerExtension: started. Listening on port &lt;port&gt;". This confirms the MID Server is listening.
    -   Verify events are being created: Navigate to Event Management &gt; All Events \(or the em\_event table\) and filter by source = Oracle EM. If OEM is sending traps and the listener is working, events should appear here.
    -   Check the event rule matched: Open an event and verify the event\_class field shows "Trap From Enterprise 111" and the OEM-specific fields \(like oraEMNGEvent\_Severity, oraEMNGEventHost\_Name, etc.\) are populated in additional info.
    -   Check alert creation: Navigate to Alerts and verify alerts are created from the OEM events, with the "View Target Status" and "View Event" launch-in-context actions available.
    Some basic troubleshooting:

    -   Port binding error: If the MID Server log shows "IOException starting the SNMP listener", the port is likely already in use. Choose a different port or check for conflicts.
    -   No events appearing: Enable MID Server debug logging — the listener logs full trap details \(PDU, variable bindings, OIDs\) when debug is on. This helps confirm whether traps are reaching the MID Server at all.
    -   Authentication failures \(v3 only\): The log will show "Authentication failure" messages with the sender address and SNMP USM error code. Common causes: wrong credentials, mismatched engine ID, or security level mismatch.
5.  Click **Submit**.

    **Note:**

    Ensure all required SNMP MIB files are uploaded on the instance. For more information, see [Load a MIB module](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/t_LoadAMIBModule.md).

    .


## What to do next

In Oracle Enterprise Manager Cloud Control, configure the MID Server as a trap listener target.

**Parent Topic:**[Configure event collection for SNMP traps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/t_EMSNMPTrapEvent.md)

