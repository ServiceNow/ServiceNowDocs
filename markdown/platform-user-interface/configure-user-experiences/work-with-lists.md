---
title: Work with lists in workspace
description: Open a list of records in workspace so you can choose one to work on.Make updates to a record directly from a list, without leaving the list.Sort the records displayed in list view to more easily find the records you want to work on.Filter the records to reduce the number of records displayed in list view so you can find the records you want to work on.Group the records displayed in list view to more easily find the records you want to work on.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-user-interface/configure-user-experiences/work-with-lists.html
release: zurich
product: Configure User Experiences
classification: configure-user-experiences
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 8
breadcrumb: [Using lists to find work to do, Finding issues to work on in your Workspace, Use, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Work with lists in workspace

Open a list of records in workspace so you can choose one to work on.

## Before you begin

Role required: workspace\_user

## About this task

List view enables you to see high-level information for all records in a list filter. Normally, clicking a field in a record in a list opens that record. If the field is clickable \(a reference, document ID, or URL\), clicking it does not open the record, it opens the record or URL that the clickable field points to.

\[Omitted image "list-view.png"\] Alt text: List of unassigned open incidents in workspace

**Last refreshed** indicates how long ago the values in the list were last refreshed. To refresh the values, refresh the page.

Each list has an associated URL. You can bookmark a list to enable quick access to it.

Here's how to open a list to find records you want to work on.

## Procedure

1.  Click the list icon \(\[Omitted image "list-icon-black.png"\] Alt text: List icon\).

2.  Find a list category that contains the records you want to work on, for example, **Tasks**.

3.  Click one of the list filters under it.

    For example, under **Tasks**, you might click on a list filter called **My Work**. That would open up a list of task records assigned to you. The list filter title and the number of records in the list appear at the top of the list. In the previous image, the **All** list contains 8383 records.

4.  To preview a record before opening it, move your mouse over a record and click the information icon \(\[Omitted image "icon-information.png"\] Alt text: Information icon\).

    \[Omitted image "preview-record-from-list-view.png"\] Alt text: Preview record

    A side panel opens that shows the record.

5.  To move to a different page of records, click a page number or one of the arrows to move forward or backwards a page, or to the first or last page of records.

    \[Omitted image "list-pagination.png"\] Alt text: List pagination

6.  To change the number of records displayed on a page, click the number beside rows per page and select a number from the menu.

    \[Omitted image "list-rows-per-page.png"\] Alt text: Rows per page

7.  Click a record number to open it.

8.  To export the records in a list in one of the following formats: CSV, XLSX, JSON, or PDF, click the gear icon \[Omitted image "gear-outline.png"\] Alt text: Gear icon and select **Export**.


## What to do next

Now that you know how to open a list and the records in it, find out how to [edit records in list view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-user-interface/configure-user-experiences/work-with-lists.md).

## Edit records in list view

Make updates to a record directly from a list, without leaving the list.

### Before you begin

Role required: agent\_workspace\_user

### About this task

You can revise one or more records while in list view. To learn more about a record before editing it, view and revise it in [record view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-user-interface/configure-user-experiences/finding-answers.md).

### Procedure

1.  Revise a single record from a list.

    1.  Click the Open Preview icon \[Omitted image "circle-info-outline.png"\] Alt text: Open preview icon.

        The record opens.

        \[Omitted image "list-edit-record.png"\] Alt text: Edit record from list

    2.  Revise the values in the fields and click **Update**.

2.  Revise multiple records at once.

    1.  In list view, click the boxes to the left of all the records you want to revise.

        \[Omitted image "records-to-revise.png"\] Alt text: Records to revise

    2.  Click **Edit**.

        A preview pane opens and shows you the fields you can edit in the selected records.

        \[Omitted image "list-edit-6-records.png"\] Alt text: Edit multiple records at once

    3.  Revise the values in the fields and click **Update**.


### What to do next

Now that you know how to edit a record in list view, find out how to [sort and filter the records displayed in a list](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-user-interface/configure-user-experiences/work-with-lists.md).

## Sort records in lists

Sort the records displayed in list view to more easily find the records you want to work on.

### Before you begin

Role required: agent\_workspace\_user

### About this task

Filtered lists can contain thousands of records. Sorting them by field values can help you find the records you want to work on. You can sort the entire list based on any of the columns in the list.

### Procedure

1.  To change the field the records are sorted by, double click a column heading.

    An arrowhead icon \(\[Omitted image "icon-arrowhead-up-full.png"\] Alt text: Ascending sort\) appears to the right of the column heading you clicked and workspace sorts the list of records based on the values in that column. An arrowhead pointed down means the values are sorted from highest to lowest values.

    \[Omitted image "sort-column-arrowhead.png"\] Alt text: Sort column

2.  To reverse the sorting order, click the arrowhead icon so the arrowhead reverses direction.


### What to do next

Instead of sorting records, you might want to [Filter records in lists](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-user-interface/configure-user-experiences/work-with-lists.md) to reduce the number of records displayed in list view.

## Filter records in lists

Filter the records to reduce the number of records displayed in list view so you can find the records you want to work on.

### Before you begin

Role required: agent\_workspace\_user

### About this task

Filtering removes records from a list so you can view only those records you're interested in working on.

Workspace provides the following ways of filtering records displayed in a list:

-   Use the filter icon \(\[Omitted image "filter-outline.png"\] Alt text: Filter icon\).
-   Filter directly in the list using the column heading.
-   Filter directly in the list using the values in the columns.

### Procedure

1.  To filter out records using the filter icon \(\[Omitted image "filter-outline.png"\] Alt text: Filter icon\):

    1.  Click the filter icon \(\[Omitted image "filter-outline.png"\] Alt text: Filter icon\).

    2.  Click **Advanced View**.

    3.  Use the condition builder to specify the conditions one or more field values must meet for a record to appear in the list.

        For example, \[Active\]\[is\]\[true\], and \[Urgency\]\[is\]\[1- High\].

    4.  To add more conditions, click **New condition set** and supply a condition.

    5.  Select **Save Filter**, enter a filter name, and choose permissions to determine who can use the filter.

        Retrieve the filter by selecting **Use existing filter** and select the filter.

    6.  Click **Update**.

        The list filter icon \[Omitted image "ListFilterBadge.png"\] Alt text: List filter icon with badge shows the number of conditions that apply to the current list.

2.  Filter records based on field values displayed.

    You can work directly with list columns to filter out records.

    1.  Click the **More UI Actions** icon \[Omitted image "ellipsis-v-fill.png"\] Alt text: More UI Actions icon to the right of a column heading.

    2.  Click the downward pointing arrowhead icon \(\[Omitted image "icon-down-arrow-full.png"\] Alt text: Down arrowhead\) and select a filter condition, such as **is not**, **starts with**, or **contains**.

        \[Omitted image "column-filtering-1.png"\] Alt text: Column filtering

    3.  Enter the field value to filter the list on the bottom line and click **Apply**.

        In the following example, the only records that appear have **Caller** values that start with **David**.

        \[Omitted image "column-filter.png"\] Alt text: Column filter

        **Note:** Not all field types support column filtering. You can use the Advanced Filter panel and condition builder to create a filter for those field types.

    4.  If the values come from the sys\_choice table, the possible values \(choices\) appear with boxes beside them.

        \[Omitted image "column-filtering-lists.jpg"\] Alt text: Column filtering

        If there are more than ten fields, workspace displays a **Filter**, as shown here, so you don't have to scroll to find a field value. If there are less than ten choices, there's no entry filter under **Filter**.

        You can click **All** to select all of the fields or **None** to uncheck all of the fields. **All** selects all of the field values that meet the filter conditions, not just those shown in the pop up. Likewise, **None** unchecks all of the fields that meet the filter conditions, not just those shown in the pop up. You can combine these functions. For example, you can filter on `Windows` and select **All**, and then filter on `2000` and select **None** and wind up with rows that contain Windows but not Windows 2000.

        You cannot configure the number of fields \(10\) that makes the **Filter** entry field appear.

    5.  To remove the filter and restore all of the records, click the **More UI Actions** icon \(\[Omitted image "ellipsis-v-fill.png"\] Alt text: More UI Actions icon\) and click **Clear**.

3.  Filter out records based on field values.

    This feature is similar to the one in the previous step but you can't enter a term to filter the records.

    1.  Click a field in the record.

    2.  Click the More UI Actions icon \(\[Omitted image "ellipsis-v-fill.png"\] Alt text: More UI Actions icon\).

        \[Omitted image "show-matching.png"\] Alt text: Show matching

    3.  To remove all records that don't have the same field value, click **Show Matching**.

    4.  To remove all records in the list that have the same field value, click **Filter Out**.

        By default, a column sorts in an ascending order unless the column data type is a date. Dates sort in a descending order.


### What to do next

Instead of filtering records, you might like to [group records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-user-interface/configure-user-experiences/work-with-lists.md) in list view.

## Group records in lists

Group the records displayed in list view to more easily find the records you want to work on.

### Before you begin

Role required: agent\_workspace\_user

### About this task

You can group records that have the same values in a column so you can see similar records.

### Procedure

1.  Move the mouse over a column heading and click the More Options icon \(\[Omitted image "ellipsis-v-fill.png"\] Alt text: More UI Actions icon\).

2.  Click the first option, **Group by &lt;column-heading-name&gt;** where &lt;column-heading-name&gt; is the name of the column you're clicking in.

    \[Omitted image "group-records-by-field-value.png"\] Alt text: Group records by field value

    The records are grouped based on the values in the selected column.

    \[Omitted image "group-by-short-description.png"\] Alt text: Group list by column

    The display shows the number of records in each group.

3.  Open a group by clicking its arrowhead icon \(\[Omitted image "icon-arrowhead-right.png"\] Alt text: Expand icon\).

4.  To ungroup the records, mouse over the same column heading, click the More Options icon \(\[Omitted image "ellipsis-v-fill.png"\] Alt text: More UI Actions icon\) and click **Ungroup by &lt;column-heading-name&gt;**.


### What to do next

Instead of grouping records, you might like to [Filter records in lists](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-user-interface/configure-user-experiences/work-with-lists.md).

