---
title: Monitor visualized log data on a predefined dashboard in Health Log Analytics
description: Use visualizations to monitor log data on the built-in Operational Dashboard in Service Operations Workspace Log Analytics and address issues as they occur in the system.
locale: en-US
release: australia
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Dashboards for real-time visualization of log data, Log Analytics in SOW for ITOM, Using SOW for ITOM, Service Operations Workspace for ITOM, ITOM AIOps, IT Operations Management]
---

# Monitor visualized log data on a predefined dashboard in Health Log Analytics

Use visualizations to monitor log data on the built-in Operational Dashboard in Service Operations Workspace Log Analytics and address issues as they occur in the system.

## Before you begin

Role required: evt\_mgmt\_operator or viz\_admin

**Important:** From the Vancouver release onward, this feature is deprecated and replaced with the AIOps [HLA Operational dashboard](../../../use/dashboards/application-content-packs/hla-operational-dashboard.md). For more information about AIOps dashboards, see [AIOps Dashboards in Service Operations Workspace for ITOM](../../service-operations-workspace-itom/concept/aiops-dashboards-sow-itom.md). You can also build a custom dashboard per your needs. For more information, see [Create log data dashboards and visualizations in Health Log Analytics](../../health-log-analytics-admin/task/hla-log-data-dashboard-create.md).

## Procedure

1.  Open the **Log Viewer** using one of the following methods:

    -   Navigate to **Workspaces** &gt; **Service Operations Workspace** and select the Log Viewer icon \(![Log Viewer icon.](../image/icon-log-viewer-sow.png)\).
    -   While viewing log entries for an alert on the **Surrounding logs** tab, select **Log Viewer**.
2.  Select the selection icon at the top right of the **Log viewer** tab, and then choose **Manage my dashboards** from the drop-down list.

    The **Operational Dashboard** tab displays.

    By default, the dashboard visualizes log data that was ingested in the last 24 hours.

    ![Operational dashboard.](../../service-operations-workspace-itom/image/dashboard-log-data.png)

3.  Change the time range for which data is shown by selecting the required range from the **Date** drop-down.

    You can specify a custom range by selecting **Custom** and then selecting the required start and end dates.

4.  Monitor the visualized log data and use it to identify and address issues.

<table id="table_slb_cky_z5b"><thead><tr><th>

Name

</th><th>

Description

</th><th>

How to use the data

</th></tr></thead><tbody><tr><td>

Logs processed

</td><td>

The number of logs that were processed and analyzed in the selected period.

</td><td>

Ensure that the log data is streaming as expected.

</td></tr><tr><td>

Logs per Application Service

</td><td>

The number of logs streamed for each application service in the selected period.

</td><td>

Ensure that log data is streaming as expected for each application service.

</td></tr><tr><td>

Error rate per Application Service

</td><td>

The number of logs with errors for each application service in the selected period.**Note:** Health Log Analytics automatically creates alerts for Error anomalies.

</td><td>

Identify errors in the logs.

</td></tr><tr><td>

Logs per Host

</td><td>

The number of processed logs for each host in the selected period.

</td><td>

Identify hosts that are logging more data, or less data, than expected.

</td></tr><tr><td>

Error rate per Component

</td><td>

The number of logs with errors for each component in the selected period.

</td><td>

Ensure that the components have a normal Error rate.

</td></tr><tr><td>

Severity rate

</td><td>

The severity level rate of the logs for the streaming sources.

</td><td>

Ensure that Critical and Error level rates are as expected.

</td></tr></tbody>
</table>
**Parent Topic:**[Dashboards for real-time visualization of log data in Health Log Analytics](../../health-log-analytics-admin/concept/hla-dashboard-visualizations.md)

