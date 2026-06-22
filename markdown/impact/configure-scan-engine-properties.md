---
title: Configure Scan Engine properties
description: Configure the primary scanning capabilities and configuration options for scheduled, on-demand and real-time scans.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/configure-scan-engine-properties.html
release: australia
product: Impact
classification: impact
topic_type: task
last_updated: "2026-06-11"
reading_time_minutes: 4
breadcrumb: [Activate Scan Engine and review settings, Configure the Impact Store Application, Configuring Impact, Impact]
---

# Configure Scan Engine properties

Configure the primary scanning capabilities and configuration options for scheduled, on-demand and real-time scans.

## Before you begin

Reference these properties in preparation to [Run your first scan with the Scan Engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/run-scan-engine.md) or to make changes to Scan Engine behavior.

Role required: Scan Engine admin and Impact admin

## Procedure

1.  Navigate to **ALL** &gt; **Impact** &gt; **Configuration** &gt; **Scan Engine Properties**.

2.  Select **Activate Scan Engine** to ensure the Scan Engine runs against your instance.

3.  Select **Run Scheduled Scan** to schedule nightly, weekly, or monthly scans, and then configure the following options.

<table id="choicetable_rs4_qpx_2hc"><thead><tr><th align="left" id="d25426e109">

Schedule option

</th><th align="left" id="d25426e112">

Description

</th></tr></thead><tbody><tr><td id="d25426e118">

**Run**

</td><td>

Daily, Weekly, or Monthly scheduled scan run times.

</td></tr><tr><td id="d25426e127">

**Day of Week**

</td><td>

The day of the week on which to run weekly scans.

</td></tr><tr><td id="d25426e136">

**Day of Month**

</td><td>

The day of the month on which to run monthly scans.

</td></tr><tr><td id="d25426e145">

**Time Zone**

</td><td>

Your time zone.

</td></tr><tr><td id="d25426e155">

**Time**

</td><td>

-   Field type = `glide_utc_time`
-   The time the scan should begin in 24-hour format \(HH:MM:SS\).


</td></tr></tbody>
</table>4.  Choose what to scan and how to track the findings.

<table id="choicetable_a4y_xpx_2hc"><thead><tr><th align="left" id="d25426e184">

Setting

</th><th align="left" id="d25426e187">

Description

</th></tr></thead><tbody><tr><td id="d25426e193">

**Scan Non-Configuration Records**

</td><td>

Includes non-configuration tables \(which do not extend `sys_metadata`\) in the scan.

</td></tr><tr><td id="d25426e205">

**Scan Read-Only Records**

</td><td>

-   Includes read-only records in the scan.
-   `scan_read_only`: Default value is `true`.
-   Read-only records are scanned by default.


</td></tr><tr><td id="d25426e231">

**Track Resolved Findings**

</td><td>

Logs any resolved findings as part of the scan and includes them in the View Resolved Findings module of the dashboard.

</td></tr><tr><td id="d25426e240">

**Scan Findings Limit**

</td><td>

-   Field name: `scan_findings_limit`
-   The maximum number of findings that can be generated for each definition during a scan.
-   The limit is applied per applicable table. For example, if the limit is set to 100, a maximum of 100 findings will be generated for each applicable table.
-   Prevents excessive or redundant findings and optimizes scan performance.


</td></tr><tr><td id="d25426e267">

**Custom Workday**

</td><td>

By default, technical debt is calculated as a 24-hour day, which allows you to specify a number of hours for a workday. For example, developer workdays can be set to 8 hours instead of 24.**Note:** This is used to calculate various metrics that appear in the Analytics Dashboards.

</td></tr><tr><td id="d25426e278">

**Average hourly rate of development**

</td><td>

This figure calculates the cost of technical debt that displays on your dashboard by multiplying it by the estimated time to resolve each finding in the system.

</td></tr><tr><td id="d25426e287">

**Batch Record Size**

</td><td>

-   Field name: `full_scan_batch_size`
-   Default value = 50,000 records.
-   Specifies the maximum number of records allowed to be analyzed in a single batch scan for an applicable table.
-   This value does not limit the total number of records that can be scanned. When a table's record count exceeds this threshold \(50,000\), the table is assigned to its own dedicated batch during scan processing to optimize performance.
-   This value determines when an applicable table warrants its own batch during scans.

**Note:** This is a read-only system property that cannot be modified through the UI.

</td></tr><tr><td id="d25426e318">

**Scheduled Scan Logging Frequency**

</td><td>

-   Default value = `false`
-   Leave blank to disable verbose logging. When set, logs scan progress after processing the specified number of records


</td></tr><tr><td id="d25426e338">

**Days of scan finding histories to keep**

</td><td>

-   Field name: `keep_days_finding_history`
-   Sets the retention period for finding history records.

**Note:** This controls how long historical scan data is retained, not the findings themselves.The default value is 30 days.

</td></tr><tr><td id="d25426e360">

**Include review findings in technical debt**

</td><td>

Displays findings on the dashboard where the level of the rule is equal to Review.

</td></tr><tr><td id="d25426e370">

**Enable instance specific definitions**

</td><td>

-   Field name: `instance_specific_definitions`
-   Select to restrict scan definitions to run only on designated instances.
-   When disabled, all active definitions run on all instances.
-   When enabled without matching instances, only 'All Instances' definitions execute.

**Note:** Configuration option that controls whether definitions run only on specified instances.

</td></tr><tr><td id="d25426e398">

**Scan Non-Configuration Records**

</td><td>

-   Field name: `scan_non_configuration_records`
-   Default value = `true`
-   When enabled, includes non-configuration tables \(tables that do not extend sys\_metadata\) in full scans.


</td></tr></tbody>
</table>
-   **[Configure scanning properties per persona](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/teamdev-scanning-properties.md)**  
You can view and configure a variety of information, formatted into lists, that the Scan Engine uses to permit users, team leads, and admins to access content.
-   **[Configure Scan Engine instance integration settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/add-view-scan-engine-related-lists.md)**  
You can view and configure a variety of information, formatted into lists, that the Scan Engine uses to implement its various scanning types.
-   **[Configure definition properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/additional-scan-engine-properties.md)**  
You can configure additional capabilities and configuration options for the definition ruleset.
-   **[Configure real-time scanning properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/configure-real-time-scanning-properties.md)**  
Real-time scanning properties allow control over which users have access to real-time scanning, and how the scan operates within their environment. Perform the following procedure to configure real time scanning properties.
-   **[Configure exception reason properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/exception-reason-properties.md)**  
When real-time enforcement, `enforce_real_time_validation` is set to `true`, Recommend level findings require an approved exception reason before the form can be saved.
-   **[Configure update set scanning properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/update-set-scanning-properties.md)**  
The Scan Engine provides several options to further configure update set scanning and enhance the governance over update set management. Update set scanning occurs during scheduled instance scans. The settings on this tab define which update sets will be scanned, and the parameters those update sets have to meet in order to be marked complete.

**Parent Topic:**[Activate Scan Engine and review settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/configure-initial-scan-engine-settings.md)

