---
title: Create and delete views
description: Administrators can create views and delete any views they have created. You can create or delete views from either the list view or the form view.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [View management, User interface configuration, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Create and delete views

Administrators can create views and delete any views they have created. You can create or delete views from either the list view or the form view.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to the application or module you want to create or delete the view for.

2.  If you are creating a view for a list, perform the appropriate action for your list version.

    |Version|Action|
    |-------|------|
    |**List v2**|Right-click the header and select **Configure** &gt; **List Layout**.|
    |**List v3**|Open the context menu and select **List Layout**.|

3.  If you are creating a view for a form, open a record, then right-click the header and select **Configure** &gt; **Form Layout**.

4.  Under the List View section, select the view on which you want to base your new view.

    The fields visible for that view appear in the **Selected** list.

5.  From the choice list, select **New**.

    The Create New View form appears.

6.  Enter the descriptive name of the view.

    View names should be unique and cannot use special characters or spaces, only the characters **A-Z**, **a-z**, **0-9** and **\_**.

7.  Select **OK**.

    The fields in the **Available** column are the same as the first view you based the new view on.

8.  Select the fields to appear in this view by adding or removing the fields from the **Selected** column, or you can adjust the order they appear on the form by moving the fields up or down.

    If you are creating a view for a form, you can select a form section and configure the fields for that section. You can also create views in the same manner when you configure a related list.

9.  To delete a view, navigate to **System UI** &gt; **Views**.

10. Select the view to delete.

11. Select **Delete** on the form header.

    **Warning:** In the views list, you may see multiple entries formatted as `rpt-temp<sys_id><user>`. The instance creates these views to store the current state of reports. Avoid deleting these records, as it may impact the state of active reports.

    Do not delete the base system views.


**Parent Topic:**[View management](../concept/view-management-overview.md)

