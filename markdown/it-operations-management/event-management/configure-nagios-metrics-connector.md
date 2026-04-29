---
title: Configure the Nagios metrics connector instance
description: Configure the Nagios metric connector instance to receive Metric Intelligence raw data from the Nagios server.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 2
breadcrumb: [Configure a pull connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Configure the Nagios metrics connector instance

Configure the Nagios metric connector instance to receive Metric Intelligence raw data from the Nagios server.

## Before you begin

To activate metric collection, ensure that the MID Server that retrieves metrics is configured with the Metric Intelligence extension and that the extension is in **Started** mode. See [Manually configure the Metric Intelligence extension](configure-itoa-metric-extension.md).

-   Create basic authentication credentials on ServiceNow instance with Nagios SQL database username and password.
-   ServiceNow does not support discovery for Nagios. Therefore, create the CI entry manually in the respective table using the hostname configured on the Nagios platform.

Role required: evt\_mgmt\_admin

## About this task

By default, CI binding will occur for the following entities:

-   HOST HTTP Endpoint: The event rule applies to the Nagios metric HTTP if you are running a check that includes command\_name as service\_http.
-   MySQL Instance: The event rule applies to the Nagios metric MySQL if you are running a check that includes command\_name as mysql.

If you are running any other checks on HTTP endpoints or MySQL, you can edit the existing event rule to add the command\_name. For other entities, configure event rules based on CI binding requirements.

## Procedure

1.  Navigate to **Event Management** &gt; **Integrations** &gt; **Connector Instances**.

2.  Select **New** and create a connector instance.

    For details on the connector instance fields displayed on the page, see [Nagios connector instance form](../reference/nagios-connector-instance-form.md).

3.  Select and hold \(or right-click\) the form header and select **Save**.

    The connector instance values are added to the form and the parameters that are relevant to the connector appear.

4.  In the Connector Instance Values section, you can edit the values of the mandatory Nagios parameters.

    For details on the connector instance value parameters, see [Nagios connector instance value parameters](../reference/nagios-connector-instance-value-parameters.md).

5.  In the MID Servers for Connectors section, add a MID Server for the Nagios connector to use.

6.  Ensure that the CIs related to the metrics exist in the instance.

7.  Create an event rule to perform CI binding, as needed.

    For details, see [Create or edit an event rule](create-or-edit-event-rule.md).

8.  Select **Test Connector** to verify the connection between the MID Server and the connector.

9.  After a successful test, select the **Active** check box and then select **Update**.


**Parent Topic:**[Configure a pull connector](t_EMConfigureConnectorInstance.md)

