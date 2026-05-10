---
title: Send an email from a touchpoint
description: Send emails to customers and stakeholders directly from a touchpoint record without having to leave the workspace. Emails are stored in the CRM system so other agents, managers, and customer success managers have full context about interactions with the customer or account.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Activity Management, Lead and opportunity apps, Use, Sales Customer Relationship Management]
---

# Send an email from a touchpoint

Send emails to customers and stakeholders directly from a touchpoint record without having to leave the workspace. Emails are stored in the CRM system so other agents, managers, and customer success managers have full context about interactions with the customer or account.

## Before you begin

The User Mailbox Integration plugin \(com.glide.email.user\_mailbox.integration\) must be installed on your ServiceNow instance to enable agents to send emails from the touchpoint record. For setup instructions, see [Personal corporate mailbox](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/personal-corporate-mailbox.md).

Role required: sn\_crm\_touchpoint.touchpoint\_writer

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  Select the List icon ![](../../../reuse/icons/product-icons/list-outline-24.svg).

3.  Navigate to **Touchpoints** &gt; **All Touchpoints**.

4.  Open the touchpoint record you want to work with.

5.  Select **Compose Email**.

6.  Draft the email message in the New Email Draft form.

    1.  In the **To** field, enter the recipient's email address.

    2.  In the **CC** or **BCC** fields, enter the name of recipients.

    3.  Review the text in the **Subject** field and change it if necessary.

    4.  Either compose an original email in the body field or use a template if templates are available.

        -   If templates are available and you want to use a template, select a template from the Email templates pane.

        -   Compose an original email in the text field.

            Toolbar options are available to format the text.

    5.  Add attachments to your email by selecting the Attach file icon ![](../../tmt-telecom-network-inventory/image/attachments-icon.png) and selecting the file.

7.  Either save the email as a draft or send it right away.

    -   To save the email as a draft to send later, close the form.

        The draft is automatically saved and accessible from the **Draft Emails** tab.

    -   To send the email right away, select **Send email**.

        The email is sent to the recipients and can be viewed from the touchpoint's **Emails** tab.


**Parent Topic:**[Using Activity Management](../concept/using-activity-management.md)

