---
title: Configure the Zabbix metrics connector instance
description: Configure the Zabbix Metric connector instance to receive Metric Intelligence raw data from the Zabbix server.
locale: en-US
release: yokohama
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 2
breadcrumb: [Configure a pull connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Configure the Zabbix metrics connector instance

Configure the Zabbix Metric connector instance to receive Metric Intelligence raw data from the Zabbix server.

## Before you begin

To activate metric collection, ensure that the MID Server that retrieves metrics is configured with the Metric Intelligence extension and that the extension is in **Started** mode. See [Manually configure the Metric Intelligence extension](configure-itoa-metric-extension.md).

Create basic authentication credentials on ServiceNow instance with Zabbix server username and password.

Role required: evt\_mgmt\_admin

## About this task

ServiceNow does not support discovery for Zabbix, so CI entries must be manually created in the appropriate table using the hostname configured in the Zabbix platform.

-   Create an Event Rule to bind specific CIs.
-   Users can add tag information to Zabbix items, and the relevant tags will be included in the metric-to-CI records. These tags can also be used as filter conditions in the Event Rule for CI binding.

## Procedure

1.  Navigate to **Event Management** &gt; **Integrations** &gt; **Connector Instances**.

2.  Select **New** and create a connector instance.

    For details on the connector instance fields displayed on the page, see [Zabbix connector instance form](../reference/zabbix-connector-instance-form.md).

3.  Select and hold \(or right-click\) the form header and select **Save**.

    The connector instance values are added to the form and the parameters that are relevant to the connector appear.

4.  In the Connector Instance Values section, you can edit the values of the mandatory Zabbix parameters.

    For details on the connector instance value parameters, see [Zabbix connector instance value parameters](../reference/zabbix-connector-instance-value-parameters.md).

5.  In the MID Servers for Connectors section, add a MID Server for the Zabbix connector to use.

6.  Select **Test Connector** to verify the connection between the MID Server and the connector.

7.  After a successful test, select the **Active** check box and then select **Update**.

    **Note:** ServiceNow supports only unsigned float and unsigned integer metric types for Zabbix.


**Parent Topic:**[Configure a pull connector](t_EMConfigureConnectorInstance.md)

