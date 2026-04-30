---
title: Create an email template
description: You can create an email template with rich HTML formatting, rather than plain text.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Email templates, Email and SMS notifications, System notifications, Notifications, Configure core features, Administer]
---

# Create an email template

You can create an email template with rich HTML formatting, rather than plain text.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Notifications** &gt; **Email** &gt; **Templates**.

2.  Click **New**.

3.  Fill in the form fields \(see table\).

<table id="table_jnc_ch3_54"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a unique name for the template. For example, `change.update.risk`.

</td></tr><tr><td>

Application

</td><td>

The type of scoped application.

</td></tr><tr><td>

Email layout

</td><td>

If the message body for the template is to be formatted using a predefined [email layout](create-email-layout.md), select the layout.

</td></tr><tr><td>

Table

</td><td>

Select the name of the table involved. For example, **Change Request** `[change_request]`.

</td></tr><tr><td>

Subject

</td><td>

Enter a subject line that explains the purpose of the email. Select the appropriate variables for the subject line from the fields available on the selected table. Place the cursor where you want the variable to appear, and click the field name in the **Select variables** column. For example:```
${sys_class_name} ${number} with ${risk} risk has been assigned to you.
```

</td></tr><tr><td>

Message HTML

</td><td>

Enter the content of the email template message. You can use the HTML editor toolbar to format the HTML, and you can include variables from the **Select variables** column. Variables map to column names available from the notification table, its parent tables, and reference tables. Use variables to include values from a record in the table such as an incident short description or comments and work notes.Notes:

-   When a template is applied to a notification, the contents of this field are used when you select **HTML and plain text** or **HTML** in the **Content Type** field in the Email Notification form.
-   You cannot use HTML code to control the appearance of the contents in the `${comments}` variable.
-   If you want to include a link to the record that triggered the notification, see [Enable links to records](../../../script/server-scripting/concept/c_EnableLinksToServiceNowRecords.md).


</td></tr><tr><td>

Message Text

</td><td>

Enter the notification message to send in plain text. **Note:** When a template is applied to a notification, the contents of this field are used when you select **HTML and plain text** or **Text** in the **Content Type** field in the Email Notification form.

</td></tr><tr><td>

SMS alternate

</td><td>

Create a different message to be delivered to an SMS device. Enter a brief message, showing the most important information only. If this message field is blank, the contents of the **Message Text** field are used for the SMS message. **Note:** The message in this field is used when the message is sent to a device configured as SMS.

</td></tr></tbody>
</table>
**Parent Topic:**[Email templates](../concept/c_EmailTemplates.md)

**Related topics**  


[Create an email layout](create-email-layout.md)

