---
title: Configure Scan Engine parameters
description: Configure the primary scanning capabilities and configuration options for scheduled, on-demand, and real-time scans.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/impact/configure-scan-engine-properties.html
release: zurich
topic_type: task
last_updated: "2026-06-11"
reading_time_minutes: 3
keywords: [impact scan engine, scan properties, scheduled scans]
breadcrumb: [Scan Engine, Platform Health, Using Impact, Impact]
---

# Configure Scan Engine parameters

Configure the primary scanning capabilities and configuration options for scheduled, on-demand, and real-time scans.

## Before you begin

Review these properties before you [Run your first scan with the Scan Engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/impact/run-scan-engine.md) or to make changes to Scan Engine behavior.

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
