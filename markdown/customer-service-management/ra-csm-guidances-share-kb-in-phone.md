---
title: Share knowledge articles in phone interactions
description: During a phone conversation, agents can send helpful knowledge base \(KB\) articles to customers through SMS using the Add link in message option.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Guidances, Recommended Actions, Recommended Actions configuration, Implement Intelligence, Configure, Customer Service Management]
---

# Share knowledge articles in phone interactions

During a phone conversation, agents can send helpful knowledge base \(KB\) articles to customers through SMS using the **Add link in message** option.

## Before you begin

Required plugins: To enable the **Add link in message** functionality, install the following plugins:

-   Conversational SMS Service Channel \(sn\_awa\_sms\_int\)
-   Agent Messaging Component \(sn\_agent\_messaging\)
-   Agent-Initiated Messaging Interface \(sn\_agent\_initiated\)
-   SMS Adapter Plugin \(for example, sn\_sms\_aws\_adapter, or any other supported SMS adapter\)

    **Note:** The system supports multiple SMS adapters. Verify that your selected adapter is compatible with the Conversational SMS framework.


If the required plugins are not installed, the **Add link in message** action is not available. Instead, the system displays other guidance actions such as:

-   Copy link \(default primary action\)
-   Read article in full view
-   Mark article as helpful
-   Flag article

Role required: none

## Procedure

1.  Select **Add link in message** in the interaction record.

    The Compose Message modal opens with a preview to the article and a pre-filled message.

2.  Customize the message as needed.

3.  Review how the **To** field is populated.

    During phone interactions, the system auto-populates the To field using the following order:

    -   If the **Contact** field is populated, the phone number from that contact is used.
    -   If the **Contact** field is empty, the system uses the phone number from the Opened For field.
    -   If both fields are empty, agents can manually enter a valid phone number.
4.  If an agent manually changes the phone number in the To field:

    -   The system treats it as a new interaction.
    -   The previous message is logged as sent to the original number.
    -   The new message is tracked separately to maintain clarity on what was shared and with whom.
5.  Select **Send** to send the message to the customer.

6.  After the message is sent:

    -   A confirmation appears in the Notifications panel.
    -   Select **View interaction** from the notification to open the related interaction record.
    -   The message also appears in the Active SMS side panel.

