---
title: Configure an action function
description: Action functions enable the user to change something in the database. For example, making an update or adding a comment to a record requires an action function.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Action functions, Mobile functions, Mobile app components, Building mobile apps, Mobile Platform]
---

# Configure an action function

Action functions enable the user to change something in the database. For example, making an update or adding a comment to a record requires an action function.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you are working in and then select the name of the application screen.

    The Mobile App Builder categories home screen displays.

3.  Select **Functions** in the menu, and then select **New**.

4.  On the form, fill in the fields.

<table id="table_lvf_xd1_n2b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

**Properties**

</td></tr><tr><td>

Name

</td><td>

The name of the function. Choose a name that is easy to identify.

</td></tr><tr><td>

Description

</td><td>

Additional information about the function.

</td></tr><tr><td>

Type

</td><td>

The type of function. Select **Action item**.

</td></tr><tr><td>

Context

</td><td>

The level to apply the action to. -   **Record**: Applies an action at the record level. For example, use this option to create a button that changes the state of a record. You can set the context to Record for actions on a particular field, a particular record, or swipe actions. If the action function includes a UI parameter with the **Input source** field set to **Auto fill**, you must specify the table in the **Table** field.
-   **Global**: Applies an action at the global, or list level. For example, use this option to add a button that creates a record. Do not use the Global setting for actions that are in the context of a record, or actions that include a UI parameter with the **Input source** field set to **Auto fill**.
 For more information on button locations, see [Associate a function with a location in the app](../reference/sg-studio-button-instances.md).

</td></tr><tr><td>

Available offline

</td><td>

Whether this function is available when the device is offline. **Note:** This option is only supported on the ServiceNow Mobile Agent app.

</td></tr><tr><td>

Action item

</td><td>

Action item to associate with the action. For more information, see [Configure an action item](sg-studio-create-action-item.md).

</td></tr><tr><td colspan="2">

**Settings**

</td></tr><tr><td>

Allow images upload

</td><td>

Allows images to be uploaded. Images are stored in the attachment \[sys\_attachment\] table.

</td></tr><tr><td>

Show signature field

</td><td>

Requires a user signature before submitting the action. Users can either sign with their fingers or type their names in the signature field. If **Allow images upload** is selected, an image of the signature is sent to the Signature Images \[signature\_image\] table when the action executes. If selected, the signature form displays on a separate page. To overlay the signature form, use the **Signature** option in the **Preconditions** field.

</td></tr><tr><td>

Use Overlay

</td><td>

Overlays a text input parameter on the current details screen. Exactly one text input parameter must be defined for the action. If this option is not defined, the input parameter displays on a separate screen.

</td></tr><tr><td>

Preconditions

</td><td>

Select an option to require user confirmation before submitting the action. -   **None**: Do not require user confirmation. This option is the default.
-   **HR Task Signature**: Require a user signature before submitting the action. Users can either sign with their fingers or type their names in the signature field. If **Allow images upload** is selected, an image of the signature is sent to the Signature Images \[signature\_image\] table when the action executes. When this option is selected, the signature form overlays the current screen.
-   **HR Task Credentials**: Require users to input their credentials before submitting the action. This option is supported only with local authentication.
-   **Re-authentication**: Requires users to re-authenticate their credentials before executing an action. For more information, see [Configure mobile re-authentication system properties](../concept/mobile-reautentication-concept.md).


</td></tr><tr><td colspan="2">

**Data**

</td></tr><tr><td>

Table

</td><td>

The table that the action applies to. Selecting a table is required if the **Context** is set to **Record**.

 If the **Context** is set to **Global**, selecting a table is optional.

</td></tr><tr><td class="sub-head" colspan="2">

**Conditions**

</td></tr><tr><td>

Condition

</td><td>

Conditions that must be met to use the action. For example, you could prevent users from resolving an incident that is in a state of closed, resolved, or canceled.

</td></tr><tr><td class="sub-head" colspan="2">

**Messages**

</td></tr><tr><td>

Show confirmation message

</td><td>

Displays a confirmation message to verify whether a user wants to continue with the action.

</td></tr><tr><td>

Confirmation message

</td><td>

The confirmation message to display.**Note:** Displays only if **Show confirmation message** is selected.

</td></tr><tr><td>

Confirm label

</td><td>

Label of the button to confirm the action.**Note:** Displays only if **Show confirmation message** is selected.

</td></tr><tr><td>

Cancel label

</td><td>

Label of the button to cancel the action.**Note:** Displays only if **Show confirmation message** is selected.

</td></tr><tr><td>

Success message

</td><td>

Text for a success confirmation message. Use curly braces to create a dynamic success message. For example, `{{number}} has successfully updated.`

</td></tr><tr><td>

Failure message

</td><td>

Text for a failure confirmation message. Use curly braces to create a dynamic failure message. For example, `{{number}} could not be updated.`

</td></tr><tr><td class="sub-head" colspan="2">

**Acknowledgment messages**

</td></tr><tr><td>

Show acknowledgment text

</td><td>

Require user acknowledgment before submitting the action. If this field is enabled, the **Context** field must be **Record**.

</td></tr><tr><td>

Acknowledgment field

</td><td>

Field that includes the acknowledgment text you want to display to the user. Select the table for the field in the **Data** area. Only String fields are supported. **Note:** Displays only if **Show acknowledgment text** is selected.

</td></tr><tr><td>

Confirm label

</td><td>

Label for the confirmation button that appears below the acknowledgment text. The default value is **I Agree**.**Note:** Displays only if **Show acknowledgment text** is selected.

</td></tr><tr><td class="sub-head" colspan="2">

**Action completion**

</td></tr><tr><td>

Refresh full screen after action

</td><td>

Option for the current screen to automatically refresh when an action completes.This option is available only when **Context** is set to **Global**.

 **Note:** The refresh option is supported for screens \(applets\) but not launcher screens.

</td></tr><tr><td>

Jump to previous screen

</td><td>

Redirects the user to the previous screen after completing an action.

</td></tr><tr><td>

Show refresh on previous screen

</td><td>

Shows a New Update message after the user completes the action and redirects back to previous screen.

</td></tr><tr><td>

Jump to screen after successful action completion

</td><td>

Displays additional screen navigation configuration options after the user completes an action. Use this field to determine whether user interaction is required before navigating to a specified screen.This option is available only when a table is selected in the **Condition** area of the form.

</td></tr><tr><td>

Jump to screen without user interaction

</td><td>

Sends the user to the destination screen.-   If selected, redirection to the destination screen occurs automatically without user interaction.
-   If not selected, redirection occurs only with user interaction on a success message. To define a success message, you must complete the mandatory fields in the **Messages** section of the form.
 **Note:** This option is available only when **Jump to screen after successful action completion** is selected.

</td></tr><tr><td>

Auto-populate screen parameters

</td><td>

Automatically populates parameters in the destination screen.**Note:** This option is available only when **Jump to screen after successful action completion** is selected.

</td></tr><tr><td>

Jump to destination screen

</td><td>

Specifies the screen that the user is redirected to after successful action completion. This screen displays newly created records, if available.**Note:** This option is available only when **Jump to screen after successful action completion** is selected.

</td></tr><tr><td>

UI parameters

</td><td>

Automatically populates parameters in the destination screen.**Note:** This option is available only when **Jumpt to screen after successful action completion** is selected.

</td></tr><tr><td>

Grouped inputs

</td><td>

This field is not used to configure an action function. Grouped input enables the users to scan several barcodes sequentially. You can configure grouped inputs with UI Parameters to accept multiple barcode scans. For information about grouped inputs, see [Configure a grouped input for multiple scans](sg-configure-multiscan.md)

</td></tr><tr><td>

Button attributes

</td><td>

Specifies an additional attribute for a button. Select **New** to configure this option. You can select from the following button attributes:-   **alerts\_require\_dismissal**: The button attribute when set to `true` enables the banner messages to persist until the user dismisses it. By default, banner messages are automatically dismissed.
-   **used\_for\_deeplink**: The button attribute when set to `true` determines that the button is used for deep linking. For more information, see [Deep linking for mobile](../concept/deep-link-mobile.md).
-   **trigger\_offline\_cache\_download**: The button attribute when set to `true` triggers offline cache generation. After the cache is successfully generated, a download of it is triggered.
-   **check\_acl\_on\_url\_parameter\_field**: When this button attribute is selected and set to `true`, any field in the URL string is checked against the ACL \(access control list\). For example, a string like \{\{meeting\_id\}\}. If a field does not pass this check, the field value is not included in the URL. By default, the URL parameter field is not checked against the ACL for backward compatibility.


</td></tr><tr><td>

Role access

</td><td>

Limit user access to an action by role.

</td></tr></tbody>
</table>    **Note:** While all the options in the **Action completion** area of the form can be set, their actions might overlap with each other. Make sure that you test the settings so the results produce the outcomes that you expect.

5.  Select **Save**.


## What to do next

After you create an action function, you must associate it with a specific location in the mobile app. You can add an action function to a top menu, a swipe action, or to a specific field. For more information on associating the action function to a location, see [Associate a function with a location in the app](../reference/sg-studio-button-instances.md).

