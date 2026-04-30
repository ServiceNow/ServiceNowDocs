---
title: Push connector instance form
description: Push Connector Instance form displays the fields that you must fill when you create or modify a connector.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Event Management reference, Event Management, ITOM Health, IT Operations Management]
---

# Push connector instance form

Push Connector Instance form displays the fields that you must fill when you create or modify a connector.

<table id="table_wck_dqc_2yb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

A unique name for the connector instance record, such as the name of an event source host.

</td></tr><tr><td>

Description

</td><td>

Any optional information that the administrator wants to use to identify this record.

</td></tr><tr><td>

Push Connector definition

</td><td>

Select the definition for the external system from which you want to receive events.

 You can select any existing definition, for example:

 -   Thousandeyes
-   Dynatrace
-   Catchpoints

 For a list of the connector definitions available in the base system, see [Configure Event Management connectors](connectors-and-listeners.md).

 **Note:**

If there are available configuration parameters for the push connector type you select, they appear under Push Connector Instance Configuration Parameters.

</td></tr><tr><td>

MID Server

</td><td>

It shows the list of MID Servers that has at least one MID Server Event Listener context up and running.

 The MID Server section appears only when the MID type of definition is selected.

</td></tr><tr><td>

URL

</td><td>

This field is auto-populated only after saving the details of the connector instance.

 Instance: The URL has to be configured in an external system with the ServiceNow credential having a evt\_mgmt\_integration role to receive the events.

 MID push connector instance: The URL has to be configured from an external system with [Configure the MID Web Server extension](../task/configure-mid-web-server-extension.md) credential to receive the events.

 This field appears only after the form has been saved.

</td></tr><tr><td>

Active

</td><td>

Select this check box to enable receiving the events from this external event source.

 This field appears only after the form has been saved.

</td></tr></tbody>
</table>**Parent Topic:**[Event Management reference](event-management-reference.md)

