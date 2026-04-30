---
title: Configure a default MID Server for connectors
description: You can set a default MID Server for connectors to ensure that there is always a MID Server available to receive external events.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure a pull connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM Health, IT Operations Management]
---

# Configure a default MID Server for connectors

You can set a default MID Server for connectors to ensure that there is always a MID Server available to receive external events.

## Before you begin

Role required: evt\_mgmt\_operator

## About this task

The default MID Server must have connectivity to all external event sources.

## Procedure

1.  Enter `sys_properties.list` in the navigation filter to open the System Property \[sys\_properties\] table.

2.  Select the `mid.server.connector_default` system property.

3.  On the form, fill in the fields.

<table id="table_d5j_thl_xw"><thead><tr><th align="left">

Field

</th><th align="left">

Description

</th></tr></thead><tbody><tr id="row_ConnectorDefault"><td>

mid.server.connector\_default

</td><td id="MIDServerDefault">

Default MID Server for connectorsDetermines the MID Server connectors to use when no MID Server is specified. Must match a MID Server name.

 -   **Type**: select `string` from the list
-   **Value**: enter the name of an existing MID Server, for example, SNC MID Server
-   **Location**: System Property \[sys\_properties\] table


</td></tr></tbody>
</table>    **Note:** You can reset the default MID Server by clearing the **mid.server.connector\_default** property or by updating the value of this property to a different MID Server. This property is not automatically reset in all scenarios.

4.  Click **Update**.


**Parent Topic:**[Configure a pull connector](t_EMConfigureConnectorInstance.md)

