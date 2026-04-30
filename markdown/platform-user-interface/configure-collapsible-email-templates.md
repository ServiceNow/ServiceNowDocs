---
title: Set up collapsed content in email templates
description: Collapse content in email templates by hiding it behind an ellipsis.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Set up email templates in Configurable Workspace, Administering emails in Configurable Workspace, Administering Configurable Workspace, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Set up collapsed content in email templates

Collapse content in email templates by hiding it behind an ellipsis.

## Before you begin

Role required: email\_client\_admin

## Procedure

1.  Navigate to **All** &gt; **Email Client** &gt; **Email Client Templates**.

2.  Configure a new email template by selecting the **New** button in the Email Client Templates page.

3.  Complete the fields with the template settings you want.

4.  In the Body HTML field, add the content you want to display.

5.  Collapse additional email content behind an ellipsis.

    **Note:** Since the ellipsis will only display at the end of the email, add collapsed content at the end of the email template body.

    1.  In the Body HTML field, enter the opening tag `<div id:collapsible-content>`.

    2.  Add all content you want collapsed after the opening tag.

    3.  Enter the closing tag `<div id:collapsible-content>`.

6.  Select **Submit**.


## Result

An email template is created with collapsed content hidden behind an ellipsis.

**Note:** Once you expand collapsed content by selecting the ellipsis, it's not possible to collapse the content again.

![Collapsed content behind and ellipsis](../image/y-email-collapse-content.png)

