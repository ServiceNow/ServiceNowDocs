---
title: Configure the Datadog metrics connector instance
description: The Datadog Metrics connector retrieves performance metrics from your Datadog environment and sends them to your ServiceNow instance. Users can use SN anomaly detection capabilities and correlate metric anomalies with events and logs alerts.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/event-management/configure-datadog-connector.html
release: zurich
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-06-20"
reading_time_minutes: 3
breadcrumb: [Configure a pull connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Configure the Datadog metrics connector instance

The Datadog Metrics connector retrieves performance metrics from your Datadog environment and sends them to your ServiceNow instance. Users can use SN anomaly detection capabilities and correlate metric anomalies with events and logs alerts.

## Before you begin

To activate metric collection, ensure that the MID Server that retrieves metrics is configured with the Metric Intelligence extension and that the extension is in **Started** mode. See [Manually configure the Metric Intelligence extension](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/metric-intelligence/configure-itoa-metric-extension.md).

-   -   Create an API key and Application Key in Datadog. These are used in the connector to call the Datadog REST API.
-   Configure the Service graph connector for Datadog. This is configured in the instance and discovers Datadog CIs. For details on configuring this connector, see .

Create a Credentials record in your ServiceNow instance:

1.  Navigate to **Credentials &amp; Connections** &gt; **Credentials**.
2.  Select **New** and select **API Key Credentials**.
3.  In the **Name** field, enter a descriptive name. For example, Datadog API Key.
4.  In the **API Key** field, enter your Datadog API key.
5.  Select **Submit** to save the record.

Role required: evt\_mgmt\_admin

## Procedure

1.  Navigate to **Event Management** &gt; **Integrations** &gt; **Connector Instances**.

2.  In the list, select **Datadog Metrics**.

    The form displays the default parameters for the connector. You typically do not need to modify these parameters on the definition itself.

    **Note:** The blue information banner at the top of the page serves as a permanent reminder of the automatic capping applied to key performance parameters to ensure system stability.

3.  In the Connector Instances related list, click **New**.

4.  On the Connector Instance form, fill in the fields.

    For details on the connector instance fields displayed on the page, see [Datadog connector instance form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/datadog-connector-instance-form.md).

5.  Right-click the form header and select **Save**.

    The Connector Parameters and Connector Instance Metrics related lists appear. For details on the connector instance value parameters, see [Datadog connector instance value parameters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/datadog-connector-instance-value-parameters.md).

6.  To add custom, select **New** and fill the form.

<table id="table_m2c_jnz_zbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Metric name

</td><td>

Display name for the metric to be configured in the ServiceNow instance.

</td></tr><tr><td>

Metric connector instance

</td><td>

Set by default to **Datadog connector instance**.All metrics are collected for the Datadog connector instance.

</td></tr><tr><td>

Metric type

</td><td>

The name of the Datadog entity type which the metric belongs to.

</td></tr><tr><td>

Metric ID

</td><td>

The Datadog metric ID of the metric being collected.

</td></tr><tr><td>

Active

</td><td>

Select for the metrics to collect.

</td></tr></tbody>
</table>    -   Ensure that the CIs related to the metrics exist in the instance.
    -   Create an event rule to perform CI binding, as needed. For details, see [Create or edit an event rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/create-or-edit-event-rule.md).
7.  Select **Test Connector** to verify the connection between the MID Server and the connector.

8.  After a successful test, select the **Active** check box and then select **Update**.


**Parent Topic:**[Configure a pull connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/t_EMConfigureConnectorInstance.md)

