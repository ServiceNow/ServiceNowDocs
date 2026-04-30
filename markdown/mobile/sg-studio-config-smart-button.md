---
title: Configure a smart button
description: Smart buttons are actions that allow you to perform another action, such as sending an email, making a phone call, pulling up a location, or navigating directly to a URL.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Smart button functions, Mobile functions, Mobile app components, Building mobile apps, Mobile Platform]
---

# Configure a smart button

Smart buttons are actions that allow you to perform another action, such as sending an email, making a phone call, pulling up a location, or navigating directly to a URL.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you are working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Select **Functions** from the menu and then select **New**.

4.  Complete the following fields as needed.

<table id="table_yrx_2qc_clb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Properties

</td></tr><tr><td>

Name

</td><td>

Name for your smart button

</td></tr><tr><td>

Description

</td><td>

Unique description for your smart button to make it easy to identify.

</td></tr><tr><td>

Type

</td><td>

Type of smart button. Select from:-   **URL**
-   **Phone**
-   **Address**
-   **Email**
-   **Upload attachment**
-   **Chat launcher**
**Note:** Choose a field appropriate to the type of smart button you are creating. For example, if you are creating a smart button with the type **Phone**, select a field that includes a phone number.

</td></tr><tr><td>

Context

</td><td>

Context for your smart button. Select from:-   **Record**
-   **Global**
Use **Record** context navigation functions in situations where the navigation depends on information from a record. For example, you want to navigate from the **Assigned to** field in an incident record to the assignee's user record.

Use **Global** context navigation functions in situations where the navigation does not depend on information from a record.

 **Note:** Smart buttons using the **Address** type must use the **Record** context. The **Context** field returns an error if you select **Global** context for an **Address** type smart button

</td></tr><tr><td class="sub-head" colspan="2">

Data

</td></tr><tr><td>

Table

</td><td>

Select the table where you want to use your smart button.**Note:** This option is only shown when the **Context** is set to **Record**.

</td></tr><tr><td class="sub-head" colspan="2">

Settings

</td></tr><tr><td>

Take source value from field

</td><td>

Use a specific field from a table as the source of the smart button type.

</td></tr><tr><td colspan="2">

Depending on what smart button type you select, you can specify the following settings.

</td></tr><tr><td>

URL smart button

</td><td>

-   **Link URL**: The URL to which your smart button will navigate.
-   **Link label**: The visible label of your URL link.


</td></tr><tr><td>

Phone smart button

</td><td>

-   **Phone type**: Type of phone the smart button communicates with. Select from:
    -   **Cellular**
    -   **Landline**
-   **Phone number**
-   **SMS**: The SMS message sent by the smart button. This field is only visible when you select **Cellular** in the **Phone type** field.


</td></tr><tr><td>

Email smart button

</td><td>

-   **Mail subject**: Subject for the email message.
-   **Mail content**: Content of the email message.
-   **Mail address**: Email address to which the email is sent.


</td></tr><tr><td class="sub-head" colspan="2">

Conditions \(optional\)

</td></tr><tr><td>

Condition Type

</td><td>

Type of condition to use. Create conditions to limit when the smart button appears. For example, if you are creating a Phone type of smart button, you could create a condition to require a value in the phone number field.

 The following condition types appear if **Context** is set to **Record** and a **Table** is selected:

 -   **Declarative**: Adds a condition builder to the form. For more information, see [Condition builder](https://www.servicenow.com/docs/access?context=c_ConditionBuilder&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).
-   **Script**: Adds a script condition field to the form.


</td></tr><tr><td>

Conditions

</td><td>

This option appears if **Context** is set to **Global**. This is a condition that must be met for the function to be visible in the app for the user to click on.

</td></tr><tr><td>

Button attributes

</td><td>

\(Optional\) Specifies an additional attribute for your smart button. Select **New** to create one of the following button attributes:

 -   **alerts\_require\_dismissal**: When set to `true`, this button attribute enables the banner messages to persist until the user dismisses it. By default, banner messages are automatically dismissed.
-   **used\_for\_deeplink**: When set to `true`, this button attribute specifies that the button is used for deep linking. For more information, see [Deep linking for mobile](../concept/deep-link-mobile.md).
-   **trigger\_offline\_cache\_download**: When set to `true`, this button attribute triggers offline cache generation. After the cache is successfully generated, a download of it is triggered.
-   **check\_acl\_on\_url\_parameter\_field**: When set to `true`, any field in the URL string, is checked against the ACL \(access control list\). For example, a string like `{{meeting_id}}`. If a field does not pass this check, the field value is not included in the URL. By default, the URL parameter field is not checked against the ACL for backward compatibility.
-   **hidden\_attachment\_sources**: Enter values in the **Value** field from where you don’t want images sourced from. Values can be `camera`, `files` or `gallery`, or any combination separated by commas. If this field is left blank, then images and files can be sourced from all locations. For more information, see [Define attachment sources available to users](attachment-source-define.md).


</td></tr><tr><td>

Role access

</td><td>

Limit user access to an action by role.

</td></tr></tbody>
</table>5.  Select **Save**.


## Result

## What to do next

After you create a smart button function, you must associate it with a specific location in the mobile app. You can add a smart button function to a top menu, a swipe action, or to a specific field. For more information on associating the smart button function to a location, see [Associate a function with a location in the app](../reference/sg-studio-button-instances.md).

