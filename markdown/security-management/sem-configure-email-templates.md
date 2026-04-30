---
title: Configure email templates in Unified Security Exposure Management
description: Create and manage preconfigured email templates for sending notifications.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Implement, Unified Security Exposure Management, Security Operations]
---

# Configure email templates in Unified Security Exposure Management

Create and manage preconfigured email templates for sending notifications.

## Before you begin

Role required: See [Access control lists \(ACLs\) for administration rules](../concept/sem-acls-for-admin-rules.md)

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Exposure Management Workspace**.

2.  Select **Administration** in the navigation pane.

3.  Under **Others**, select **Review** on the **Email templates** tile.

4.  Select **New**.

5.  Fill in the form fields.

<table id="table_jnc_ch3_54"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a unique name for the template.

</td></tr><tr><td>

Table

</td><td>

Select the name of the table involved. For example, **Change Request** `[change_request]`.

</td></tr><tr><td>

Email layout

</td><td>

Select a predefined layout.

</td></tr><tr><td>

Subject

</td><td>

Enter a subject line that explains the purpose of the email. Select the appropriate variables for the subject line from the fields available on the selected table. Place the cursor where you want the variable to appear, and select the field name in the **Select variables** column. For example:```
${sys_class_name} ${number} with ${risk} risk has been assigned to you.
```

</td></tr><tr><td>

Message HTML

</td><td>

Enter the content of the email template message. You can use the HTML editor toolbar to format the HTML, and you can include variables from the **Select variables** column. Variables map to column names available from the notification table, its parent tables, and reference tables. Use variables to include values from a record in the table such as an incident short description or comments and work notes.Notes:

-   When a template is applied to a notification, the contents of this field are used when you select **HTML and plain text** or **HTML** in the **Content Type** field in the Email Notification form.
-   You cannot use HTML code to control the appearance of the contents in the `${comments}` variable.
-   If you want to include a link to the record that triggered the notification, see [Enable links to records](https://www.servicenow.com/docs/access?context=c_EnableLinksToServiceNowRecords&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).


</td></tr><tr><td>

Message Text

</td><td>

Enter the notification message to send in plain text. **Note:** When a template is applied to a notification, the contents of this field are used when you select **HTML and plain text** or **Text** in the **Content Type** field in the Email Notification form.

</td></tr><tr><td>

SMS alternate

</td><td>

Create a different message to be delivered to an SMS device. Enter a brief message, showing the most important information only. If this message field is blank, the contents of the **Message Text** field are used for the SMS message. **Note:** The message in this field is used when the message is sent to a device configured as SMS.

</td></tr></tbody>
</table>    For detailed instructions for creating email templates, see [Construct an email message with a template](https://www.servicenow.com/docs/access?context=r_ConstructAnEmailMessage&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

6.  Select **Save**.


