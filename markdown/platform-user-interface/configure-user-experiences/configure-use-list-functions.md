---
title: Configure and use list functions
description: All users can interact with lists for the tables their role permits them to access. Some list and column header menu options are controlled by permissions grated to the user role.You can quickly find information in a list by sorting the list. The method that the system uses to sort a list depends on the type of record in the sort column.You can enable or disable modern cell coloring for list field status indicators. This setting is available when you personalize a list. This setting is available in your system settings.You can customize the number of records, or rows, to display on each page of a list. The default is 20 rows per page.A view defines the elements that appear when a user opens a list.Remove the calculation of the total number of records in a list to speed up loading lists.Action check boxes enable you to perform actions on one or more items in a list.Some lists may be embedded in forms. Use list controls to work with records in an embedded list within a form.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-user-interface/configure-user-experiences/configure-use-list-functions.html
release: zurich
product: Configure User Experiences
classification: configure-user-experiences
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Lists in the classic environment, Working in the classic environment, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Configure and use list functions

All users can interact with lists for the tables their role permits them to access. Some list and column header menu options are controlled by permissions grated to the user role.

## Before you begin

Role required: admin

## About this task

The following procedures describe functions that users can configure or use with lists.

**Parent Topic:**[Lists in the classic environment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-user-interface/configure-user-experiences/c_UseLists.md)

## Sort a list

You can quickly find information in a list by sorting the list. The method that the system uses to sort a list depends on the type of record in the sort column.

### Before you begin

Role required: none

### About this task

Consider the example record: Label=**Requested Item**; Value=**sc\_req\_item**. Field types other than choice list types are sorted based on the label. The example record label, **Requested Item**, would be sorted with records whose labels start with "r."

A choice list field lets the user select from a pre-defined set of choices. Choice list fields are sorted by the underlying dictionary entry value of the field, not by the label. The example record value, **sc\_req\_item** would be sorted with records whose values start with "s."

Sorting by value can be useful. For example, choices for the **State** of tasks are ordered **New** &gt; **Work in Progress** &gt; **Closed**. Based on the label, the sort would be **Closed** &gt; **New** &gt; **Work in Progress**.

An arrow next to the column name indicates the current sort order. A downward pointing arrow indicates that the column is sorted in descending order. Only the primary sort order is indicated.

**Note:** The following sorting rules apply to lists:

-   In a translated instance, only translated\_text, translated\_field, and translated\_html type columns support sorting.
-   The column label should be created in English first then translated accordingly.
-   You cannot sort a list by an array-based field, such as a Glide list.

To sort a list, use one of the following methods:

### Procedure

-   Click a column name to sort the list in ascending order.

    Click again to sort in reverse order.

-   Right-click a column name and select **Sort \(a to z\)** or **Sort \(z to a\)** to sort in ascending or descending order, respectively.

-   Specify a sort order with a filter.

    Filters provide for sorting by more than one column \(for example, by Category and then Subcategory\).


**Related topics**  


[bundle-platadm.c_ChoiceLists]

[bundle-platadm.c_IntValsForDfltChoiceList]

## Configure field status indicators

You can enable or disable modern cell coloring for list field status indicators. This setting is available when you personalize a list. This setting is available in your system settings.

### Before you begin

Role required: none

### About this task

Field status indicators on lists are displayed with modern cell coloring, as a colored circle on the left side of the field. You can select the style of the field status indicator. You can revert to using a field background color by disabling modern cell coloring.

\[Omitted image "Modern\_cell\_coloring.png"\] Alt text: Modern cell coloring on

### Procedure

1.  The process depends on the version.

    1.  Click the personalize list icon \(\[Omitted image "IconPersonalizeList.png"\] Alt text: Personalize list icon\) in the list.

    2.  Select the **Modern cell coloring** check box to use the style field status indicator.

    3.  Click **OK**.

    For more information, see [Creating Personal Lists](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-user-interface/configure-user-experiences/c_PersonalLists.md).


## Customize the number of list rows per page

You can customize the number of records, or rows, to display on each page of a list. The default is 20 rows per page.

### Before you begin

Role required: none

### About this task

When you customize the number of rows, it applies to all lists that you can access.

### Procedure

1.  Open a list.

2.  Right-click the list title and select **Show** &gt; **&lt;Number&gt; rows per page**.

    The list refreshes to display the number of records selected, or, if there are fewer than the number of rows you are displaying, the total number of records. The page control is updated to show your selected number of records \(\[Omitted image "PageControl.png"\] Alt text: Page control\).


## Switch between list views

A view defines the elements that appear when a user opens a list.

### Before you begin

Role required: none

### About this task

You can switch between list views to which you have access.

### Procedure

1.  Open the list.

2.  Open the list title menu and select **View** &gt; **\(view name\)**.

    The page refreshes with in the selected view.


## Speed up loading large lists

Remove the calculation of the total number of records in a list to speed up loading lists.

### Before you begin

Role required: admin

### About this task

Calculating the total number of records to be included in a list filtered from extremely large tables can take a long time.

To improve performance, you can remove that calculation for all or specified views.

### Procedure

1.  On a list, click the menu icon \(\[Omitted image "MenuIconUI14.png"\] Alt text: Menu icon\) and navigate to **Configure** &gt; **List Control**.

2.  On the List Control page, select a check box:

    -   **Remove pagination count**—Removes pagination calculation from all views.
    -   **Remove pagination count for specified views**—Removes pagination calculation from specified views.
3.  If you selected **Remove pagination count for specified views**, click the lock icon \(\[Omitted image "icon-lock.png"\] Alt text: Lock icon\) and select the views that suppress displaying the number of pages in the list.

4.  Verify that the pagination is not calculated for your view by switching to that view.

    On a list, click the menu icon \(\[Omitted image "MenuIconUI14.png"\] Alt text: Menu icon\) and navigate to **View** &gt; **&lt;a view&gt;**.

    The pagination calculation should not appear and the fast forward icon \(\[Omitted image "icon-fast-forward.png"\] Alt text: Fast forward icon\) should be grayed out.


## Perform actions on selected items in a list

Action check boxes enable you to perform actions on one or more items in a list.

### Before you begin

Role required: admin

### About this task

\[Omitted image "ActionList.png"\] Alt text: Action check boxes and action choice list.

### Procedure

1.  Select the check boxes beside the records you want to affect.

    To select all records on the page, select the check box at the top of the list.

2.  Apply the desired action.

    -   In the column context menu, select **Update Selected** to update all the selected records.
    -   In the Action on selected rows menu, select an action such as **Delete** \(administrators only\), or **Add to Visual Task Board**. The available actions vary depending on the list and which plugins are activated.

## Embedded lists

Some lists may be embedded in forms. Use list controls to work with records in an embedded list within a form.

Use these controls to work with an embedded list. For more information, see [Edit a form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-user-interface/configure-user-experiences/t_EditingInForms.md).

|Task|Icon|Action|
|----|----|------|
|Expand an embedded list|\[Omitted image "UI11FormExpand.png"\] Alt text: Expand embedded list icon.|Click the expand icon in the list header.|
|Collapse an embedded list|\[Omitted image "UI11FormCollapse.png"\] Alt text: Collapse embedded list icon.|Click the collapse icon in the list header.|
|Insert a new row|\[Omitted image "InsertRow.png"\] Alt text: Insert a row.|Select **Add** and identify the record you want to add to the embedded list.|
|Edit a row| |Double-click in an empty area of that field. See [Use the list editor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-user-interface/configure-user-experiences/t_UseTheListEditor.md).|
|Delete a row|\[Omitted image "RowDeleteIcon.png"\] Alt text: Delete row icon.|Click the delete icon beside the row. New rows are removed immediately. Existing rows are designated for deletion when the record is saved. To clear this designation, click the delete icon again.|

\[Omitted image "FormEmbeddedList.png"\] Alt text: Embedded list

