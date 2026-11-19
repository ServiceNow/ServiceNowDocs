---
title: Configure Scan Engine properties
description: Configure the primary scanning capabilities and configuration options for scheduled, on-demand, and real-time scans.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/configure-scan-engine-properties.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 5
keywords: [impact scan engine, scan properties, scheduled scans]
breadcrumb: [Scan Engine properties, Activate Scan Engine and review settings, Configuring Impact, Impact]
---

# Configure Scan Engine properties

Configure the primary scanning capabilities and configuration options for scheduled, on-demand, and real-time scans.

## Before you begin

Review these properties before you [Run Scan Engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/run-scan-engine.md) or to make changes to Scan Engine behavior.

Role required: scan\_engine\_admin and Impact \_admin

## Procedure

1.  Navigate to **ALL** &gt; **Impact** &gt; **Configuration** &gt; **Scan Engine Properties**.

2.  Select **Activate Scan Engine** to ensure the Scan Engine runs against your instance.

3.  Select **Run Scheduled Scan** to schedule nightly, weekly, or monthly scans and configure these options.

<table id="table_rs4_qpx_2hc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Run

</td><td>

Select the scan frequency:-   Daily
-   Weekly: The day of the week to run weekly scans
-   Monthly: The day of the month to run monthly scans.Day of Week


</td></tr><tr><td>

Time Zone

</td><td>

Your time zone.

</td></tr><tr><td>

Time

</td><td>

-   The time the scan should begin in 24-hour format \(HH:MM:SS\).
-   Field type = `glide_utc_time`


</td></tr></tbody>
</table>4.  Configure scan scope and finding tracking configuration settings.

<table id="table_a4y_xpx_2hc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Scan Non-Configuration Records

</td><td>

-   Field: **scan\_non\_configuration\_records**
-   Default: `true`
-   When enabled, includes non-configuration tables \(tables that don't extend sys\_metadata\) in full scans.


</td></tr><tr><td>

Scan read-only records

</td><td>

-   Include read-only records in the scan
-   API name: **scan\_read\_only**
-   Read-only records are set to scan by default


</td></tr><tr><td>

Track resolved findings

</td><td>

Logs any resolved findings as part of the scan and includes them in the View Resolved Findings module of the dashboard.

</td></tr><tr><td>

Custom workday

</td><td>

Select this option to specify the number of hours for a workday. By default, technical debt is calculated as a 24-hour workday. For example, developer workdays can be set to 8 hours instead of 24.**Note:** This is used to calculate various metrics that appear in the Analytics Dashboards.

</td></tr><tr><td>

Average development rate

</td><td>

This figure calculates the cost of technical debt that displays on your dashboard by multiplying the hourly development rate by the estimated time to resolve each finding in the system.

</td></tr><tr><td>

Batch Record Size

</td><td>

-   Field: **full\_scan\_batch\_size**
-   Default: 50,000 records.
-   Specifies the maximum number of records allowed to be analyzed in a single batch scan for an applicable table.
-   This value does not limit the total number of records that can be scanned.
    -   This value determines when an applicable table warrants its own batch during scans.
    -   When a table's record count exceeds this threshold \(50,000\), the table is assigned to its own dedicated batch during scan processing to optimize performance.
    -   **Note:** This is a read-only system property that can't be modified through the UI.

</td></tr><tr><td>

Scheduled scan logging frequency

</td><td>

-   Default: `false`
-   Leave blank to disable verbose logging. When set, logs scan progress after processing the specified number of records.


</td></tr><tr><td>

Days of scan finding histories to keep

</td><td>

-   Field: **keep\_days\_finding\_history**
-   Sets the retention period for finding history records.
-   The default value is 30 days.

**Note:** This controls how long historical scan data is retained, not the findings themselves.

</td></tr><tr><td>

Include review findings in technical debt

</td><td>

Select to display findings on the dashboard where the level of the finding is equal to **Review**. **Note:** See [Understand scan results and findings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/understand-scan-engine-results-findings.md) for information on findings levels.

</td></tr><tr><td>

Scan Findings Limit

</td><td>

-   Field: **scan\_findings\_limit**
-   The maximum number of findings that can be generated for each definition during a scan to prevent excessive or redundant findings and optimizes scan performance.
-   The limit is applied per applicable table. For example, if the limit is set to 100, a maximum of 100 findings will be generated for each applicable table.


</td></tr><tr><td>

Max Scan Retry Attempts

</td><td>

-   The maximum number of times the Scan Recovery job retries a stalled Full or Delta scan before it cancels the scan. A scan counts as stalled when its cluster node stopped mid-scan with no activity for over an hour.
-   After the maximum number of retries, the job cancels the scan outright, along with any of its batches not yet completed or skipped.
-   Select **None** to never retry a stalled scan and cancel it instead.
-   This limit applies only to stalled scans. Scans that resume after a routine, expected platform or application upgrade pause don't count against it.
-   This limit does not apply to on-demand scans, which have their own separate pre-start requeue limit.


</td></tr><tr><td>

Enable instance specific definitions

</td><td>

-   Configuration option that controls whether definitions run only on specified instances. Select to restrict scan definitions to run only on designated instances.
-   Field: **instance\_specific\_definitions**
-   When disabled, all active definitions run on all instances.
-   When enabled without matching instances:
    -   If the `*sn\_se\_my\_sn\_instances*`*table is empty, all definitions run \(system assumes feature is not in use\)*
    -   If the `*sn\_se\_my\_sn\_instances*`*table __has entries__ but the current instance is not listed, only 'All Instances' definitions execute"*


</td></tr></tbody>
</table>
-   **[Configure definition properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/additional-scan-engine-properties.md)**  
You can configure additional capabilities and configuration options for the definition ruleset.
-   **[Configure scan filters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/configure-scan-engine-filters.md)**  
Create scan filters to exclude applications, tables, or individual records from scans.
-   **[Configure real-time scanning properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/configure-real-time-scanning-properties.md)**  
Real-time scanning properties allow control over which users have access to real-time scanning, and how the scan operates within their environment. Perform the following procedure to configure real time scanning properties.
-   **[Configure real-time code resolution with AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/configure-ai-code-fix-for-platform-health.md)**  
Follow these steps to configure real-time code resolution with AI suggested fixes for Impact Platform Health.
-   **[Configure exception reason properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/exception-reason-properties.md)**  
When real-time enforcement, `enforce_real_time_validation`, is enabled, exception reasons can be configured for Suggest, Review, Recommend, and Act level findings based on the exception reason scope. The scope controls which finding levels can have exceptions. It doesn't decide which findings block a save.
-   **[Configure update set scanning properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/update-set-scanning-properties2.md)**  
The Scan Engine provides several options to further configure update set scanning and enhance the governance over update set management. Update set scanning occurs during scheduled instance scans and when developers attempt to mark update sets complete.
-   **[Configure Team Dev scanning properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/teamdev-scanning-properties.md)**  
You can view and configure a variety of information, formatted into lists, that the Scan Engine uses to permit users, team leads, and admins to access content.
-   **[Define My SN Instance environments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/add-view-scan-engine-related-lists.md)**  
Configure instance integration settings to define the different environments for your ServiceNow instances and to take advantage of exception processing, definition syncing, and user story tracking in Impact.

**Parent Topic:**[Scan Engine properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/scan-engine-properties-overview.md)

