---
title: Configure Scan Engine parameters
description: Configure the primary scanning capabilities and configuration options for scheduled, on-demand, and real-time scans.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/configure-scan-engine-properties.html
release: australia
topic_type: task
last_updated: "2026-06-11"
reading_time_minutes: 4
keywords: [impact scan engine, scan properties, scheduled scans]
breadcrumb: [Activate Scan Engine and review settings, Run Impact Guided Setup, Configuring Impact, Impact]
---

# Configure Scan Engine parameters

Configure the primary scanning capabilities and configuration options for scheduled, on-demand, and real-time scans.

## Before you begin

Review these properties before you [Run your first scan with the Scan Engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/run-scan-engine.md) or to make changes to Scan Engine behavior.

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

Daily, Weekly, or Monthly scheduled scan run times.

</td></tr><tr><td>

Day of Week

</td><td>

The day of the week on which to run weekly scans.

</td></tr><tr><td>

Day of Month

</td><td>

The day of the month on which to run monthly scans.

</td></tr><tr><td>

Time Zone

</td><td>

Your time zone.

</td></tr><tr><td>

Time

</td><td>

-   Field type = `glide_utc_time`
-   The time the scan should begin in 24-hour format \(HH:MM:SS\).


</td></tr></tbody>
</table>4.  Configure scan scope and finding tracking configuration settings.

<table id="table_a4y_xpx_2hc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Scan Non-Configuration Records

</td><td>

Includes non-configuration tables \(which do not extend `sys_metadata`\) in the scan.

</td></tr><tr><td>

Scan Read-Only Records

</td><td>

-   Includes read-only records in the scan.
-   **scan\_read\_only**: Default: `true`.
-   Read-only records are scanned by default.


</td></tr><tr><td>

Track Resolved Findings

</td><td>

Logs any resolved findings as part of the scan and includes them in the View Resolved Findings module of the dashboard.

</td></tr><tr><td>

Scan Findings Limit

</td><td>

-   **scan\_findings\_limit**
-   The maximum number of findings that can be generated for each definition during a scan.
-   The limit is applied per applicable table. For example, if the limit is set to 100, a maximum of 100 findings will be generated for each applicable table.
-   Prevents excessive or redundant findings and optimizes scan performance.


</td></tr><tr><td>

Custom Workday

</td><td>

By default, technical debt is calculated as a 24-hour day, which allows you to specify a number of hours for a workday. For example, developer workdays can be set to 8 hours instead of 24.**Note:** This is used to calculate various metrics that appear in the Analytics Dashboards.

</td></tr><tr><td>

Average hourly rate of development

</td><td>

This figure calculates the cost of technical debt that displays on your dashboard by multiplying it by the estimated time to resolve each finding in the system.

</td></tr><tr><td>

Batch Record Size

</td><td>

-   **full\_scan\_batch\_size**
-   Default: 50,000 records.
-   Specifies the maximum number of records allowed to be analyzed in a single batch scan for an applicable table.
-   This value does not limit the total number of records that can be scanned. When a table's record count exceeds this threshold \(50,000\), the table is assigned to its own dedicated batch during scan processing to optimize performance.
-   This value determines when an applicable table warrants its own batch during scans.

**Note:** This is a read-only system property that cannot be modified through the UI.

</td></tr><tr><td>

Scheduled Scan Logging Frequency

</td><td>

-   Default: `false`
-   Leave blank to disable verbose logging. When set, logs scan progress after processing the specified number of records


</td></tr><tr><td>

Days of scan finding histories to keep

</td><td>

-   **keep\_days\_finding\_history**
-   Sets the retention period for finding history records.

**Note:** This controls how long historical scan data is retained, not the findings themselves.The default value is 30 days.

</td></tr><tr><td>

Include review findings in technical debt

</td><td>

Displays findings on the dashboard where the level of the rule is equal to Review.

</td></tr><tr><td>

Enable instance specific definitions

</td><td>

-   **instance\_specific\_definitions**
-   Select to restrict scan definitions to run only on designated instances.
-   When disabled, all active definitions run on all instances.
-   When enabled without matching instances:

    -   If the `*sn\_se\_my\_sn\_instances*`*table is empty, all definitions run \(system assumes feature is not in use\)*
    -   If the `*sn\_se\_my\_sn\_instances*`*table __has entries__ but the current instance is not listed, only 'All Instances' definitions execute"*
**Note:** Configuration option that controls whether definitions run only on specified instances.

</td></tr><tr><td>

Scan Non-Configuration Records

</td><td>

-   **scan\_non\_configuration\_records**
-   Default: `true`
-   When enabled, includes non-configuration tables \(tables that do not extend sys\_metadata\) in full scans.


</td></tr></tbody>
</table>
-   **[Configure scanning properties per persona](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/teamdev-scanning-properties.md)**  
You can view and configure a variety of information, formatted into lists, that the Scan Engine uses to permit users, team leads, and admins to access content.
-   **[Configure application scanning properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/configure-application-scanning-properties.md)**  
The Scan Engine provides options to configure application scanning and enhance governance over Team Dev push approval. Configure which applications are scanned, the parameters applications must have to satisfy Team Dev approval, and whether developers can use Suite Scans for faster, focused validation.
-   **[Configure update set scanning properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/update-set-scanning-properties2.md)**  
The Scan Engine provides several options to further configure update set scanning and enhance the governance over update set management. Update set scanning occurs during scheduled instance scans and when developers attempt to mark update sets complete.
-   **[Define My SN Instance environments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/add-view-scan-engine-related-lists.md)**  
Configure instance integration settings to define the different environments for your ServiceNow instances and to take advantage of exception processing, definition syncing, and user story tracking in Impact.
-   **[Manage definition properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/additional-scan-engine-properties.md)**  
You can configure additional capabilities and configuration options for the definition ruleset.
-   **[Configure real-time scanning properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/configure-real-time-scanning-properties.md)**  
Real-time scanning properties allow control over which users have access to real-time scanning, and how the scan operates within their environment. Perform the following procedure to configure real time scanning properties.
-   **[Configure real-time code resolution with AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/configure-ai-code-fix-for-platform-health.md)**  
Follow these steps to configure real-time code resolution with AI suggested fixes for Impact Platform Health.
-   **[Configure exception reason properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/exception-reason-properties.md)**  
When real-time enforcement, `enforce_real_time_validation` is set to `true`, Recommend level findings require an approved exception reason before the form can be saved.

**Parent Topic:**[Activate Scan Engine and review settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/configure-initial-scan-engine-settings.md)

