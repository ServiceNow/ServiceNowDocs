---
title: Create a navigation function for your chart screen
description: Create a navigation function to direct your users from the chart screen to a parametrized list.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure a navigation from a chart to a list screen, Chart screen, Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Create a navigation function for your chart screen

Create a navigation function to direct your users from the chart screen to a parametrized list.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder

2.  Search for the application scope you are working in and then select the name of the application scope.

    The Mobile App Builder

3.  Select the **Functions** category, and then select **New**.

4.  Complete the following fields as needed.

<table id="table_ylz_xms_xlb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of your navigation function

</td></tr><tr><td>

Description

</td><td>

A unique description for your navigation function.

</td></tr><tr><td>

Type

</td><td>

The type of the function. Since you are creating a navigation to a chart screen, select **Navigation**.

</td></tr><tr><td>

Context

</td><td>

Whether the function uses the global or record context. For this example, select **Global**.

 Use record context navigation functions in situations where the navigation depends on information from a record. For example, you want to navigate from the **Assigned to** field in an incident record to the assignee's user record. Use global context navigation functions in situation where the navigation does not depend on information from a record.

</td></tr><tr><td>

Available offline

</td><td>

Option to determine whether the navigation function will be active on Offline mode or not.

</td></tr><tr><td>

Destination type

</td><td>

The type of record your navigation function will bring users to. Since you are creating a navigation to a chart screen, select **Screen**

</td></tr><tr><td>

Destination screen

</td><td>

The screen or screen launcher to use for your navigation function’s destination. Either select an existing chart screen or select **New** to create a new chart screen.

</td></tr><tr><td>

Condition type

</td><td>

The conditions applied to the chart screen.

-   **Declarative:** Adds a conditional builder to the form. For more information, see Condition builder.
-   **Script:** Adds a script condition field to the form.
**Note:** Displays only if **Context** is set to **Record**.

</td></tr><tr><td>

Condition

</td><td>

This is a condition that must be met for the function to be visible in the app for the user to click on. For example, if you don’t want to let someone navigate to a screen of tasks until after they have clocked in for the day.

</td></tr><tr><td>

Redirection destination fields

</td><td>

Option to connect a function to a screen that uses a parameterized data item.

</td></tr><tr><td>

Button attributes

</td><td>

Specifies an additional attribute for a button. Select **New** to configure this option. You can select from the following button attributes:

 -   **alerts\_require\_dismissal**: The button attribute when set to true enables the banner messages to persist until the user dismisses it. By default, banner messages are automatically dismissed.
-   **used\_for\_deeplink**: The button attribute when set to true determines that the button is used for deep linking. For more information, see [Deep linking for mobile](../concept/deep-link-mobile.md).
-   **trigger\_offline\_cache\_download**: The button attribute when set to true triggers offline cache generation. After the cache is successfully generated, a download of it is triggered.
-   **check\_acl\_on\_url\_parameter\_field**: When this button attribute is selected and set to true, any field in the URL string, is checked against the ACL \(access control list\). For example, a string like `{{meeting_id}}`. If a field does not pass this check, the field value is not included in the URL. By default, the URL parameter field is not checked against the ACL for backward compatibility.


</td></tr><tr><td>

Role access

</td><td>

Determine which user roles can access this function. If you have selected no roles, users with any role will have access to the screen.

</td></tr></tbody>
</table>5.  In the **Destination screen** section, either select an existing record or create a new one.

6.  Select **Save**.


## What to do next

Assign your navigation function to your chart screen. For more information, see [Assign the navigation function to the chart screen](nav-chart-to-list-3.md).

**Parent Topic:**[Configure a navigation from a chart to a list screen](../concept/nav-chart-to-list.md)

