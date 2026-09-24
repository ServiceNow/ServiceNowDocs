---
title: Run on-demand scans
description: You can initiate on-demand scans outside of the already regularly scheduled instance scans.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/using-impact-scan-engine.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [Scan your instance, Impact Guided Setup, Configuring Impact, Impact]
---

# Run on-demand scans

You can initiate on-demand scans outside of the already regularly scheduled instance scans.

Following on-demand scan types are available.

<table id="table_jxp_zlk_hhc"><thead><tr><th>

Scan type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Application scans

</td><td>

Scan in-development applications to identify definition findings before publishing to the application repository. Application scans give insight into health scores, the number of findings, and the total impact of findings within your custom applications. **Note:** View application health scores in the Application Health dashboard by navigating to **ALL &gt; Impact &gt; Platform Health &gt; Application Health**. Health scores are calculated based on finding severity, count, and policy impact.

</td></tr><tr><td>

Limited definition scans 

</td><td>

Scan your instance against a single specified definition or definition suite.

</td></tr><tr><td>

Update set scans 

</td><td>

Scan open update sets for findings to get insights into what you are importing and exporting across your environments. 

</td></tr><tr><td>

Instance scans 

</td><td>

Scan your ServiceNow instance for findings. These scans return the findings and store them in the Opens Findings table.  **Note:** Only users with the Scan Engine Admin role can initiate instance scans.

</td></tr></tbody>
</table>Scans are initiated in different ways. They run using the properties you configured. Scheduled instance scans can be executed immediately using the **Execute Now** action, but they cannot bypass their configured schedule settings. Real-time scans run automatically during record saves and cannot be manually triggered.

For more information, see [Configure Scan Engine parameters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/configure-scan-engine-properties.md) and [Manage definition properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/additional-scan-engine-properties.md).

**Note:** The Scan Engine integrates with certain development tools, such as App Engine Studio, ServiceNow Studio, and script editors. It scans business rules, script `includes`, UI scripts, client scripts, ACLs, record producers, and other script-containing records in real-time as they are saved.

## Concurrency rules and scan behavior

Full and Delta scan supports update set scans and application scope scans. The Scan Engine enforces specific concurrency rules to protect instance performance and manage resource allocation:

-   **First scan behavior:** If the instance does not have any prior full scan, selecting **Initiate Scan** triggers a Full Instance Scan. Consecutive scans will be Delta Instance Scans.
-   **In-progress alerts:** If a scan is already in progress, attempting to initiate another scan displays an alert: "Cannot initiate a delta scan while another scan is in progress. Wait for the current scan to complete or use Force Full Scan to override."
-   **Full Instance Scan blocking:** Only one Full Instance Scan can run at a time. The system prevents parallel full scans to avoid excessive resource load. Additional full scan requests are blocked with an alert message.
-   **Force Full Scan override:** Administrators can use the **Force Full Scan** button to cancel the current scan and immediately start a new Full Instance Scan. The current scan is cancelled automatically, and the new full scan is initiated.
-   **Parallel scan allowance:** While certain scans run, Update Set Scans and Application Scans can still execute concurrently without blocking.
-   **Scan status visibility:** Users can see scan states in real-time on the Scan Results list view, including "Getting ready," "Complete," and "Cancelled" status indicators.

## User notifications and status indicators

The system provides contextual notifications and visual indicators to keep users informed:

-   **Scan triggered message:** When a scan is successfully initiated, users see: "A new scan has been triggered and it will take a moment to reflect in the queue. Refresh the page for the latest scan results."
-   **Scan in progress alert:** When attempting to initiate a scan while one is already running, an alert displays: "Cannot initiate a delta scan while another scan is in progress. Wait for the current scan to complete or use Force Full Scan to override."
-   **Trigger Scan modal:** When using Force Full Scan while a Delta Scan is in progress, a confirmation modal appears with the title "Trigger Scan" and message: "A Delta Scan is currently in progress. Do you want to cancel the ongoing Delta Scan and start a Full Scan instead?" Users can select **OK** to proceed or **Cancel** to terminate.
-   **Real-time updates:** The Scan Results list view displays scan metadata.

**Note:** Users must refresh the page to see the latest scan status updates in the queue.

## Access control by persona

Scan initiation capabilities are determined by user roles:

|Role|Permissions|
|----|-----------|
|Admin|Initiate scans and Force Full Scan|
|AI Fix User|Initiate scans only|
|Scan User|No scan initiation buttons \(view only\)|
|Read User|No scan initiation buttons \(view only\)|

**Note:** See [Roles installed with Impact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/impact-roles.md) for additional information on user roles.

-   **[Manage and monitor scans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/initiate-manage-scan-engine.md)**  
Initiate scans, monitor scan status, and manage scan execution using the Initiate Scan and Force Full Scan buttons.
-   **[Initiate application scans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/initiating-on-demand-scans-scan-engine.md)**  
Scan applications to identify definition findings before publishing to the application repository. Application scans give insight into health scores, the number of findings, and the total impact of findings within your custom applications. When Suite Scan is enabled, choose between scanning all active definitions or a curated suite.
-   **[Initiate update set scans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/initiate-update-set-scans.md)**  
Scan open update sets for findings to gain insights into what you're importing and exporting across your environments. When Suite Scan is enabled, choose between scanning all active definitions or a curated suite.
-   **[Initiate instance scans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/initiate-instance-scans.md)**  
You can scan your ServiceNow instance for findings.
-   **[Initiate limited definition scans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/initiate-limited-def-scans.md)**  
You can scan individual definitions or suites of definitions on-demand.

**Parent Topic:**[Run Scan Engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/run-scan-engine.md)

**Related topics**  


[Monitor and manage instance health](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/scan-engine-parallel-processing.md)

[Manage and monitor scans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/initiate-manage-scan-engine.md)

