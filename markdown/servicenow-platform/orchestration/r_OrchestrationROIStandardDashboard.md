---
title: Orchestration ROI standard reports
description: The dashboard of standard ROI reports provides summaries, estimated costs, and calculated costs for automated processes. To access the ROI standard dashboard, navigate to Orchestration ROI Reports Dashboard .The scheduled job that calculates Orchestration ROI standard reports is active by default and controlled by system properties.
locale: en-US
release: zurich
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Orchestration ROI reports, Orchestration ROI, Orchestration applications, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Orchestration ROI standard reports

The dashboard of standard ROI reports provides summaries, estimated costs, and calculated costs for automated processes. To access the ROI standard dashboard, navigate to **Orchestration** &gt; **ROI Reports** &gt; **Dashboard**.

## Summary tab

The Summary tab contains four reports on automation categories.

![What the ROI summary report may look like.](../image/ROISummaryReportSample.png "ROI summary report sample")

<table id="table_bdv_jjs_zs"><thead><tr><th>

Report

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Manual Tasks by Category Over Time

</td><td>

Trend of manual tasks by category over time. For example, if you use automations to perform a portion of the necessary tasks, the report shows the number of tasks still executed manually, decreasing over time. -   **Type**: Line chart
-   **Table**: Detailed Savings Report \[detailed\_savings\_report\]

</td></tr><tr><td>

Automations by Category Over Time

</td><td>

Trend of automated tasks by category over time. For example, this chart can show the increase in the number of automated tasks as a workflow automation rolls out slowly over time.-   **Type**: Line chart
-   **Table**: Detailed Savings Report \[detailed\_savings\_report\]

</td></tr><tr><td>

Automation Savings by Category Over Time \(Uses Estimated Duration\)

</td><td>

Amount of savings from automated tasks over time, based on the estimated duration of the task, the number of automations performed, and the cost from the labor rate card.-   **Type**: Line chart
-   **Table**: Detailed Savings Report \[detailed\_savings\_report\]

</td></tr><tr><td>

Automation Savings by Category Over Time \(Uses Calculated Duration\)

</td><td>

Amount of savings from automated tasks over time, based on the calculated duration of the task, the number of automations performed, and the cost from the labor rate card.-   **Type**: Line chart
-   **Table**: Detailed Savings Report \[detailed\_savings\_report\]

</td></tr></tbody>
</table>## Estimated Costs tab

The Estimated Costs tab contains eight reports on estimated time and expense for automations.

![ROI estimated time and expense report](../image/ROIEstimatedReportsSample1.png "ROI estimated time and expense report samples") ![ROI estimated reports sample](../image/ROIEstimatedReportsSample2.png "ROI estimated time and expense report samples")

<table id="table_c3m_r1t_zs"><thead><tr><th>

Report

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Estimated Time Spent by Task Category

</td><td>

Total estimated time spent, in minutes, on all tasks by task category. -   **Type**: Pie chart
-   **Table**: Automation Entry Form \[automation\_entry\_form\]

</td></tr><tr><td>

Estimated Volume of Manual Tasks per Month by Category

</td><td>

Total estimated volume of all tasks per month by task category. -   **Type**: Pie chart
-   **Table**: Automation Entry Form \[automation\_entry\_form\]

</td></tr><tr><td>

Predicted Hours Spent Monthly by Category \(Uses Estimated Duration &amp; Volume\)

</td><td>

Total predicted hours spent monthly on all manual tasks by category, using the estimated duration of each task and the estimated volume of each task per month.-   **Type**: Bar chart
-   **Table**: Expense and Savings \[run\_rate\_predicted\_savings\]

</td></tr><tr><td>

Predicted Monthly Expense by Category \(Uses Estimated Duration &amp; Volume\)

</td><td>

Total predicted monthly expense for all manual tasks by category, using the estimated duration of each task, estimated volume of each task per month, and the cost from the labor rate card. **Note:** This report uses negative numbers to express an expense.

 -   **Type**: Bar chart
-   **Table**: Expense and Savings \[run\_rate\_predicted\_savings\]

</td></tr><tr><td>

Predicted Hours Spent Quarterly by Category \(Uses Estimated Duration &amp; Volume\)

</td><td>

Total predicted hours spent quarterly on all manual tasks by category, using the estimated duration of each task and the estimated volume of each task per month.-   **Type**: Bar chart
-   **Table**: Expense and Savings \[run\_rate\_predicted\_savings\]

</td></tr><tr><td>

Predicted Quarterly Expense by Category \(Uses Estimated Duration &amp; Volume\)

</td><td>

Total predicted quarterly expense for all manual tasks by category, using the estimated duration of each task, estimated volume of each task per month, and the cost from the labor rate card. **Note:** This report uses negative numbers to express an expense.

 -   **Type**: Bar chart
-   **Table**: Expense and Savings \[run\_rate\_predicted\_savings\]

</td></tr><tr><td>

Predicted Hours Spent Annually by Category \(Uses Estimated Duration &amp; Volume\)

</td><td>

Total predicted hours spent annually on all manual tasks by category, using the estimated duration of each task and the estimated volume of each task per month.-   **Type**: Bar chart
-   **Table**: Expense and Savings \[run\_rate\_predicted\_savings\]

</td></tr><tr><td>

Predicted Annual Expense by Category \(Uses Estimated Duration &amp; Volume\)

</td><td>

Total predicted annual expense for all manual tasks by category, using the estimated duration of each task, estimated volume of each task per month, and the cost from the labor rate card. **Note:** This report uses negative numbers to express an expense.

 -   **Type**: Bar chart
-   **Table**: Expense and Savings \[run\_rate\_predicted\_savings\]

</td></tr></tbody>
</table>## Costs from Correlated Tasks tab

The Costs from Correlated Tasks tab contains eight reports on time and expense for automations based on actual calculations.

![ROI calculated time and expense report sample](../image/ROICalculatedReportsSample1.png "ROI calculated time and expense report samples") ![Projected monthly expense by category sample](../image/ROICalculatedReportsSample2.png "ROI calculated time and expense report samples")

<table id="table_dt3_dpt_zs"><thead><tr><th>

Report

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Time Spent by Task Category

</td><td>

Total actual time spent, in minutes, on all tasks by task category.-   **Type**: Pie chart
-   **Table**: Automation Entry Form \[automation\_entry\_form\]

</td></tr><tr><td>

Volume of Manual Tasks per Month by Category

</td><td>

Total actual volume of all tasks per month by task category.-   **Type**: Pie chart
-   **Table**: Automation Entry Form \[automation\_entry\_form\]

</td></tr><tr><td>

Projected Hours Spent Monthly by Category \(Uses Calculated Duration &amp; Volume\)

</td><td>

Total projected hours spent monthly on all manual tasks by category, using the calculated duration of each task and the calculated volume of each task per month. -   **Type**: Bar chart
-   **Table**: Expense and Savings \[run\_rate\_predicted\_savings\]

</td></tr><tr><td>

Projected Monthly Expense by Category \(Uses Calculated Duration &amp; Volume\)

</td><td>

Total projected monthly expense for all manual tasks by category using the calculated duration of each task, the calculated volume of each task per month, and the cost from the labor rate card.**Note:** This report uses negative numbers to express an expense.

 -   **Type**: Bar chart
-   **Table**: Expense and Savings \[run\_rate\_predicted\_savings\]

</td></tr><tr><td>

Projected Hours Spent Quarterly by Category \(Uses Calculated Duration &amp; Volume\)

</td><td>

Total projected hours spent quarterly on all manual tasks by category, using the calculated duration of each task and the calculated volume of each task per month. -   **Type**: Bar chart
-   **Table**: Expense and Savings \[run\_rate\_predicted\_savings\]

</td></tr><tr><td>

Projected Quarterly Expense by Category \(Uses Calculated Duration &amp; Volume\)

</td><td>

Total projected quarterly expense for all manual tasks by category using the calculated duration of each task, the calculated volume of each task per month, and the cost from the labor rate card.**Note:** This report uses negative numbers to express an expense.

 -   **Type**: Bar chart
-   **Table**: Expense and Savings \[run\_rate\_predicted\_savings\]

</td></tr><tr><td>

Projected Hours Spent Annually by Category \(Uses Calculated Duration &amp; Volume\)

</td><td>

Total projected hours spent annually on all manual tasks by category, using the calculated duration of each task and the calculated volume of each task per month. -   **Type**: Bar chart
-   **Table**: Expense and Savings \[run\_rate\_predicted\_savings\]

</td></tr><tr><td>

Projected Annual Expense by Category \(Uses Calculated Duration &amp; Volume\)

</td><td>

Total projected annual expense for all manual tasks by category using the calculated duration of each task, the calculated volume of each task per month, and the cost from the labor rate card.**Note:** This report uses negative numbers to express an expense.

 -   **Type**: Bar chart
-   **Table**: Expense and Savings \[run\_rate\_predicted\_savings\]

</td></tr></tbody>
</table>**Parent Topic:**[Orchestration ROI reports](../concept/c_OrchestrationROIDashboards.md)

## Schedule Orchestration ROI calculations for standard reports

The scheduled job that calculates Orchestration ROI standard reports is active by default and controlled by system properties.

### Before you begin

Role required: orchestration\_manager, admin

### About this task

The system provides a default scheduled job called Processing ROI Schedule that allows you to configure when Orchestration calculates the ROI for standard reports. This schedule allows scripting for advanced conditions. To modify the schedule or write a script to run, open Processing ROI Schedule from **System Scheduler** &gt; **Scheduled Jobs** &gt; **Scheduled Jobs** and click **Configure Job Definition**. To execute the schedule directly from the job definition, click **Execute Now**

To control the running of the schedule job with the Orchestration properties.

### Procedure

1.  Navigate to **Orchestration ROI** &gt; **Properties**.

2.  Configure the following properties:

<table id="table_jdv_fvr_3v"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

roi.processing.active

</td><td>

Activate scheduled job for ROI processing. This property activates the Processing ROI Schedule scheduled job.-   **Type**: true \| false
-   **Default**: true


</td></tr><tr><td>

roi.processing.interval

</td><td>

Scheduled ROI processing interval \(hours\). This property sets the repeat interval for the scheduled job that processes savings reports and correlated tasks.-   **Type**: integer
-   **Default**: 24


</td></tr></tbody>
</table>3.  Click **Save** to save your changes.


