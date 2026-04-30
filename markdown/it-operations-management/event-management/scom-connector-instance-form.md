---
title: SCOM connector instance form
description: The SCOM connector instance form displays the fields you must fill in when creating a SCOM connector instance.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Event Management reference, Event Management, ITOM Health, IT Operations Management]
---

# SCOM connector instance form

The SCOM connector instance form displays the fields you must fill in when creating a SCOM connector instance.

<table id="table_fdl_2fc_ybc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for the SCOM connector instance.

</td></tr><tr><td>

Description

</td><td>

Description for the use of the SCOM event collection instance.

</td></tr><tr><td>

Active

</td><td>

Select to activate the connector instance.Appears only when selecting a connector instance that has already been created.

</td></tr><tr><td>

Connector definition

</td><td>

The vendor and protocol used to gather events from the external event source.For a regular SCOM connector, select **SCOM**.

For a connector instance that you want to monitor metrics, select **SCOM Metrics**. When selecting this option, the fields in the **Connector instance - metrics fields** table appear.

</td></tr><tr><td>

Assignment group

</td><td>

Select the group to whom the connector instance is assigned.For example, this may be a group of administrators or a support group.

</td></tr><tr><td>

Host IP

</td><td>

Specify the SCOM IP address.This field does not appear when **SCOM metrics** is selected as the Connector definition.

</td></tr><tr><td>

Credential

</td><td>

Select Windows credentials.**Note:** When configuring Windows credentials, if the credential applies to specific MID servers, ensure that the MID Servers you specify on the credential record match the MID Servers specified in the **MID Servers for Connectors** section on the Connector Instance form.

This field does not appear when **SCOM metrics** is selected as the Connector definition.

</td></tr><tr><td>

Event collection last run time

</td><td>

The last event collection run time value updates automatically.This field does not appear when **SCOM metrics** is selected as the Connector definition.

</td></tr><tr><td>

Last event collection status

</td><td>

The last event collection run time status updates automatically.This field does not appear when **SCOM metrics** is selected as the Connector definition.

</td></tr><tr><td>

Event collection schedule \(seconds\)

</td><td>

The frequency in seconds that the system checks for new events from SCOM Operations.This field does not appear when **SCOM metrics** is selected as the Connector definition.

</td></tr><tr><td>

Bi-directional

</td><td>

Select to invoke the bi-directional option. This option enables the bi-directional exchange of values to-and-from the external event source. There is default implementation for SCOM. The **Last bi-directional status** option displays only when this option is selected.This field does not appear when **SCOM metrics** is selected as the Connector definition.

</td></tr><tr><td>

Last bi-directional status

</td><td>

The value of this field populates automatically.This field does not appear when **SCOM metrics** is selected as the Connector definition.

</td></tr><tr><td>

Last error message

</td><td>

The last error message field is automatically updated. This message is the last error message received by the connector. If the test connector fails, an error message is displayed in this field.This field does not appear when **SCOM metrics** is selected as the Connector definition.

</td></tr><tr><td>

MID Servers \(MID Server for Connectors section\)

</td><td>

Specify one or more MID Servers that are up and valid. MID Servers sort according to the order that their details were entered into the MID Server for Connectors section. The port requirement from the MID Server to the SCOM server is `1433`. If the specified MID Server is in a cluster, it may not be selected and another available MID Server is selected in its place. Ensure that the specified MID Servers match the MID Servers specified on the Windows Credentials page, as the connector uses Windows credentials to access MID Servers.

If no MID Server is specified, an available MID Server that has a matching IP range is used.

</td></tr></tbody>
</table><table id="table_ewf_xrc_ybc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Metrics collection

</td><td>

Selected by default. Read-only.

</td></tr><tr><td>

Metrics collection last run time

</td><td>

The last run time of the Metrics Collection scheduled job.This field is read-only.

</td></tr><tr><td>

Last metrics collection status

</td><td>

Status of the Metric Intelligence collection activity. The value of this field populates automatically.This field is read-only.

</td></tr><tr><td>

Metrics collection schedule \(seconds\)

</td><td>

The time, in seconds, to repeat the Metric Intelligence Collection scheduled job.

</td></tr><tr><td>

Metrics database host

</td><td>

The IP address or the host name of the metrics database host.

</td></tr><tr><td>

Connect using a named instance

</td><td>

When selected, the connection is made using the specified named instance. Otherwise, the connection is made using the specified port.

</td></tr><tr><td>

Metrics database port

</td><td>

The port used by the metrics database. The connection is made using JDBC. Default port number is 1433.If **Connect using a named instance** is selected, this option does not appear.

</td></tr><tr><td>

Metrics database named instance

</td><td>

The metrics database instance name.

</td></tr><tr><td>

Database login with Windows authentication

</td><td>

Perform database login with the credentials of the logged-in user defined on the MID Server service.

</td></tr><tr><td>

Metrics database credential

</td><td>

Credentials for the metric database. Use JDBC credentials for the local database user. If **Database login with Windows authentication** is selected, this option does not appear.

</td></tr></tbody>
</table>**Parent Topic:**[Event Management reference](event-management-reference.md)

