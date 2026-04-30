---
title: Map Microsoft Azure email to ServiceNow instance
description: Create a custom email field to use Microsoft Teams app to initiate call for the agents to resolve the tickets raised by users.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure Notify connector, Microsoft Teams integration for Agent Experience, Configure, ServiceNow for Microsoft Teams and Microsoft 365, Employee Service Management]
---

# Map Microsoft Azure email to ServiceNow instance

Create a custom email field to use Microsoft Teams app to initiate call for the agents to resolve the tickets raised by users.

## Before you begin

Role required: admin

## About this task

If your email field on the sys\_user table in your ServiceNow® instance does not match email on the Microsoft Azure tenant for the user, then mapping is required. The default mapping is to the email field and stored in the system property field sn\_now\_azure.user\_email\_field. Use this procedure to change the email field value as needed.

## Procedure

1.  Copy the user\_email\_field value.

    1.  Open your ServiceNow instance.

    2.  Navigate to **All** &gt; **System Security** &gt; **Users and Groups** &gt; **Users**.

    3.  Select a user.

    4.  Right-click on the form header and select **Configure** &gt; **Form Layout**.

    5.  In the Create new field section, fill in the fields.

<table id="table_cx1_dmv_gsb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter the name of the field as you want it to appear on forms and lists.

 Example: User Principal Name.

</td></tr><tr><td>

Type

</td><td>

Select a field type as **String**.

</td></tr><tr><td>

Field length

</td><td>

Select a field length. This field is visible only for certain field types.

</td></tr></tbody>
</table>    6.  Select **Add**.

        ![Create new field](../../sn-teams/images/create-new-field.png)

    7.  In the Selected slush bucket column, move the field in the desired location on the form.

    8.  Select **Save**.

        The field now appears on the form in the designated location.

        ![New field added to form](../../sn-teams/images/upn-field.png)

        The admin must enter the email used for Microsoft Teams in this field.

        You need to configure the newly created field value as the default field for initiating chats with the employee in Microsoft Teams.

    9.  Right-click on the field and select **Show &lt;value of the field name&gt;**.

        ![Show field name](../../sn-teams/images/show-field-name.png)

        The dictionary info of the field name can be viewed.

        ![Field name](../../sn-teams/images/field-name2.png)

    10. Right-click on the **Field** and copy the value.

2.  Change the email field value.

    1.  Navigate to **Notify** &gt; **Microsoft Teams** &gt; **Properties**.

    2.  Paste the copied email field value in the field **Specify a valid teams email field value. This field value will be used when a new Microsoft Teams Conference Call is initiated** of the Microsoft Teams Properties form.

        The default value is `email`.

    3.  Select **Save**.

        **Note:** Ensure that the email address for all the users for the newly created field is updated with the email associated with Microsoft Teams app.


**Parent Topic:**[Configure Notify connector for Microsoft Teams](../concept/config-notify-ms-teams.md)

