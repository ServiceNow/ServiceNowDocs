---
title: Add a field function to screen
description: Add field functions to the details screen in your record screens using Mobile App Builder.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Add functions to your details screens, Configure a details screen for a record screen, Record screen, Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Add a field function to screen

Add field functions to the details screen in your record screens using Mobile App Builder.

## Before you begin

Role required: admin

Field functions are functions that users can access by tapping or swiping on a specific field on your form. Use this option for functions relating to data in a specific field. You can add functions to fields by creating a function instance in any details screen that is embedded within your record screen.

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder appears in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you're working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Select the **Screens** category and then select the record screen.

4.  Use the configuration tree on the left to find and select the details screen where you want to add a field function.![Details screen within the Mobile App Builder configuration tree](../image/add-func-to-details-1.png)

5.  In the configuration panel, find the **Field function instances** section and click the **New** button.![Field function instances section of the details screen panel](../image/add-func-to-details-2.png)

6.  In the **New function instance** control panel, fill in the fields as needed.

<table id="table_ypn_qv3_twb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the function instance. This name is for administration not visible to app users.

</td></tr><tr><td>

Description

</td><td>

Description of the function instance. This description is for administration and not visible to app users.

</td></tr><tr><td>

Display label

</td><td>

Label displayed in the app for the function.

</td></tr><tr><td>

Order

</td><td>

Order in which the function is displayed in the app.

</td></tr><tr><td>

Active

</td><td>

Whether the field function instance is active. Inactive function instances don't appear in the app.

</td></tr><tr><td>

Disable offline

</td><td>

Whether the function instance is available

</td></tr><tr><td>

Icon

</td><td>

Option icon used for your field function.To use an existing icon, click the **Choose** button, select an icon, and click **Apply**.

To create an icon, click the **New** button. You’re redirected to the **New icon** panel. For details on creating icons see [Mobile icons](../reference/sg-mobile-icon.md).

</td></tr><tr><td>

Field Name

</td><td>

Field that will use this field function.

</td></tr><tr><td>

Function

</td><td>

Function to use on the field selected in the **Field Name** field.To use an existing function, click the **Choose** button, select a function, and click **Apply**.

To create function, click the **New** button. You’re redirected to the **New function** panel. For details on creating functions see [Mobile functions](../concept/sg-studio-mobile-button-types.md).

</td></tr></tbody>
</table>7.  Click **Save** in the upper right corner to save your function instance.


