---
title: Configure the Dynatrace metrics connector instance
description: Configure the Dynatrace connector instance to receive Metric Intelligence raw data from the Dynatrace server.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure a pull connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Configure the Dynatrace metrics connector instance

Configure the Dynatrace connector instance to receive Metric Intelligence raw data from the Dynatrace server.

## Before you begin

To activate metric collection, ensure that the MID Server that retrieves metrics is configured with the Metric Intelligence extension and that the extension is in **Started** mode. See [Manually configure the Metric Intelligence extension](configure-itoa-metric-extension.md).

-   Create an access token in Dynatrace with Read Metrics \(metrics.read\) scope permissions, to enable fetching metric data. This token is used in the connector to call the Dynatrace REST API.
-   Configure the Service graph connector for Dynatrace. This is configured in the instance and discovers Dynatrace CIs. For details on configuring this connector, see [Configure Service Graph Connector for Observability - Dynatrace using guided setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/configure-dynatrace-integration.md).

Role required: evt\_mgmt\_admin

## About this task

By default, the Dynatrace service graph connector discovers CIs and supports metric collection for the following entity types:

-   HOST
-   APPLICATION
-   SERVICE
-   PROCESS\_GROUP\_INSTANCE

Configure other entity metrics for collection when creating event rules for CI binding.

## Procedure

1.  Navigate to **Event Management** &gt; **Integrations** &gt; **Connector Instances**.

2.  Select **New** and create a connector instance.

    For details on the connector instance fields displayed on the page, see [Dynatrace connector instance form](../reference/dynatrace-connector-instance-form.md).

3.  Select and hold \(or right-click\) the form header and select **Save**.

    The connector instance values are added to the form and the parameters that are relevant to the connector appear.

4.  In the Connector Instance Values section, you can edit the values of the mandatory Dynatrace parameters.

    For details on the connector instance value parameters, see [Dynatrace connector instance value parameters](../reference/dynatrace-connector-instance-value-parameters.md).

5.  In the MID Servers for Connectors section, add a MID Server for the Dynatrace connector to use.

6.  In the Related Links section, select **Configure metrics to collect**.

    Only metrics with the value **Active=true** are collected by the instance.

7.  Configure the metrics you want the instance to collect with the value **Active=true**.

    Metrics with the value **Active=false** are not collected by the instance.

8.  Select **New** to create new metrics.

    Configure the fields on the Connector instance metrics - New record \(sn\_em\_connector\_instance\_metric\) page.

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

Set by default to **Dynatrace connector instance**.All metrics are collected for the Dynatrace connector instance.

</td></tr><tr><td>

Metric type

</td><td>

The name of the Dynatrace entity type which the metric belongs to.

</td></tr><tr><td>

Metric ID

</td><td>

The Dynatrace metric ID of the metric being collected.

</td></tr><tr><td>

Active

</td><td>

Select for the metrics to collect.

</td></tr></tbody>
</table>    -   Ensure that the CIs related to the metrics exist in the instance.
    -   Create an event rule to perform CI binding, as needed. For details, see [Create or edit an event rule](create-or-edit-event-rule.md).
9.  Select **Test Connector** to verify the connection between the MID Server and the connector.

10. After a successful test, select the **Active** check box and then select **Update**.


**Parent Topic:**[Configure a pull connector](t_EMConfigureConnectorInstance.md)

