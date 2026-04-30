---
title: Add an email notification
description: Build notifications in App Engine Studio \(AES\) to create automated emails for events using templates or custom messages.
locale: en-US
release: zurich
product: App Engine Studio
classification: app-engine-studio
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Add logic and automation, Enhance your app, Build, App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Add an email notification

Build notifications in App Engine Studio \(AES\) to create automated emails for events using templates or custom messages.

## Before you begin

You can perform this task if you're either an administrator or a developer for the application. The required developer permission is **All File Types**. For more information on being a developer for an application, see [Delegated development in App Engine Studio](../concept/aes-app-dev-workflow.md).

Role required: admin or delegated\_developer

## About this task

Email notifications enable you to send emails to the selected users about activities in the system, such as updates to incidents or change requests.

**Note:** You can't currently create any other types of automatic notifications, such as SMS messages.

Creating an email notification involves specifying when to send it, who receives it, and what it contains.

If your administrator has created an email template in the ServiceNow AI Platform, you can use it as is or override its content. For more information on email templates, see [Email Templates](https://www.servicenow.com/docs/access?context=c_EmailTemplates&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US). Also check with your administrator to see if they are using email layouts to control the header, body, and footer. For more information on email layouts, see [Email layouts](https://www.servicenow.com/docs/access?context=email-layouts&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **App Engine Studio**.

2.  From the My Apps page, open your application.

3.  In your application, in the Logic and Automation section, select **Add**.

4.  Select the card for **Email**.

    ![Select to add an email notification](../image/add-email-notification-purple.png "Add email notification")

5.  On the form, fill in the fields for the basic settings.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the email notification. Descriptive names help identify the purpose of the email notification. For example, `Incident Opened & Unassigned`.|
    |Short description|A brief explanation of the purpose of the notification.|

6.  On the Notification trigger settings section of the form, fill in the fields.

<table id="table_z5l_kqn_1tb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Send email notification

</td><td>

Situation where a notification is sent, such as after something happens or when a table is modified. Choices are as follows:-   **When a record is created or updated**
-   **Only when a record is created**
-   **Only when a record is updated**
-   **When triggered via Flow Action**
-   **When event is fired**
 This field is automatically set to **When a record is created or updated**.

 After you create an email notification with a [Flow Action](https://www.servicenow.com/docs/access?context=noti-flow-action&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US) as the trigger, you specify the notification when creating a flow in Workflow Studio. For more information, see [Notification step](https://www.servicenow.com/docs/access?context=trigger-notification-action-designer&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).

</td></tr><tr><td>

Table

</td><td>

The database table that hosts the records to link the notification trigger to. For example, the Incident \[incident\] table. If you set the **Send email notification** field to one of the following values, the table is required:

-   **When a record is created or updated**
-   **Only when a record is created**
-   **Only when a record is updated**
You can select from two sections: Tables that are already available in your app, and all tables outside the app scope.

</td></tr><tr><td>

Event name

</td><td>

Event that triggers the notification. This field appears only when **When event is fired** is selected from the **Send email notification** field.

</td></tr></tbody>
</table>    If the same trigger generates multiple notifications, the system only sends one notification. The system considers all other notifications, even if they have a different subject and body, as duplicates. The Ignore Duplicates business rule controls this functionality.

7.  Make the trigger conditional by using the condition builder.

    Define the condition sets and values that must be met for the notification trigger. For more information, see [Condition builder](https://www.servicenow.com/docs/access?context=c_ConditionBuilder&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).

    **Note:** If you specify that the notification trigger is a Flow Action, the condition builder isn't available.

8.  In the Recipients section of the form, specify who receives the notification.

    You can:

    -   Search for users or groups.
    -   Define dynamic recipients by selecting **Add**, which requires you to specify a table in the notification trigger details.
<table id="table_h3l_dj4_1tb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Users and groups from table fields

</td><td>

Dynamic users and groups who receive the email based on the table. For example, if a notification uses the Incident \[incident\] table, you can select the **Opened by** field to send the notification to users or groups who opened the incident. For some fields, you can also select values contained by a reference field, such as **Opened by** &gt; **Manager**.Select the **Add** button to search for dynamic users and groups based on fields from the specified table.

**Note:** If you don't specify a table, the **Add** button isn't available.

</td></tr><tr><td>

People and groups

</td><td>

Static addresses for users and groups who receive the email notification. You can also search for users and groups.

</td></tr></tbody>
</table>    ![Specify recipient by table field](../image/recipient-field-refine-purple.png)

9.  In the Email content section of the form, select a template or write original content.

<table id="table_nym_5p4_1tb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Email template

</td><td>

Predefined email template that you can use to apply existing content, which you can override. You can select only templates that have the following:-   The same table as the notification
-   No specified table
 If you use a template and don't override it, then when your administrator updates the template, the content of your email notification is also automatically updated.

</td></tr><tr><td>

Override template

</td><td>

Option to override the contents of the selected email template. If you use an email template, any images from the template still belong to the template regardless of whether you override it. Images in the notification are automatically updated when administrators update the template.

 If you override an email template and then change the selected template, the system removes the overrides and replaces them with content from the new template.

</td></tr><tr><td>

Subject

</td><td>

Subject line for the email.To make the subject dynamic, use the **Email variables** field next to the **Email message** to generate variable syntax in the message body. You cam then copy and paste the variable syntax in the subject line.

If empty, the system uses the **Subject** value from the email template. If you enter a value in this field, it overrides the template.

</td></tr><tr><td>

Email message

</td><td>

Content of the email notification message, which can include variables.You can format the contents of the email message using the rich text editor icons.

 If empty, the system uses the **Message** value from the email template. If you enter a value in this field, it overrides the template value.

</td></tr><tr><td>

Add variables

</td><td>

Dynamic variables, or values, derived from fields in the specified table. **Note:** You must specify a table for the **Add variables** button to appear.

 Select variables in the **Email variables** field and use the arrow to move them into the **Email message**.

Use variables to include values from a record in the table, such as an incident short description or comments and work notes. Variables are available fields from the specified table.

</td></tr></tbody>
</table>10. Select **Create**

    The notification is saved, and you can preview it.

11. View how the email notification appears by selecting **Preview**.

    Check the preview that appears. To see how a notification renders, select the search icon in the preview and select the record you want to preview.

    ![Search to preview the email notification for a specific record](../image/preview-email-notification-purple.png)


## Result

When you create a notification in AES, the notification is saved only to the application that you’re currently building.

-   **[Modify an email notification](edit-notification.md)**  
Edit an email notification created for an app in App Engine Studio \(AES\) to change it. For example, modify when to send the email notification, who receives it, and what it contains.

**Parent Topic:**[Add logic and automation](../concept/add-automation.md)

