---
title: Create a threshold for each KPI in a KPI group
description: Create a threshold for each KPI in a KPI group to monitor the indicator status and analyze your team’s performance. Define the threshold with upper- and lower-limit values to assess team performance for each indicator.
locale: en-US
release: xanadu
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Setting up Teams in Workforce Optimization for ITSM, Teams in Workforce Optimization for ITSM, Workforce Optimization for ITSM, IT Service Management]
---

# Create a threshold for each KPI in a KPI group

Create a threshold for each KPI in a KPI group to monitor the indicator status and analyze your team’s performance. Define the threshold with upper- and lower-limit values to assess team performance for each indicator.

## Before you begin

Role required: sn\_team\_perf.team\_performance\_admin

## Procedure

1.  Navigate to **All** &gt; **Workforce Optimization for ITSM** &gt; **Team Performance** &gt; **KPI Groups**.

2.  Open any KPI group for which you want to create a KPI threshold, for example, IT Service.

3.  Open any KPI, for example, Closed incidents.

4.  Select the **KPI Thresholds** tab.

5.  On the form, fill in the fields.

<table id="table_ydz_ncc_gxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

KPI

</td><td>

Name of the KPI that you selected. This field is auto-filled.

</td></tr><tr><td>

Lower Threshold

</td><td>

Lower limit defined for this KPI.

</td></tr><tr><td>

Upper Threshold

</td><td>

Upper limit defined for this KPI.

</td></tr><tr><td>

Status

</td><td>

The status for the defined threshold: Critical, Positive, or Warning.

 **Note:** The corresponding icon for each status is displayed in the Workforce Optimization workspace when the **Show Icon** check box is enabled for the status. This option is enabled by default for the critical status.

</td></tr><tr><td>

Order

</td><td>

A number for the defined threshold limits. This number must be unique for each set of limits.

</td></tr><tr><td>

Show Icon

</td><td>

Corresponding icon for each status. The icons are displayed only on the Manager Workspace when the **Show Icon** check box is selected.

 The parent KPI related to the KPI group shows the icons based on a threshold in the grid component, if applicable.

 Users can view the following icons based on a threshold in the Workforce Optimization workspace.

-   The critical icon \(![Critical icon.](../image/critical-icon.png)\)
-   The positive icon \(![Positive icon.](../image/positive-icon.png)\)
-   The warning icon \(![Warning icon.](../image/warning-icon.png)\)
 The icons are displayed on all the pages where the parent KPIs are related to the KPI group based on the values that you set for the lower- and upper-threshold limits.

</td></tr></tbody>
</table>6.  Select **Submit**.

    **Note:** In the Manager workspace, when users drill down into a KPI, the single scorecard component shows a threshold warning for critical thresholds nearing or exceeding the threshold limit. The following are examples of the messages that the scorecard shows:

    -   Approaching threshold of 95%
    -   Exceeded threshold of 170
    The scorecard shows the warnings corresponding to the followings conditions:

    -   **For maximize type KPIs**
        -   Value &lt; Lower Threshold \(Critical\): Exceeded &lt;Lower Threshold Value&gt;
        -   Lower Threshold \(Critical\) &lt; Value &lt; Upper Threshold \(Critical\): Approaching &lt;Lower Threshold Value&gt;
    -   **For minimize type KPIs**
        -   Value &gt; Upper Threshold \(Critical\): Exceeded &lt;Upper Threshold Value&gt;
        -   Lower Threshold \(Critical\) &lt; Value &lt; Upper Threshold \(Critical\): Approaching &lt;Upper Threshold Value&gt;

**Parent Topic:**[Setting up Teams in Workforce Optimization for ITSM](../concept/setup-teams-configurable-workforce-optimization-itsm.md)

