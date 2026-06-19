---
title: Create custom email field to initiate Microsoft Teams chat
description: Create a custom email field to use Microsoft Teams app to initiate chat conversation for the agents to resolve the IT and HR related issues of the users.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/employee-experience-foundation/create-upn-field.html
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [HR Service Delivery integration, Microsoft Teams Integration for Employee Experience, Configure, ServiceNow for Microsoft Teams and Microsoft 365, Unified Employee Experience, Employee Service Management]
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

    \[Omitted image "create-new-field.png"\] Alt text: Create new field

6.  In the Selected slush bucket column, move the field in the desired location on the form.

7.  Click **Save**.

    The field now appears on the form in the designated location.

    \[Omitted image "upn-field.png"\] Alt text: New field added to form

    The admin must enter the email used for Microsoft Teams in this field.

    You need to configure the newly created field value as the default field for initiating chats with the employee in Microsoft Teams.

8.  Right-click on the field and click **Show &lt;value of the field name&gt;**.

    \[Omitted image "show-field-name.png"\] Alt text: Show field name

    The dictionary info of the field name can be viewed.

    \[Omitted image "field-name2.png"\] Alt text: Field name

9.  Right click the **Field** and copy the value.

10. In the search field, enter `sys_properties.LIST` to view the system properties.

    \[Omitted image "sys-properties2.png"\] Alt text: System properties

11. In the Name column, search for `*user_email` property.

12. Click the entry.

    \[Omitted image "email-field2.png"\] Alt text: Email field properties

    If the record is not editable, click **Edit** on the header to edit the record.

13. Update the **Value** field with the new field name that is created.

    The default value is **email**.

    \[Omitted image "updtae-email-field.png"\] Alt text: Updtae email field

14. Click **Update**.

    **Note:** Ensure that the email address for all the users for the newly created field is updated with the email associated with Microsoft Teams app.


**Parent Topic:**[Configure HR Service Delivery integration with Microsoft Teams](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/employee-experience-foundation/sn-ms-teams-config-hr.md)

