---
title: Create a navigation function
description: Create a navigation function that directs to a screen or launcher screen.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configure navigation to a launcher screen, Navigation functions, Mobile functions, Mobile app components, Building mobile apps, Mobile Platform]
---

# Create a navigation function

Create a navigation function that directs to a screen or launcher screen.

## Before you begin

Role required: admin

Navigation functions enable you to define simple ways for end users to navigate within the mobile platform. For example, navigating to a record from a field on another record. Before you create a navigation function, you should have a source and a destination for your navigation.

## About this task

In the following steps you create a navigation function to direct your users to an existing screen or launcher. You will need to have an existing screen or screen launcher to use as a destination for this function. For detail on creating screen launchers, see [Launcher screens](../concept/sg-mobile-applet-launcher.md).

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you are working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

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

Additional information about your navigation function.

</td></tr><tr><td>

Type

</td><td>

The type of the function. Since you are creating a navigation function, select **Navigation**.

</td></tr><tr><td>

Context

</td><td>

Whether the function uses the global or record context. For this example, select **Global**.

 Use record context navigation functions in situations where the navigation depends on information from a record. For example, you want to navigate from the **Assigned to** field in an incident record to the assignee's user record. Use global context navigation functions in situation where the navigation does not depend on information from a record.

</td></tr><tr><td>

Available offline

</td><td>

Option to determine whether the navigation function will be available in Offline mode.

</td></tr><tr><td>

Destination type

</td><td>

The type of record your navigation function will bring users to. Select **Screen** for navigation to a screen, or select **Launcher** for navigation to a screen launcher.

</td></tr><tr><td>

Auto-populate screen parameters

</td><td>

Automatically populates parameters in the destination screen when the toggle is enabled.

</td></tr><tr><td>

Destination screen or Destination launcher

</td><td>

The screen or screen launcher to use for your navigation function’s destination. Either select an existing screen or select **New** to create a new screen.

</td></tr><tr><td>

Condition type

</td><td>

Type of condition to use.

-   **Declarative:** Adds a conditional builder to the form. For more information, see [Condition builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/c_ConditionBuilder.md).
-   **Script:** Adds a script condition field to the form.
**Note:** Displays only if **Context** is set to **Record**.

</td></tr><tr><td>

Condition

</td><td>

Conditions that must be met to use the action. For example, you could prevent users from resolving an incident that is in a state of closed, resolved, or canceled.

 You can choose to use your own Declarative condition picker or write your own conditions using script.

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
</table>5.  If you added a destination screen that has a parameterized data item, in the **Redirection destination fields** section, select the field **Name** to update the redirection parameter fields.

    1.  Complete the following fields as needed.

<table id="table_ytd_zkv_qwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Destination UI parameter

</td><td>

The name of the parameter you created for the data item.

</td></tr><tr><td>

Type

</td><td>

Source of information for the parameter. The available options are: -   **Field:** The parameter gets the information from a field on a table.
-   **Constant:** The parameter uses a constant value.
-   **Source UI parameter**


</td></tr><tr><td>

Function table

</td><td>

This field is automatically populated.

</td></tr><tr><td>

Function

</td><td>

This field is automatically populated.

</td></tr><tr><td>

Source field

</td><td>

UI parameters for the source screen.**Note:** Displays only if the redirection parameter **Type** value is set to **Source UI parameter**.

</td></tr></tbody>
</table>6.  Select **Save**.


**Parent Topic:**[Configure navigation to a launcher screen](../concept/sg-launcher-nav-example.md)

