---
title: Change the navigation and menu settings in your UI Builder workspace experience
description: Select pages for side navigation in your UI Builder workspace experience. From any page in the workspace experience, users can navigate to the pages you selected.
locale: en-US
release: xanadu
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configure UI Builder workspace experiences, Configure how users interact with your applications in UI Builder, Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Change the navigation and menu settings in your UI Builder workspace experience

Select pages for side navigation in your UI Builder workspace experience. From any page in the workspace experience, users can navigate to the pages you selected.

## Before you begin

This task has the following prerequisites:

-   You have an existing workspace experience on UI Builder. For more information, see [Configure how users interact with your applications in UI Builder](../concept/work-experiences.md).
-   This workspace experience was created with the Workspace App Shell.
-   This workspace experience includes at least two pages.
-   You want users to be able to navigate from a page to other pages that you specify.

Role required: ui\_builder\_admin

## About this task

You can add up to seven pages to your side navigation.

You must be in the correct application scope to edit the experience settings. If you are in a different scope, the experience settings are read-only. To change your application scope, go to the main header, select the application picker \(![Application picker.](../image/application-picker.png)\), and then select the application scope that you want. For more information about the application scope, see [Learn about security and roles](security-roles.md).

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Open your workspace experience in the UI Builder.

3.  Select **View experience settings** in the upper-right.

    ![Arrow pointing to the View experience settings link on the experience view page.](../image/experience-settings-navigation.png)

4.  Scroll down to **Side navigation**.

5.  Select **+ Add**.

    ![Arrow pointing at the +Add button for adding pages to a side navigation.](../image/settings-side-nav.png)

6.  Fill in the following fields:

<table id="table_skg_kfv_dsb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

URL path \(required\)

</td><td>

Select the page that you want to navigate to.**Tip:** The landing page is usually the first page that you want a link to.

</td></tr><tr><td>

Icon

</td><td>

Select an icon for the link.Default: No icon

</td></tr><tr><td>

Label \(required\)

</td><td>

Enter a name for the page, which appears in a tooltip for the link.

</td></tr><tr><td>

Group

</td><td>

Place the link in the top or the bottom group of the side navigation panel.Default: Top

</td></tr></tbody>
</table>7.  Add more pages as needed.

8.  Select **Save**.

9.  Select the experience name \(for example, Demo Experience\) in the UI Builder header.

10. Select the **URL path** link to open the experience in a new tab and check that the side navigation is displayed on the left side.

    **Tip:** If the side navigation doesn’t work as expected, consider reviewing the UX Page Property \[sys\_ux\_page\_property\] record underlying the side navigation. Reopen the Side Navigation experience settings, as described in Steps [3](workspace-side-navigation-settings.md#step_edit-exp-settings)-[4](workspace-side-navigation-settings.md#step_side-nav). Select **Advanced side navigation settings** to open the record. Verify that the fields have the correct values, such as Type=`json`.


**Parent Topic:**[Configure UI Builder workspace experiences](../concept/ui-builder-workspace-settings.md)

