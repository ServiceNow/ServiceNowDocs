---
title: Integrate Event Integration \(EIF\) format event connector
description: Use the push connector that allows events to be forwarded from products, generally from IBM, that support the Event Integration \(EIF\) format to a MID Server.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Integrate with push connectors, Configure a push connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM Health, IT Operations Management]
---

# Integrate Event Integration \(EIF\) format event connector

Use the push connector that allows events to be forwarded from products, generally from IBM, that support the Event Integration \(EIF\) format to a MID Server.

## Before you begin

Ensure that the Event Management Connectors \(sn\_em\_connector\) plugin is installed on the ServiceNow AI Platform instance.

Ensure the MID Server is assigned with `EventManagement` or `ALL applications`.

Role required: evt\_mgmt\_integration

## About this task

Configure the Event Management environment for the collection of events from products that support the EIF format to a MID Server.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Integrations** &gt; **EIF listener context**.

2.  Click **New**.

3.  Create a new EIF listener context by completing the EIF listener context form:

    1.  On the form, fill in the fields.

<table id="table_qvn_lrm_hpb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for the EIF listener context.

</td></tr><tr><td>

Short Description

</td><td>

Short description of the MID Server extension execution context.

</td></tr><tr><td>

Port

</td><td>

Port for the EIF listener to receive EIF events. The default value is **9998**. However, if the port is already in use, you can use any other free port instead.

</td></tr><tr><td>

Status

</td><td>

The status of the EIF listener. This field is blank until the listener is run. After the listener has run, the value is automatically populated to one of the following statuses:-   Started: The listener is running.
-   Stopped: The listener is not running.
-   Offline: The MID Server is down.
-   Error: The listener failed with an error.


</td></tr><tr><td>

Execute on

</td><td>

The MID Server location for running the listener.

</td></tr><tr><td>

MID Server

</td><td>

The name of the designated MID Server when you select **Specific MID Server** in the **Execute on** field.

</td></tr><tr><td>

Executing on

</td><td>

The name of the MID Server on which the extension is running. This field is automatically populated with the name of the MID Server even if it's down. If you stop the extension, this field is empty.

</td></tr></tbody>
</table>    2.  On the form, you can select the related links on the EIF listener context form.

        |Related Link|Description|
        |------------|-----------|
        |Start|Select this option if the listener is not running. The listener is started on the configured MID Server and port number.|
        |Stop|Select this option to stop the running listener on the configured MID Server.|
        |Restart|Select this option to stop then start the listener on the configured MID Server and port number.|
        |Update Parameters|Select this option if you want to make changes to the listener configuration of the current running listener. If the parameters are valid, the listener disconnects and reconnects with new parameters.|
        |Test Parameters|Select this option to test if the port is a valid number.|

4.  When you're finished, right-click the form header and select **Save**.

5.  Click **Update**.

6.  If you want to check the incoming EIF traffic, complete the following steps:

    1.  Navigate to **MID Server** &gt; **Servers**.

    2.  Select the MID Server the EIF extension is running.

    3.  Under the **Configuration Parameters** tab, add the **mid.log.level** properties.


## What to do next

If the MID Server fails to start, you can review the MID Server log errors.

-   **[EIF events warning severity](../reference/eif-events-severity.md)**  
If the EIF event payload has a warning severity, it will be mapped differently in the ServiceNow instance.

**Parent Topic:**[Integrate with push connectors](configure-listener-transform-script.md)

