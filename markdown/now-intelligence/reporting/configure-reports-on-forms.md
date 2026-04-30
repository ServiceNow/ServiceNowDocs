---
title: Configure charts on forms
description: You can add reports to forms such as change requests, and configure the report visualizations to display information relevant to the user of the form. The configuration is specific to the current view.
locale: en-US
release: yokohama
product: Reporting
classification: reporting
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Advanced reporting topics, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Configure charts on forms

You can add reports to forms such as change requests, and configure the report visualizations to display information relevant to the user of the form. The configuration is specific to the current view.

## Before you begin

Role required: admin

The following report types are not supported on forms: List, Pivot, Multilevel Pivot, Calendar, and Single Score.

## Procedure

1.  Select the table on which you want to configure a form with a report in the **Filter navigator** and select a record.

    For example, select a record from `task.list`.

2.  From the context menu \(![Context menu icon](../../performance-analytics/image/ContextMenu.png)\), select **Configure** &gt; **Form Layout**.

    ![Configure form layout menu path](../image/config-form-layout.png)

3.  From the **Available** list, add `*Chart` to the **Selected** column.

    Use the up and down arrows to position the report on the form.![Configure form layout options with *Chart highlighted in the Available column, highlighting the arrows.](../image/config-form-layout-options.png)

4.  Specify a label for the chart.

    This option appears when you select the up or down arrow to specify the report's place on the form. The label appears next to the report in the form. If you do not specify a label, the label New Chart is used.

5.  Select **Save**.

    The text **Configure chart** appears on the form in the specified position.

6.  Select **Configure chart**.

7.  Select the search icon \(![](../image/SearchIcon.png)\) to select a report.

    ![Form chart form with the search icon highlighted](../image/config-form-select-report.png)

8.  Specify the height of the chart.

    The default value is 300 pixels.

9.  You can filter the data in the report based on selected fields or based on a scripted filter or an encoded query.

    The first field must be visible on the form. To add fields to the form, select **Configure** &gt; **Form Layout** move the field from the **Available** column to **Selected**.

    On the **Report condition extension** tab, select the form field on which the report is updated and the field on the report source table to which the form field is compared.

    To specify a scripted filter or an encoded query, select **Advanced condition Extension** and paste the script in the **Report Qual** text box. Advanced condition extensions, if present, override report condition extensions.

10. Select **Update**.

11. To change the configuration, right click on the label and select **Configure chart**.

    ![Report on form label with context menu highlighting Configure chart.](../image/configure-chart-form.png)


## Result

The selected report appears on all forms which are of the same type as the one selected. These reports are filtered based on the report condition extensions.

**Parent Topic:**[Advanced reporting topics](../concept/c_AdvancedReporting.md)

