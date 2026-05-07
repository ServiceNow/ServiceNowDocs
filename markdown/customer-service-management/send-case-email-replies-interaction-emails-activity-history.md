---
title: Send case email replies containing interaction emails in activity history
description: Include emails from related interactions in agent case email responses to provide full context of prior email communications. The history is created by embedding an email script within an email client template.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Email to case, Email channel, Enable communication channels, Configure, Customer Service Management]
---

# Send case email replies containing interaction emails in activity history

Include emails from related interactions in agent case email responses to provide full context of prior email communications. The history is created by embedding an email script within an email client template.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Email Client** &gt; **Email Client Templates**.

2.  Search and select **reply-for-customer-service**.

    **Note:** If a message appears about the application scope, select **here** to be able to edit the record.

3.  On the Content tab, in the  **Body HTML ** field, enter `<div id="collapsible-content">${mail_script:get_activity_of_case_and_related_interaction_for_email}</div>`.

    **Note:**

    -   The number of emails in the activity history matches the value set in the system properties, **include\_system\_emails\_in\_notification and number\_of\_activities\_in\_reply**.
    -   You can also create a client template and map it to the Interaction table. For more information, see [Create an email client template](https://www.servicenow.com/docs/access?context=t_CreateAnEmailClientTemplate&version=australia&pubname=australia-platform-administration&ft:locale=en-US).
4.  Select **Update**.


## Result

The get\_activity\_of\_case\_and\_related\_interaction\_for\_email script retrieves and formats cases and related interaction email history, adding it to the email client in the agent workspace. The content is hidden behind ellipses within a DIV tag with the ID “collapsible-content".

**Related topics**  


[Enable agents to respond to customers with email activity history](enable-agent-respond-customer-email-activity-history.md)

