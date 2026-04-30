---
title: Review log streaming data and adjust integration settings in Health Log Analytics
description: Review the log data streaming status and streaming sources of an active integration for Health Log Analytics on the integration's Overview screen. From this tab, you can investigate streaming issues and refine the integration settings. Leverage the displayed data to refine how HLA reads the log data by adjusting the integration's configuration.
locale: en-US
release: zurich
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
keywords: [log data, streaming, sources, status, overview, integration, ServiceNow, Health Log Analytics, HLA]
breadcrumb: [Log data flow monitoring and configuration optimization, Set up integrations from Integrations Launchpad, Set up HLA on your instance, Configuring, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Review log streaming data and adjust integration settings in Health Log Analytics

Review the log data streaming status and streaming sources of an active integration for Health Log Analytics on the integration's Overview screen. From this tab, you can investigate streaming issues and refine the integration settings. Leverage the displayed data to refine how HLA reads the log data by adjusting the integration's configuration.

## Before you begin

Confirm that the integration has been activated on the Integrations Launchpad. For more information, see [Set up integrations for Health Log Analytics from the Integrations Launchpad](../concept/hla-data-input-setup-integrations.md).

For MID-less or OpenTelemetry Protocol \(OTLP\) integrations, verify that the **mid.hla.itom\_gateway\_streaming.enabled** property is set to true in the MID Server properties to enable displaying the ITOM Gateway component on the Overview screen.

To access the Log Viewer from the Overview tab with context from the integration, you must have the ServiceNow Service Operations Workspace Log Analytics application installed.

Role required: evt\_mgmt\_admin

## About this task

For more information about the data shown in the **Overview** screen, see [Monitoring log data flow and optimizing integration settings in Health Log Analytics](../concept/hla-integration-overview-tab.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  From the bottom of the navigation pane, select the AIOps configuration center icon ![ITOM AIOps configuration center icon](../image/icon-itom-aiops-config.png).

    The ITOM AIOps configuration center page appears. The configuration center is a centralized workspace. Use it to configure and manage AIOps features from a single place.

3.  From the Integrate section, under Integrations, select **Manage installed integrations**.

    The Integrations Launchpad appears.

4.  In the **Installed integrations** tab, search for an active integration and open it.

    The **Overview** screen displays, showing the integration's data streaming status and its log data sources data.

    **Note:** The ServiceNow System Logs Retriever integration doesn't run on a MID Server. Therefore, for this integration the **Overview** screen doesn’t display the MID Server streaming status.

5.  Analyze the provided data and investigate any data streaming issues.

6.  Adjust the configuration of the integration, if needed.

    Use the options on the View menu \(![View menu icon.](../image/icon-actions.png)\) to navigate to the relevant table or the Log Viewer.

    **Note:** The View menu content changes dynamically depending on whether the referenced tables contain data.

<table id="table_wrd_plh_4dc"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Data Input Mapping

</td><td>

Opens the **Data Input Mapping** page. On this page, you can map sources manually if HLA didn't discover properties automatically. For more information, see [Map raw log data in Health Log Analytics](hla-data-input-mapping.md).

</td></tr><tr><td>

Source Type Structure

</td><td>

Opens the **Source Type Structures** page. In the Source Type Structure, log data is classified and organized based on its origin or type. You can adjust the structure and verify that the HLA AI engine extracts properties properly and classifies them correctly. For more information, see [Source type structure adjustment in Health Log Analytics](../concept/hla-source-type-structure-adjustment.md).

</td></tr><tr><td>

Log Sources

</td><td>

Opens the **Log Sources** table. This table enables you to verify that HLA has created all your log sources. If a log source is missing, you can add it manually. For more information, see [Verify your log sources in Health Log Analytics](hla-log-sources-review.md).

</td></tr><tr><td>

Log Viewer

</td><td>

Opens the **Log Viewer**, which shows the frequency of anomalies in the log data during a specific time period. For more information, see [Reviewing the logs that are connected with an alert on the Log Viewer in Health Log Analytics](../../health-log-analytics-operator/concept/hla-op-logs-log-viewer-concept.md). **Note:** The Log Viewer option appears only if the Service Operations Workspace Log Analytics application is installed.

</td></tr></tbody>
</table>7.  When you have resolved any data streaming issues and fixed the configuration, select **Test and save**.

    The system saves the updated configuration to the database and tests the configured port, returning either success or an error. If an error is returned, fix the configuration according to the suggestions on the screen and then select **Test and save** again. Once the test is successful, continue with the next step.

8.  Reactivate the integration.


**Parent Topic:**[Set up Health Log Analytics on your ServiceNow instance](../concept/hla-implement.md)

