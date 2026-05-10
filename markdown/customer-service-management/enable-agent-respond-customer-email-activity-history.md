---
title: Enable agents to respond to customers with email activity history
description: Enable agents to respond to customers with email activity history, which is created by embedding a mail script in an email client template.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Email Interaction for CSM]
breadcrumb: [Email Interaction, Email channel, Enable communication channels, Configure, Customer Service Management]
---

# Enable agents to respond to customers with email activity history

Enable agents to respond to customers with email activity history, which is created by embedding a mail script in an email client template.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Email Client** &gt; **Email Client Templates**.

2.  Search and select **Email response to customer**.

    **Note:** If a message appears about the application scope, select **here** to be able to edit the record.

3.  In the  **Body HTML ** field, enter `<div id="collapsible-content">${mail_script:get_email_interaction_activity_history_for_reply}</div>`.

    **Note:**

    -   The number of emails in the activity history matches the value set in the system property, number\_of\_activities\_in\_notification.
    -   You can also create a client template and map it to the Interaction table. For more information, see [Create an email client template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_CreateAnEmailClientTemplate.md).
4.  Select **Update**.


## Result

The get\_activity\_of\_case\_and\_related\_interaction\_for\_email script retrieves and formats cases and related interaction email history, adding it to the email client in the agent workspace. The content is hidden behind ellipses within a DIV tag with the ID “collapsible-content".

**Related topics**  


[Send case email replies containing interaction emails in activity history](send-case-email-replies-interaction-emails-activity-history.md)

