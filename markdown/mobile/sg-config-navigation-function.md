---
title: Configure a navigation to a screen
description: Navigation functions enable you to define simple ways for end users to navigate within the mobile platform, for example, navigating to a record from a field on another record.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Navigation functions, Mobile functions, Mobile app components, Building mobile apps, Mobile Platform]
---

# Configure a navigation to a screen

Navigation functions enable you to define simple ways for end users to navigate within the mobile platform, for example, navigating to a record from a field on another record.

## Before you begin

Before you create a navigation function, you should have a source screen and a destination screen for your navigation.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you are working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Select **Functions** from the menu and then select **New**.

4.  In the Function form, complete the following fields.

<table id="table_aw2_rvd_pwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Properties

</td></tr><tr><td>

Name

</td><td>

The name of your navigation function.

</td></tr><tr><td>

Description

</td><td>

Unique description for your navigation function to make it easy to identify.

</td></tr><tr><td>

Type

</td><td>

Type of function. Select **Navigation**.

</td></tr><tr><td>

Context

</td><td>

Whether the function uses the **Global** or the **Record** context.

 Use **Record** context navigation functions in situations where the navigation depends on information form a record. For example, if you want to navigate from the **Assigned to** field in an incident record to the assignee's user record.

 Use **Global** context navigation functions in situations where the navigation does not depend on information from a record. For example, select **Global** for navigating to a screen.

</td></tr><tr><td>

Available offline

</td><td>

Whether the navigation function is available offline.**Note:**

-   The screen and the application that contains the navigation function must be marked as available offline for the navigation function to work when the device is offline.
-   Offline is only supported for the Mobile Agent.
For more information about offline mode, see [Offline mode](../concept/mobile-offline-mode.md).

</td></tr><tr><td class="sub-head" colspan="2">

Settings

</td></tr><tr><td>

Destination type

</td><td>

The type of destination to which you want to navigate. Select either **Screen** or **Launcher**.

</td></tr><tr><td>

Auto-populate screen parameters

</td><td>

Automatically populates parameters in the destination screen.

</td></tr><tr><td>

Destination screen/launcher

</td><td>

The destination screen or launcher to which you want to navigate. Select **Choose**, select the screen or launcher, and then select **Apply** to add it to your navigation function.

</td></tr><tr><td class="sub-head" colspan="2">

Data

</td></tr><tr><td>

Table

</td><td>

Select the table that contains the field you want to use for the function. This option only appears if you select **Record** for the **Context**.

</td></tr><tr><td>

Conditions

</td><td>

The condition that must be met for the function to be visible in the app to end users. For example, if you don't want an end user to navigate to a screen of tasks until after they have clocked in for the day.

</td></tr></tbody>
</table>5.  If you added a destination screen that has a parametrized data item, in the **Redirection destination fields** section, select the **Name** field to update the redirection parameter fields for the destination screen.

    If you need to add a destination screen, select **New** to add one. Complete the following fields as needed.

<table id="table_l4k_yyd_pwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Destination UI parameter

</td><td>

The name of the parameter you created for the data item. Select **Choose** to search for the parameter and then select **Apply**.

</td></tr><tr><td class="sub-head" colspan="2">

Settings

</td></tr><tr><td>

Type

</td><td>

Source of information for the parameter. The available options are:-   **Field**: The parameter gets the information from a field on a table.
-   **Constant**: The parameter uses a constant value.
-   **Source UI parameter**: The parameter gets the information from a source field.


</td></tr><tr><td>

Function table

</td><td>

The table that you select in Step 4 if the function uses a **Record** context. This table is automatically populated in the form.

</td></tr><tr><td>

Function

</td><td>

This is the function you created in Step 4. The function name is automatically populated in the form.

</td></tr><tr><td>

Source field

</td><td>

UI parameter for the source screen. This field appears only if **Source UI Parameter** is the redirection parameter **Type** value.

</td></tr></tbody>
</table>6.  Select **Save** in the **Redirection destination fields form**, and then select the function in the navigation menu to navigate back to the function you created in Step 4.

7.  In the **Button attributes** section, select an existing button attribute record or select **New** to add one.

    If you need to add a new button attribute record, in the Button Attribute form, complete the following fields as needed.

<table id="table_l2d_d12_pwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Button

</td><td>

Name of the button record. This information is automatically populated from the function record.

</td></tr><tr><td>

Name

</td><td>

The button attribute. Select from:-   used\_for\_deeplink
-   alerts\_require\_dismissal
-   trigger\_offline\_cache\_download
-   check\_acl\_on\_url\_parameter\_field
**Note:** The **trigger\_offline\_cache\_download** button attribute is only available when the **Available offline** option has been turned on in Step 4.

</td></tr><tr><td>

Value

</td><td>

Whether the attribute is turned on. Enter `true` to turn on the attribute. By default, the Value is set to `true`.

</td></tr></tbody>
</table>8.  In the **Role access** section, select **Choose** to add the roles that can use the navigation function.

9.  In the Function form, select **Save**.


## What to do next

After you create a navigation function, you must associate it with a specific location in the mobile app. For more information, see [Associate a function with a location in the app](../reference/sg-studio-button-instances.md).

