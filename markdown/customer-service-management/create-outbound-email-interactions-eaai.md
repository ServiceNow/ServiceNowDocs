---
title: Create outbound email interactions
description: Initiate an outbound email interaction from a contact or consumer record to proactively engage with a customer. The system automatically creates and tracks the interaction.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use emails, Customer communication, Use, Customer Service Management]
---

# Create outbound email interactions

Initiate an outbound email interaction from a contact or consumer record to proactively engage with a customer. The system automatically creates and tracks the interaction.

## Before you begin

The Email Interaction for CSM application must be installed and activated.

When multiple agents initiate outbound emails for the same customer, the system consolidates drafts by default. For details on the behavior, see Multiple agents composing for the same customer in [Using Email Interaction for Customer Service Management](../concept/using-email-interaction-customer-service-management.md) Customer Service Management.

Role required: sn\_customerservice\_agent

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  Select the List icon \( ![List icon](../image/List_icon.jpg)\).

3.  In the Interactions section, select **My Interactions**.

4.  Open a contact or consumer record.

5.  Initiate an email using one of the following methods:

    -   Select **Compose Email** on the record.
    -   Select the email address on the contact or consumer record.
    The email editor opens in a modeless dialog with the To field pre-filled with the contact or consumer email address. The system automatically creates a Work-In-Progress \(WIP\) outbound interaction and assigns it to the agent.

    **Note:** If you add more than one contact or consumer to the To field, or edit the To field, the interaction remains associated with the original contact or consumer.

6.  Compose your email.

7.  Select the Send email \(![Send email to contact or customer icon](../image/send-email-icon-eaai.png) \) icon.


## Result

-   The email is sent and associated with the outbound interaction.
-   The interaction is linked to the contact or consumer record in the related list.
-   When the customer responds, the response is associated with the same interaction and you’re notified on the **Ongoing** tab.
-   If a reminder is configured, the system sends an automatic reminder email to the customer if no response is received within the configured period.
-   If the email remains in draft state for more than 30 days, the interaction is automatically closed with a state of Closed Abandoned. The 30-day period resets each time the agent opens the draft or creates a new draft.

