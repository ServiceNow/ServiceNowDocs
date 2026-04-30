---
title: Workflow run time metrics
description: You can enable the collection of workflow run time metrics to determine whether workflows are performing as expected or consuming additional resources.Provide an estimated run time that can be compared to actual workflow run times.Workflow run times are identified as outliers when they are longer or shorter than the outlier range that is computed for the workflow.When a workflow runs within the outlier range, its estimated run time is automatically updated.
locale: en-US
release: yokohama
product: Legacy Workflow
classification: legacy-workflow
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Workflow administration, Classic Workflow, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Workflow run time metrics

You can enable the collection of workflow run time metrics to determine whether workflows are performing as expected or consuming additional resources.

Outlying run times for a workflow are identified by comparing actual run times to an outlier range calculated with the outlier threshold and estimated run time defined in the workflow properties.

You can monitor the results of these metrics on the Workflow Operations Dashboard and custom homepages with workflow gauges.

**Important:**

The functionality found in homepages, arranging information from your instance to tell a story about your data, is found in dashboards on new instances. On upgraded instances with Next Experience enabled, users can view existing homepages if they have a direct URL, but they can't create or edit them. Responsive dashboards and Analytics Center dashboards take over homepage functionality.

Use the [Homepage deprecation help tool](https://www.servicenow.com/docs/access?context=homepage-deprecation-help-tool&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US) to convert the homepages on your instance to responsive dashboards.

For more information, see:

-   [Dashboards in the Analytics Center](https://www.servicenow.com/docs/access?context=analytics-center-dashboards&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US).
-   [Working with responsive dashboards](https://www.servicenow.com/docs/access?context=c_ResponsiveDashboards&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US).

**Parent Topic:**[Workflow administration](../../workflow/concept/c_WorkflowAdministration.md)

## Enable workflow run time metrics

Provide an estimated run time that can be compared to actual workflow run times.

### About this task

For baseline workflows, you must also manually enable the collection of run time metrics. The system automatically enables the collection of run time metrics for new workflows.

### Procedure

1.  Navigate to **All** &gt; **Workflow** &gt; **Workflow Editor**.

2.  Open and check out the workflow.

3.  In the title bar, click the menu icon and select **Properties**.

4.  In the Workflow Properties dialog box, click the **Estimated Runtime** tab.

5.  To enable the collection of run time metrics, check that the **Requires ERT** option is selected.

6.  Open a configuration from the **Estimated Run Time** column.

7.  In **Estimated Run Time**, enter an initial estimate for the workflow's run time.

    The system compares this initial estimate to actual run time results to create outlier reports. The system can automatically update this field in certain circumstances. Workflow designers can also manually update this field.

8.  In the **Outlier Percentage Threshold for ERT** field, enter the percentage deviation from the estimated run time that identifies an outlier workflow run time.

    The system uses a default value of **20**.

9.  Click **Update**.


## Outlying workflow run times

Workflow run times are identified as outliers when they are longer or shorter than the outlier range that is computed for the workflow.

The outlier range is automatically computed with the **Estimated Run Time** and **Outlier Percentage Threshold for ERT** values in the workflow properties. These values are used in the following formulas.

<table id="table_bg2_xp3_dr"><thead><tr><th>

Value computed

</th><th>

Computation used

</th><th>

Example

</th></tr></thead><tbody><tr><td>

Outlier Value

</td><td>

**Estimated Run Time** \* \(**Outlier Percentage Threshold for ERT** / 100\)

</td><td>

10 seconds \* \(20 / 100\) 10 seconds \* 0.2 = 2 seconds

</td></tr><tr><td>

Outlier Range

</td><td>

\(**Estimated Run Time** - *Outlier Value*\) to \(**Estimated Run Time** + *Outlier Value*\)

</td><td>

\(10 seconds - 2 seconds\) to \(10 seconds + 2 seconds\) = 8 to 12 seconds

</td></tr></tbody>
</table>When a workflow runs within the outlier range, its estimated run time is automatically updated.

If a workflow has an outlying run time, it appears in any outlier workflow gauges on the Workflow Operations Dashboard and custom home pages.

## Workflow estimated run time updates

When a workflow runs within the outlier range, its estimated run time is automatically updated.

The estimated run time is updated with the cumulative moving average of the latest run time value in relation to previous run times. The computed value is rounded to the nearest second and stored as a [GlideDateTime](https://www.servicenow.com/docs/access?context=p_GlideServerAPIs&version=yokohama&pubname=yokohama-api-reference&section=c_GlideDateTime&ft:locale=en-US).

For example:

|Data point|Latest value|Cumulative running average \(CRA\)|CRA after rounding to the nearest second|
|----------|------------|----------------------------------|----------------------------------------|
|1|10 seconds|10 seconds|10 seconds|
|2|12 seconds|11 seconds|11 seconds|
|3|9 seconds|10.333 seconds|10 seconds|

**Note:** Because the system rounds to the nearest second, the calculation is less precise with short durations.

You can also manually update the estimated run time in the workflow properties.

