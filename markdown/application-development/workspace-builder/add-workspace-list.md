---
title: Create lists for a workspace in Workspace Builder
description: Create list categories in Workspace Builder to add pages that list table records. You can add filter conditions and change columns to create variations on the list.
locale: en-US
release: zurich
product: Workspace Builder
classification: workspace-builder
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Use, Workspace Builder, Builder library, Developing your application, Building applications]
---

# Create lists for a workspace in Workspace Builder

Create list categories in Workspace Builder to add pages that list table records. You can add filter conditions and change columns to create variations on the list.

## Before you begin

Role required:

-   admin or Guided Application Creator for ServiceNow Studio.
-   sn\_app\_eng\_studio.user or delegated\_developer for AES. For more information, see [Delegate developers using AES](../concept/aes-app-dev-workflow.md).

## About this task

**Note:**

-   You can launch and view workspaces in Workspace Builder as well. However, you can only edit workspaces created through ServiceNow Studio and App Engine Studio within those specific platforms only.

-   If you remove the list page/route, you must use UI Builder to edit the workspace, not Workspace Builder.

## Procedure

1.  Navigate to Workspace Builder.

    For details on how to open Workspace Builder in ServiceNow Studio or AES, see [Accessing Workspace Builder](../../workspace-builder/concept/accessing-workspace-builder-aes-crs.md).

2.  If they aren't already activated, activate lists to enable them for the workspace.

    You must be in the **Navigation configuration** tab. If you're already in the **Navigation configuration** tab, you can't select it.

    1.  In the navigation panel, select **List**.

    2.  In the list, select **Task** &gt; **Open**.

    3.  In the configuration panel, select the **Activate list** option.

    ![Workspace list view with lists activated](../image/wb-list-example-purple.png)

3.  Add a list category.

    1.  In the navigation panel, select **Add list category**.

        If the table associated with the workspace isn't a core table, you must add new list categories.

    2.  On the form, fill in the fields.

<table id="table_vkh_z4y_g5b"><thead><tr><th>

Field

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to identify the list category.

</td></tr><tr><td>

Description

</td><td>

Brief description of the contents of the list category to help developers understand the purpose.**Note:** Workspace users don't see the description.

</td></tr></tbody>
</table>    3.  Select **Add**.

4.  To rearrange the order in which list categories appear, drag them to a new position.

5.  Add a filtered list to a list category.

    For example, in the list category for the Task table, you could create separate filtered lists for Opened, Unassigned, and Closed tasks.

    1.  In the navigation panel, expand the list category you want to create a filtered list for.

    2.  Select **Add filtered list**.

    3.  On the form, fill in the fields.

        |Field|Definition|
        |-----|----------|
        |Name|Name to identify the filtered list.|
        |Table|Table that contains the subset of records that appear in the filtered list.You can select from two sections: Tables that are already available in your app, and all tables outside the app scope.|

    4.  Select **Add**.

    The preview canvas displays the contents of the filtered list.

6.  Refine how the filtered list displays its content by adding filter conditions to narrow what it displays.

    You can make additional configurations to the filtered list.

    1.  In the navigation panel, select the filtered list to edit.

    2.  In the configuration panel, specify the additional settings.

<table id="table_apx_ylq_35b"><thead><tr><th>

Field

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Activate list

</td><td>

Option to enable users to work with the filtered list.

</td></tr><tr><td>

Manage columns

</td><td>

Option to select and arrange the columns that appear. In the Manage columns dialog box, move columns from **Available columns** to **Selected columns**, drag to rearrange the columns, and select **Apply**.

You can select a field on a related table by dot-walking to it. For more information, see [Dot-walking to data in related tables](https://www.servicenow.com/docs/access?context=c_DotWalking&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).

</td></tr><tr><td>

Apply conditions

</td><td>

Option to add a filter condition to the list. In the dialog box that appears, you can do the following:-   To apply a predefined filter, select **Use existing filter** and search for the filter.
-   To view existing conditions, expand the **Filter overview** section.
-   To create a filter condition, use the condition builder. For more information on building conditions, see [Condition builder](https://www.servicenow.com/docs/access?context=c_ConditionBuilder&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).
-   To change the sort order of the filtered results, expand the **Sort by** section and make changes.
-   To save the filter condition that you created for reuse, select **Save filter**.
 When you're done creating the filter condition, select **Apply filter**.

 For more information on working with filters for lists, see [Filters](https://www.servicenow.com/docs/access?context=c_Filters&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).

</td></tr></tbody>
</table>    3.  Select **Apply filter**.

    4.  In the configuration panel, select **Save**.

7.  Complete any additional actions on the list.

<table id="choicetable_uch_4kg_cvb"><tbody><tr><td id="d246239e590">

**Edit a list category**

</td><td>

1.  In the navigation panel, select the list category.
2.  In the configuration panel, specify its **List category settings**.
3.  Select **Save**.


</td></tr><tr><td id="d246239e617">

**Change how the filtered list appears by selecting the list in the navigation panel**

</td><td>

1.  In the configuration panel, select **Manage columns**.
2.  In the form that appears, move columns from **Available columns** to **Selected columns**, drag to rearrange the columns, and select **OK**.
3.  Refresh the canvas preview by selecting the refresh icon \(![Refresh icon on preview canvas](../image/workspace-list-refresh-icon-purple.png)\) in the canvas header.


</td></tr><tr><td id="d246239e656">

**Delete a list category**

</td><td>

1.  In the navigation panel, select the list category.
2.  In the configuration panel, select **Delete list category**.
3.  In the confirmation dialog, select **Delete**.


</td></tr><tr><td id="d246239e683">

**Delete a filtered list**

</td><td>

1.  In the navigation panel, select the filtered list.
2.  In the configuration panel, select **Delete filtered list**.
3.  In the confirmation dialog, select **Delete**.


</td></tr></tbody>
</table>
