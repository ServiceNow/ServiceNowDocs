---
title: Drilling down within Core UI reports
description: You can drill down within a report to visualize a subset of its data. For example, you can click on the critical section of a report sorted by priority to view the categories of those critical incidents.You can define a report drilldown to enable reporting users to view subsets of the report data. When you define a report drilldown, it applies only to the report for which you define it.
locale: en-US
release: australia
product: Reporting
classification: reporting
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Advanced Core UI reporting topics, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Drilling down within Core UI reports

You can drill down within a report to visualize a subset of its data. For example, you can click on the critical section of a report sorted by priority to view the categories of those critical incidents.

For reports with a defined drilldown, click on a portion of the chart to display a subset of data. The subset may use a different chart type. In the example, the user clicks on the critical incidents in a bar chart to reveal the categories of critical incidents in a semi-donut chart.

**Note:** This topic refers to Reporting in the Core UI. For instances migrated to Platform Analytics experience and new Australia instances, see [Chart interactions in a data visualization](../../par-for-workspace/concept/dv-chart-interactions.md).

![Drilldown example with two report types](../image/drilldown-example-2.png "Drilldown example")

All chart types except for list, histogram, calendar, control, box, and trendbox charts support drilling down. Drilling down is not available on charts added to forms, and charts embedded as iframes. You can define any number of drilldown levels for a report.

**Note:** Drilldown reports do not export to PDF. If you select **Export to PDF** on a drilldown, a PDF of the top level report is generated.

**Parent Topic:**[Advanced Core UI reporting topics](c_AdvancedReporting.md)

## Define a report drilldown

You can define a report drilldown to enable reporting users to view subsets of the report data. When you define a report drilldown, it applies only to the report for which you define it.

### Before you begin

Role required: itil, report\_user, report\_group, report\_global, report\_admin, or admin. To create a meaningful report, you must have the right to access the data you want to report on.

The report that you want to define a drilldown for must exist.

**Note:** You can only drill down to data in the same table as the report. The following report types do not support the drilldown feature: list, histogram, calendar, control, box, and trendbox.

This topic refers to Reporting in the Core UI. If your instance is migrated to Platform Analytics experience, see the Chart interaction section of the data visualization type you're configuring.

### Procedure

1.  Navigate to **All** &gt; **Reports**.

2.  Select the report you want to add a drilldown to.

3.  Select **View Report**.

4.  Select the **Show report structure** icon \(![Show report structure](../image/Form_ShowReportStructureIcon.png)\).

    A badge on the Report structure icon displays the number of defined drilldowns.

5.  Select the Add drilldown icon \(![Plus sign button](../../dashboards/image/AddWidgetButton.png)\).

    ![Drilldown example with two levels](../image/drilldown-example.png "Drilldown example")

6.  Enter a **Title** for the drilldown and select **Next**.

7.  Select the report **Type** to display the data and select **Next**.

    See [Report types](../reference/report-types-creation-details-rd.md). The drilldown report type can be different than the parent report.

8.  Configure the drilldown report the same way you would configure any other report.

    Configuration options depend on the selected drilldown report **Type**.

9.  Select **Save drilldown**.


### Result

The user can drill down from the top-level report to the specified drilldown report visualizations.

**Note:** All users can view report visualizations, such as pie charts and column reports. However, the last level of a drilldown is always a list. Platform access control lists determine user access to list information. Users may see a message indicating that rows were removed from the list by Security constraints. For more information, see [Access control list rules](https://www.servicenow.com/docs/access?context=access-control-rules&version=australia&pubname=australia-platform-security&ft:locale=en-US).

