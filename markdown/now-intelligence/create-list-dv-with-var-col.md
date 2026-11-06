---
title: Add variable or question columns to a Platform Analytics list
description: You can create a list data visualization with variables or questions as columns based on a data source or table that has variables associated with it. For example, if an item has a variable called Storage, you can create a list that has a column for the values in this variable.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/now-intelligence/create-list-dv-with-var-col.html
release: australia
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [List visualizations, Create, Data visualizations, Platform Analytics experience, Platform Analytics]
---

# Add variable or question columns to a Platform Analytics list

You can create a list data visualization with variables or questions as columns based on a data source or table that has variables associated with it. For example, if an item has a variable called **Storage**, you can create a list that has a column for the values in this variable.

## Before you begin

You need a List visualization with a data source that is a table with a predefined condition. For information about creating a List, see [Create a Platform Analytics list visualization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/now-intelligence/create-dv-analytics-list.md).

Role required: Anyone with access to data can create a visualization of that data on any dashboard that they can edit. Users with the itil, report\_user, admin, or viz\_creator role can create a visualization in the Visualization Designer. When you create a visualization in the Visualization Designer, it is saved to the Library. For more information on access, see [Report\_view access control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/now-intelligence/report-view-access-control.md) and [Platform Analytics roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/now-intelligence/platform-analytics-roles.md).

## Procedure

1.  Create a Platform Analytics List or open one for editing.

2.  Verify that it has a data source with a predefined condition.

    In the editing page for the data source, open the Filters section and see if you have any choices for the Predefined conditions field.

    \[Omitted image "data-source-predef-conditions.png"\] Alt text: Data source editing page showing available preconfigured conditions.

3.  In the Presentation section of the configuration panel, expand **Columns and rows** and select **+Add**.

4.  Select all of the currently displayed columns that you want to keep.

    If you add a column without doing this first, all the default columns are removed.

5.  At the end of the list of fields, expand the arrow next to **Variables** or **Questions**.

    Depending on system configuration, you can add fields from tables that extend the selected table.\[Omitted image "choose-fields-variables-1.png"\] Alt text: The Choose fields dialog with Variables option highlighted and the pointer on the the Open item: Variables arrow.

6.  In the Variables or Questions column, select the boxes next to the variables or questions that you want to add to the visualization.

    The variables or questions you check are added to the list of selected columns.\[Omitted image "choose-fields-variables-2.png"\] Alt text: The Choose fields dialogue with three variables checked that are also highlighted in the Selected column.

7.  Select **Apply**.

8.  Select **Save**.


**Parent Topic:**[Create a Platform Analytics list visualization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/now-intelligence/create-dv-analytics-list.md)

