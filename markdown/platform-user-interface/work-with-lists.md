---
title: Work with lists in workspace
description: Open a list of records in workspace so you can choose one to work on.Make updates to a record directly from a list, without leaving the list.Sort the records displayed in list view to more easily find the records you want to work on.Filter the records to reduce the number of records displayed in list view so you can find the records you want to work on.Group the records displayed in list view to more easily find the records you want to work on.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 8
breadcrumb: [Using lists to find work to do, Finding issues to work on in your Workspace, Using Configurable Workspace, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Work with lists in workspace

Open a list of records in workspace so you can choose one to work on.

## Before you begin

Role required: workspace\_user

## About this task

List view enables you to see high-level information for all records in a list filter. Normally, clicking a field in a record in a list opens that record. If the field is clickable \(a reference, document ID, or URL\), clicking it does not open the record, it opens the record or URL that the clickable field points to.

![List of unassigned open incidents in workspace](../image/list-view.png)

**Last refreshed** indicates how long ago the values in the list were last refreshed. To refresh the values, refresh the page.

Each list has an associated URL. You can bookmark a list to enable quick access to it.

Here's how to open a list to find records you want to work on.

## Procedure

1.  Click the list icon \(![List icon](../image/list-icon-black.png)\).

2.  Find a list category that contains the records you want to work on, for example, **Tasks**.

3.  Click one of the list filters under it.

    For example, under **Tasks**, you might click on a list filter called **My Work**. That would open up a list of task records assigned to you. The list filter title and the number of records in the list appear at the top of the list. In the previous image, the **All** list contains 8383 records.

4.  To preview a record before opening it, move your mouse over a record and click the information icon \(![Information icon](../image/icon-information.png)\).

    ![Preview record](../image/preview-record-from-list-view.png)

    A side panel opens that shows the record.

5.  To move to a different page of records, click a page number or one of the arrows to move forward or backwards a page, or to the first or last page of records.

    ![List pagination](../image/list-pagination.png)

6.  To change the number of records displayed on a page, click the number beside rows per page and select a number from the menu.

    ![Rows per page](../image/list-rows-per-page.png)

7.  Click a record number to open it.

8.  To export the records in a list in one of the following formats: CSV, XLSX, JSON, or PDF, click the gear icon ![Gear icon](../image/gear-outline.png) and select **Export**.


## What to do next

Now that you know how to open a list and the records in it, find out how to [edit records in list view](work-with-lists.md#).

## Edit records in list view

Make updates to a record directly from a list, without leaving the list.

### Before you begin

Role required: agent\_workspace\_user

### About this task

You can revise one or more records while in list view. To learn more about a record before editing it, view and revise it in [record view](../concept/finding-answers.md).

### Procedure

1.  Revise a single record from a list.

    1.  Click the Open Preview icon ![Open preview icon](../image/circle-info-outline.png).

        The record opens.

        ![Edit record from list](../image/list-edit-record.png)

    2.  Revise the values in the fields and click **Update**.

2.  Revise multiple records at once.

    1.  In list view, click the boxes to the left of all the records you want to revise.

        ![Records to revise](../image/records-to-revise.png)

    2.  Click **Edit**.

        A preview pane opens and shows you the fields you can edit in the selected records.

        ![Edit multiple records at once](../image/list-edit-6-records.png)

    3.  Revise the values in the fields and click **Update**.


### What to do next

Now that you know how to edit a record in list view, find out how to [sort and filter the records displayed in a list](work-with-lists.md#).

## Sort records in lists

Sort the records displayed in list view to more easily find the records you want to work on.

### Before you begin

Role required: agent\_workspace\_user

### About this task

Filtered lists can contain thousands of records. Sorting them by field values can help you find the records you want to work on. You can sort the entire list based on any of the columns in the list.

### Procedure

1.  To change the field the records are sorted by, double click a column heading.

    An arrowhead icon \(![Ascending sort](../image/icon-arrowhead-up-full.png)\) appears to the right of the column heading you clicked and workspace sorts the list of records based on the values in that column. An arrowhead pointed down means the values are sorted from highest to lowest values.

    ![Sort column](../image/sort-column-arrowhead.png)

2.  To reverse the sorting order, click the arrowhead icon so the arrowhead reverses direction.


### What to do next

Instead of sorting records, you might want to [Filter records in lists](work-with-lists.md#) to reduce the number of records displayed in list view.

## Filter records in lists

Filter the records to reduce the number of records displayed in list view so you can find the records you want to work on.

### Before you begin

Role required: agent\_workspace\_user

### About this task

Filtering removes records from a list so you can view only those records you're interested in working on.

Workspace provides the following ways of filtering records displayed in a list:

-   Use the filter icon \(![Filter icon](../image/filter-outline.png)\).
-   Filter directly in the list using the column heading.
-   Filter directly in the list using the values in the columns.

### Procedure

1.  To filter out records using the filter icon \(![Filter icon](../image/filter-outline.png)\):

    1.  Click the filter icon \(![Filter icon](../image/filter-outline.png)\).

    2.  Click **Advanced View**.

    3.  Use the condition builder to specify the conditions one or more field values must meet for a record to appear in the list.

        For example, \[Active\]\[is\]\[true\], and \[Urgency\]\[is\]\[1- High\].

    4.  To add more conditions, click **New condition set** and supply a condition.

    5.  Select **Save Filter**, enter a filter name, and choose permissions to determine who can use the filter.

        Retrieve the filter by selecting **Use existing filter** and select the filter.

    6.  Click **Update**.

        The list filter icon ![List filter icon with badge](../image/ListFilterBadge.png) shows the number of conditions that apply to the current list.

2.  Filter records based on field values displayed.

    You can work directly with list columns to filter out records.

    1.  Click the **More UI Actions** icon ![More UI Actions icon](../image/ellipsis-v-fill.png) to the right of a column heading.

    2.  Click the downward pointing arrowhead icon \(![Down arrowhead](../image/icon-down-arrow-full.png)\) and select a filter condition, such as **is not**, **starts with**, or **contains**.

        ![Column filtering](../image/column-filtering-1.png)

    3.  Enter the field value to filter the list on the bottom line and click **Apply**.

        In the following example, the only records that appear have **Caller** values that start with **David**.

        ![Column filter](../image/column-filter.png)

        **Note:** Not all field types support column filtering. You can use the Advanced Filter panel and condition builder to create a filter for those field types.

    4.  If the values come from the sys\_choice table, the possible values \(choices\) appear with boxes beside them.

        ![Column filtering](../image/column-filtering-lists.jpg)

        If there are more than ten fields, workspace displays a **Filter**, as shown here, so you don't have to scroll to find a field value. If there are less than ten choices, there's no entry filter under **Filter**.

        You can click **All** to select all of the fields or **None** to uncheck all of the fields. **All** selects all of the field values that meet the filter conditions, not just those shown in the pop up. Likewise, **None** unchecks all of the fields that meet the filter conditions, not just those shown in the pop up. You can combine these functions. For example, you can filter on `Windows` and select **All**, and then filter on `2000` and select **None** and wind up with rows that contain Windows but not Windows 2000.

        You cannot configure the number of fields \(10\) that makes the **Filter** entry field appear.

    5.  To remove the filter and restore all of the records, click the **More UI Actions** icon \(![More UI Actions icon](../image/ellipsis-v-fill.png)\) and click **Clear**.

3.  Filter out records based on field values.

    This feature is similar to the one in the previous step but you can't enter a term to filter the records.

    1.  Click a field in the record.

    2.  Click the More UI Actions icon \(![More UI Actions icon](../image/ellipsis-v-fill.png)\).

        ![Show matching](../image/show-matching.png)

    3.  To remove all records that don't have the same field value, click **Show Matching**.

    4.  To remove all records in the list that have the same field value, click **Filter Out**.

        By default, a column sorts in an ascending order unless the column data type is a date. Dates sort in a descending order.


### What to do next

Instead of filtering records, you might like to [group records](work-with-lists.md#) in list view.

## Group records in lists

Group the records displayed in list view to more easily find the records you want to work on.

### Before you begin

Role required: agent\_workspace\_user

### About this task

You can group records that have the same values in a column so you can see similar records.

### Procedure

1.  Move the mouse over a column heading and click the More Options icon \(![More UI Actions icon](../image/ellipsis-v-fill.png)\).

2.  Click the first option, **Group by &lt;column-heading-name&gt;** where &lt;column-heading-name&gt; is the name of the column you're clicking in.

    ![Group records by field value](../image/group-records-by-field-value.png)

    The records are grouped based on the values in the selected column.

    ![Group list by column](../image/group-by-short-description.png)

    The display shows the number of records in each group.

3.  Open a group by clicking its arrowhead icon \(![Expand icon](../image/icon-arrowhead-right.png)\).

4.  To ungroup the records, mouse over the same column heading, click the More Options icon \(![More UI Actions icon](../image/ellipsis-v-fill.png)\) and click **Ungroup by &lt;column-heading-name&gt;**.


### What to do next

Instead of grouping records, you might like to [Filter records in lists](work-with-lists.md#).

