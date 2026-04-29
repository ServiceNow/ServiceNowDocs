---
title: Review Unified Security Exposure Management integrations
description: The integration dashboard provides an overview of the installed third-party applications and the status of the integration runs.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Integrate, Unified Security Exposure Management, Security Operations]
---

# Review Unified Security Exposure Management integrations

The integration dashboard provides an overview of the installed third-party applications and the status of the integration runs.

In the chart, point to any part \(bar, pie, data point, and so on\) to view general data specific to that part. If you select any part of a report, a list opens to provide detailed information.

## Access the Integration Dashboard

To open the dashboard, navigate to **Workspaces** &gt; **Security Exposure Management Workspace** &gt; **Administration** and select **Review** on any integration.

## Data visualization

**Note:** To learn more about a widget, select the information icon ![Information icon](../../vulnerability-response/image/info-icon.png).

<table id="table_n43_yv4_mbc"><thead><tr><th>

Metrics

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Integration runs

</td><td>

Vertical Bar![Bar](../../../reuse/reporting/image/trend.svg)

</td><td>

The number of integration runs completed for each integration. Shows both successful and failed runs in the past 7 and 30 days. The most common causes for a failed run include:

-   Network interruption
-   Bit decay in the data transfer resulting in corrupted data during the transform

If you encounter any of these conditions, select the **Full data import** check box, click **Execute Now**, and rerun the integration.

</td></tr><tr><td>

Ingestion health

</td><td>

Highlights

</td><td>

Provides information on the following:-   Import queue processing time.
-   Import queue wait time.
-   REST API time.

</td></tr><tr><td>

Processing health

</td><td>

Multiple lines

</td><td>

Provides performance metrics for assignment rules, remediation task rules, CI lookup time, risk rules, and VI creation time for the last 30 days, to identify the cause for any deviations in performance. The performance is calculated based on the time taken for each activity. These parameters are calculated and associated at the integration run level. Each parameter is color coded for easy identification.

</td></tr></tbody>
</table>**Note:** Multiple factors can impact the performance of the integration run, like the amount of data and time taken to process this data.

|Name|Description|
|----|-----------|
|Name|Name of the integration.|
|Active|Status of the integration whether active or not.|
|Run|Run schedule of the integration|
|Day|Day on which the integration runs.|
|Time|Time at which the integration runs.|
|Last run status|Status of the last integration run whether failed or successful.|
|Notes|Notes|

**Note:** If a Tenable.sc integration run fails for any reason, the authentication token for Tenable.sc automatically expires and a message is displayed on the Vulnerability Integration Process record. A new token is automatically generated for the next integration process. All the integration processes, failed and successful, are displayed on the Vulnerability Integration Process tab on the Vulnerability Integration Process record.

During integration execution, multiple processes are generated, and data is received in the form of pages. Each process can contain one or more import queue entries with attached data in pages. These entries must process the data within the one-hour time limit. However, if the payload size is large, the processing time may exceed one hour or get stuck, resulting in an integration timeout error. The integration continues to process the data despite the timeout error. To avoid this miscommunication, timestamps \(heartbeats\) are sent periodically to indicate if the queue is active and processing data. The **Last Record Processed** field in the Import Queue Entry page is updated based on the count of records the import queue creates or updates. In case an import queue entry exceeds the one-hour time limit, the system checks the **Last Record Processed** field to see if it is also older than one hour. If it is, this indicates that the import queue entry is stuck, and it is timed out to prevent any further delays in processing. The **Last Record Processed** field is updated based on what is defined in the following system properties:

-   sn\_sec\_cmn.record\_threshold\_heartbeat: Defines the number of processed records, after which the heartbeat \(timestamp\) is sent to the import queue entry.
-   sn\_sec\_cmn.maximum\_heartbeat\_delay: Defines the time after which the import queue entry must be timed out.

**Parent Topic:**[Unified Security Exposure Management integrations](../../security-exposure-management-workspace/concept/integrating-usem.md)

