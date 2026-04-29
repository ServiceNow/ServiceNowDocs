---
title: Configure an email template with collapsed content
description: Configure email templates with collapsed content by hiding it behind an ellipsis.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Emails, Administer, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Configure an email template with collapsed content

Configure email templates with collapsed content by hiding it behind an ellipsis.

## Before you begin

Role required: email\_client\_admin

## Procedure

1.  Navigate to **All** &gt; **Email Client** &gt; **Email Client Templates**.

2.  From the Email Client Templates list, select an email template or create a new one.

    For instructions on creating an email template, see [Configure an email template](configure-email-templates.md).

3.  Select the **Content** tab.

4.  In the Content Type field, select **HTML**.

5.  In the Body HTML field, add the content you want to display.

6.  Collapse additional email content behind an ellipsis.

    **Important:** Since the ellipsis will only display at the end of the email, add collapsed content at the end of the email template body.

    1.  Enter the opening tag `<div id:collapsible-content>`.

    2.  Add all content you want collapsed after the opening tag.

    3.  Enter the closing tag `<div id:collapsible-content>`.

7.  Select **Update** or **Submit**.


## Result

The email template's content is hidden behind an ellipsis.

**Note:** Once you expand collapsed content by selecting the ellipsis, it's not possible to collapse the content again.

![Collapsed content behind and ellipsis](../image/y-email-collapse-content.png)

