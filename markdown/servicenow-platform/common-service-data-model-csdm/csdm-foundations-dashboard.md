---
title: Configure the CSDM Data Foundations dashboard
description: Use the CSDM Data Foundations dashboard to monitor and evaluate key foundational metrics of the CSDM framework.
locale: en-US
release: yokohama
product: Common Service Data Model \(CSDM\)
classification: common-service-data-model-csdm
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Implement, CSDM, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure the CSDM Data Foundations dashboard

Use the CSDM Data Foundations dashboard to monitor and evaluate key foundational metrics of the CSDM framework.

## Before you begin

For an introduction to the dashboard, see [CSDM Data Foundations dashboard](../concept/csdm-data-foundations-dashboard.md).

-   Before you use the dashboard for the first time, populate the CSDM metrics: Navigate to **All** &gt; **System Scheduler** &gt; **Scheduled Jobs** and run the **CSDM Get Well Metric Collection** job.
-   The CSDM Data Foundations dashboard adds the following scheduled jobs that must be running:
    -   **CSDM Get Well Metric Collection**: Calculates and stores details for compliant CIs associated with metrics. Data appears on the dashboard only after the first run of this scheduled job. metrics' scores are stored in the CSDM Data Foundations Metric Scores \[sn\_getwell\_csdm\_score\] table. The job runs daily by default.
    -   **CSDM Data Foundations PA Metric Collection**: Calculates the total count of non-compliant CIs that are associated with each metric. It also provides trending data over time for the non-compliant CIs associated with metrics.
    -   **CMDB Get Well CIs Processed Via IRE Metric Batch Collection**: Invoked once a day \(by default\) by the **CMDB Get Well Metric Collection** job. Repeatedly executes a 10-minute run/one-minute pause cycle to process as many batch files as possible.
-   Role required: app\_service\_admin, app\_service\_user, asset, cmdb\_read, itil\_admin, portfolio\_admin, service\_viewer, or technology\_service\_owner

## Procedure

1.  Navigate to **All** &gt; **CSDM** &gt; **Configuration** &gt; **CSDM Data Foundations Dashboard**.

2.  Select a tab.

    The reports on each tab display the data metrics that are appropriate for the maturity of your organization's CSDM implementation stage \(foundation, crawl, walk, run, and fly\).

3.  Review the reports.

    Note the percentages and color-coding in the **Result** column for each metric.

    -   If the percentage is 100%, the CSDM framework has the information it needs. You don't need to do anything else.
    -   Otherwise, required information is missing and additional actions are required. Continue with [step 5](csdm-foundations-dashboard.md#access-pa-widgets).
    Note the metrics on the **Foundation** tab:

    -   **Named Product Models with Product Owners**

        Shows cmdb\_model records that meet the following conditions:

        -   **Status** = **In production**
        -   **Name** and **Owner** is not empty
    -   **Configuration Item Status Values**

        Shows the percentage of CIs with default status values.

        -   80%: At least 1 to 5 CIs have custom status values.
        -   60%: 6 to 10 CIs have custom status values.
        -   40%: 11 to 15 CIs have custom status values.
        -   20%: 16 or more CIs have custom status values.
        To view the default base-system status values, enter `sn_getwell_oob_status_table_field.list` in the navigator **Filter** text box. The Configuration Item Status Values form displays the list of elements and associated tables. Select a table name to see the list of default labels and values.

        ![Configuration item status values.](../../configuration-management/image/config-item-status-value.png)

    -   **Business Units with Companies**

        Shows business unit records where the **Company** field is not empty.

        **Locations with Parents**.

        Shows cmdb\_ci records that meet the following conditions:

        -   **Status** = installed
        -   **Operational status** = operational
        -   **Location** and **Location.parent** is not empty
4.  Select the tiles associated with the foundational metrics to access Performance Analytics widgets.

    [Performance Analytics widgets](https://www.servicenow.com/docs/access?context=c_Widgets&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US) are provided by the **CSDM PA Metric Collection** scheduled job. These widgets provide trending data over time for the non-compliant CIs associated with the metric.

    -   Ensure that the real-time option is selected \(![real-time option.](../../configuration-management/image/RealTimeFoundationsDashboard.png)\) and then select **Show Records** to view the list of CIs.
    -   Select the **Breakdowns** context menu to view available breakdowns.
5.  Scroll to the list of CIs in the **Custom Status Values** related list.

    The charts show the number of custom values that have been defined for each element. Select a chart to view custom values that have been defined for the element. This example shows custom label-value combinations for the install\_status element.

    ![Custom status values for configuration items.](../../configuration-management/image/custom-config-item-status-value.png)

6.  Select a CI to drill down to the form view.

    The form view provides the required information. If you don't see the form, you might not have sufficient access privileges. Contact your ServiceNow administrator.

7.  When you're finished using the form, select **Update** or **Delete** to return to the list view.

8.  Navigate to return to the CSDM Data Foundations dashboard.


## Result

The key foundational metric results are available for you to review and analyze.

**Parent Topic:**[Implementing the CSDM framework in stages](../concept/csdm-implementation-stages.md)

