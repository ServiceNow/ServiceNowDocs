---
title: Monitoring log data flow and optimizing integration settings in Health Log Analytics
description: The Overview screen in Health Log Analytics provides a comprehensive view of the components in the log-processing pipeline of a specific active integration. From this screen, you can troubleshoot any streaming issues for this integration and adjust its settings if needed.
locale: en-US
release: australia
product: Health Log Analytics
classification: health-log-analytics
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Set up integrations from Integrations Launchpad, Set up HLA on your instance, Configuring, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Monitoring log data flow and optimizing integration settings in Health Log Analytics

The Overview screen in Health Log Analytics provides a comprehensive view of the components in the log-processing pipeline of a specific active integration. From this screen, you can troubleshoot any streaming issues for this integration and adjust its settings if needed.

The **Overview** screen shows the log data streaming status and streaming sources of an active integration. It provides direct access to the **Data Input Mapping**, **Source Type Structures**, and **Log Sources** pages, as well as the **Log Viewer**, all with context from the current integration.

![Integration Overview screen and View menu items.](../image/hla-connector-overview-tab.png "Overview screen and View menu items")

## Streaming status

The **Streaming status** section on the **Overview** screen shows the status of data streaming between the log source and the MID Server and between the MID Server and the HLA engine. In addition, it displays the number of logs per minute passing through the MID Server and through the HLA engine.

**Note:** For the ServiceNow System Logs Retriever integration, the **Overview** screen doesn’t display the MID Server streaming status because that integration doesn't run on a MID Server.

The ServiceNow AIOps component shows the total number of alerts that the HLA engine has created. These statistics are updated when the **Overview** screen loads and are automatically refreshed every minute to show live data. You can change the default auto-refresh time interval through the system property **sn\_itom\_integ\_app.overview\_page\_data\_input\_stats\_auto\_refresh\_interval\_seconds**.

If data streaming fails, the integration is automatically deactivated and the **Streaming status** marks the component where the failure occurred. In addition, a banner explains the failure and either proposes steps to take to fix it or refers to ServiceNow support.

![Streaming status failure.](../image/il-connector-hla-status-failed.png)

For MID-less or OpenTelemetry Protocol \(OTLP\) integrations, such as Amazon Data Firehose, the **Overview** screen displays the ITOM Gateway as a component in the log-processing pipeline. The MID Server component is not shown in the pipeline, because log data is sent directly from the source to the ITOM Gateway. The logs are then processed by the HLA engine to find anomalies. ![Overview screen displaying the ITOM Gateway component.](../image/hla-overview-tab-itom-gateway.png)

For these integrations, the **Overview** screen shows the average rate of logs per minute over the last 15 minutes passing through the ITOM Gateway and the HLA engine, similar to the metrics shown for MID-based ingestion.

**Note:** The ITOM Gateway component is shown only if the MID Server property **mid.hla.itom\_gateway\_streaming.enabled** is set to true. For more information, see [MID Server properties](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

When the integration isn't streaming live data from the source, a warning message is displayed. There is a 4-hour interval between the last log source time and the current time before this message is generated. You can change the default time interval through the system property **sn\_itom\_integ\_app.overview\_page\_log\_source\_time\_threshold\_hours**.

**Note:** The warning message is displayed only when the HLA engine is up and running.

## Log streaming sources

The **Log streaming sources** section displays all sources that are currently streaming log data to HLA through this integration. Depending on your integration, the **Log streaming sources** table displays the following information about the integration's log streaming sources.

**Note:** This table isn’t available for the ServiceNow System Logs Retriever integration.

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

Data input

</td><td>

The integration streaming the data to your ServiceNow instance.

</td></tr><tr><td>

MID Server

</td><td>

The MID Server to which the log data is streaming.

</td></tr><tr><td>

Last event time

</td><td>

The time when the integration received the latest event.

</td></tr><tr><td>

Last log processing time

</td><td>

The time when the last log was received or processed.

</td></tr><tr><td>

Raw log lines/sec

</td><td>

The average number of raw log lines that streamed to the MID Server per second in the last one-minute interval.**Note:** This value represents the number of raw log lines before preprocessing.

</td></tr><tr><td>

Pre-processed log lines/sec

</td><td>

The average number of preprocessed log lines that streamed to the MID Server per second in the last one-minute interval.**Note:** This value can differ from the number of raw log lines per second. For example, the difference can be a result of logs having been dropped during preprocessing.

</td></tr></tbody>
</table>## Example

As an admin, you use the integration **Overview** page to verify continuous data flow into the ServiceNow instance. If log streaming fails, HLA doesn't receive the real-time data needed to detect anomalies or generate alerts.

For example, the **Streaming Status** for an active Elasticsearch integration may show a red circle with a white X for the MID Server component in the log-processing pipeline. This indicates that logs are not reaching the MID Server.

The **Log Streaming Sources** table shows a state of Authentication Failed or Connection Error, with an error message indicating invalid credentials. This points to an issue with the Elasticsearch credentials. Fixing the credentials and either restarting the log service or waiting for the next polling cycle, restores the connection.

The **Log Streaming Sources** table now shows a connection state of Connected or Active with successful authentication. The **Streaming Status** displays a green circle with a white check mark for the MID Server component. With log streaming restored, HLA can resume processing data and generating anomaly alerts.

**Parent Topic:**[Set up Health Log Analytics on your ServiceNow instance](hla-implement.md)

**Related topics**  


[Review log streaming data and adjust integration settings in Health Log Analytics](../task/il-connector-overview-tab.md)

