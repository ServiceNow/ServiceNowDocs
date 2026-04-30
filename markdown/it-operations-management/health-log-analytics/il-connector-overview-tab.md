---
title: Review log data streaming status and sources of an integration
description: Review the log data streaming status and sources of an active integration for Health Log Analytics on the integration's Overview tab. From this tab, you can investigate streaming issues and refine the integration's configuration.
locale: en-US
release: xanadu
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2024-09-03"
reading_time_minutes: 4
keywords: [log data, streaming, sources, status, overview, integration, ServiceNow, Health Log Analytics, HLA]
breadcrumb: [Set up integrations from Integrations Launchpad, Health Log Analytics data input setup, Configuring Health Log Analytics, Health Log Analytics, ITOM Health, IT Operations Management]
---

# Review log data streaming status and sources of an integration

Review the log data streaming status and sources of an active integration for Health Log Analytics on the integration's Overview tab. From this tab, you can investigate streaming issues and refine the integration's configuration.

## Before you begin

Confirm that the integration has been activated on the Integrations Launchpad. For more information, see [Set up integrations from Integrations Launchpad](../concept/hla-data-input-setup-integrations.md).

Role required: evt\_mgmt\_admin

## About this task

The Overview tab for an active integration allows you to check the integration's log data streaming status and sources. From here, you can troubleshoot any streaming issues and adjust the integration’s settings. Additionally, the Overview tab provides direct access to the Data Input Mapping, Source Type Structures, and Log Sources pages, as well as the Log Viewer, all with context from the integration.

**Note:** To access the Log Viewer from the Overview tab with context from the integration, you must have the ServiceNow Service Operations Workspace Log Analytics application installed.

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  From the left pane, select the Integrations Launchpad icon \(![Integration Launchpad icon](../../service-operations-workspace-itom/image/integrations-launchpad.png)\)

3.  On the **Installed integrations** tab, search for an active integration and open it.

    The **Overview** tab displays.

    ![Integration Overview tab and View menu items.](../image/hla-connector-overview-tab.png "Overview tab and View menu items")

    The **Streaming status** shows the integration's data streaming stats between the log source and the MID Server, and the MID Server and the AI engine. It also shows the total number of alerts that the AI engine created in the ServiceNow AIOps table. These statistics are updated when the **Overview** tab loads. If there's a streaming issue, an error message appears. If data streaming fails, the integration is automatically deactivated, and the **Streaming status** indicates where the failure happened. A banner explains the failure and steps to take.

    ![Streaming status failure.](../image/il-connector-hla-status-failed.png)

    **Note:** The ServiceNow System Logs Retriever integration doesn't run on a MID Server. Therefore, the **Overview** tab for this integration doesn’t display the MID Server streaming status.

    The **Log streaming sources** table displays the following information about the integration's log data sources.

<table id="table_gjq_xtk_pcc"><thead><tr><th>

Column

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name of the log data source.

</td></tr><tr><td>

Status

</td><td>

The streaming status: Active or Not active.

</td></tr><tr><td>

MID Server

</td><td>

The MID Server to which the log data is streaming.

</td></tr><tr><td>

Data input

</td><td>

The integration streaming the data to your ServiceNow instance.

</td></tr><tr><td>

Last event time

</td><td>

The date and time when the integration received the latest event.

</td></tr><tr><td>

Raw log lines/sec

</td><td>

The average number of raw log lines that streamed to the MID Server per second in the last one-minute interval.**Note:** This value represents the number of raw log lines before pre-processing.

</td></tr><tr><td>

Pre-processed log lines/sec

</td><td>

The average number of pre-processed log lines that streamed to the MID Server per second in the last one-minute interval.**Note:** This value can differ from the number of raw log lines per second. For example, the difference can be a result of logs having been dropped during pre-processing.

</td></tr></tbody>
</table>    **Note:** This table isn’t available for the ServiceNow System Logs Retriever integration.

4.  Investigate data streaming issues.

5.  Adjust the configuration of the integration, if needed.

    Navigate to relevant tables or the Log Viewer from the View menu \(![View menu icon.](../image/icon-actions.png)\).

    **Note:** The View menu content changes dynamically depending on whether the referenced tables contain data.

<table id="table_wrd_plh_4dc"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Data Input Mapping

</td><td>

This option opens the **Data Input Mapping** page. On this page, you can map sources manually if HLA didn't discover properties automatically. For more information, see [Map raw log data](hla-data-input-mapping.md).

</td></tr><tr><td>

Source Type Structure

</td><td>

This option opens the **Source Type Structures** page. In the Source Type Structure, log data is classified and organized based on its origin or type. You can adjust the structure and verify that the HLA AI engine extracts properties properly and classifies them correctly. For more information, see [Source type structure adjustment](../concept/hla-source-type-structure-adjustment.md).

</td></tr><tr><td>

Log Sources

</td><td>

This option opens the **Log Sources** table. This table enables you to verify that HLA has created all your log sources. If a log source is missing, you can add it manually. For more information, see [Verify your log sources](hla-log-sources-review.md).

</td></tr><tr><td>

Log Viewer

</td><td>

This option opens the **Log Viewer**, which shows the frequency of anomalies in the log data during a specific time period. For more information, see [Viewing the logs for an alert on the Log viewer](../../health-log-analytics-operator/concept/hla-op-logs-log-viewer-concept.md).**Note:** The Log Viewer option appears only if the Service Operations Workspace Log Analytics application is installed.

</td></tr></tbody>
</table>6.  When you have resolved any streaming issues and fixed the configuration, test and save the integration, and then reactivate it.

    For more information, see the documentation on configuring individual integrations.


**Parent Topic:**[Set up integrations from Integrations Launchpad](../concept/hla-data-input-setup-integrations.md)

