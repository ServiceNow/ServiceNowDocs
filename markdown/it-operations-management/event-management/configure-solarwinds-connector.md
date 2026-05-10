---
title: Configure the SolarWinds metrics connector instance
description: Configure the SolarWinds connector instance to receive Metric Intelligence raw data from the SolarWinds server.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-05-09"
reading_time_minutes: 3
breadcrumb: [Configure a pull connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Configure the SolarWinds metrics connector instance

Configure the SolarWinds connector instance to receive Metric Intelligence raw data from the SolarWinds server.

## Before you begin

To activate metric collection, ensure that the MID Server that retrieves metrics is configured with the Metric Intelligence extension and that the extension is in **Started** mode. See [Manually configure the Metric Intelligence extension](configure-itoa-metric-extension.md).

Configure the Service graph connector for SolarWinds. This is configured in the instance and discovers SolarWinds CIs. For details on configuring this connector, see [Service Graph Connector for SolarWinds](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-integration-solarwinds.md).

Role required: evt\_mgmt\_admin

## About this task

By default, the Solarwinds Metric Connector Collects metrics from the following tables:

-   Orion.CPULoad
-   Orion.NPM.InterfaceTraffic
-   Orion.VolumePerformanceHistory
-   Orion.VolumeUsageHistory
-   Orion.ResponseTime

## Procedure

1.  Navigate to **Event Management** &gt; **Integrations** &gt; **Connector Instances**.

2.  Select **New** and create a connector instance.

    For details on the connector instance fields displayed on the page, see [Solarwinds connector instance form](../reference/solarwinds-connector-instance-form.md).

3.  Select and hold \(or right-click\) the form header and select **Save**.

    The connector instance values are added to the form and the parameters that are relevant to the connector appear.

4.  In the Connector Instance Values section, you can edit the values of the mandatory SolarWinds parameters.

    For details on the connector instance value parameters, see [Solarwinds connector instance value parameters](../reference/solarwinds-connector-instance-value-parameters.md).

5.  In the MID Servers for Connectors section, add a MID Server for the SolarWinds connector to use.

6.  In the Related Links section, select **Configure metrics to collect**.

    Only metrics with the value **Active=true** are collected by the instance.

7.  Configure the metrics you want the instance to collect with the value **Active=true**.

    Metrics with the value **Active=false** are not collected by the instance.

8.  Select **New** to create new metrics.

    Configure the fields on the Connector instance metrics - New record \(sn\_em\_connector\_instance\_metrics\_solarwinds\) page.

<table id="table_m2c_jnz_zbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Metric name

</td><td>

Name for the metric to be configured in the ServiceNow instance.

</td></tr><tr><td>

Metric connector instance

</td><td>

Set by default to **SolarWinds connector instance**.All metrics are collected for the SolarWinds connector instance.

</td></tr><tr><td>

Additional columns

</td><td>

List of additional columns to fetch for CI-related information.

 For example: DateTime, Node, Resource.

 If **DateTime** is not provided, the current time is used as the metric timestamp. If **Node** and **Resource** are provided, they are populated accordingly. To reference fields from a parent table, use dot-walking format, such as `Interface.InterfaceName`. If a field should populate a specific standard field \(like **Resource**\), use an alias with the same name. For example, to use `InterfaceName` as the resource, specify it as `Interface.InterfaceName AS Resource`.

</td></tr><tr><td>

Table Name

</td><td>

Name of the table from which metrics are collected.

</td></tr></tbody>
</table>    -   Ensure that the CIs related to the metrics exist in the instance.
    -   Create an event rule to perform CI binding, as needed. For details, see [Create or edit an event rule](create-or-edit-event-rule.md).
9.  Select **Test Connector** to verify the connection between the MID Server and the connector.

10. After a successful test, select the **Active** check box and then select **Update**.

    **Note:** Ensure that **Registration Mode** is enabled for the SolarWinds source in the Metric Sources table.


**Parent Topic:**[Configure a pull connector](t_EMConfigureConnectorInstance.md)

