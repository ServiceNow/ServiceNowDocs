---
title: Create custom email field to initiate Microsoft Teams chat
description: Create a custom email field to use Microsoft Teams app to initiate chat conversation for the agents to resolve the IT and HR related issues of the users.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [IT Service Management integration, Microsoft Teams Integration for Employee Experience, Configure, ServiceNow for Microsoft Teams and Microsoft 365, Employee Service Management]
---

# Create custom email field to initiate Microsoft Teams chat

Create a custom email field to use Microsoft Teams app to initiate chat conversation for the agents to resolve the IT and HR related issues of the users.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Security** &gt; **Users and Groups** &gt; **Users**.

2.  Click a user.

3.  Right-click on the form header and select **Configure** &gt; **Form Layout**.

4.  In the Create new field section, fill in the fields.

    |Field|Description|
    |:----|:----------|
    |Name|Enter the name of the field as you want it to appear on forms and lists. Example: User Principal Name.|
    |Type|Select a field type as **String**.|
    |Field length|Select a field length. This field is visible only for certain field types.|

5.  Click **Add**.

    ![Create new field](../images/create-new-field.png)

6.  In the Selected slush bucket column, move the field in the desired location on the form.

7.  Click **Save**.

    The field now appears on the form in the designated location.

    ![New field added to form](../images/upn-field.png)

    The admin must enter the email used for Microsoft Teams in this field.

    You need to configure the newly created field value as the default field for initiating chats with the employee in Microsoft Teams.

8.  Right-click on the field and click **Show &lt;value of the field name&gt;**.

    ![Show field name](../images/show-field-name.png)

    The dictionary info of the field name can be viewed.

    ![Field name](../images/field-name2.png)

9.  Right click the **Field** and copy the value.

10. In the search field, enter `sys_properties.LIST` to view the system properties.

    ![System properties](../images/sys-properties2.png)

11. In the Name column, search for `*user_email` property.

12. Click the entry.

    ![Email field properties](../images/email-field2.png)

    If the record is not editable, click **Edit** on the header to edit the record.

13. Update the **Value** field with the new field name that is created.

    The default value is **email**.

    ![Updtae email field](../images/updtae-email-field.png)

14. Click **Update**.

    **Note:** Ensure that the email address for all the users for the newly created field is updated with the email associated with Microsoft Teams app.


**Parent Topic:**[Configure IT Service Management integration with Microsoft Teams](../concept/sn-ms-teams-config-it.md)

