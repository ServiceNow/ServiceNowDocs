---
title: Convert an email template to rich HTML
description: If you have an email template created prior to the Eureka release, you can convert it to rich HTML.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Email templates, Email and SMS notifications, System notifications, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Convert an email template to rich HTML

If you have an email template created prior to the Eureka release, you can convert it to rich HTML.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Policy** &gt; **Email** &gt; **Templates**.

2.  Open the email template you want to convert.

    ![Viewing template content](../image/legacy-email-template.png)

3.  Click **Switch to Rich HTML Editor**.

    When content is converted, these changes are made to the content:

    -   HTML Editor: Any raw HTML in the **Message** field is rendered as WYSIWYG text in the **Message HTML** field. The content can be edited in a feature-rich HTML editor.
    -   Simplified Mail Scripts: Any mail scripts in the body are automatically saved to the Email Script \[sys\_script\_email\] table and are replaced in the notification body with an embedded script tag. This makes the template body easier to read and makes it easier to reuse scripts in multiple email templates.
    ![Content converted to rich HTML](../image/Template_converted.png)

4.  Modify the message text, as needed, using the WYSIWYG editor or by editing the underlying HTML.

    **Note:** The letter "P" at the bottom of the screen shows the location of your cursor within the **Message** field. In this case, the cursor is in a line containing an &lt;HTML&gt; tag.

    **Note:** Email templates that are already formatted with rich HTML do not show the **Switch to Rich HTML Editor** button.


## Example

Whether you are working with templates converted from earlier versions or creating new templates in the rich HTML format, it is a good practice to write mail scripts in **System Notification** &gt; **Email** &gt; **Notification Email Scripts**. When the scripts are completed, a `${mail_script:script name}` embedded script tag should be added to the email template body. This makes it easy to use the same scripts in multiple email templates. All that must be copied and pasted from one template to the next is the embedded script tag.

If you manually enter a mail script in the body of a new or converted email notification or template, and then attempt to save the record, a message asks whether the mail script should be converted. Unconverted mail scripts often fail to run from inside the HTML editor. If you select **Yes**, the script is added to the Email Script \[sys\_script\_email\] table and is automatically replaced in the body with an embedded script tag.

You can view the mail scripts in their original form by opening the email template and clicking the **Show Notification Scripts** related link.

**Parent Topic:**[Email templates](../concept/c_EmailTemplates.md)

