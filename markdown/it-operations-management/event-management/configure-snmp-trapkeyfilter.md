---
title: Configure message keys to spread SNMP object identifiers
description: By default, most SNMP trap events are processed by a single Event Management processing job. This can negatively effect event processing. Configure message keys on the MID Server to ensure that more than one processing job is invoked, ensuring optimal SNMP trap performance.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure event collection for SNMP traps, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM Health, IT Operations Management]
---

# Configure message keys to spread SNMP object identifiers

By default, most SNMP trap events are processed by a single Event Management processing job. This can negatively effect event processing. Configure message keys on the MID Server to ensure that more than one processing job is invoked, ensuring optimal SNMP trap performance.

## Before you begin

Role required: evt\_mgmt\_admin

## Procedure

1.  Navigate to **All** &gt; **MID Server** &gt; **Servers**.

    The **MID Servers** page opens.

2.  Select the relevant MID Server and on the MID Server page, select the **Configuration Parameters** tab.

3.  Click **New**.

4.  In the **Parameter name** field, select **mid.snmp.event.oid.keys**.

5.  In the **Value** field, enter a comma separated list of OIDs to be used for the message key.

6.  Click **Submit**.

    **Note:** The OID trap counter may cause problems activating event rules. To remove the trap counter from the OID, navigate to **MID Server** &gt; **Properties** and set the **mid.em.snmp\_oid\_key\_counter\_cut.enabled** property to **true**.

7.  To set conditions in a script that determine the message key to be used based on the SNMP traps received:

    1.  Navigate to **MID Server** &gt; **Script Includes**.

    2.  Locate and select **SNMPTrapKeyFilter**.

    3.  In the **Script** field, set conditions for which OIDs are to be used based on the SNMP trap event received.

    4.  Select the **Active** check box to activate the script.

    5.  Click **Update**.


**Parent Topic:**[Configure event collection for SNMP traps](t_EMSNMPTrapEvent.md)

