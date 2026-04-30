---
title: Create an email layout
description: Create an email layout to specify the HTML content you want to appear in the body of one or more email templates.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Email layouts, Email and SMS notifications, System notifications, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Create an email layout

Create an email layout to specify the HTML content you want to appear in the body of one or more email templates.

## Before you begin

-   Role required: admin
-   Record required: email template record

## Procedure

1.  Navigate to **All** &gt; **System Policy** &gt; **Email** &gt; **Layouts**.

    The system displays the list of existing email layouts.

2.  Click **New**.

    The system displays a blank email layout form.

3.  Fill in the form.

<table id="table_vhx_qvz_5w"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Specify a unique name for the record.

</td></tr><tr><td>

Application

</td><td>

Lists the parent application to which this record belongs.

</td></tr><tr><td>

Description

</td><td>

Specify an optional description of the layout.

</td></tr><tr><td>

Advanced

</td><td>

Select whether to display the **Advanced Layout** field.

</td></tr><tr><td>

Layout

</td><td>

Use the inline editor to add HTML elements. The system displays HTML from this field in the body of any email template that uses the layout. Include notification variables to show content from the related record. For more information notification variables see [Notification variables](../concept/notification-variables.md).

 **Note:** The editor automatically formats any HTML code you enter from the **Source code** view.

</td></tr><tr><td>

Advanced Layout

</td><td>

Use this field to manually enter HTML code. The system displays HTML from this field in the body of any email template that uses the layout.

 **Note:** To enter text in this field, select **Click here to disable syntax highlighting and script formatting**.

</td></tr></tbody>
</table>4.  Click **Submit**.

    The system creates the email layout record.

5.  Navigate to **System Notification** &gt; **Email** &gt; **Templates**.

    The system displays the list of existing email templates.

6.  Select the email template which you want to use an email layout.

    The system displays the email template record.

7.  In **Email layout**, select the email layout you want to use to format the body of email messages.

8.  Click **Update**.

    The email template uses the selected email layout to format the body of email messages.


**Parent Topic:**[Email layouts](../concept/email-layouts.md)

