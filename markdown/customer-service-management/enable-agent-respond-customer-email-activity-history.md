---
title: Enable agents to respond to customers with email activity history
description: Enable agents to respond to customers with email activity history, which is created by embedding a mail script in an email client template.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
keywords: [Email Interaction for CSM]
breadcrumb: [Email Interaction, Configuring the email channel, Configure communication channels, Enable communication channels, Configuring Customer Service Management, Customer Service Management]
---

# Enable agents to respond to customers with email activity history

Enable agents to respond to customers with email activity history, which is created by embedding a mail script in an email client template.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Email Client** &gt; **Email Client Templates**.

2.  View **Email response to the customer**.

3.  Select **Email response to customer**.

4.  In the  **Body HTML ** field, enter `<div id="collapsible-content">${mail_script:get_email_interaction_activity_history_for_reply}</div>`.

    This script, get\_email\_interaction\_activity\_history\_for\_reply \(available by default\), retrieves and formats email activity history, adding it to the email client in the agent workspace. The content is hidden behind ellipses within a DIV tag with the ID “collapsible-content".

    The number of emails in the activity history matches the value set in the system property, number\_of\_activities\_in\_notification.

    **Note:** You can also create a client template and map it to the Interaction table. For more information, see [Create an email client template](https://www.servicenow.com/docs/access?context=t_CreateAnEmailClientTemplate&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).


