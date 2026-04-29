---
title: Configure flows for incoming emails that create and update interactions
description: The default email flows are available once you activate the Email Interaction for CSM application. Enable the email flows to activate email processing for automatic creation and updating interactions.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Email Interaction for CSM]
breadcrumb: [Email Interaction, Email channel, Configure, Enable communication channels, Configure, Customer Service Management]
---

# Configure flows for incoming emails that create and update interactions

The default email flows are available once you activate the Email Interaction for CSM application. Enable the email flows to activate email processing for automatic creation and updating interactions.

-   **Create Interaction from Email**: Creates an interaction of type Email for each new inbound email from a customer.
-   **Update Interaction from Email**: Updates the interaction with the reply email received from the customer.

    If a reply email is received on a closed interaction, a new interaction of type Email is created. It includes the link to the previous closed interaction.

-   **Update Case via Reply for EmaiI**: Updates the case record with the reply email received from Customer on the case.

    This flow creates an interaction of type Email if a reply email is received on the closed case record. The new interaction includes a link to the closed case.


Alternatively, customers can use Inbound Actions to create and update email interactions.

The execution order of the Inbound Flows takes a higher precedence over Inbound Actions meaning that when an email flow executes, it helps prevent execution of Inbound Actions.

