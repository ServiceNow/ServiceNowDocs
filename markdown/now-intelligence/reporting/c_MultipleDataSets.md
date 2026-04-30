---
title: Using multiple datasets in Core UI reports
description: You can create reports that use datasets from up to five tables in a single report. Add up to five extra datasets to visualize data from multiple sources in a single report.
locale: en-US
release: zurich
product: Reporting
classification: reporting
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Advanced Core UI reporting topics, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Using multiple datasets in Core UI reports

You can create reports that use datasets from up to five tables in a single report.

The following report types support multiple datasets: bar, horizontal bar, column, line, step line, area, spline.

Multiple **Group by**s are not supported on multiple datasets. When using multiple datasets, the report legend is always displayed.

![Multiple data sets](../image/MultipleDataSetsINTPRB.png "Incident and Problem data in one report")

## Restrictions

Bear the following restrictions in mind when creating a report with multiple data sets:

-   Up to a maximum of 5 additional datasets can be added to any particular report. Keep in mind that each additional dataset will require additional processing and querying of the database, so if a particular report is experiencing performance issues, it could be due to the fact the report has multiple associated data sets.
-   All datasets associated with a parent report must be of the same type \(such as bar, donut, or pie\) as the parent report.
-   For multiple datasets associated with a time series chart, all additional data sets must have the same setting in the **Per** field as the parent report.
-   For multiple datasets on a Bar or Horizontal Bar chart, all associated datasets must have the same Group By value.
-   The Show Legends option is always, by default, displayed on a report with multiple datasets, even if the parent report has this option unselected.

**Parent Topic:**[Advanced Core UI reporting topics](c_AdvancedReporting.md)

## Add an additional dataset to a report

Add up to five extra datasets to visualize data from multiple sources in a single report.

### Before you begin

Role required: itil, report\_user. The property **glide.ui.doctype** must be enabled.

### Procedure

1.  Navigate to **All** &gt; **Reports** &gt; **View / Run**.

2.  Create a report of a type that supports multiple datasets, or select an existing report of one of these types.

    You can add additional sets to bar, horizontal bar, line, column, area, and spline reports.

3.  Click the **Show report structure** icon \(![Show report structure](../image/Form_ShowReportStructureIcon.png)\).

    ![Add dataset example: Open Show report structure from a bar report](../image/show-report-structure-add-dataset.png)

4.  Select **Add dataset**.

5.  On the **Data** tab, provide a custom name for the additional data set to appear in the legend of the report, select a data source, and click the **Configure** tab.

    ![Add dataset example: Name the dataset from the Data tab](../image/add-dataset-group-by-example.png)

6.  On the **Configure** tab, specify applicable fields the same way that you would configure a standalone report.

    The dataset must have the same Group by and Stack by values as the parent report. The dataset should also have the same aggregation on the same field. Note attention to the following fields on applicable report types.

    ![Add dataset example: Specify grouping and stacking from the Configure tab](../image/add-dataset-group-by-example-config-tab.png)

    **Note:** The **Display data table** option is not available from the **Add dataset** module, but is only available from the **Configure** tab of the main Report Designer. If the **Display data table** option is selected, only the first dataset will display on the data table.

7.  On the **Style** tab, specify the following fields the same way that you would configure a standalone report.

8.  Click **Save dataset**.


### Result

The report is generated with the information from the additional dataset.

