---
title: Configure event collection for SNMP traps
description: The SNMP listener runs on the MID Server, which acts as a collection endpoint for SNMP traps. The MID Server sends the traps to the ServiceNow instance for further processing as an event by Event Management.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Configure event collection for SNMP traps

The SNMP listener runs on the MID Server, which acts as a collection endpoint for SNMP traps. The MID Server sends the traps to the ServiceNow instance for further processing as an event by Event Management.

## Before you begin

Role required: agent\_admin

**Note:**

-   To view the MID SNMP Trap Listener in the UI: agent\_admin
-   To perform other operations, any one of the following roles is required: agent\_admin, evt\_mgmt\_integration, or evt\_team\_operator

Ensure that the MID Server is assigned with either `EventManagement` or `ALL applications`.

## About this task

Use the **MID SNMP Trap Listener** to listen for SNMP traps. In this configuration, the specified MID Server acts as a collection endpoint for SNMP traps.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Integrations** &gt; **MID SNMP Trap Listener**.

2.  Click **New**.

3.  Complete the SNMP Trap Collector Context form.

<table><thead><tr><th align="left" id="d429587e126">

Option

</th><th align="left" id="d429587e129">

Description

</th></tr></thead><tbody><tr><td id="d429587e135">

**Name**

</td><td>

Unique name for the SNMP Trap Collector.

</td></tr><tr><td id="d429587e144">

**Short description**

</td><td>

Short description of the MID Server extension execution context.

</td></tr><tr><td id="d429587e153">

**SNMP version**

</td><td>

Specify the SNMP version:-   v1 and v2c
-   v3


</td></tr><tr><td id="d429587e171">

**Minimum Security Level**

</td><td>

The valid security level values are: -   None - No security level value set.
-   noAuthnoPriv - Communication without authentication and privacy
-   authNoPriv - Communication with authentication and without privacy.
-   authPriv - Communication with authentication and privacy.
 **Note:** This field appears only when `v3` is selected in the **SNMP version** field.

</td></tr><tr><td id="d429587e205">

**UDP Port**

</td><td>

UDP port for SNMP Trap Collector to receive SNMP Traps. The default value is **1,162**. However, if the port is already in use, you can use any other free port instead.

</td></tr><tr><td id="d429587e217">

**Status**

</td><td>

The status of the trap listener. This field is blank until the listener is run. After the listener has run, the value is automatically populated to one of these statuses:

 -   **Started:** The listener is running.
-   **Stopped:** The listener is not running.
-   **Offline:** The MID Server is down.
-   **Error:** The listener failed with an error.


</td></tr><tr><td id="d429587e252">

**Execute on**

</td><td>

The MID Server location for running this listener. Select from specific MID Server. The recommended setting is **Specific MID Server**. Network hardware typically has to be configured to send to a specific IP address.

</td></tr><tr><td id="d429587e264">

**MID Server**

</td><td>

Specify the name of the designated MID Server when you select **Specific MID Server** in the **Execute on** field.

</td></tr><tr><td id="d429587e279">

**EngineID**

</td><td>

Displays only when **SNMP version=v3**.

 -   When sending an SNMP Inform message, include the default value of this field in the message.
-   When sending an SNMP Trap message, include a value other than the default value of this field in the message.


</td></tr><tr><td id="d429587e306">

**Executing on**

</td><td>

The name of the MID Server on which the extension is running. This field shows the name of the MID Server even if the MID Server is down. If you stop the extension, this field is empty.

This field is automatically populated.

</td></tr></tbody>
</table>4.  Right-click the form header and select **Save**.

5.  In the **Credentials for SNMPs** section, specify the required SNMP v3 credentials that the SNMP listener uses for authentication.

    **Note:** The **Credentials for SNMPs** section appears only when `v3` is selected in the **SNMP version** field.

6.  In the **Related Links** section, click **Test parameters**.

7.  Click **Update**.

8.  If the MID Server fails to start, review the MID Server log errors.

    When working with object identifiers \(OIDs\), the OID trap counter may cause problems activating event rules. To remove the trap counter from the OID, navigate to **MID Server** &gt; **Properties** and set the **mid.em.snmp\_old\_key\_counter\_cut.enabled** property to **true**.


## What to do next

In **Related Links**, these actions may be run against the SNMP traps listener:

|Related Link|Description|
|------------|-----------|
|Start|If it is currently not running, starts the listener. The listener is started on the configured MID Server and port number.|
|Stop|Stops the running listener on the configured MID Server. If the listener is not running, no action is taken.|
|Restart|Stops, then starts the listener on the configured MID Server and port number.|
|Test parameters|Tests that the port is a valid number.|
|Update parameters|If you make changes to the listener configuration, use this option to update the parameters of the currently running listener. First, the parameters are tested for validity. If the parameters are valid, the listener disconnects and reconnects with the new parameters.|

**Note:** Updates to the SNMP trap listener take effect only after clicking **Restart** or **Update parameters**.

-   **[Configure the SNMP traps listener to receive OEM traps](configure-snmp-trap-listener.md)**  
Configure the SNMP trap listener to receive traps from Oracle Enterprise Manager \(OEM\).
-   **[Configure SNMP Trap collection for high availability](../concept/c_EMSNMPtrapHA.md)**  
For SNMP traps, the MID Server requires failover configuration for the trap listener.
-   **[Configure message keys to spread SNMP object identifiers](configure-snmp-trapkeyfilter.md)**  
By default, most SNMP trap events are processed by a single Event Management processing job. This can negatively effect event processing. Configure message keys on the MID Server to ensure that more than one processing job is invoked, ensuring optimal SNMP trap performance.

**Parent Topic:**[Configure Event Management connectors](../reference/connectors-and-listeners.md)

**Related topics**  


[SNMP probe MIB modules](../../discovery/reference/r_SNMPProbeMIBModules.md)

[Configure the SNMP traps listener to receive OEM traps](configure-snmp-trap-listener.md)

