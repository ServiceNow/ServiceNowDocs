---
title: Create a navigation function to a chart screen
description: Configure a navigation function to direct your users to your chart screen.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Chart screen, Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Create a navigation function to a chart screen

Configure a navigation function to direct your users to your chart screen.

## Before you begin

Role required: admin or delegated developer

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you're working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Select the **Functions** category, and then select **New**.

4.  Complete the following fields as needed.

<table id="table_wch_2jy_slb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

**Properties**

</td></tr><tr><td>

Name

</td><td>

Name of your navigation function.

</td></tr><tr><td>

Description

</td><td>

Additional information about the navigation function.

</td></tr><tr><td>

Type

</td><td>

The type of the function. Since you're creating a navigation to a chart screen, select **Navigation**.

</td></tr><tr><td>

Context

</td><td>

Whether the function uses the global or record context. For this example, select **Global**.

 Use record context navigation functions in situations where the navigation depends on information from a record. For example, you want to navigate from the **Assigned to** field in an incident record to the assignee's user record. Use global context navigation functions in a situation where the navigation doesn’t depend on information from a record.

</td></tr><tr><td>

Available offline

</td><td>

This option isn't available for data visualizations.

</td></tr><tr><td>

Destination type

</td><td>

The type of record your navigation function brings users to. Since you're creating a navigation to a chart screen, select **Screen**.

</td></tr><tr><td>

Auto-populate screen parameters

</td><td>

Automatically populates parameters in the destination screen.

</td></tr><tr><td>

Destination screen

</td><td>

The screen or screen launcher to use for your navigation function’s destination. Either select an existing chart screen or select **New** to create a new chart screen.

</td></tr><tr><td>

Table

</td><td>

Table that the function uses.

 This field is only visible when the **Context** field is set to **Record**.

</td></tr><tr><td colspan="2">

**Conditions**

</td></tr><tr><td>

Condition Type

</td><td>

The conditions applied to the chart screen.

 -   **Declarative**: Adds a condition builder to the form. For more information, see [Condition builder](https://www.servicenow.com/docs/access?context=c_ConditionBuilder&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).
-   **Script**: Adds a script condition field to the form.
 This field is only visible when the **Context** field is set to **Record**.

</td></tr><tr><td>

Condition Definition

</td><td>

This is a condition that must be met for the function to be visible in the app for the user to select. For example, if you don’t want to let someone navigate to a screen of tasks until after they've clocked in for the day.This field is only visible when the **Context** field is set to **Record**.

</td></tr><tr><td>

Condition

</td><td>

This is a condition that must be met for the function to be visible in the app for the user to select. For example, if you don’t want to let someone navigate to a screen of tasks until after they've clocked in for the day.

</td></tr><tr><td>

Redirection destination fields

</td><td>

Allows you to connect the function to a screen that uses a parameterized data item.

</td></tr><tr><td>

Button attributes

</td><td>

Specifies an additional attribute for a button. Select **New** to configure this option. You can select from the following button attributes:

 -   **alerts\_require\_dismissal:** The button attribute when set to true enables the banner messages to persist until the user dismisses it. By default, banner messages are automatically dismissed.
-   **used\_for\_deeplink:** The button attribute when set to true determines that the button is used for deep linking. For more information, see [Deep linking for mobile](../concept/deep-link-mobile.md).
-   **trigger\_offline\_cache\_download:** The button attribute when set to `true` triggers offline cache generation. After the cache is successfully generated, a download of it is triggered.
-   **check\_acl\_on\_url\_parameter\_field:** When this button attribute is selected and set to `true`, any field in the URL string is checked against the ACL \(access control list\). For example, a string like `{{meeting_id}}`. If a field doesn't pass this check, the field value isn't included in the URL. By default, the URL parameter field isn't checked against the ACL for backward compatibility.


</td></tr><tr><td>

Role access

</td><td>

Determine which user roles can access this screen. If you have selected no roles, users with any role will have access to the screen.

</td></tr></tbody>
</table>5.  Select Navigation from the **Type** field.

6.  Select Global from the **Context** field.

7.  Select Screen from the **Destination type** field.

8.  From the Destination screen field, select the chart screen you created in the topic [Create a chart screen for a data visualization](config-single-score-applet.md).

9.  Select **Save**.


## What to do next

After you create a navigation link to the chart screen, you must associate this navigation function to the analytics preview. For details on this process, see [Add a navigation function to an analytics preview](config-chart-nav-2.md).

-   **[Add a navigation function to an analytics preview](config-chart-nav-2.md)**  
Configure your analytics preview to use a navigation function. This function directs your users to your chart screen from the analytics preview on your screen launcher.

